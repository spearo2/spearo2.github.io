---
layout: post
category: dev
---

# Docker at a higher level

Honetly, we are not that interested in internal architecture of Docker (Maybe we should).<br>
This is because we seek to practice it rather than understanding it.<br>
We want to <br>
```
# 1. make sure that my project is runnable at any random environment.
# 2. secure my coding environment.
# 3. run someone's project that is deployed as a Docker image
# 4. run someone's project but doesn't want to mess up my local dependincies.
```
Docker is well-optimized virtual machine orginizer which is outstanding in many aspects<br>
including dependency control, security, and project deployment.<br><br>
## However, that is not what I want to talk about here.<br>
I would like to divide this post into 5 steps.<br>
### Build
To run certain VM, we need something called `image`<br>
We could either pull an image from the dockerhub (repository for built images like githun for source code) or<br>
We could build the image.<br><br>
If you want to build an image, you could build it from the scratch, or you could build it on top of the <br>existing image you could get from the repository.

Building an image is done by creating a `DockerFile` (Make sure that the name of the file is literally "DockerFile")

The following example shows how to make the Dockerfile
<img src="{{site.url}}/assets/images/dev/docker1.png" style="border:white;" width="500" height="auto" alt="docker1"><br>

You need to know these dockerfile commands<br>
```
# From --> pull the base image (in the above example, I pulled the empty ubuntu OS image)
# ENV --> set the environment variable
# RUN --> run a shell command at build time
# CMD --> run a shell command after build time, which means that this command will execute at the beginning of the execution of the image(execution != build)
COPY/ADD <source path> <dest path> --> copy a local file/directory into the image
```

Basically, add the above command then continue the regular shell commands.

For the `From` command, you can add dockerhub name instead of the empty ubuntu OS image.

So, yea. You need to know how to write shell commands to write a Dockerfile<br>

If this is written, you can start building the image by the following command at the directory where the Dockerfile is located.<br>

`$ docker build -t <image name>:<tag> .`

If you don't specify a tag it is `latest` by default.<br>
You can also replace `.` at the end for the location where the Dockerfile is located.

Then, you can check the image built by the following command

`$ docker image ls`

### Execution

If you found your image, copy the image ID of your image from the `docker image ls` command.
and run the following command<br>
`$ docker run -it <image ID> /bin/bash`

if you add `-d` option before the image ID, it will only run the container but not executing it.<br>
In this case you can join into the container by `docker exec -it <container ID>`
<br>
Now, Container is basically a running image.<br>
conainers can be seen by the following commands<br>
`$docker ps` or `$docker ps -a`
`-a` option will show you even the stopped container, otherwise it only shows the running container.

Now, whatever you do in your image will be saved in the same image ID.<br>
You can quit the container by `$ exit` command.<br>

By the way, if you don't want to update your image after exiting the image, you can add `--rm` option after the `-it` option.

### Restart

Same as before, you can restart the container by the
`$ docker run -it <image ID> /bin/bash` command.
Then, your previous work will be saved here.

### Delete

Both the container and the image consumes a log of resources.<br>
For containers,<br>

`$ docker stop <Container ID>`<br>
`$ docker rm <Container ID>`<br>

For images,<br>
`$ docker image rm <Image ID>`

Make sure that the image removed has to be re-built.

### Dump

Dumping could be done in two ways<br>
You could dump the container you are working on<br>
OR<br>
Your could dump the image.
#### If you are dumping the container,

`docker export <Container name OR Container ID> > <new name>.tar`

You can create an image out of this compressed container(tar file) by the following command.

`docer import <file path OR URL> - <image name>:tag`

#### If you are dumping the image,

`docker save -o <dumpped file name> <Image name:tag>`

You can convert the tar file back to an image by

`docker load -i <tar file>`


## Conclusion
Docker provides more sophisticated features such as docker inside docker or pulling files from the container to the local(host) OS, vice versa.

But the basic flow of making and working with Docker is simple as this.

Hope this helps someone.