# DNS Troubleshooting

## Symptoms
- A hostname cannot be resolved.
- An application works by IP address but not by hostname.
- Resolution is slow or inconsistent.

## Windows

```powershell
ipconfig /all
nslookup example.com
ipconfig /flushdns
```

## Linux

```bash
getent hosts example.com
resolvectl status
```

## Diagnostic Steps
1. Confirm the exact hostname and affected client.
2. Check which DNS servers the client is using.
3. Query the hostname with `nslookup` or `getent hosts`.
4. Compare results with a known-good client or approved DNS resolver.
5. Check VPN, split-DNS, and internal DNS requirements.
6. Escalate with timestamp, resolver address, and query result.

Only clear local DNS caches when appropriate; cache flushing does not repair an incorrect DNS record or resolver configuration.
