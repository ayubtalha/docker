### Docker CLI Commands

#### build docker container

> docker build -t ayubtalha/simpleweb .

#### run docker container

> docker run ayubtalha/simpleweb

#### check running container

> docker ps

#### stopping the docker

> docker stop <container id>

#### define a port

first 8080 is your local machine port while second 8080 is the port inside docker

> docker run -p 8080:8080 ayubtalha/simpleweb

#### startup a shell

> docker run -it ayubtalha/simpleweb sh

### Docker Compose Commands

#### run conatiner

> docker-compose up

#### rebuild the container after changing files

> docker-compose up --build

#### launch in background

> docker-compose up -d

#### stop containers

> docker-compose down

#### check running container

> docker-compose ps
