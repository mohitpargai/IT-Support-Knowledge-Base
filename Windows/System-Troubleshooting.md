# Windows System Troubleshooting

## Useful Tools
- **Task Manager:** process and resource usage.
- **Event Viewer:** application, system, and security event logs.
- **Reliability Monitor:** timeline of application and Windows failures.
- **Device Manager:** device and driver status.
- **System Information:** hardware and OS details.

## Useful Commands

Run commands with appropriate permissions.

```powershell
systeminfo
sfc /verifyonly
DISM /Online /Cleanup-Image /CheckHealth
chkdsk C: /scan
```

These are inspection-oriented checks. Some repair options can modify the system or require a restart; review Microsoft documentation and organizational change policy before using repair commands.

## Troubleshooting Workflow
1. Capture the exact error, timestamp, and user impact.
2. Check recent Windows updates, driver changes, and installed software.
3. Review relevant Event Viewer entries.
4. Check disk space and system resource usage.
5. Run approved diagnostic checks.
6. Validate the system after any authorized repair.
7. Escalate with logs and collected evidence if the issue persists.
