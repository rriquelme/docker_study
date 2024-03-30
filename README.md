# Docker Study Repo
## Useful resources:
- https://devopswithdocker.com/getting-started/ -> Great site to understand the basics
- https://labs.play-with-docker.com/
- https://learndocker.online/
- https://github.com/veggiemonk/awesome-docker


## Basic commands:
- *docker pull*: This command is used to pull an image or a repository from a registry. It's the equivalent of "git pull", fetching the latest version of an image.
- *docker images*: This command lists all the Docker images that are currently stored in your system.
- *docker inspect*: This command is used to get detailed information on Docker objects such as images, containers, volumes, and networks. It returns a JSON object describing the object you're inspecting.
- *docker run*: This command is used to create a new container and run a command in it. This is one of the most commonly used Docker commands. It combines the functionality of docker create and docker start.
- *docker build*: This command is used to build Docker images from a Dockerfile and a "context". The build process can refer to any of the files in the context. The context is typically set to the current directory (.).

## Dockerfile, basic commands:
- FROM: This command sets the base image for subsequent instructions. In every valid Dockerfile, FROM is the first instruction.
- ENV: This command sets the environment variable. These variables consist of “key=value” pairs which can be accessed within the container.
- RUN: This command will execute any commands in a new layer on top of the current image and commit the results. The resulting committed image will be used for the next step in the Dockerfile.
- WORKDIR: This command sets the working directory for any instructions that follow it in the Dockerfile. If the directory does not exist, Docker will create it.
- ADD: This command copies new files, directories or remote file URLs from src and adds them to the filesystem of the image at the path dest.
- COPY: This command is similar to ADD, but without the extra features of ADD like extracting a tarball from source or downloading a file from a URL.
- EXPOSE: This command informs Docker that the container listens on the specified network ports at runtime. Note that it does not actually publish the port.
- CMD: This command provides defaults for an executing container. These can include an executable, or they can omit the executable, in which case you must specify an ENTRYPOINT command.
- STOPSIGNAL: This command sets the system call signal that will be sent to the container to exit. It can be a valid unsigned number that matches a position in the kernel’s syscall table, for instance 9, or a signal name in the format SIGNAME, for instance SIGKILL.
- HEALTHCHECK: This command tells Docker how to test a container to check that it is still working. This can detect cases such as a web server that is stuck in an infinite loop and unable to handle new connections, even though the server process is still running.

## Tips For Efficiency:
- Use multilayer: change things that are less likely to change on lower layer levels
- bundle layers not too much layer
- not unnecessary files
- multistage build 
- https://www.youtube.com/watch?v=wGz_cbtCiEA

## Idea of Labs to practice:
- [ ] Lab 1: install docker and add user to group docker
- [ ] Lab 2: launch docker and launch hello world
- [ ] Lab 3: launch docker from systemctl
- [ ] Lab 4: review where is the file of the settings on docker
- [ ] Lab 5: resume commands that I use, 
- [ ] commonly used flags, it d rm restart -memory memory-reservation
- [ ] Lab 6: interactive container
- [ ] Lab 7: -- restart unless-stopped / always etc
- [ ] Lab 8: docker start, view the logs of the container
- [ ] Lab 9: docker exec
- [ ] Lab 10: docker cp
- [ ] Lab 11: rename container -> docker rename
- [ ] Lab 12: docker stats
- [ ] Lab 13: curl web address nginx / inspect
- [ ] Lab 14: docker commit 
- [ ] Lab 15: create a dockerfile and build, docker diff
- [ ] Lab 16: create a base image
- [ ] Lab 17: summary dockerfile layers
- [ ] Lab 18: docker image inspect
- [ ] Lab 19: upload to dockerhub
- [ ] Lab 20 make labs introduction to containers and docker

## Examples of Dockerfiles:
- 

## Experiments:
- Wordpress multiple sites to design themes.