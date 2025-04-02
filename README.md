# Proxmox-lab
# Proxmox Wi-Fi Adapter Passthrough to Kali Linux(other operating systems)
This guide demonstrates how to pass a **Realtek RTL88x2bu Wi-Fi adapter** to a Kali Linux VM in Proxmox.

1. **Edit VM Configuration**:  
   Open the VM configuration file located at `/etc/pve/qemu-server/<vmid>.conf` and add:  
   `usb0: host=0bda:b812` (Replace `<vmid>` with your VM ID).

2. **Restart the VM**:  
   Run `qm reboot <vmid>` to apply changes.
   Run reboot pvenode if possible, and if the above reboot does not work.

4. **Verify in Kali**:  
   After rebooting, check with `lsusb` to ensure the adapter is recognized. Then, use `iwconfig` and `ifconfig` to confirm the interface.
---
