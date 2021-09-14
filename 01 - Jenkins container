# Criando Primeiro Container -  Jenkins

### Instalar docker 

curl -sSL https://get.docker.com/ | CHANNEL=stable sh

systemctl start docker

### Instalar Docker compose

 sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

sudo chmod +x /usr/local/bin/docker-compose

sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose

docker-compose --version

### Criando docker-compose.yaml para parametros do jenkins Server

cd /opt

cat > docker-coimpose  
version: '3.7'
services:
  jenkins:
    image: jenkins/jenkins:lts
    privileged: true
    user: root
    ports:
      - 8000:8080
      - 50003:50000
    container_name: jenkins
    volumes:
      - ./jenkins_data:/var/jenkins_home
      - /var/run/docker.sock:/var/run/docker.sock

> Digite Ctrl + c para terminar a edição

## Instalando Nexus

version: '3.7'
services:
  nexus:
    image: sonatype/nexus3
    privileged: true
    user: root
    ports:
      - 8081:8081
    container_name: nexus
    command: /bin/bash -c "nexus.sh"
    volumes:
      - nexus-data:/nexus-data  


## instalando minikube no host do jenkins

sudo apt-get update -y && sudo apt-get upgrade -y


sudo apt-get install curl  apt-transport-https -y && sudo apt install virtualbox virtualbox-ext-pack -y

#### Baixando minikube

wget https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64

sudo cp minikube-linux-amd64 /usr/local/bin/minikube

sudo chmod 755 /usr/local/bin/minikube

sudo ln -s /usr/local/bin/minikube /usr/bin/

minikube version

## Instalando Kubectl

curl -LO https://storage.googleapis.com/kubernetes-release/release/`curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt`/bin/linux/amd64/kubectl

chmod +x ./kubectl

sudo mv ./kubectl /usr/bin/kubectl

kubectl version -o json

minikube start

kubectl config view

kubectl cluster-info

kubectl get nodes


kubectl get pod


minikube ssh

exit
