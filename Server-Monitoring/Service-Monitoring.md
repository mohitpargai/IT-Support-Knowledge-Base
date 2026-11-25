# Service Monitoring

## Linux (systemd)

```bash
systemctl is-active <service>
systemctl status <service>
systemctl list-units --type=service --state=failed
journalctl -u <service> --since "30 minutes ago"
```

## Windows

PowerShell examples:

```powershell
Get-Service
Get-Service -Name "<service-name>"
```

## Monitoring Checklist
1. Confirm service state.
2. Check response time and application health, not only process state.
3. Review logs for errors and repeated restarts.
4. Check dependencies such as database, DNS, storage, and network.
5. Correlate service failures with deployments or infrastructure changes.
6. Follow approved recovery and escalation procedures.
