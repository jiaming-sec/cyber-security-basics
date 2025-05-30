# Networking Fundamentals

## OSI Model
The OSI ("Open Systems Interconnection") model represents an easy and intuitive way to standardize the different parts required to communicate across networks.
| Layer       | Description |
|-------------|-------------|
| Layer 7     | Application (includes API, HTTP, etc.) - Where humans process data and information |
| Layer 6     | Presentation - Ensures data is in a usable format |
| Layer 5     | Session - Capable of maintaining connections|
| Layer 4     | Transport (TCP/UDP) - Data is forwarded to a service capable of handling requests |
| Layer 3     | Network (Routing) - 	Responsible for which path packets should travel on a network |
| Layer 2     | Data Link (Error checking, frame synchronization) - Responsible for which physical devices packets should go to |
| Layer 1     | Physical (Bits over fibre) - 	The physical infrastructure to transport data |

Layer 4, the Transport layer, connects the software with the hardware layers.

Layer 7 - Application Layer
The business logic and functionality of the application lies here. This is what the users use to interact with services across a network. 

Most of the applications you use are on the Application Layer, with the complexity of the other layers hidden.

Examples of Layer 7 Applications:

- HTTP ("Hypertext Transfer Protocol") - Enables us to access web applications
- FTP ("File Transfer Protocol") - Allows users to transfer files
- SNMP ("Simple Network Management Protocol") - Protocol to read and update network device configurations
There are many applications which uses these protocols like Google Chrome, Microsoft Skype and FileZilla.

---

## Firewalls

- Rules to prevent incoming and outgoing connections.
(A firewall is a network security device that acts as a barrier between a trusted internal network and an untrusted external network, such as the internet. It monitors and controls network traffic, blocking or allowing data packets based on a set of security rules.)

## NAT

- Useful to understand IPv4 vs IPv6.(A NAT (Network Address Translation) device, typically a router or firewall, translates these private IP addresses into a public IP address (assigned by the ISP) when sending data to the internet. )

---

## DNS (Port 53)
(From client -> Recursive DNS resolver -> DNS Root Nameserver -> DNS TLD nameserver -> Authoritative Server)
- Requests are usually UDP unless redirected to TCP.
- DNS cache lookup happens first.
- DNS exfiltration: sending data as subdomains (e.g., `26856485f6476a567567c6576e678.badguy.com`).
- Reverse DNS Lookup (PTR): e.g., `2.152.80.208.in-addr.arpa → 208.80.152.2`.
- DNS sinkholes to detect/block malicious domains.

## DNS exfiltration
(a technique used by attackers to steal data from a network by embedding it within DNS queries.)
- Sending data as subdomains.
- 26856485f6476a567567c6576e678.badguy.com
- Doesn’t show up in http logs.
### DNS Configs

- **SOA** – Start of Authority (Indicates the authoritative DNS server for a domain or subdomain and provides administrative details like the domain's administrator email, serial number, and time-to-live (TTL) settings.) 
- **A / AAAA** – IP addresses  
- **MX** – Mail Exchangers  
- **NS** – Name Servers  
- **PTR** – Reverse DNS  
- **CNAME** – Aliases  

---

## ARP

- Maps MAC addresses to IP addresses.

---

## DHCP (UDP 67 - Server, 68 - Client)

- Dynamic IP address allocation.
- Process: `DHCPDISCOVER → DHCPOFFER → DHCPREQUEST → DHCPACK`.

---

## Multiplexing

- Timeshare, statistical sharing – useful to understand.

---

## Traceroute

- Uses UDP, ICMP Echo Request, or TCP SYN.
- TTL (Time-to-Live) / hop-limit:  
  - Windows: 128  
  - Linux/Unix: 64  
- Destination returns ICMP Echo Reply.

---

## Nmap

- Network scanning tool.

---

## Intercepts (Person-in-the-Middle)

- Understand Public Key Infrastructure (PKI).

---

## VPN

- Hides traffic from ISP.
- Traffic is exposed to VPN provider.

---

## Tor

- Easily detectable on a network.
- Law enforcement may use traffic correlation to identify users.

---

## Proxy

- Why using "7 proxies" won't help hide you completely.

---

## BGP (Border Gateway Protocol)

- The protocol that keeps the internet routing together.

---

## Network Traffic Tools

- **Wireshark**  
- **Tcpdump**  
- **Burp Suite**
