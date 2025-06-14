## IDS
- Intrusion Detection System (signature based (eg. snort) or behaviour based).
- Snort/Suricata/YARA rule writing
- Host-based Intrusion Detection System (eg. OSSEC)

## SIEM
- Security Information and Event Management.
  
## IOC
- Indicator of compromise (often shared amongst orgs/groups).
- Specific details (e.g. IP addresses, hashes, domains)

## Things that create signals
- Honeypots, snort

## Things that triage signals
- SIEM, eg splunk

## Things that will alert a human
- Automatic triage of collated logs, machine learning.
- Notifications and analyst fatigue.
- Systems that make it easy to decide if alert is actual hacks or not.

## Signatures
- Host-based signatures
- Eg changes to the registry, files created or modified.
- Strings in found in malware samples appearing in binaries installed on hosts (/Antivirus).
- Network signatures
- Eg checking DNS records for attempts to contact C2 (command and control) servers.
