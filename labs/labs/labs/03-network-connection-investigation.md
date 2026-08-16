# 🌐 Lab 03 — Network Connection Investigation

## 🎯 Objective

The objective of this lab is to understand active network connections, listening ports, and basic network activity from a SOC Analyst L1 perspective.

## 🧪 Lab Environment

* **Platform:** Kali Linux
* **Focus:** Network monitoring and investigation
* **Environment:** Authorized educational lab

## 🛠️ Investigation Commands

### View listening ports and network connections

```bash
ss -tuln
```

### View active connections with process information

```bash
sudo ss -tup
```

### Display network interfaces

```bash
ip addr
```

### Review routing information

```bash
ip route
```

## 🔍 Investigation Methodology

During network investigation, review:

| Area           | What to Check                           |
| -------------- | --------------------------------------- |
| Local Address  | Which local IP/interface is involved?   |
| Port           | Which port is being used?               |
| Protocol       | TCP or UDP?                             |
| State          | Listening, established, etc.            |
| Process        | Which process owns the connection?      |
| Remote Address | Is there an unexpected remote endpoint? |

## 🚨 SOC Analyst L1 Perspective

A listening port or external connection is **not automatically malicious**.

An analyst should determine:

1. Which port is involved?
2. Which process owns the connection?
3. Is the service expected?
4. Is the remote endpoint expected?
5. Is the connection established or only listening?
6. Does the activity correlate with any other suspicious event?
7. Is further investigation or escalation required?

## 🧠 Investigation Workflow

```text
Network Connection
       ↓
Identify IP & Port
       ↓
Identify Process
       ↓
Determine Expected Service
       ↓
Review Remote Endpoint
       ↓
Correlate With Other Evidence
       ↓
Document Finding
       ↓
Escalate if Required
```

## 📋 Evidence

Practical command output and screenshots can be added after performing the investigation in the authorized lab environment.

## 📝 Findings

**Current status:** Investigation procedure documented.

No specific connection or port is classified as malicious without reviewing actual system evidence.

## 🎓 Key Learning

This lab demonstrates a basic network investigation workflow:

**Connection → Port → Process → Endpoint → Context → Finding**

## 🔐 Security Note

All activities are performed for educational purposes in an authorized environment. Sensitive information, credentials, tokens, or private data must not be uploaded to this repository.
