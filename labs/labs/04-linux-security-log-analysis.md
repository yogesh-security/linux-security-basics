# 📋 Lab 04 — Linux Security Log Analysis

## 🎯 Objective

The objective of this lab is to understand Linux security-related logs and practice identifying authentication and system activity relevant to SOC Analyst L1 investigations.

## 🧪 Lab Environment

* **Platform:** Kali Linux
* **Focus:** Security log analysis
* **Environment:** Authorized educational lab

## 🛠️ Log Sources

Depending on the Linux configuration, relevant security information may be available through:

* `/var/log/auth.log`
* `journalctl`
* System and service logs under `/var/log/`

## 🔎 Investigation Commands

### Review recent authentication events

```bash id="7q2e1a"
sudo tail -n 50 /var/log/auth.log
```

### Search for failed authentication attempts

```bash id="2p7h0z"
sudo grep -i "failed" /var/log/auth.log
```

### Search for successful authentication events

```bash id="x0q9bn"
sudo grep -i "accepted" /var/log/auth.log
```

### Review recent system journal events

```bash id="f8s2wq"
sudo journalctl -n 50
```

### Filter journal events by priority

```bash id="7r3k1m"
sudo journalctl -p warning -n 50
```

## 🔍 Investigation Methodology

When analyzing security logs, examine:

| Field     | What to Check                                     |
| --------- | ------------------------------------------------- |
| Timestamp | When did the event occur?                         |
| User      | Which account was involved?                       |
| Event     | What action occurred?                             |
| Source    | What system/IP generated the event, if available? |
| Result    | Successful or failed?                             |
| Frequency | Is the activity repeated?                         |
| Context   | Is the activity expected?                         |

## 🚨 SOC Analyst L1 Perspective

A log entry should be evaluated in context.

An L1 analyst should:

1. Identify the event.
2. Determine when it occurred.
3. Identify the affected account or service.
4. Determine whether the event succeeded or failed.
5. Look for repeated or unusual activity.
6. Correlate related events when possible.
7. Document the evidence.
8. Escalate according to the investigation process when necessary.

## 🧠 Investigation Workflow

```text id="4m7q2v"
Log Source
    ↓
Identify Event
    ↓
Extract Timestamp & Account
    ↓
Check Success / Failure
    ↓
Look for Repeated Activity
    ↓
Correlate With Other Evidence
    ↓
Determine Risk
    ↓
Document Finding
    ↓
Escalate if Required
```

## 📊 Evidence

Practical command output and screenshots can be added after performing the investigation in the authorized lab environment.

## 📝 Findings

**Current status:** Investigation methodology documented.

No specific event is classified as malicious without reviewing actual log evidence and environmental context.

## 🎓 Key Learning

This lab demonstrates how security logs can support:

* Authentication monitoring
* Event investigation
* Suspicious activity detection
* Evidence collection
* SOC escalation decisions

## 🔐 Security Note

This lab is intended for authorized educational practice only.

Do not upload passwords, authentication tokens, API keys, private credentials, or other sensitive information to the repository.
