# CPU and Memory Monitoring

## Linux

```bash
uptime
top
free -h
vmstat 1 5
```

## Windows
- Task Manager: review CPU and memory utilization.
- Resource Monitor: inspect processes and resource consumers.
- Performance Monitor: collect counters over time.

## Monitoring Checklist
1. Record the observation time and host.
2. Compare current usage with the normal baseline.
3. Identify the processes consuming the most resources.
4. Check whether the load is sustained or temporary.
5. Correlate with application traffic, scheduled jobs, and recent changes.
6. Check service response and user impact.
7. Escalate sustained abnormal usage with evidence.

High CPU or memory use alone does not prove a fault. Compare against workload and baseline before taking action.
