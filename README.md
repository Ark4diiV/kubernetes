# Kubernetes
## Deploy Kubernetes into 2 nodes
This playbook was made for study purpose. It was tested on Ubuntu 22.04 aarch64 but probably work on amd64. It uses containerd container runtime and flannel CNI plugin.   
Pod cidr and service cidr into kubernetes-masters/vars/main.yaml variables.   
Installation playbook will install:
- conainerd (latest)
- kubeadm (1.24.3-00)
- kubectl (1.24.3-00)
- kubelet (1.24.3-00)
- flannel (0.19.0)

## Prerequesites
Ansible modules:
- ansible.posix

## Deploy Kubernetes
`aplaybook -i inventory k8s-deploy.yml`   

## Reset cluster and purge everything
`aplaybook -i inventory k8s-reset.yml`