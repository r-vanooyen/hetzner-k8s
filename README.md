# hetzner

// need to be checked with this tutorial https://community.hetzner.com/tutorials/install-kubernetes-cluster
sources: 
- https://medium.com/geekculture/5-steps-to-auto-install-k8s-with-cloud-config-ad2935c559c7

## setup nodes with 
- disabled ipv4
- cloud-init script https://gist.github.com/ngaffa/15d46c98dd82620c8120ddf7398d6dbd
- network


## on master node
- remove default containerd config `rm /etc/containerd/config.toml` https://github.com/containerd/containerd/issues/4581 and restart `systemctl restart containerd`
- `sudo kubeadm init --pod-network-cidr=LOCALNETWORK/SUBNET`
