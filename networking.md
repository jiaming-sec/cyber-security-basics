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

## NAT (Network Address Translation)

- Useful to understand IPv4 vs IPv6.(A NAT device, typically a router or firewall, translates these private IP addresses into a public IP address (assigned by the ISP) when sending data to the internet. )

---

## DNS (Port 53) - Domain Name System
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
- **A / AAAA** – IP addresses (A (Address): Maps a domain name to a IPv4 address. / AAAA (Quad-A): Maps a domain name to an IPv6 address. )
- **MX** – Mail Exchangers ( Specifies the mail servers responsible for receiving email for a domain. )
- **NS** – Name Servers (Identifies the DNS servers that are authorized to provide information about the domain. ) 
- **PTR** – Reverse DNS  (Maps an IP address back to its domain name, used for reverse lookups. )
- **CNAME** – Aliases  (the primary or preferred domain name for a particular web server or set of resources)

---

## ARP - Address Resolution Protocol

- Maps MAC addresses to IP addresses.(ARP is a communication protocol used to map IP addresses (logical addresses) to MAC addresses (physical addresses) on a local network. )
- Like: "Hey network, who has 192.168.1.10?"
--  Device with that IP responds: "Me! My MAC is XX:XX:XX:XX."
---

## DHCP (UDP 67 - Server, 68 - Client) - Dynamic Host Configuration Protocol
- DHCP gives devices IP addresses automatically.
- Dynamic IP address allocation.
- Process: `DHCPDISCOVER → DHCPOFFER → DHCPREQUEST → DHCPACK`.
- DHCPDISCOVER – Device shouts: "Anyone give me an IP?"
- DHCPOFFER – Server replies: "Here’s one."
- DHCPREQUEST – Device says: "I’ll take it."
- DHCPACK – Server confirms.

---

## Multiplexing

- Multiplexing is sharing one line for multiple data streams.
- Example: 1 cable carries multiple Zoom calls or streams （allows better bandwidth use）

---

## Traceroute
(a network diagnostic tool that displays the path packets take when traveling from a source to a destination across an IP network)
- Uses UDP, ICMP Echo Request, or TCP SYN.
- TTL (Time-to-Live) / hop-limit:  
  - Windows: 128  
  - Linux/Unix: 64
  - Uses:
  - ICMP Echo Requests (ping-style)
  - UDP/TCP with increasing TTL (Time to Live).
Useful for network troubleshooting and latency checks

---

## Nmap

- Network scanning tool.
- What devices are on a network (e.g., IPs, MACs),
- Which ports are open,
- What services or OS versions are running.
  
Example use cases
- Find vulnerable hosts (e.g., open SSH without patching).
- Detect unauthorized devices on a corporate network.
- Run stealth scans to avoid detection (e.g., nmap -sS).
---

## Intercepts (Person-in-the-Middle)
MITM attack is when someone secretly sits between two parties communicating, like intercepting messages between your computer and a website.
- A rogue Wi-Fi hotspot at a coffee shop fakes being “FreeCafeWiFi” and reads your traffic.
- PKI (Public Key Infrastructure): Ensures secure encryption and digital identity verification.
- Certificate Authority (CA): Trusted org that issues certificates (e.g., DigiCert).
- Private/Public Key Pairs: For asymmetric encryption.
- Digital Signatures: Ensure authenticity.

---

## VPN (Virtual Private Network)
A VPN creates an encrypted tunnel between your device and a VPN server.
- ISP sees encrypted gibberish; it can’t tell what websites you visit.
- VPN provider can see your traffic — so you need to trust your VPN.

---

## Tor (The Onion Router)
Tor anonymizes your traffic by routing it through multiple volunteer-run nodes.
- Easily detectable on a network.
- Law enforcement may use traffic correlation to identify users.

---

## Proxy
A proxy acts as a middleman between you and the internet.(When you use a forward proxy server, the server is not aware of the actual client and thinks the proxy is the client)
- Can cache content, filter traffic, or hide your IP.
- E.g., You → Proxy → Google (Google sees the proxy’s IP).

---

## BGP (Border Gateway Protocol)
a critical routing protocol that facilitates communication between different network systems on the internet. BGP is the postal system of the internet. It ensures that data packets can find the most efficient path to their destination across interconnected networks.
- The protocol that keeps the internet routing together.

---

## Network Traffic Tools

- **Wireshark**  - Graphical tool for analyzing packets (e.g., DNS, HTTP, TCP handshakes).
- **Tcpdump**  - Command-line version of Wireshark. Fast for automation/scripting.
- **Burp Suite** - 	Web security testing tool. Can intercept, modify, and replay HTTP/S requests. Used in AppSec.
