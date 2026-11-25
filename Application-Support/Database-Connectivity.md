# Database Connectivity Troubleshooting

Use this guide when an application cannot connect to its database, experiences connection timeouts, or reports database-related errors.

## 1. Initial Checks

- Confirm the affected application and environment.
- Identify the database type and approved database hostname.
- Confirm whether the issue affects one application instance or multiple services.
- Check whether a planned maintenance or database incident is in progress.
- Record the error text and timestamp.

## 2. Connectivity Checks

From an authorized application host, verify DNS resolution and network reachability to the approved database endpoint.

Examples:

```bash
getent hosts <database-hostname>
```

For a known TCP port, use an approved connectivity test:

```bash
nc -vz <database-hostname> <port>
```

If the utility is unavailable, use the organization's approved network diagnostic tool. A successful TCP connection does not prove that database authentication or queries will succeed.

## 3. Application Configuration Checks

Verify through the approved secret/configuration management process:
- Database hostname and port
- Database/service name
- Environment-specific configuration
- Secret or credential reference validity
- Connection pool settings
- TLS requirements and certificate status

Never paste passwords or full connection strings containing credentials into tickets, chat, screenshots, or this public repository.

## 4. Database and Application Checks

Coordinate with the database administrator or service owner to check:
- Database service availability
- Connection limits and active sessions
- Database resource utilization
- Relevant database logs
- Account status and required permissions
- Recent schema, network, or configuration changes

## 5. Resolution and Validation

1. Confirm the cause with the responsible service owner.
2. Follow change approval for configuration or infrastructure changes.
3. Test the application's database-dependent workflow.
4. Confirm that the application has recovered.
5. Document the evidence, fix, validation, and prevention steps.

Do not restart a database, terminate sessions, change permissions, or modify production data without explicit authorization.
