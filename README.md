**Refresh package index**
```bash
sudo apt update
```


# Enable bridge network filtering (required for container networking)
```
sudo modprobe br_netfilter
```

# Enable IP forwarding (allow host to route container traffic)
```
sudo sysctl -w net.ipv4.ip_forward=1
```
