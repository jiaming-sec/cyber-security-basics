# Networking Fundamentals

## OSI Model
The OSI ("Open Systems Interconnection") model represents an easy and intuitive way to standardize the different parts required to communicate across networks.
| Layer       | Description |
|-------------|-------------|
| Layer 7     | Application (includes API, HTTP, etc.) - Where humans process data and information |
| Layer 6     | Presentation - Ensures data is in a usable format |
| Layer 5     | Session - Capable of maintaining connections|
| Layer 4     | Transport (TCP/UDP) |
| Layer 3     | Network (Routing) |
| Layer 2     | Data Link (Error checking, frame synchronization) |
| Layer 1     | Physical (Bits over fibre) |

---

## Firewalls

- Rules to prevent incoming and outgoing connections.

## NAT

- Useful to understand IPv4 vs IPv6.

---

## DNS (Port 53)

- Requests are usually UDP unless redirected to TCP.
- DNS cache lookup happens first.
- DNS exfiltration: sending data as subdomains (e.g., `26856485f6476a567567c6576e678.badguy.com`).
- Reverse DNS Lookup (PTR): e.g., `2.152.80.208.in-addr.arpa → 208.80.152.2`.
- DNS sinkholes to detect/block malicious domains.

### DNS Configs

- **SOA** – Start of Authority  
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
