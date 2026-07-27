# Commands

## Display Hostname

```bash
hostname
```

**Purpose**

Displays the hostname (name) of the current machine.

---

## Display Private IP Address

```bash
hostname -I
```

**Purpose**

Displays the private IP address assigned to the machine.

**Example Output**

```text
192.168.x.x
```

---

## Display Network Interfaces

```bash
ip addr
```

**Purpose**

Displays all network interfaces and their IP addresses, including the loopback interface (`127.0.0.1`).

---

## Scan localhost

```bash
nmap localhost
```

**Purpose**

Scans the local machine using the `localhost` hostname.

**Observation**

- `localhost` resolves to `127.0.0.1`.
- The host responded successfully.
- Port **631** was open.
- The remaining scanned ports were closed.

---

## Scan Loopback Address

```bash
nmap 127.0.0.1
```

**Purpose**

Scans the local machine using the loopback IP address.

**Observation**

- Produced the same results as `localhost`.
- Both refer to the same machine.

---

## Scan Private IP Address

```bash
nmap <private-ip>
```

Example:

```bash
nmap 192.168.x.x
```

**Purpose**

Scans the local machine using its private IP address.

