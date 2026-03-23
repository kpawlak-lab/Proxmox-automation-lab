### 🛠 Phase 1: Core Infrastructure (COMPLETED 2026-03-23)
- **Hypervisor Setup:** Configured Proxmox VE on physical hardware (Intel i5-8600K).
- **Network Virtualization:** Implemented two Linux Bridges (`vmbr0` for WAN, `vmbr1` for isolated SOC LAN).
- **Firewall Deployment:** - Installed OPNsense with ZFS file system.
    - Assigned virtual interfaces (`vtnet0` -> WAN, `vtnet1` -> LAN).
    - Configured DHCP server for the internal 192.168.1.0/24 subnet.
- **Management Node:** Initiated deployment of Kubuntu-based workstation within the isolated segment to manage the environment.
