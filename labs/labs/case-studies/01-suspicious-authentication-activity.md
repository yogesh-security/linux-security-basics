# 🚨 Case Study 01 — Suspicious Authentication Activity

## 📌 Scenario

A Linux system shows multiple unsuccessful authentication attempts for a user account.

The objective is to investigate the activity from a **SOC Analyst L1** perspective and determine what additional evidence should be collected.

> This is a simulated educational scenario. No real attack or unauthorized system is involved.

## 🎯 Investigation Objectives

* Identify authentication-related events
* Determine the affected account
* Establish the timeline
* Identify the source of the activity, where available
* Determine whether the pattern is unusual
* Document evidence and recommended next steps

## 🔎 Initial Investigation

Relevant authentication logs should be reviewed.

Example:

```bash
sudo grep -i "failed" /var/log/auth.log
```

If the system uses systemd journal:

```bash
sudo journalctl | grep -i "failed"
```

## 📊 Evidence to Collect

| Evidence              | Purpose                       |
| --------------------- | ----------------------------- |
| Timestamp             | Establish event timeline      |
| Username              | Identify affected account     |
| Source IP             | Identify origin, if available |
| Authentication result | Determine success/failure     |
| Number of attempts    | Identify repeated activity    |
| Related events        | Establish context             |

## 🧠 L1 Analysis

The analyst should avoid immediately declaring the activity malicious.

The following questions should be answered:

1. Is the affected account expected to receive login attempts?
2. Are the attempts coming from an expected source?
3. Are failures occurring repeatedly?
4. Did a successful login occur after multiple failures?
5. Are there related process or network events?
6. Is the activity consistent with normal system behavior?

## 🚦 Initial Assessment

**Status:** Requires investigation.

The scenario cannot be classified as malicious without reviewing actual evidence and environmental context.

## 🛡️ Recommended Next Steps

If the activity appears suspicious, an L1 analyst should:

* Preserve relevant log evidence
* Record the timeline
* Identify the affected account
* Review related authentication events
* Correlate with network and process activity
* Follow the organization's escalation procedure

## 📝 Analyst Notes

### Timeline

**Not populated — simulated case study.**

### Evidence

**Not populated — no real incident data used.**

### Final Finding

**Investigation required.**

No real-world security incident is being claimed by this case study.

## 🎓 Skills Demonstrated

* Linux log analysis
* Authentication monitoring
* Evidence collection
* Timeline analysis
* SOC L1 investigation methodology
* Incident documentation
* Escalation decision-making

## ⚠️ Disclaimer

This case study is created for educational and portfolio purposes using a simulated scenario. It does not represent a real security incident.
