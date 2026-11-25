# Linux Network Troubleshooting

## Symptoms
- Host cannot reach another server.
- Name resolution fails.
- Network interface has no expected IP address.
- Intermittent packet loss or high latency.

## Diagnostic Commands
| Command | Purpose |
|---|---|
| `ip addr` | Display interface addresses |
| `ip route` | Display routing table |
| `ping -c 4 <host>` | Test basic reachability |
| `getent hosts <hostname>` | Test name resolution |
| `resolvectl status` | Inspect resolver configuration on supported systems |
| `ss -tulpen` | Inspect listening sockets |
| `traceroute <host>` | Trace network path, if installed |

## Troubleshooting Sequence
1. Confirm whether the issue affects one host or multiple hosts.
2. Check interface state and IP configuration using `ip addr`.
3. Confirm the default route using `ip route`.
4. Test the configured gateway, then a known reachable IP.
5. Test DNS separately using `getent hosts <hostname>`.
6. Check relevant firewall rules and service ports with the authorized administrator.
7. Review system and network logs.

## Interpretation
- IP connectivity works but hostnames fail: investigate DNS.
- No valid address or route: investigate DHCP or network configuration.
- Local gateway is unreachable: investigate local network, VLAN, interface, or gateway.
- Only one application port fails: investigate service state, listening port, and firewall policy.

## Caution
Do not flush firewall rules, replace resolver configuration, or restart network services on a remote production server without an approved change and an alternate access path.
