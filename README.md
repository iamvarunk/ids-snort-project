# Intrusion Detection System (IDS) using Snort 3

##  Overview
This project demonstrates the deployment, configuration, monitoring, and customization of a Network Intrusion Detection System (IDS) using Snort 3 on Kali Linux.

##  Tools & Technologies
- Snort 3 (Snort++)
- Kali Linux
- Nmap
- Custom Snort Rules
- Git & GitHub

##  Project Structure
```text
ids-snort-project/
├── README.md
├── screenshots/
│   ├── phase0_*.png
│   ├── phase1_*.png
│   ├── phase2_*.png
│   └── phase3_*.png
├── rules/
│   └── local.rules
└── docs/

##  Project Phases

### Phase 0 – Environment Setup
- Installed and validated Snort 3
- Verified rule loading and configuration

### Phase 1 – Traffic Monitoring
- Identified active network interface
- Ran Snort in passive IDS mode
- Observed live packet processing

### Phase 2 – Attack Detection
- Simulated reconnaissance using Nmap
- Analyzed IDS behavior
- Observed limitations of default rule sets

### Phase 3 – Custom Rules
- Authored custom ICMP detection rule
- Integrated rules using Snort 3 IPS configuration
- Successfully triggered real-time alerts

### Phase 4 – Analysis & Reporting
- Analyzed alerts and traffic
- Classified true positives vs false positives
- Documented IDS limitations and findings

##  How to Run
1. Validate Snort configuration:
   ```bash
   sudo snort -T -c /etc/snort/snort.lua
2. Run Snort in IDS mode:
   sudo snort -c /etc/snort/snort.lua -i eth0
3. Trigger detection:
   ping -c 4 8.8.8.8

##  Key Learnings
- Signature-based IDS requires tuning
- Not all attacks trigger default rules
- Custom rules significantly improve detection
- Snort 3 uses Lua-based configuration and IPS policies

##  Screenshots
See the `screenshots/` directory for evidence of each phase.

##  Disclaimer
All attacks were performed in a controlled lab environment on owned systems only.
