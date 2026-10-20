# Common Network Protocols

A network protocol defines rules that devices use to communicate. Some protocols transfer files, some provide remote access, and others protect web traffic.

## 1. SSH (Secure Shell)
SSH provides encrypted remote access, commonly to a command-line interface on another computer or server.

- **Default port:** TCP 22
- **Example:** Connecting to a Linux server remotely.
- **Security:** Use strong authentication, protect private keys, and restrict access.

## 2. RDP (Remote Desktop Protocol)
RDP allows users to control a remote computer through a graphical desktop.

- **Default port:** TCP 3389; UDP may also be used.
- **Example:** Remotely accessing a Windows computer.
- **Security:** Exposing RDP directly to the internet increases risk. Use VPNs or secure gateways, strong authentication, and access restrictions.

## 3. FTP (File Transfer Protocol)
FTP transfers files between a client and a server.

- **Control connection:** TCP 21
- **Example:** Uploading files to a traditional FTP server.
- **Security:** Standard FTP does not encrypt credentials or file contents. Avoid using it for sensitive transfers over untrusted networks.

## 4. SFTP (SSH File Transfer Protocol)
SFTP securely transfers and manages files over an SSH connection.

- **Common port:** TCP 22
- **Example:** Uploading files securely to a Linux server.
- **Security:** Protect SSH credentials and restrict account permissions.

**Important:** SFTP is not the same as FTPS. SFTP operates over SSH, while FTPS adds TLS security to FTP.

## 5. SSL/TLS
TLS (Transport Layer Security) protects data exchanged between applications by providing encryption and integrity, and it can authenticate the server.

- **SSL:** An older protocol that is obsolete and should not be used.
- **TLS:** The modern successor to SSL.
- **Example:** TLS protects connections to HTTPS websites.
- **Security:** Use current TLS configurations and validate certificates correctly.

## 6. HTTP (Hypertext Transfer Protocol)
HTTP is used to exchange web content between browsers and web servers.

- **Default port:** TCP 80
- **Example:** Loading a web page.
- **Security:** Plain HTTP does not provide transport encryption, so data can be exposed or altered in transit.

## 7. HTTPS (HTTP Secure)
HTTPS is HTTP protected by TLS.

- **Default port:** TCP 443
- **Example:** Logging into a website over an encrypted connection.
- **Security:** HTTPS protects data in transit, but it does not automatically mean a website is legitimate or safe.

## Quick Comparison

| Protocol | Main Purpose | Common Port |
|---|---|---|
| SSH | Secure remote command-line access | TCP 22 |
| RDP | Remote graphical desktop | TCP 3389 |
| FTP | File transfer without built-in encryption | TCP 21 for control |
| SFTP | Secure file transfer over SSH | TCP 22 |
| TLS | Protects application data in transit | Depends on the application |
| HTTP | Web communication without TLS | TCP 80 |
| HTTPS | Web communication protected by TLS | TCP 443 |

## Cybersecurity Revision
- Prefer SSH over insecure remote administration methods.
- Use SFTP or another properly secured file-transfer method instead of plain FTP.
- Secure RDP using restricted access and strong authentication.
- Use HTTPS and current TLS configurations for web traffic.
- Never assume HTTPS alone proves that a website is trustworthy.

## Remember
SSH = Secure shell access.  
RDP = Remote graphical desktop.  
FTP = Traditional file transfer.  
SFTP = File transfer over SSH.  
TLS = Transport security.  
HTTP = Web communication.  
HTTPS = HTTP protected by TLS.
