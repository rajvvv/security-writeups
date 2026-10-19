# Networking Terminology

## 1. VLAN (Virtual Local Area Network)
A VLAN logically divides a physical switched network into separate Layer 2 broadcast domains.

- Groups devices logically, regardless of their physical location.
- Devices in different VLANs generally need Layer 3 routing to communicate.
- **Security use:** Network segmentation and access control.

**Example:** VLAN 10 for students, VLAN 20 for administration.

## 2. DMZ (Demilitarized Zone)
A DMZ is a separate network segment used to host services accessible from less-trusted networks, such as the internet.

- Firewalls control traffic between the internet, DMZ, and internal network.
- Limits exposure of internal systems if a public-facing service is compromised.
- **Security use:** Protecting internal resources.

**Example:** Hosting a public web server in a DMZ.

## 3. ARP (Address Resolution Protocol)
ARP resolves an IPv4 address to a MAC address on a local network.

- Sends a broadcast request when the MAC address is unknown.
- Stores discovered IP-to-MAC mappings in an ARP cache.
- **Security risk:** ARP spoofing can redirect or disrupt local network traffic.

**Example:** Finding the router's MAC address for `192.168.1.1`.

## 4. VM (Virtual Machine)
A VM is a software-based computer that runs an operating system using virtualized hardware.

- Managed by a hypervisor such as VirtualBox or VMware.
- Can run a different operating system from the host.
- **Security use:** Isolated practice labs, penetration testing, and malware analysis.

**Example:** Running Kali Linux inside Windows.

## 5. DHCP (Dynamic Host Configuration Protocol)
DHCP automatically provides devices with IP configuration, such as an IP address, subnet mask, gateway, and DNS server.

**IPv4 DORA process:**
- Discover
- Offer
- Request
- Acknowledge

**Security risk:** A rogue DHCP server can provide malicious network settings.

**Example:** Automatically assigning an IP address when joining Wi-Fi.

## 6. DNS (Domain Name System)
DNS translates domain names into records, including IP addresses.

- Helps devices locate internet and internal services.
- Common record types include A, AAAA, CNAME, and MX.
- **Security use:** DNS filtering, malicious-domain detection, and investigation of suspicious traffic.

**Example:** Resolving `example.com` to an IP address.

## 7. NAT (Network Address Translation)
NAT modifies IP address information as packets pass through a network device.

- Commonly translates private source IP addresses to a public-facing address.
- Helps multiple devices share a public IPv4 address.
- **Security note:** NAT is not a replacement for a firewall.

**Example:** A router translating `192.168.1.10` to its public-facing address.

## 8. IP (Internet Protocol)
IP provides logical addressing and packet delivery across interconnected networks.

- IPv4 uses 32-bit addresses.
- IPv6 uses 128-bit addresses.
- Routers forward packets based on destination IP addresses and routing tables.
- **Security use:** Network monitoring, traffic analysis, and firewall rules.

**Example:** `192.168.1.10` is an IPv4 address.

## 9. Router
A router forwards IP packets between different networks using a routing table.

- Connects networks and determines the next hop for traffic.
- Often acts as the default gateway for local devices.
- **Security use:** Routing controls, firewall policies, and network isolation.

**Example:** A home router forwarding traffic to an ISP.

## 10. Switch
A typical Layer 2 Ethernet switch forwards frames using MAC addresses.

- Learns which MAC addresses are reachable through its ports.
- Connects devices within a LAN.
- Managed switches can support VLANs and port-security features.
- **Security use:** Network segmentation and limiting unauthorized access.

**Example:** Connecting computers and printers in an office.

## 11. VPN (Virtual Private Network)
A VPN creates a logical connection between endpoints, commonly using encryption and authentication to protect traffic.

- Enables secure remote access to private resources.
- Can route some or all device traffic through a tunnel.
- **Security note:** A VPN does not guarantee anonymity or protect against every attack.

**Example:** Connecting to a university network remotely.

---

## Quick Revision

| Term | Main purpose |
|---|---|
| VLAN | Separates Layer 2 broadcast domains |
| DMZ | Segments exposed services |
| ARP | Resolves local IPv4 addresses to MAC addresses |
| VM | Runs a virtual computer |
| DHCP | Automatically provides IP configuration |
| DNS | Resolves domain names into records |
| NAT | Translates IP address information |
| IP | Provides logical addressing and packet delivery |
| Router | Forwards packets between networks |
| Switch | Forwards Ethernet frames within a LAN |
| VPN | Creates a logical tunnel, commonly encrypted |
