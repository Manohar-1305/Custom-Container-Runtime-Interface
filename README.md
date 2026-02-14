**Prerequisites**

__Refresh package index__

```
sudo apt update
```

** Install container runtime and required tools**
```
sudo apt install -y runc skopeo umoci iproute2 iptables jq
```

Load OverlayFS kernel module (for layered container filesystems)

sudo modprobe overlay


Enable bridge network filtering (required for container networking)

sudo modprobe br_netfilter


Enable IP forwarding (allow host to route container traffic)

sudo sysctl -w net.ipv4.ip_forward=1
