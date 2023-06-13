# Basic Steps For Docker Container

1. Pull Image From Docker Hub
``` 
sudo docker pull balapradeeps/firstrepo:v2 
```

2. Verify the pulled image
``` 
sudo docker image ls (or) docker images
```

3. Verify the port is not assigned to any services
```
netstat -tpuln |grep 80 
```

4. Run the docker container in detach mode with specify port First port(8082) need to open in security group and Second is assigend to docker inside service,
``[docker container run -d -p 8082(hostport):80(containerport) 04c243890076]`` host port will change but container port will never change untill we change config file. 

``` 
sudo docker container run -d -p 8082:80 04c243890076 
```

5. Interact the docker container with Container ID or Container Name
``` 
sudo docker container exec -it b1544a796c65 /bin/bash (or) sudo docker container exec -it beasm/bin/bash
```

6. Stop the Docker container using Container ID or Container Name
```
sudo docker stop b1544a796c65 (or) sudo docker stop webserver
```

7. Verify the container status  
```
sudo docker ps 
```

8. Remove the container using Container ID or Container Name
```
sudo docker rm b1544a796c65 (or )sudo docker rm  webserver
```

9. Verify the all container status 
```
sudo docker ps -a 
```

10. Remove docker image using image ID or image Name
```
sudo docker image rm 04c243890076 (or) sudo docker rmi web-fe
```
