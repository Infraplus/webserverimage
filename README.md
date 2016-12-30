# webserverimage
Webserver Docker Image that display Ip address of the running container (Used for Docker Swarm Tutoriel)

# Prerequistes 
Docker installed

## Docker installation:
echo "deb https://apt.dockerproject.org/repo ubuntu-$(grep CODENAME /etc/lsb-release | awk -F'=' '{print $NF}') main" | sudo tee /etc/apt/sources.list.d/docker.list

sudo apt-get update

sudo apt-get install apt-transport-https ca-certificates -y

sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80  --recv-keys 58118E89F3A912897C070ADBF76221572C52609D

sudo apt-get install linux-image-extra-$(uname -r) linux-image-extra-virtual docker-engine -y

For more information: https://docs.docker.com/engine/installation/linux/ubuntulinux/
