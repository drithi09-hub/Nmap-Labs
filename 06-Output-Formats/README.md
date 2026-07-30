# Output Formats

## Objective



By default, Nmap displays scan results only in the terminal. If you close the terminal without saving them, the results are lost. Output formats allow you to store scan results for documentation, scripting, and sharing with your team.

---

# Normal Output (`-oN`)

Normal output saves scan results in a human-readable text file that looks similar to what is displayed in the terminal.

### Example

```bash
nmap -oN scan.nmap localhost
```

**Use when:**
- Saving scan reports
- Sharing results with teammates

---

# XML Output (`-oX`)

XML stores scan results in a structured format that can be easily parsed by scripts and other security tools.

### Example

```bash
nmap -oX scan.xml localhost
```

**Use when:**
- Automating analysis with Python or other languages
- Importing results into security tools


---

# Grepable Output (`-oG`)

Grepable output stores scan results in a simplified format that is easy to search using command-line tools such as `grep`.

### Example

```bash
nmap -oG scan.gnmap localhost
```

**Use when:**
- Searching for specific ports or services
- Working with older scripts


> **Note:** `-oG` is considered a legacy format. Most modern tools prefer XML.

---

# All Output Formats (`-oA`)

The `-oA` option saves the scan in all supported output formats with a single command.

### Example

```bash
nmap -oA assessment localhost
```

This command creates:

```
assessment.nmap
assessment.xml
assessment.gnmap
```

**Use when:**
- You want readable reports and machine-readable files together
- You're unsure which format you'll need later

---

# Real-World Example

```bash
nmap -Pn -p- -sV -v --reason -oA assessment localhost
```

This command:

- Skips host discovery
- Scans every TCP port
- Detects service versions
- Shows scan progress
- Displays the reason for port states
- Saves the results in all output formats

