# 🔎 Lab 01 — Linux Authentication Log Investigation

## 🎯 Objective

This lab focuses on understanding Linux authentication logs and developing basic log-analysis skills relevant to a SOC Analyst L1 role.

## 🧪 Lab Environment

* **Platform:** Kali Linux
* **Focus:** Authentication monitoring and log analysis
* **Environment:** Authorized educational lab

## 🛠️ Investigation Commands

### Identify the Linux environment

```bash
cat /etc/os-release
```

### Review available system logs

```bash
ls -l /var/log/
```

### Check authentication events

```bash
sudo tail -n 20 /var/log/auth.log
```

### Alternative: systemd journal

If `auth.log` is not available:

```bash
sudo journalctl -n 20
```

## 🔍 Investigation Methodology

When reviewing authentication activity, the following information should be examined:

| Field     | What to Check                                    |
| --------- | ------------------------------------------------ |
| Timestamp | When did the event occur?                        |
| Account   | Which user account was involved?                 |
| Event     | Login, logout, failure, privilege activity, etc. |
| Source    | Where did the authentication request originate?  |
| Result    | Successful or failed?                            |
| Frequency | Are repeated failures occurring?                 |

## 🚨 SOC Analyst L1 Perspective

A SOC Analyst should determine:

1. What happened?
2. When did it happen?
3. Which account was involved?
4. Was the authentication successful?
5. Does the activity appear expected?
6. Are there repeated or unusual authentication attempts?
7. Does the event require further investigation or escalation?

## 🧠 Investigation Workflow

```text
Log Source
    ↓
Authentication Event
    ↓
Collect Evidence
    ↓
Analyze Activity
    ↓
Determine Normal / Suspicious
    ↓
Document Finding
    ↓
Escalate if Required
```

## 📋 Evidence

Practical command output and screenshots can be added after performing the investigation in the authorized lab environment.

## 📝 Findings

**Current status:** Investigation procedure documented.

No specific security finding is claimed until actual authentication log data has been reviewed.

## 🎓 Key Learning

This lab demonstrates a basic SOC investigation workflow:

**Identify → Collect → Analyze → Document → Escalate**

## 🔐 Security & Privacy

This project is intended for authorized educational practice.

Sensitive information such as:

* Passwords
* API keys
* Authentication tokens
* Private credentials
* Personal information

must not be uploaded to this repository.
