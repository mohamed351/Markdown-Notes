## Auth in ASP.NET CORE
------------------------
## controller
```csharp
    [Route("api/[controller]")]
    [ApiController]
    public class AuthController : ControllerBase
    {

        private readonly IAuthRepository _authRepository;
        private readonly IConfiguration _configuration;

        public AuthController(IAuthRepository authRepository, IConfiguration configuration)
        {
            _authRepository = authRepository;
            _configuration = configuration;
        }
        [HttpPost("Login")]
        public async Task<ActionResult> Login(LoginUserDTO loginUserDTO)
        {

            var userResult = await _authRepository.Login(loginUserDTO.PhoneNumber, loginUserDTO.Password);
            if (userResult == null)
                return Unauthorized();
         
            var claims = new List<Claim>()
            { 
                new Claim(ClaimTypes.Name, userResult.UserName),
                new Claim(ClaimTypes.Email , userResult.Email),
                new Claim(ClaimTypes.NameIdentifier, userResult.ID.ToString()),
                new Claim(ClaimTypes.MobilePhone, userResult.PhoneNumber)
            };
            var key = new SymmetricSecurityKey(Encoding.Unicode.GetBytes((_configuration["AppSettings:Token"].ToString())));
            var signer = new SigningCredentials(key, SecurityAlgorithms.HmacSha512Signature);
            var tokenDecrptor = new SecurityTokenDescriptor()
            {
                Subject = new ClaimsIdentity(claims),
                Expires = DateTime.Now.AddDays(1),
                SigningCredentials = signer
            };
            var tokenHandler = new JwtSecurityTokenHandler();
            var token = tokenHandler.CreateToken(tokenDecrptor);


            return Ok(new { token = tokenHandler.WriteToken(token) });
        }
        [HttpPost("Register")]
        public async Task<ActionResult> Register(RegisterUserDTO registerUserDTO)
        {
            if (!await _authRepository.UserExist(registerUserDTO.Phone))
            {
                return BadRequest("The user already exist");
            }

            var userResult = await _authRepository.Registration(new AppUser()
            {
                Email = registerUserDTO.Email,
                PhoneNumber = registerUserDTO.Phone,
                IsDeleted = false,
                UserName = registerUserDTO.UserName
            }, registerUserDTO.Password);


            return StatusCode(201);
        }
    }

```
## DTOS
```csharp

 public class LoginUserDTO
    {
        public string PhoneNumber { get; set; }
        public string Password { get; set; }
    }


  public class RegisterUserDTO
    {
        public string UserName { get; set; }
        [Required]
        public string Phone { get; set; }

        public string Email { get; set; }
        [Required]
        public string Address { get; set; }
        [Required]
        public string Password { get; set; }


    }

```
