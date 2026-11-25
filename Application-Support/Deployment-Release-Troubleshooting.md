# Deployment and Release Troubleshooting

Use this guide when an application fails after a deployment, behaves differently between environments, or does not start after a release.

## 1. Capture Release Details

- Application name and version/build
- Environment and affected instances
- Deployment date, time, and timezone
- Deployment/change reference
- Deployment status and recorded errors
- Last known good version
- User impact and available workaround

## 2. Initial Checks

1. Confirm whether the issue started immediately after the release.
2. Review deployment logs and pipeline/job status.
3. Confirm the deployed artifact and version.
4. Check configuration differences between environments.
5. Check application service health and startup logs.
6. Verify database migrations and dependent service compatibility.
7. Check load balancer, routing, and health-check status where applicable.

## 3. Common Failure Areas

| Symptom | Areas to Check |
|---|---|
| Application does not start | Startup logs, runtime, configuration, permissions |
| Health check fails | Health endpoint, dependencies, port, routing |
| Feature unavailable | Artifact version, feature flags, configuration |
| Database errors | Migration status, schema compatibility, credentials reference |
| Works in test but not production | Environment variables, secrets, permissions, integrations |

## 4. Recovery

- Follow the approved release and change-management procedure.
- Do not independently roll back production systems.
- Confirm rollback compatibility, database impact, and data migration implications with the release owner.
- Record the decision, approval, execution time, and outcome.

## 5. Post-Deployment Validation

- Confirm application and dependent services are healthy.
- Test login and key business workflows.
- Verify integrations and scheduled jobs where relevant.
- Review logs and error rates after deployment.
- Confirm with the service owner or users.
- Record lessons learned and preventive actions.
