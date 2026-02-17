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
**Pocker Pull**

![1](https://github.com/user-attachments/assets/1e46f6e4-f7fb-4940-b67a-4a1d438603ea)


**Pocker Images**

<img width="682" height="78" alt="image" src="https://github.com/user-attachments/assets/35cdac4c-7c98-48b9-b956-1c4ffcf8f0c6" />


**Pull Images**

<img width="640" height="185" alt="image" src="https://github.com/user-attachments/assets/f0c67b48-97e9-4388-b502-147f77f4650f" />

**Pocker run**

```
pocker run ubuntu:latest
pocker run nginx:latest
```

**Pocker PS**

<img width="611" height="137" alt="image" src="https://github.com/user-attachments/assets/8e0b5c44-7e30-4c7d-bf6a-380de10c23b3" />

**You can possibly read the blog below**

https://medium.com/@tradingcontentdrive/building-a-minimal-oci-container-runtime-from-scratch-using-shell-script-no-docker-no-magic-b07ee9e088da
