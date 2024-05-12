### Docker CLI Commands

build docker container

> docker build -t ayubtalha/simpleweb .

run docker container

> docker run ayubtalha/simpleweb

check running container

> docker ps

stopping the docker

> docker stop <container id>

define a port

`first 8080 is your local machine port while second 8080 is the port inside docker`

> docker run -p 8080:8080 ayubtalha/simpleweb

startup a shell

> docker run -it ayubtalha/simpleweb sh

### Docker Compose Commands

run conatiner

> docker-compose up

rebuild the container after changing files

> docker-compose up --build

launch in background

> docker-compose up -d

stop containers

> docker-compose down

check running container

> docker-compose ps

docker volumes to have live update of local files in docker conatiner

> docker run -p 3000:3000 -v /app/node_modules -v "$(pwd):/app" 'container-id'

### KUBERNETES

Get a list of pods running in the Kubernetes cluster

> kubectl get pods

Get a list of services running in the Kubernetes cluster

> kubectl get services

Create a pod using the configuration defined in client-pod.yaml file

> kubectl apply -f client-pod.yaml

Create a NodePort service using the configuration defined in client-node-port.yaml file

> kubectl apply -f client-node-port.yaml

Get detailed information about a specific Kubernetes object (replace 'object-type-here' and 'object-name-here' with actual values)

> kubectl describe 'object-type-here' 'object-name-here'

Delete the pod specified in client-pod.yaml file

> kubectl delete -f client-pod.yaml

Get a list of deployments running in the Kubernetes cluster

> kubectl get deployments

Get a detailed list of pods, including additional information such as node name and IP addresses

> kubectl get pods -o wide

Update the image of client-deployment to ayubtalha/multi-client:v1. This is useful for deploying new versions or rolling back to previous versions of the application running in the Kubernetes cluster.

> kubectl set image deployment/client-deployment client=ayubtalha/multi-client:v1

delete deployment

> kubectl delete deployment client-deployment

set secrets

> kubectl create secret generic pgpassword --from-literal PGPASSWORD=`<secret-password-here>`

get secrets

> kubectl get secrets
