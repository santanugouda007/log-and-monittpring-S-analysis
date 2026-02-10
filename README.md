# log-and-monittpring-S-analysis

# Task 12: Log Monitoring & Analysis

## 📌 Objective
The objective of this task is to analyze system logs to detect suspicious activities such as failed login attempts, anomalies, and potential brute-force attacks. Log monitoring is a critical skill in cybersecurity and SOC operations for early incident detection and response.

---

## 🛠 Tools Used
- Linux Authentication Logs (`/var/log/auth.log`)
- Terminal commands (`cat`, `grep`)
- *(Alternative tools: Windows Event Viewer, SIEM tools like Splunk Free)*

---

## 🔍 Task Description
In this task, Linux authentication logs were analyzed to:
- Monitor login activities
- Identify failed authentication attempts
- Detect anomalies such as repeated failures from the same IP
- Correlate events using timestamp, IP address, and username

---

## 🧪 Steps Performed

### Step 1: View Authentication Logs
Authentication logs were accessed using the following command:
```bash
sudo cat /var/log/auth.log
This log contains records of login attempts, SSH access, and sudo usage.

Step 2: Identify Failed Login Attempts
Failed login attempts were filtered using:

grep "Failed password" /var/log/auth.log
This helps detect unauthorized access attempts and brute-force behavior.

Step 3: Detect Anomalies
The logs showed:

Multiple failed login attempts

Repeated attempts from the same IP address

Short time intervals between attempts

These patterns indicate a possible brute-force attack.

Step 4: Correlate Events
Log entries were correlated using:

Timestamp

Source IP address

Target username

Correlation helps understand attack patterns and attacker behavior.

📄 Findings
Multiple failed authentication attempts detected

Same IP address repeated across log entries

Indicates a potential brute-force SSH attack

🔐 Importance of Log Monitoring
Incident Detection: Identifies attacks in early stages

Forensics: Helps investigate security incidents

Compliance: Required for audits and security standards

✅ Conclusion
Log monitoring is essential for maintaining system security. Regular analysis of authentication logs enables early detection of unauthorized access attempts and helps security teams respond effectively to threats.
