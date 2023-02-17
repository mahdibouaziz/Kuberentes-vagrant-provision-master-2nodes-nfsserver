# Steps 


containerd config default | sudo tee /etc/containerd/config.toml

Usethis version (latest one)
1.26.1-00

sudo apt-get install -y kubelet=1.26.1-00  kubeadm=1.26.1-00 kubectl=1.26.1-00

kubeadm init --apiserver-advertise-address=192.168.56.2 --pod-network-cidr=172.30.0.0/16 

kubeadm join 192.168.56.2:6443 --token xqs8bm.vvanp2jdgtmwrymr --discovery-token-ca-cert-hash sha256:060676155e31ef5fce30f37ffbe265adf4bc840ad505b301804c5076de841729 --v=2


addons solution
wget https://github.com/weaveworks/weave/releases/download/v2.8.1/weave-daemonset-k8s.yaml 
then apply