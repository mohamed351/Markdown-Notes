## Docker in Action 

### Create a 3 Tier Applcation 

- Database 
- BackEnd
- FrontEnd

### Setup database
docker compose part of database MongoDb
```yml
service: "3.8"
  mongodb:
    image: "mongo"
      volumes: 
       - ./data:/data/db
      ports:
       - "9000:27017" 
      environment:
       MONGO_INITDB_ROOT_USERNAME: 'max'
       MONGO_INITDB_ROOT_PASSWORD: 'secret'

          
```
it Equals the command 
```bash
docker  run --name 
mongodb
-e MONGO_INITDB_ROOT_USERNAME=max
-e MONGO_INITDB_ROOT_PASSWORD=secret
-p 9000:27017
--rm 
-d 
--network goals-net
mongo
```


