# Course 4 — Linux & SQL

**Platform:** Google Cybersecurity Professional Certificate, Coursera  
**Duration:** ~24 hours

---

## What This Course Covers

Using Linux command line and SQL to perform security analysis tasks — the daily tools of a SOC analyst.

---

## Key Topics

### Linux for Security

**Why Linux matters in cybersecurity:**
- Most servers and security tools run on Linux
- Full control over system via command line
- Essential for log analysis, file management, and forensics

**Core Commands Used in Security Work:**

```bash
# Navigation
pwd          # Where am I?
ls -la       # List all files with permissions
cd /var/log  # Navigate to log directory

# File reading
cat auth.log           # Read authentication logs
grep "FAILED" auth.log # Search for failed logins
tail -100 syslog       # Last 100 lines of system log

# User management
whoami                 # Current user
id username            # User's group and UID
sudo useradd newuser   # Add a user
```

### File Permissions in Linux

Permissions format: `-rwxrwxrwx`  
Positions: [file type][owner][group][others]  
Characters: `r` = read (4), `w` = write (2), `x` = execute (1)

```bash
# View permissions
ls -la /home/user/projects

# Change permissions
chmod o-w filename.txt     # Remove write from others
chmod g-x directory/       # Remove execute from group
chmod 640 sensitive.txt    # Owner rw, Group r, Others none
```

**Lab activity:** Updated permissions across a research team's project directory to enforce least privilege — removed unauthorized write access from `project_k.txt`, secured the hidden file `.project_x.txt`, and restricted directory access to a single authorized user.

### SQL for Security Analysis

Security logs are stored in databases. SQL lets analysts query millions of records instantly.

```sql
-- Find failed logins after business hours
SELECT *
FROM log_in_attempts
WHERE login_time > '18:00:00'
AND success = FALSE;

-- Find logins from outside expected countries
SELECT *
FROM log_in_attempts
WHERE country NOT IN ('IN', 'US');

-- Join employees to machines for patch audit
SELECT employees.name, machines.device_id, machines.OS_patch_date
FROM employees
INNER JOIN machines ON employees.device_id = machines.device_id
WHERE machines.OS_patch_date < '2024-01-01';
```

---

## Skills Gained
`Linux CLI` `Bash` `File permissions` `chmod` `Log analysis` `SQL filtering` `Database queries` `Security investigation`
