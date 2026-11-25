# Network Connectivity Troubleshooting

## Diagnostic Sequence
1. Identify the source and destination systems.
2. Confirm whether the issue is isolated or widespread.
3. Check local interface and IP configuration.
4. Test gateway reachability.
5. Test destination reachability where ICMP is permitted.
6. Test the required application port.
7. Inspect route, firewall, VPN, proxy, and service dependencies.

## Useful Commands

**Windows PowerShell**
```powershell
Test-NetConnection <hostname> -Port <port>
tracert <hostname>
```

**Linux**
```bash
ping -c 4 <hostname>
ip route
ss -tulpen
```

## Escalation Evidence
Include source/destination, timestamp and timezone, affected users, error message, test results, and recent changes. A failed ping alone does not prove a host or service is down; ICMP may be blocked.
