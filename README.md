# IT Support Knowledge Base

A practical, structured knowledge base for IT support professionals. This repository documents common incidents, diagnostic commands, troubleshooting workflows, and resolution steps for Linux, Windows, servers, networking, and end-user support.

## Purpose
- Build a practical reference for day-to-day IT support.
- Document repeatable troubleshooting procedures.
- Improve incident diagnosis, resolution, and escalation.
- Maintain clear, reusable technical documentation.

## Repository Structure
```text
IT-Support-Knowledge-Base/
├── README.md
├── Linux/
│   ├── Basic-Commands.md
│   ├── Network-Troubleshooting.md
│   ├── Disk-Management.md
│   └── Service-Management.md
├── Windows/
│   ├── Common-Issues.md
│   ├── Network-Troubleshooting.md
│   └── System-Troubleshooting.md
├── Server-Monitoring/
│   ├── CPU-Memory-Monitoring.md
│   ├── Disk-Monitoring.md
│   └── Service-Monitoring.md
├── Network-Troubleshooting/
│   ├── DNS-Issues.md
│   ├── IP-Configuration.md
│   └── Connectivity-Issues.md
└── Common-IT-Issues/
    ├── Internet-Not-Working.md
    ├── Printer-Not-Working.md
    └── Application-Not-Opening.md
```

## Quick Navigation
### Linux
- [Basic Linux Commands](Linux/Basic-Commands.md)
- [Linux Network Troubleshooting](Linux/Network-Troubleshooting.md)
- [Disk Management](Linux/Disk-Management.md)
- [Service Management](Linux/Service-Management.md)

### Windows
- [Common Windows Issues](Windows/Common-Issues.md)
- [Windows Network Troubleshooting](Windows/Network-Troubleshooting.md)
- [Windows System Troubleshooting](Windows/System-Troubleshooting.md)

### Server Monitoring
- [CPU and Memory Monitoring](Server-Monitoring/CPU-Memory-Monitoring.md)
- [Disk Monitoring](Server-Monitoring/Disk-Monitoring.md)
- [Service Monitoring](Server-Monitoring/Service-Monitoring.md)

### Networking
- [DNS Issues](Network-Troubleshooting/DNS-Issues.md)
- [IP Configuration](Network-Troubleshooting/IP-Configuration.md)
- [Connectivity Issues](Network-Troubleshooting/Connectivity-Issues.md)

### Common IT Issues
- [Internet Not Working](Common-IT-Issues/Internet-Not-Working.md)
- [Printer Not Working](Common-IT-Issues/Printer-Not-Working.md)
- [Application Not Opening](Common-IT-Issues/Application-Not-Opening.md)

## Standard Troubleshooting Workflow
1. **Identify:** Record the user, device/server, affected service, symptoms, and business impact.
2. **Scope:** Determine whether one user, multiple users, one system, or an entire service is affected.
3. **Check:** Review recent changes, availability, connectivity, resource usage, and relevant logs.
4. **Diagnose:** Test one hypothesis at a time and record results.
5. **Resolve:** Apply the least disruptive approved fix.
6. **Validate:** Confirm the service works and the user can complete the required task.
7. **Document:** Record root cause, actions, outcome, and preventive recommendations.
8. **Escalate:** Share evidence and completed troubleshooting when specialist access is required.

## Incident Documentation Template
| Field | Details |
|---|---|
| Issue | Short incident title |
| Environment | OS, device, application, or server |
| Symptoms | What the user observed |
| Impact | Users/services affected and business impact |
| Checks Performed | Commands, logs, and tests |
| Root Cause | Confirmed cause, or "Under investigation" |
| Resolution | Steps taken to resolve |
| Validation | How the fix was verified |
| Prevention | Recommended preventive action |

## Important Safety Notes
- Run administrative commands only with appropriate authorization.
- Understand a command before executing it, especially commands that modify files, permissions, disks, network settings, or services.
- Do not publish passwords, API keys, personal data, or production logs containing secrets.
- Take backups and follow change-management procedures before production changes.
- Prefer read-only diagnostic checks before corrective actions.

## Contribution
Contributions are welcome. Keep documentation accurate, reproducible, clearly titled, and free of confidential information. Include the operating system/version and explain how each resolution was validated.

## License
This project is licensed under the [MIT License](LICENSE).
