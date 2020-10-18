## Images

#### List images

    docker images

#### Remove images

    docker rmi {image_name/id}

    docker rmi -f {image_name/id}

## Container

#### Create container

    docker run -d {image:tag}

    -d => stands for de-attach mode

#### List containers

    docker ps -l

    docker ps -a

#### Remove container

    docker rm {Container Id}

    Use force `-f` To remove running container 

    docker rm -f {container_id}

#### Start contaier

    docker start {}

#### Name the container

    docker run -d --name {container name} -p 80:80 nginx

#### Expose Port

To expose port use `-p-`

    docker run -d -p {host_os_port}:{docker_port} {image:tag}
    docker run -d -p 9090:80 nginx:alpine

## RUN

Use to install application

    FROM ubuntu
    RUN apt-get install git

## CMD

Command to execute

    From ubuntu
    RUN apt-get install nginx
    ngnixctl -DFOREGROUND

The process must be `foregroud`, otherwise the docker will exit.
If there is no `foreground` process then use the following command `ti` (terminal) to keep alive for debug

    docker run -d -ti --name {Container_name} -p {PORT:PORT} {image} 

### Login/Access Container

    docker exec -ti {containerName} bash


