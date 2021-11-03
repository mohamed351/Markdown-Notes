## Docker Network 
if you want to connect to database that in your localhost 
you can replace localhost with 

```nodejs
mongodb://host.docker.internal:27017/
```
and is going to replace it with internal local ip address 
```bash
host.docker.internal
```
to use Network in docker container 
```bash
docker run  -d --name= mongodb  --network favoriate-net 
```
this fails to run you should create network first 
to create a network 
```bash
docker network create favoriate-net 
```
to list a network 
```bash
docker network ls
```