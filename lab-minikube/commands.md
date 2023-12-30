# Boxes centos 7 - minikube 1.14.0 - kubernetes 1.23.1

A vagrant box is available here : https://app.vagrantup.com/bstephsorel/boxes/centos7-minikube/versions/1.0

Below a subset of the command used to install minikube 1.14.1 / kubernetes 1.23.1.

# Commands used to install minikube 1.14.1 / kubernetes 1.23.1

`sudo yum -y update`

`sudo yum -y install epel-release`

`sudo yum -y install git libvirt qemu-kvm virt-install virt-top libguestfs-tools bridge-utils`

`sudo yum install socat -y`

`sudo yum install -y conntrack`

`sudo curl -fsSL https://get.docker.com -o get-docker.sh`

`sudo sh get-docker.sh`

`sudo usermod -aG docker vagrant`

`sudo systemctl start docker`

`sudo yum -y install wget`

`sudo wget https://storage.googleapis.com/minikube/releases/v1.14.1/minikube-linux-amd64`

`sudo chmod +x minikube-linux-amd64`

`sudo mv minikube-linux-amd64 /usr/bin/minikube`

`sudo curl -LO https://storage.googleapis.com/kubernetes-release/release/v1.23.1/bin/linux/amd64/kubectl`

`sudo chmod +x kubectl`

`sudo mv kubectl /usr/bin/`

`sudo echo '1' > /proc/sys/net/bridge/bridge-nf-call-iptables`

`sudo systemctl enable docker.service`

`minikube start --driver=none --kubernetes-version v1.23.1`

for autocompletion :

`echo 'source <(kubectl completion bash)' >> ${HOME}/.bashrc && source ${HOME}/.bashrc`

