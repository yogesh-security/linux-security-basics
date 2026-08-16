# ⚙️ Lab 02 — Linux Process & Service Investigation

## 🎯 Objective

The objective of this lab is to understand running processes and system services and develop basic host-monitoring skills relevant to a SOC Analyst L1 role.

## 🧪 Lab Environment

* **Platform:** Kali Linux
* **Focus:** Process and service monitoring
* **Environment:** Authorized educational lab

## 🛠️ Investigation Commands

### View running processes

```bash
ps aux
```

### View processes interactively

```bash
top
```

### Identify processes using system resources

```bash
ps aux --sort=-%cpu | head
```

### Review running services

```bash
systemctl --type=service --state=running
```

### Check a specific service

```bash
systemctl status <service-name>
```

## 🔍 Investigation Methodology

During process and service analysis, review:

| Area           | What to Check                            |
| -------------- | ---------------------------------------- |
| Process        | Name and PID                             |
| User           | Which account owns the process?          |
| Parent Process | What started the process?                |
| CPU/Memory     | Is resource usage unusual?               |
| Service        | Is the service expected?                 |
| Network        | Does the process communicate externally? |

## 🚨 SOC Analyst L1 Perspective

A suspicious process should not automatically be considered malicious.

An L1 analyst should first establish:

1. What process is running?
2. Which user started it?
3. What is its parent process?
4. Is the process expected on this system?
5. Is it consuming unusual resources?
6. Is it associated with unexpected network activity?
7. Does the activity require escalation?

## 🧠 Investigation Workflow

```text
Process / Service
       ↓
Identify Owner
       ↓
Review Parent Process
       ↓
Check Resource Usage
       ↓
Check Network Activity
       ↓
Determine Expected / Suspicious
       ↓
Document Finding
       ↓
Escalate if Required
```

## 📋 Evidence

Practical command output and screenshots can be added after performing the investigation in the authorized lab environment.

## 📝 Findings

**Current status:** Investigation procedure documented.

No specific process or service is classified as malicious without reviewing actual system evidence.

## 🎓 Key Learning

This lab demonstrates how a SOC analyst can approach host-based investigation by correlating:

**Process → User → Parent Process → Resource Usage → Network Activity**

## 🔐 Security Note

All activities are performed for educational purposes in an authorized environment. Sensitive information must not be uploaded to the repository.
