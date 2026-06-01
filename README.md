# Hybrid-Virtualized-Network-Infrastructure-pfSense-Proxmox-VLANs-IPv4-IPv6-Embedded-Linux-

Designed and implemented a multi-layer dual-stack (IPv4/IPv6) network infrastructure lab simulating enterprise-style segmentation and routing using pfSense on Proxmox, VLAN segmentation, WireGuard VPN, and a proprietary vendor-customized embedded Linux ISP edge router.

The environment includes routed VLAN domains with isolated network zones, inter-VLAN security boundaries, NAT (IPv4), IPv6 SLAAC/RA, and centralized services including DNS filtering and time synchronization. The architecture integrates upstream ISP routing with a virtualized firewall stack and repurposed legacy networking hardware as Layer 2 switching infrastructure.

Performed low-level reverse engineering of vendor-specific VLAN implementation on stripped embedded Linux router firmware via UART serial console access. Mapped switch ASIC VLAN tables to Linux bridge/interface configurations beyond OEM management capabilities, enabling custom topology design not exposed in the official interface.

Implemented persistent system modifications via embedded Linux boot script changes and resolved firmware-level time synchronization issues using internal NTP infrastructure. Created firmware “golden images” of router flash (MTD partitions) with cryptographic hash verification for rollback and recovery of system states after low-level changes.

Deployed WireGuard VPN tunnels for secure remote access into segmented networks, implemented centralized DNS filtering (pfBlockerNG), and resolved IPv6/DHCPv6 service conflicts between upstream ISP equipment and internal routing.

Technologies: pfSense, Proxmox VE, Embedded Linux, proprietary ISP firmware, WireGuard, IPv4/IPv6, VLANs, NAT, DHCP, IPv6 RA, DNS, NTP, UART serial access, BusyBox, network security, virtualization.
