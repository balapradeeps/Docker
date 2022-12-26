
sudo docker pull balapradeeps/firstrepo:v2
sudo docker container run -d -p 8082:80 04c243890076
netstat -tpuln |grep 80
sudo docker container exec -it b1544a796c65 /bin/bash 
sudo docker container exec -it <dockercontainername> /bin/bash

sudo docker stop b1544a796c65
sudo docker ps
sudo docker rm b1544a796c65
sudo docker ps -a
sudo docker image rm 04c243890076
sudo docker image ls