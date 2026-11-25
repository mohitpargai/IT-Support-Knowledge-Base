# API Troubleshooting

Use this guide when an application cannot call an API, receives unexpected responses, or experiences slow API requests.

## 1. Information to Collect

- API endpoint and HTTP method
- Environment (test, staging, or production)
- Request timestamp and timezone
- HTTP status code and sanitized response body
- Request/correlation ID, if available
- Expected versus actual result
- Whether the issue affects all clients or one client

Do not publish authorization headers, API keys, bearer tokens, or personal data.

## 2. Basic Connectivity Check

Where command-line testing is authorized, use a safe request against an approved endpoint:

```bash
curl -i --connect-timeout 10 https://api.example.com/health
```

Replace the example URL with the approved environment endpoint. Avoid sending production data in diagnostic requests.

## 3. Common HTTP Status Categories

| Status | General Meaning | Initial Checks |
|---|---|---|
| 2xx | Request succeeded | Verify response content and business result |
| 3xx | Redirection | Review URL, redirect target, and proxy rules |
| 400 | Bad request | Check request format and required fields |
| 401 | Authentication required or failed | Check token validity and authentication flow |
| 403 | Request forbidden | Check role, scope, and access policy |
| 404 | Resource not found | Check path, route, and resource identifier |
| 429 | Too many requests | Review rate limits and retry guidance |
| 5xx | Server-side failure | Check API service health, logs, and dependencies |

A status code alone does not establish root cause. Correlate it with server logs and request details.

## 4. Troubleshooting Sequence

1. Confirm the endpoint, method, and environment.
2. Check DNS and network reachability.
3. Check TLS/certificate validity where relevant.
4. Verify authentication and required permissions.
5. Validate request headers and payload format using a sanitized sample.
6. Check API gateway and application logs using the request/correlation ID.
7. Check downstream dependencies such as databases or external services.
8. Re-test with an approved request and document the response.

## 5. Escalation Evidence

Share the endpoint (without secrets), method, timestamp, status code, correlation ID, sanitized request/response details, and checks already performed.
