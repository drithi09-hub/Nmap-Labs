# 02 - Port Scanning

## Objective

Learn how Nmap checks if a port is open and understand the difference between TCP Connect Scan (`-sT`) and SYN Scan (`-sS`).

---

## Important Terms

### Port Scanning

Port scanning is the process of checking which ports on a host are open, closed, or filtered.

### TCP Three-Way Handshake

A process used by TCP to establish a reliable connection between a client and a server.

### SYN

The first packet sent to request a TCP connection.

### SYN-ACK

The server's response indicating it is ready to establish a connection.

### ACK

The final packet sent to complete the TCP three-way handshake.

### TCP Connect Scan (`-sT`)

A scan that completes the full TCP three-way handshake.

### SYN Scan (`-sS`)

A scan that checks if a port is open without completing the TCP three-way handshake.

### Half-Open Scan

Another name for a SYN Scan because the connection is not fully established.

### Reconnaissance

The process of gathering information about a target before attempting further actions.

---

## Concepts Covered

- Port Scanning
- TCP Three-Way Handshake
- TCP Connect Scan (`-sT`)
- SYN Scan (`-sS`)
- Half-Open Scan
- Reconnaissance