# Wireshark-
Filter of wireshark 
video of network analyzing using wireshark filters
Wireshark is a popular open-source network protocol analyzer used for capturing and analyzing network traffic in real time. It helps with troubleshooting network issues, security analysis, and understanding network protocols.

Key Features of Wireshark:
Packet Capture: Captures live network traffic or reads previously captured packets.

Protocol Analysis: Supports hundreds of network protocols like TCP, UDP, HTTP, DNS, and more.

Filtering & Searching: Use display and capture filters (e.g., http, tcp.port == 80, etc.) to focus on relevant data.

Deep Packet Inspection (DPI): View detailed packet information, including headers and payload.

Decryption Support: Can decrypt certain encrypted traffic (like TLS/SSL) if keys are available.

Live & Offline Analysis: Analyze packets in real-time or open saved capture files (.pcap, .pcapng).

Cross-Platform: Works on Windows, Linux, and macOS.

Common Use Cases:
Penetration Testing & Security Analysis: Identify vulnerabilities, sniff passwords (if unencrypted), and analyze attack patterns.

Network Troubleshooting: Diagnose slow network issues, dropped packets, and connectivity problems.

Reverse Engineering: Inspect network traffic for API interactions and malware analysis.

Learning Network Protocols: Study how different network protocols work.

How to Install Wireshark on Windows, Linux, and macOS
1. Install Wireshark on Windows
Steps:

Download the latest Wireshark setup from the official website:
👉 https://www.wireshark.org/download.html

Run the installer (.exe file) and follow the setup wizard.

During installation, select Npcap (necessary for live packet capture).

Complete the installation and launch Wireshark.

✅ To capture packets on a network interface, run Wireshark as Administrator.

Here are 20 useful Wireshark filters categorized by their purpose which are used in this video:

1. Basic IP Filtering:
ip.addr == 192.168.1.1 → Show traffic involving a specific IP.

ip.src == 192.168.1.1 → Show traffic originating from a specific IP.

ip.dst == 192.168.1.1 → Show traffic destined for a specific IP.

ip.addr == 192.168.1.1 && ip.addr == 192.168.1.2 → Show traffic between two specific IPs.

2. Protocol-Based Filtering:
tcp → Show only TCP packets.

udp → Show only UDP packets.

icmp → Show only ICMP packets (useful for analyzing pings).

arp → Show only ARP packets (useful for detecting ARP spoofing).

3. Port-Based Filtering:
tcp.port == 80 → Show only HTTP traffic.

tcp.port == 443 → Show only HTTPS traffic.

udp.port == 53 → Show only DNS traffic.

tcp.port == 21 → Show only FTP traffic.

tcp.port == 22 → Show only SSH traffic.

4. Payload and Data Filtering:
http.request.method == "GET" → Show only HTTP GET requests.

http contains "password" → Show packets containing the word "password" in HTTP requests.

dns.qry.name contains "example.com" → Show only DNS queries for "example.com".

tcp.flags.syn == 1 && tcp.flags.ack == 0 → Show only TCP SYN packets (useful for detecting SYN scans).

5. Advanced Security and Attack Detection:
eth.src == aa:bb:cc:dd:ee:ff → Show packets from a specific MAC address.

ip.ttl < 10 → Show packets with a low TTL (potential sign of a traceroute or attack).

tcp.analysis.retransmission → Show only retransmitted TCP packets (useful for diagnosing network issues).
