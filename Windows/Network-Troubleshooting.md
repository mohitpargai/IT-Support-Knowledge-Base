# Windows Network Troubleshooting

## Useful Commands

| Command | Purpose |
|---|---|
| `ipconfig /all` | Show IP, gateway, DNS, and adapter details |
| `ipconfig /release` | Release a DHCP IPv4 lease |
| `ipconfig /renew` | Request a DHCP IPv4 lease |
| `ipconfig /flushdns` | Clear the DNS resolver cache |
| `ping <host>` | Test reachability |
| `nslookup <hostname>` | Query DNS |
| `tracert <host>` | Trace network path |
| `Test-NetConnection <host> -Port <port>` | Test TCP connectivity in PowerShell |

## Troubleshooting Steps
1. Check Wi-Fi or Ethernet connection status.
2. Run `ipconfig /all` and confirm address, gateway, and DNS.
3. Test the default gateway with `ping`.
4. Test a known external IP where policy permits.
5. Test DNS with `nslookup`.
6. Test the required server port with `Test-NetConnection`.
7. Check VPN and proxy settings according to organizational policy.

Record command output and timestamps when escalating.
