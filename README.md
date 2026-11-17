# Splunk-SOC-Home-Lab
SIEM Detection &amp; Triage Lab
Overview
An end-to-end virtualized Security Operations Center (SOC) lab built with Splunk Enterprise, simulating real-world enterprise log ingestion, attack generation, and alert triage mapped to the MITRE ATT&CK framework.
Architecture & Detections
• Log Ingestion: Configured Splunk Universal Forwarders on Windows and Ubuntu endpoints to ingest Sysmon, Windows Security Event Logs, and Linux auth.log.
• Attack Simulation: Executed controlled reconnaissance and credential attacks from Kali Linux using Nmap and Hydra.
• Custom SPL Detection Rules:
	• Brute-Force Detection (T1110): Triggers alerts on bursts of failed authentication events (Event ID 4625 / SSH failures) from a single source IP within a 5-minute window.
	• Network Reconnaissance (T1046): Flags rapid sequential connection attempts across multiple ports.
• Incident Playbooks: Documented step-by-step triage checklists (scope verification, IOC extraction, containment recommendation) for each alert.
