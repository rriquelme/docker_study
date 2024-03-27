# Docker Study Repo
## Useful resources:
- https://devopswithdocker.com/getting-started/
- https://labs.play-with-docker.com/
- https://learndocker.online/
- https://github.com/veggiemonk/awesome-docker


## Commands:
- docker pull: This command is used to pull an image or a repository from a registry. It's the equivalent of "git pull", fetching the latest version of an image.
- docker images: This command lists all the Docker images that are currently stored in your system.
- docker inspect: This command is used to get detailed information on Docker objects such as images, containers, volumes, and networks. It returns a JSON object describing the object you're inspecting.
- docker run: This command is used to create a new container and run a command in it. This is one of the most commonly used Docker commands. It combines the functionality of docker create and docker start.
- docker build: This command is used to build Docker images from a Dockerfile and a "context". The build process can refer to any of the files in the context. The context is typically set to the current directory (.).

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

## Labs to practice:
