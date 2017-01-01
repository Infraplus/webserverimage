# webserverimage
Webserver Docker Image that display Ip address of the running container (Used for Docker Swarm Tutoriel)

# Prerequistes 
Docker installed

## Docker installation:
echo "deb https://apt.dockerproject.org/repo ubuntu-$(grep CODENAME /etc/lsb-release | awk -F'=' '{print $NF}') main" | sudo tee /etc/apt/sources.list.d/docker.list</br>
sudo apt-get update</br>
sudo apt-get install apt-transport-https ca-certificates -y</br>
sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80  --recv-keys 58118E89F3A912897C070ADBF76221572C52609D</br>
sudo apt-get install linux-image-extra-$(uname -r) linux-image-extra-virtual docker-engine -y</br>

For more information: https://docs.docker.com/engine/installation/linux/ubuntulinux/

# How to:
You can create your image or pull it directly from dockerhub:
## Create local image
$git clone git@github.com:shitana/webserverimage.git
$cd webserverimage/
$sudo docker build -t webserverphp:latest .
--snip--
$ sudo docker images
REPOSITORY                  TAG                 IMAGE ID            CREATED             SIZE
webserverphp                latest              bbe0e090daa3        41 hours ago        307 MB

## Pull image from dockerhub
$docker pull salmenhitana/webserverphp

## Run the container:
$sudo docker run -d -p 8080:80 webserverphp

The webpage should return the running container IP address
$curl localhost:8080
172.17.0.2  

# Docker swarm tutorial
To be continued !!!
