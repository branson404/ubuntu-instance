### Installing minikube:

    sudo apt update && sudo apt upgrade -y
    sudo apt install -y curl wget apt-transport-https

## Install Docker  (if using Docker driver).

    sudo apt-get install docker.io -y
    sudo systemctl start docker
    sudo systemctl enable docker
    sudo usermod -aG docker $USER && newgrp docker

## Install Minikube

    curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
    sudo install minikube-linux-amd64 /usr/local/bin/minikube

## Verify minikube

    minikube version

## Start minikube

    minikube start --driver=docker

## (You can specify other drivers like --driver=virtualbox or --driver=kvm2 if you have them installed.) Check Minikube Status.

    minikube status

## Install appropriate kubectl

    minikube kubectl -- get po -A
