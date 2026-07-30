# Commands

## Normal Output

| Command | Purpose |
|---------|---------|
| `nmap -oN scan.nmap <target>` | Save results in a readable text file |

---

## XML Output

| Command | Purpose |
|---------|---------|
| `nmap -oX scan.xml <target>` | Save results in XML format |

---

## Grepable Output

| Command | Purpose |
|---------|---------|
| `nmap -oG scan.gnmap <target>` | Save results in grepable format |

---

## All Output Formats

| Command | Purpose |
|---------|---------|
| `nmap -oA assessment <target>` | Save results in all output formats |

---

## Combined Example

```bash
nmap -Pn -p- -sV -v --reason -oA assessment localhost
```

**Purpose:** Scan all TCP ports, skip host discovery, detect service versions, show progress, explain port states, and save the results in all output formats.