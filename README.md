# Local Kubernetes cluster with Vagrant

This repo contains a Vagrantfile and a set of shell scripts to help you create a local Kubernetes cluster using Vagrant and VirtualBox. This is very useful for people willing to take CKA/CKAD/CKS exams.

Most of the work was forked from [techiescamp/vagrant-kubeadm-kubernetes](https://github.com/techiescamp/vagrant-kubeadm-kubernetes/tree/main). The main difference is that this project uses containerd instead of cri-o, and Kubernetes dashboard is not available.

Some names were also changed to make it inclusive, example: Master to Control Plane.

## Prerequisites

* [Vagrant](https://www.vagrantup.com/downloads)
* [VirtualBox](https://www.virtualbox.org/wiki/Downloads)

## Usage

1. Clone this repo
2. Change the `config.yaml` file to your needs
   1. This is important to change how much memory and CPU each VM will have and to set some components versions
3. Run `vagrant up` to create the VMs
4. Copy the `kubeconfig` file to your local machine

### To stop or shutdown the cluster

Run `vagrant halt` to stop the VMs or `vagrant suspend` to suspend them.

### To destroy the cluster

Run `vagrant destroy -f` to destroy the VMs.
