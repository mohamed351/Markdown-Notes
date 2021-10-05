## Create Nodejs Image and Run it 
- Create node app
- Create Docker file 

```dockerfile
FROM node:14
WORKDIR /app
COPY package.* .
RUN npm install
COPY . .
EXPOSE 3000
CMD ["npm","start"]
```
- To build a docker file please to write Dockerfile not anything
- and don't write "npm install" in string format 
```bash
docker build .
```
- Run an Image
```bash
docker run -p 3000:3000 <image_id>
```
- Visit Port 3000




