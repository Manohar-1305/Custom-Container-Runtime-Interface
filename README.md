sudo apt update                                  # Refresh package index from configured repositories

sudo apt install -y runc skopeo umoci iproute2 iptables jq   # Install container runtime, image tools, networking utilities, and JSON processor

sudo modprobe overlay                            # Load OverlayFS kernel module (required for layered container filesystems)

sudo modprobe br_netfilter                       # Enable bridge network filtering for container networking

sudo sysctl -w net.ipv4.ip_forward=1             # Enable IP forwarding so the host can route container traffic
