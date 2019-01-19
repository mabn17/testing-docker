# Testing docker
Testing docker (containers only) for the first time with a small flask hello world application.

## Usage
**Build** the app by Running the build command. This creates a Docker image, using the  `--tag` option.
```
docker build --tag=helloWorld .
```

**Run** the app in detached mode using `-d`, mapping your machine’s port 4000 to the container’s published port 80 using `-p`:
```
docker run -d -p 4000:80 helloWorld
```

To **end** the process you need the container id witch you can get by running `docker container ls`.
```
docker container stop {CONTAINER ID}
```