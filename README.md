# Jenkins Exercise

### Description

Jenkins pipeline (declarative) that runs two stages:
- Python main.py app inside docker container
- Python main.py app inside K8S cluster

### Environment:

This assignment was tested against the following environment (internal network behind firewall):

- CentOS Linux 7 VM
- 16 GBs Ram
- 4 CPU Cores
- 100 GB Disk
- Minikube version v1.25.1
- Jenkins 2.277 

### Prerequisites:

- Jenkins Server
- Minikube cluster running
- Kubernetes cloud needs to be setup in Jenkins Server with Token
