## Docker section 2
### Docker Pull
```bash
$ docker pull <name_of_image_in_docker_hub>
```
### Example of Creating Docker File
*example of base image in docker*
> [!NOTE]
> It must be Dockerfile => don't name it as  DockerFile
```dockerfile
FROM node
WORKDIR ./app
COPY . .
CMD node app.js
```
*to see the image*
```bash
$ docker image ls 
```
*to build an image*
```bash
$ docker build -t <tag_name> <the directory which is .>
$ docker build -t hello-node .
```
*to delete an image*
```bash
$ docker image rm hello-node
```
*if you want to delete docker image that has a container and you don't want to delete a container becasue*
*it has 1000000 container stoped*
```bash
$ docker image rm hello-node -f 
```
*f it  mean force*

-------------------------
Docker for inter-active mode

```bash
$ docker image -it ubuntu
```
------------------------

