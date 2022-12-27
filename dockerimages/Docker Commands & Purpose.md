# Docker Commands & Purpose
1. Docker Command with custom port and name tag of container,
    > * sudo docker run -d --name=docker_grafana -p 8321:3000 83f377cc32a0
 
2. Stop all running docker containers.
    > * sudo docker stop $(docker ps -aq)

3. Got permission denied while trying to connect ``or`` stop ``or`` remove to the Docker daemon socket.
    > * sudo chmod 666 /var/run/docker.sock
 
4. Remove all docker containers and ``-q`` or ``--quiet`` for show only container ID
    > * docker rm $(docker ps -aq)
 
5. Removing all docker images 
    > * docker rmi $(docker images -q)

6. Build the docker image with tag flag to identify the file 
    > * sudo docker build -t grafana-ubuntu /home/user/dockerimage
