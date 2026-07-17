# Linux Authentication Log Investigation

## Overview

This project demonstrates a practical investigation of Linux authentication logs (`/var/log/auth.log`) in an isolated lab environment. The objective was to generate authentication events, analyze login activity, identify suspicious behavior, and document the findings from a SOC analyst perspective.

## Lab Scenario

The lab simulates an SSH brute-force attack against a Linux system.

The investigation includes:

- Creating a test user
- Generating authentication events
- Simulating an SSH brute-force attack
- Reviewing authentication logs
- Identifying failed and successful logins
- Tracking attacker activity
- Verifying privilege escalation attempts
- Reviewing session history

## Tools

- Ubuntu Linux
- SSH
- Hydra
- Nmap
- Linux Authentication Logs (`auth.log`)
- Linux command-line utilities (`grep`, `awk`, `last`, `wc`)

## Project Structure

```
Linux-Authentication-Log-Investigation/
├── README.md
├── LICENSE
├── DISCLAIMER.md
├── docs/
├── commands/
├── evidence/
├── logs/
└── assets/
```

## Skills Practiced

- Linux Log Analysis
- Authentication Log Investigation
- SSH Log Analysis
- Brute Force Detection
- Incident Investigation
- Command Line Investigation
- Basic Digital Forensics

## Key Findings

- Multiple failed SSH login attempts were detected.
- Successful authentication was identified after repeated failures.
- All suspicious activity originated from a single source IP.
- An attempt to escalate privileges using `su` was unsuccessful.
- No unauthorized root access was observed.
- Administrative (`sudo`) activity was performed only by the legitimate administrator.

## Disclaimer

This project was performed in a private, isolated virtual lab for educational and defensive cybersecurity purposes only.

## Author

**Mubarak Bashr**

SOC Analyst Student
