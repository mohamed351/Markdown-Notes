# Docker -Section 
## Docker a platform for building , running and shipping applications 
*if your application works in development enviroment it will work the some way*
### Reasons "Why application doesn't the same way on client machine"
1. one or more files missing
2. software version mismatch 
3. different configuration settings
-----------------------
*example about docker command*
```bash
$ docker-compose up
```
-----------------------

*this isolated enviroment use different application side by side maybe container use node version 14 and another running container use node version 9.*

-----------------------
*example about deleteing docker easly*
```bash
$ docker-compose down --rmi all
```

*Docker : Consistently build run and ship applications* 

---------------------
### Docker Container  vs VM

|Container|VM|
|---------|---|
|an isolated enviroment for running an application| An abstraction of machine (physical hardware)
|are lightweight| Each VM needs a full blown os|
|fast to start|Slow to start
|use OS of the host|Resource intensive|
-------------------
## Docker Architecture 
*use a client server architecture. the server called docker engine. container it just a process. with a shared kernal. but what is a kernal , a kernal is a core of operating system it is like a engine of a car . a kernal manages applications  and hardware resources*

--------------------------------

