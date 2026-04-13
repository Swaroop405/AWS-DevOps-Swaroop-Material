
=============================FINAL STEPS TO INSTALL MINIKUBE==================================
dnf install -y kubelet kubeadm


systemctl enable --now kubelet


swapoff -a


sed -i '/swap/d' /etc/fstab


minikube delete


minikube start --driver=none


kubectl get nodes


systemctl start docker

systemctl enable docker

docker ps

minikube delete

minikube start --driver=docker --force

chmod 666 /var/run/docker.sock

kubectl get nodes
