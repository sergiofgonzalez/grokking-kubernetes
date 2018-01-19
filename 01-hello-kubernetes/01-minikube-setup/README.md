# 01 &mdash; Setting up minikube
> creating Docker images with a Dockerfile

## Description
This document describes how to setup minikube on a native Linux host.

Follow documentation from https://github.com/kubernetes/minikube

Type:
```bash
curl -Lo minikube https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64 && chmod +x minikube && sudo mv minikube /usr/local/bin/
```

then 
```bash
sudo minikube start --vm-driver=none
```

Then kubectl:
```bash
curl -Lo kubectl https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl && chmod +x kubectl && sudo mv kubectl /usr/local/bin/
```

To uninstall:
```bash
$ sudo minikube stop
$ sudo minikube delete
$ sudo rm /usr/local/bin/localkube /usr/local/bin/minikube
$ sudo rm /
$ sudo rm -rf ~/.kube/ ~/.minikube/
```

