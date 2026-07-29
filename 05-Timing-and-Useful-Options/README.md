
# Timing Templates

Timing templates control how quickly Nmap sends packets during a scan. Choosing the right timing can improve scan performance while reducing the chances of overwhelming the target or triggering security alerts.

| Option | Description |
|---------|-------------|
| `-T0` | Paranoid (Slowest) |
| `-T1` | Sneaky |
| `-T2` | Polite |
| `-T3` | Normal (Default) |
| `-T4` | Aggressive (Most commonly used) |
| `-T5` | Insane (Fastest) |

### Example

```bash
nmap -T4 localhost
```

**When to use:**
- `-T3` for normal scans.
- `-T4` for most authorized assessments.
- `-T5` only when speed is more important than stealth.

---

# Scan Specific Ports (`-p`)

Instead of scanning every port, Nmap allows you to scan only the ports you specify. This makes scans faster when you already know which services you're interested in.

### Examples

```bash
nmap -p 22 localhost
```

```bash
nmap -p 22,80 localhost
```

```bash
nmap -p 20-30 localhost
```

**Common Use Cases**
- Scan only SSH (22)
- Scan only HTTP/HTTPS (80,443)
- Scan a custom port range

---

# Scan All Ports (`-p-`)

By default, Nmap scans approximately the 1,000 most common ports. To discover services running on uncommon or high-numbered ports, scan every TCP port.

### Example

```bash
nmap -p- localhost
```

**Use when:**
- Performing a complete assessment.
- Looking for hidden or uncommon services.

---

# Fast Scan (`-F`)

Fast Scan checks only the 100 most common ports, making it much quicker than a default scan.

### Example

```bash
nmap -F localhost
```

**Use when:**
- Performing a quick health check.
- Scanning many hosts in a short time.

---

# Skip Host Discovery (`-Pn`)

Normally, Nmap first checks whether a host is online using host discovery (ping). If ICMP requests are blocked by a firewall, Nmap may incorrectly report that the host is down.

The `-Pn` option skips host discovery and assumes the target is online.

### Example

```bash
nmap -Pn localhost
```

**Use when:**
- Firewalls block ping requests.
- You know the target host is online.

---

# Verbose Mode (`-v`)

Verbose mode displays scan progress and discovered ports while the scan is running.

### Example

```bash
nmap -v localhost
```

**Benefits**
- Monitor scan progress.
- View discovered ports in real time.
- Useful during long scans.

---

# Show Reason (`--reason`)

The `--reason` option explains why Nmap classified a port as open, closed, or filtered.

### Example

```bash
nmap --reason localhost
```

Example output:

```
80/tcp open http syn-ack
```

In this example, `syn-ack` is the response that indicates the port is open.

---

# Real-World Example

```bash
nmap -Pn -p 22,80 -v --reason localhost
```

This command:

- Skips host discovery.
- Scans only ports 22 and 80.
- Displays scan progress.
- Explains why each port is classified as open or closed.

