# Application Log Troubleshooting

Logs help identify application errors, failed requests, dependency problems, and unexpected behaviour.

## 1. Identify the Correct Log Source

Depending on the application architecture, relevant sources may include:
- Application logs
- Web server logs (for example, IIS, Apache, or Nginx)
- Operating system event or journal logs
- API gateway or reverse proxy logs
- Database logs
- Container or orchestration platform logs

Use the application's deployment documentation to identify the authoritative log location.

## 2. Linux Checks

Examples for systems using systemd:

```bash
journalctl -u <service-name> --since "30 minutes ago"
journalctl -u <service-name> -n 100
```

For a known application log file:

```bash
tail -n 100 /path/to/application.log
grep -i "error" /path/to/application.log
```

Do not assume every Linux application writes to the same directory.

## 3. Windows Checks

- Open Event Viewer.
- Review Windows Logs > Application and System.
- Filter by the incident time and relevant Error or Warning events.
- Check the application's own log directory, if documented.
- For IIS-hosted applications, review the relevant IIS site logs and application pool events.

## 4. What to Look For

| Log Pattern | Possible Area to Investigate |
|---|---|
| Connection timeout | Network, service availability, firewall, or dependency |
| Authentication failure | Identity provider, credentials, account status, or configuration |
| Database connection error | Database availability, network path, connection settings, or capacity |
| HTTP 404 | URL, route, deployment content, or reverse-proxy mapping |
| HTTP 500 | Application exception or server-side failure |
| Out of memory | Resource limits, workload, or application behaviour |

These are starting points, not confirmed root causes.

## 5. Log Handling and Safety

- Match log timestamps with the reported incident time and timezone.
- Preserve relevant evidence before rotating or modifying logs.
- Redact tokens, passwords, personal data, and confidential identifiers before sharing.
- Do not delete or truncate production logs to resolve a disk alert without approval.
- Record the log source and exact time window used during investigation.
