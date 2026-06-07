# Course 7 — Automate Cybersecurity Tasks with Python

**Platform:** Google Cybersecurity Professional Certificate, Coursera  
**Duration:** ~30 hours

---

## What This Course Covers

Writing Python scripts to automate repetitive security tasks — parsing logs, managing files, and building reusable security functions.

---

## Key Topics

### Why Python in Cybersecurity

- Automates log parsing (thousands of lines in seconds)
- Builds custom security tools
- Integrates with APIs and security platforms
- Used in SIEM automation, malware analysis, and scripting

### Python Fundamentals Covered

```python
# Variables and data types
username = "analyst01"
failed_attempts = 7
is_locked = False
ip_list = ["10.0.0.1", "192.168.1.1", "172.16.0.5"]

# Conditional logic
if failed_attempts >= 5:
    print(f"ALERT: {username} has exceeded login attempt threshold")

# Loops for log processing
blocklist = ["192.168.1.100", "10.0.0.99"]
for ip in ip_list:
    if ip in blocklist:
        print(f"Blocked IP detected: {ip}")

# Functions
def check_failed_logins(username, attempts, threshold=5):
    if attempts >= threshold:
        return f"Lock account: {username} ({attempts} failed attempts)"
    return "Within normal range"
```

### Key Activity — Update Allow List Algorithm

A core lab activity: write an algorithm that reads an IP allow list, removes flagged IPs, and rewrites the file.

```python
def update_file(import_file, remove_list):
    # Read the current allow list
    with open(import_file, "r") as file:
        ip_addresses = file.read()

    # Convert string to list
    ip_addresses = ip_addresses.split()

    # Remove IPs that should be blocked
    for element in remove_list:
        if element in ip_addresses:
            ip_addresses.remove(element)

    # Rewrite the updated list back to file
    ip_addresses = "\n".join(ip_addresses)
    with open(import_file, "w") as file:
        file.write(ip_addresses)

# Run it
remove_list = ["192.168.97.226", "192.168.158.170", "192.168.201.40"]
update_file("allow_list.txt", remove_list)
```

### Additional Scripts Practiced

**Log parser — detect brute force:**
```python
def parse_failed_logins(log_file, threshold=5):
    failed = {}
    with open(log_file, "r") as f:
        for line in f:
            if "FAILED" in line:
                ip = line.split()[-1]
                failed[ip] = failed.get(ip, 0) + 1
    for ip, count in failed.items():
        if count >= threshold:
            print(f"ALERT: {ip} — {count} failed login attempts")
```

---

## Skills Gained
`Python scripting` `File I/O` `String manipulation` `Regular expressions` `Log parsing` `Security automation` `Functions` `Loops` `Error handling`
