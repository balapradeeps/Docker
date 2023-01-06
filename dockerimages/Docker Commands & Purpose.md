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

7. Commit the running docker container with latest installed files or updated configuration any changes we made on container we can save it using containerID
    > * sudo docker commit 25d66e2cf2f4 centos7-utilites
 
8. Pushing committed image to dockerhub we need to login to dockerhub website in cli and provide username, passwd
    > * docker login
    
9. Tag the committed image with Image ID is  ``369dd4ceb19d`` and DockerHub username is ``dockeruser`` then Image displayed on Docker hub is ``centos7-utilites`` and Give you tag name for version is ``cento7``  
    > * docker tag 369dd4ceb19d dockeruser/centos7-utilites:cento7
    
10. Push the image to Docker Hub Repository
    > * docker push dockeruser/centos7-utilites:cento7 

11. Error: unable to delete 369dd4ceb19d (must be forced) image is referenced in multiple repositories
    > * sudo docker rmi -f $(docker images -q)

12. check the disk usage of running Docker containers
    > * docker ps --size or docker ps -s 
    > * docker system  df ``total running containers``
