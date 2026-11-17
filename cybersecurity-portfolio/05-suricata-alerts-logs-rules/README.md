# Lab 05 — Examine Alerts, Logs, and Rules with Suricata

**Provider:** Google Skills training activity  
**Category:** Network Security Monitoring / IDS  
**Status:** Completed — 3 of 3 tasks reported completed

## Objective
Run Suricata against a sample PCAP using a custom rules file, then inspect generated alerts and event logs.

## Tools and files
Suricata, `cat`, `jq`, `custom.rules`, `sample.pcap`, `fast.log`, `eve.json`.

## Work performed
- Inspected the supplied custom detection rules.
- Ran Suricata in offline PCAP-analysis mode against `sample.pcap`, loading `custom.rules`.
- Reviewed `fast.log` and identified two alerts labelled “GET on wire”.
- Inspected structured events in `eve.json` with `jq`.
- Reviewed alert metadata including severity 3 and destination addresses `142.250.1.139` and `142.250.1.102`.
- Used event/flow information, including `flow_id`, to relate records during analysis.

## Commands

```bash
cat custom.rules
sudo suricata -r sample.pcap -S custom.rules -k none
cat /var/log/suricata/fast.log
cat /var/log/suricata/eve.json | jq .
```

Use the actual log paths shown by the lab environment if they differ. The commands above reflect the documented exercise.

## Command explanations
- `cat custom.rules`: displays the custom rules file.
- `suricata -r sample.pcap`: analyses a saved PCAP offline.
- `-S custom.rules`: loads the specified rules file.
- `-k none`: disables checksum validation for the exercise's capture context.
- `fast.log`: provides concise alert output.
- `eve.json`: contains structured event data.
- `jq`: formats and filters JSON for inspection.

## Findings recorded in the lab
The fast alert log contained two “GET on wire” alerts. The JSON event review showed severity 3 and destination IPs `142.250.1.139` and `142.250.1.102`. These are observations from the supplied sample PCAP and training rules, not evidence of malicious activity on a live network.

## Skills demonstrated
Introductory IDS workflow, rule-file inspection, offline PCAP analysis, alert review, JSON log inspection and event/flow correlation.

## Evidence to add
Sanitized screenshots of the rule file, Suricata execution, relevant `fast.log` alerts and selected `eve.json` fields. Remove unrelated personal or sensitive information.

## Scope
A guided lab using sample traffic and custom rules. Do not describe the alerts as a confirmed real-world attack.
