# Commands

## Timing Templates

| Command | Purpose |
|---------|---------|
| `nmap -T3 <target>` | Default scan timing |
| `nmap -T4 <target>` | Faster scan for most authorized assessments |
| `nmap -T5 <target>` | Fastest scan (more likely to be detected) |

---

## Scan Specific Ports

| Command | Purpose |
|---------|---------|
| `nmap -p 22 <target>` | Scan only SSH |
| `nmap -p 22,80 <target>` | Scan SSH and HTTP |
| `nmap -p 20-30 <target>` | Scan a range of ports |

---

## Scan All Ports

| Command | Purpose |
|---------|---------|
| `nmap -p- <target>` | Scan all 65,535 TCP ports |

---

## Fast Scan

| Command | Purpose |
|---------|---------|
| `nmap -F <target>` | Scan the 100 most common ports |

---

## Skip Host Discovery

| Command | Purpose |
|---------|---------|
| `nmap -Pn <target>` | Assume the host is online and skip ping |

---

## Verbose Output

| Command | Purpose |
|---------|---------|
| `nmap -v <target>` | Display scan progress |

---

## Show Reason

| Command | Purpose |
|---------|---------|
| `nmap --reason <target>` | Show why a port is open, closed, or filtered |

---

## Combined Example

```bash
nmap -Pn -p- -v --reason localhost
```

**Purpose:** Scan all TCP ports, skip host discovery, display progress, and explain why ports are classified as open or closed.