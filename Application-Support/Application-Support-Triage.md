# Application Support Triage

A structured approach to investigating application incidents and service requests.

## 1. Information to Collect

| Field | What to Record |
|---|---|
| Application | Name and version/build |
| Environment | Production, staging, test, or development |
| Reporter | Team or role; avoid publishing personal data |
| Time | Incident start time and timezone |
| Impact | Number of users and business functions affected |
| Symptoms | Exact error message and observed behaviour |
| Reproduction | Steps that consistently trigger the issue |
| Recent Changes | Release, configuration, infrastructure, or access changes |

## 2. Determine Scope and Priority

- Check whether the issue affects one user, a group, or all users.
- Determine whether a critical business workflow is blocked.
- Check whether a workaround exists.
- Follow the organization's incident-priority and escalation matrix.

Do not assign severity based only on the wording of an error message. Consider verified business impact and service scope.

## 3. Initial Technical Checks

1. Confirm the application URL or client entry point.
2. Check service availability and health indicators.
3. Verify DNS and network connectivity to required endpoints.
4. Check authentication and authorization behaviour.
5. Review application and platform logs around the incident time.
6. Check database, API, file storage, and external integration dependencies.
7. Compare the affected user's result with a known-good user or environment, where authorized.

## 4. Resolution and Validation

- Make only approved changes.
- Record the change and the reason for it.
- Re-test the original failing workflow.
- Confirm the result with the reporter or service owner.
- Monitor for recurrence where appropriate.

## 5. Escalation Template

Include:
- Application and environment
- Incident start time and timezone
- Business impact and affected user count
- Exact error message
- Reproduction steps
- Relevant sanitized log entries
- Checks already completed and their results
- Recent changes and suspected dependency
- Current workaround, if any

Never attach credentials, access tokens, session cookies, or unredacted sensitive data.
