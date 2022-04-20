## Notes to build, run and manage docker

### Build image
`docker build -t ubuntu:[YOURTAGHERE] .`

Use --rm together with `docker build` to remove intermediary images during the build process.

To run bash in a container
`docker exec -it [YOURCONTAINER] bash`

### Pull docker image from Docker Hub
In this case pulling the docker image `topicos:4.1.3` from my dockerhub `cmzambranat`
`docker pull cmzambranat/topicos:4.1.3`

#### Run docker-compose
This will run the docker container with settings specified in `docker-compose.yml`. The `-d` flag is to run docker in detached mode.

`docker-compose up -d`

### List docker images
`docker image ls`

### List docker containers
`docker ps`
Add `-a` flag to list all stopped containers
`docker ps -a`

### Stop container
`docker stop [CONTAINER ID]`

### Remove dangling/untagged images
`docker images -q --filter dangling=true | xargs docker rmi`

### Remove all stopped containers
`docker ps -aq --no-trunc -f status=exited | xargs docker rm`

### circleci

1. Create job in `circleci`
2. Link to github repo
3. Import variables



