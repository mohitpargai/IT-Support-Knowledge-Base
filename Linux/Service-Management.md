# Linux Service Management

Systems using systemd commonly use `systemctl` to inspect and manage services.

## Common Commands
| Command | Purpose |
|---|---|
| `systemctl status <service>` | Inspect service state |
| `systemctl is-active <service>` | Check whether service is active |
| `systemctl is-enabled <service>` | Check whether service starts at boot |
| `systemctl list-units --type=service --state=failed` | List failed services |
| `journalctl -u <service> -n 100` | Read recent service logs |

## Troubleshooting a Failed Service
1. Run `systemctl status <service>`.
2. Read recent logs with `journalctl -u <service> -n 100`.
3. Check configuration syntax using the application's documented validation command.
4. Check dependencies, ports, permissions, and disk capacity.
5. Identify recent deployments or configuration changes.
6. Restart only when authorized and after assessing user impact.
7. Verify service health and application functionality.

## Restart Command
```bash
sudo systemctl restart <service>
```
A restart can interrupt users. Follow the applicable maintenance or incident procedure before running it.
