# Cybersecurity Networking Notes

## 1. Public vs Private IP Addresses

**Public IP:** An IP address that is globally routable on the internet. It is commonly assigned by an ISP or cloud provider.

**Private IP:** Used within private networks such as homes, colleges, and offices. Private IPv4 addresses are not globally routable on the public internet.

**Private IPv4 ranges (RFC 1918):**
- `10.0.0.0/8`
- `172.16.0.0/12`
- `192.168.0.0/16`

**NAT (Network Address Translation):** Commonly translates private source IP addresses to a public address for internet access.

**Cybersecurity relevance:** Network reconnaissance, firewall configuration, and network segmentation.

---

## 2. Localhost

**Localhost** is a hostname that normally resolves to the loopback addresses of the local computer.

- IPv4: `127.0.0.1`
- IPv6: `::1`

Example:

`http://localhost:8000`

This accesses a web service running on port 8000 of the same computer.

**Key points:**
- Used for local application development and testing.
- Does not require traffic to travel to another computer.
- A port identifies a service endpoint.
- Localhost does not automatically make an application secure.

**Cybersecurity relevance:** Local web application testing, API development, and security lab environments.

---

## 3. Loopback

**Loopback** is a networking mechanism that allows a device to communicate with itself.

- IPv4 loopback range: `127.0.0.0/8`
- Common IPv4 address: `127.0.0.1`
- IPv6 loopback address: `::1`

Example command:

```bash
ping 127.0.0.1
```

A successful response indicates that local loopback communication is working, but it does not confirm internet connectivity.

**Difference:** Loopback is the mechanism or address range; `localhost` is the hostname commonly used to access it.

**Cybersecurity relevance:** Local network troubleshooting and application testing.

---

## 4. CIDR (Classless Inter-Domain Routing)

**CIDR** represents IP networks using a prefix length instead of traditional class-based addressing.

Example: `192.168.1.0/24`

- IPv4 contains 32 bits.
- `/24` means 24 network bits and 8 host bits.
- A larger prefix generally means a smaller subnet.

**Common prefixes:**

| CIDR | Subnet Mask | Usable Hosts* |
|---|---|---:|
| `/24` | `255.255.255.0` | 254 |
| `/25` | `255.255.255.128` | 126 |
| `/26` | `255.255.255.192` | 62 |
| `/27` | `255.255.255.224` | 30 |
| `/28` | `255.255.255.240` | 14 |

Formula for conventional IPv4 subnets:

`Usable hosts = 2^(32 - prefix) - 2`

*The usual formula excludes network and broadcast addresses; special cases such as `/31` differ.*

**Cybersecurity relevance:** IP range identification, firewall rules, routing, cloud networking, and authorized network scanning.

---

## 5. Subnet Mask

A **subnet mask** identifies the network and host portions of an IPv4 address.

Example:

```text
IP Address:  192.168.1.10
Subnet Mask: 255.255.255.0
CIDR:        /24
```

In binary, mask bits set to `1` represent the network portion, while bits set to `0` represent the host portion.

**Important formulas:**

- Host bits = `32 - prefix length`
- Conventional usable hosts = `2^(host bits) - 2`
- Block size = `256 - mask value` in the octet where the subnet boundary occurs

Example: `/26` has 6 host bits, giving 64 total addresses and 62 conventional usable host addresses.

**Cybersecurity relevance:** Network troubleshooting, subnet identification, IP allocation, firewall rules, and network segmentation.

---

## 6. Default Gateway

A **default gateway** is usually a router that forwards traffic toward destinations outside the local subnet when no more specific route applies.

Example:

```text
IP Address:      192.168.1.10
Subnet Mask:     255.255.255.0
Default Gateway: 192.168.1.1
```

- Local destination: Usually communicated with directly over the local network.
- Remote destination: Normally forwarded to the default gateway.

**Find the gateway:**

Windows:
```bash
ipconfig
```

Linux:
```bash
ip route
```

**Difference:**
- IP address: Identifies a network interface logically.
- Subnet mask: Defines the local IP subnet.
- Default gateway: Provides a route toward other networks.
- DNS: Resolves domain names to IP addresses.

**Cybersecurity relevance:** Routing troubleshooting, network monitoring, and detecting suspicious gateway or routing changes.
