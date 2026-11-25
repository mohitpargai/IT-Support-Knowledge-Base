# IP Configuration Troubleshooting

## Windows

```powershell
ipconfig /all
Get-NetIPConfiguration
Get-NetAdapter
```

## Linux

```bash
ip addr
ip route
nmcli device status
```

## Checklist
- Confirm the correct network adapter is connected.
- Check whether the address is expected for the network.
- Verify subnet mask/prefix and default gateway.
- Verify DNS server settings.
- Check for an APIPA address (169.254.x.x) on Windows, which can indicate DHCP configuration or reachability issues.
- Check DHCP scope availability with the network team.

Do not manually assign an address unless it is approved and confirmed to be unused.
