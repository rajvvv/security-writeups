# Essential Network Services

## 1. DHCP (Dynamic Host Configuration Protocol)
DHCP automatically assigns network configuration to devices.

It can provide:
- IP address
- Subnet mask
- Default gateway
- DNS server address

**Example:** When a laptop connects to hostel Wi-Fi, DHCP assigns it an IP address.

**Cybersecurity:** A rogue DHCP server could provide incorrect network settings and redirect traffic.

## 2. DNS (Domain Name System)
DNS translates domain names into IP addresses.

**Example:** DNS helps your device find the IP address associated with `google.com`.

**Cybersecurity:** DNS spoofing can redirect users to malicious websites. DNS filtering can help block known malicious domains.

## 3. IPAM (IP Address Management)
IPAM helps administrators plan, track, and manage IP addresses across a network.

It helps with:
- Tracking assigned and available IP addresses.
- Preventing accidental address conflicts.
- Maintaining IP address records.
- Organizing subnets.

**Example:** A college IT team uses IPAM to track IP addresses assigned to students, servers, and CCTV cameras.

**Cybersecurity:** Accurate IP records help administrators identify devices and investigate suspicious network activity.

## 4. NTP (Network Time Protocol)
NTP synchronizes device clocks with a common time source.

**Example:** A server and firewall use synchronized time so their event logs can be compared accurately.

**Cybersecurity:** Correct timestamps are important for investigating incidents and correlating security logs.

## Quick Comparison

| Service | Main Function |
|---|---|
| DHCP | Assigns network configuration automatically |
| DNS | Resolves domain names to IP addresses |
| IPAM | Manages and tracks IP address allocation |
| NTP | Synchronizes device clocks |

## Remember
- DHCP = Configuration.
- DNS = Name resolution.
- IPAM = Address management.
- NTP = Time synchronization.
