# Wireshark/tshark (WIRESHARK CHEAT SHEET ATTACHED AT BOTTOM)

## Introduction
Wireshark and tshark are powerful tools for network protocol analysis. They are used in CTF challenges to analyze packet captures (pcaps) and extract useful information. In RTARF CTF 2024, competitors were tasked with capturing live packets in order to find the flag, but it is more common for packet capture files to be provided to competitors.

## Wireshark Basics
- **Open a pcap file:**
  - `File > Open > [yourfile.pcap]`

- **Common Filters:**
  - Display filters: `tcp`, `udp`, `http`, `ip.addr == 192.168.0.1`
  - Example: `http.request.method == "GET"`

## Advanced Filters
- **Filter by protocol and port:**
  - Example: `tcp.port == 80`

- **Filter by IP address:**
  - Example: `ip.src == 192.168.0.1`

- **Filter by payload:**
  - Example: `tcp contains "password"`

## Follow Streams
- **Follow TCP Stream:**
  - Right-click on a packet > `Follow > TCP Stream`
  - Useful for reconstructing application data

- **Follow HTTP Stream:**
  - Right-click on a packet > `Follow > HTTP Stream`
  - Useful for viewing HTTP requests and responses

## Extracting Files
- **Extracting files from HTTP:**
  - `File > Export Objects > HTTP`

- **Extracting files from SMB:**
  - `File > Export Objects > SMB`

## tshark Basics
- **Display pcap file information:**
  - `tshark -r [file.pcap]`

- **Applying display filters:**
  - `tshark -r [file.pcap] -Y "http.request.method == 'GET'"`

## Advanced tshark Usage
- **Extract fields:**
  - Example: `tshark -r [file.pcap] -T fields -e ip.src -e ip.dst`

- **Export objects:**
  - Example: `tshark -r [file.pcap] --export-objects http,tmpdir/`

## What to Look For in CTF Challenges
- **Suspicious Traffic:**
  - Unusual IP addresses or ports
  - Large data transfers over unusual ports
  - Encrypted data in typically unencrypted protocols

- **Credentials and Sensitive Information:**
  - HTTP basic authentication headers
  - FTP, POP3, IMAP traffic (commonly in plaintext)
  - Telnet traffic (plaintext)

- **Data Exfiltration:**
  - DNS tunneling
  - ICMP payloads
  - Covert channels within HTTP or other protocols

- **Malware Communication:**
  - Known command-and-control (C2) patterns
  - Suspicious domains or IPs
  - Unusual protocol usage

## Useful Tips
- **Color Coding:** Use Wireshark’s color coding to quickly identify different types of traffic.
- **Statistics:** `Statistics > Protocol Hierarchy` to get a breakdown of protocols in the pcap.
- **Expert Info:** `Analyze > Expert Information` to spot anomalies and potential issues.

## References
- [Wireshark User Guide](https://www.wireshark.org/docs/wsug_html_chunked/)
- [Wireshark Display Filter Reference](https://www.wireshark.org/docs/dfref/)
- [tshark Manual](https://www.wireshark.org/docs/man-pages/tshark.html)
- [Wireshark Cheat Sheet](https://packetlife.net/media/library/23/Wireshark_Display_Filters.pdf)

![Wireshark-Cheat-Sheet-1](https://github.com/user-attachments/assets/bf034b34-b4f7-486c-bf55-1efe7daab92f)
