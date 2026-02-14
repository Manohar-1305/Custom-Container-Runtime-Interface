# Build own Container Runtime Interface
**Refresh package index**
```bash
sudo apt update
```

**Enable bridge network filtering (required for container networking)**
```
sudo modprobe br_netfilter
```
**Load Kernel Modules**
```
modprobe overlay
```

**Enable IP forwarding (allow host to route container traffic)**
```
sudo sysctl -w net.ipv4.ip_forward=1
```
**PUll Images**
![1](https://github.com/user-attachments/assets/1e46f6e4-f7fb-4940-b67a-4a1d438603ea)
![1](https://github.com/user-attachments/assets/1e46f6e4-f7fb-4940-b67a-4a1d438603ea)


