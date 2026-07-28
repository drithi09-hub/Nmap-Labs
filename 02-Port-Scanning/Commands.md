# Commands

## TCP Connect Scan

```bash
nmap -sT localhost
```

**Purpose**

Performs a TCP Connect Scan by completing the full TCP three-way handshake.

---

## SYN Scan

```bash
sudo nmap -sS localhost
```

**Purpose**

Performs a SYN Scan by sending a SYN packet and stopping before completing the TCP three-way handshake.

---

## Compare TCP Connect Scan and SYN Scan

| Scan | Handshake | Description |
|------|-----------|-------------|
| `-sT` | Complete | Establishes a full TCP connection. |
| `-sS` | Partial | Stops after receiving a response, making it a half-open scan. |