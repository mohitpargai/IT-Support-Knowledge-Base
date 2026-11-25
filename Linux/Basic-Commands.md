# Basic Linux Commands

A quick reference for common Linux administration and support tasks.

## System Information
| Command | Purpose |
|---|---|
| `uname -a` | Display kernel and system information |
| `hostnamectl` | Display hostname and OS information |
| `uptime` | Show uptime and load averages |
| `date` | Display system date and time |
| `whoami` | Show the current user |
| `id` | Show user and group identifiers |

## Files and Directories
| Command | Purpose |
|---|---|
| `pwd` | Print current directory |
| `ls -lah` | List files, including hidden files |
| `cd /path` | Change directory |
| `find /path -name "file"` | Search for a file by name |
| `du -sh /path` | Show directory size |
| `df -h` | Show filesystem capacity |

## Processes and Resources
| Command | Purpose |
|---|---|
| `top` | Interactive process/resource view |
| `ps aux` | List running processes |
| `free -h` | Show memory usage |
| `kill -TERM <PID>` | Request graceful process termination |

## Logs
- `journalctl -n 100` — show the latest 100 journal entries.
- `journalctl -u <service> --since "1 hour ago"` — inspect recent service logs.
- `tail -f /var/log/<log-file>` — follow a log file where applicable.

## Safe Usage
- Prefer read-only commands while diagnosing an unfamiliar system.
- Use elevated privileges only when required and authorized.
- Verify paths before running commands that modify files.
- Do not terminate processes until their purpose and impact are understood.
