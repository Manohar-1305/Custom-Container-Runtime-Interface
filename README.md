* Prerequisites

Run the following on the host:

sudo apt update
sudo apt install -y runc skopeo umoci iproute2 iptables jq

sudo modprobe overlay
sudo modprobe br_netfilter

sudo sysctl -w net.ipv4.ip_forward=1

Make kernel settings persistent (recommended)
echo "overlay" | sudo tee /etc/modules-load.d/pocker.conf
echo "br_netfilter" | sudo tee -a /etc/modules-load.d/pocker.conf

echo "net.ipv4.ip_forward=1" | sudo tee /etc/sysctl.d/99-pocker.conf
sudo sysctl --system
