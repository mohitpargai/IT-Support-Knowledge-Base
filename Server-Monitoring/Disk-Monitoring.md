# Server Disk Monitoring

## Linux

```bash
df -h
df -i
lsblk
sudo du -xhd1 /var 2>/dev/null | sort -h
```

## Windows PowerShell

```powershell
Get-Volume
Get-CimInstance Win32_LogicalDisk |
  Select-Object DeviceID, Size, FreeSpace
```

## Monitoring Checklist
- Track free capacity and growth rate.
- Monitor inode usage on Linux.
- Check application logs, temporary files, and backup retention.
- Review disk latency and I/O where monitoring tools are available.
- Alert based on agreed thresholds and service requirements.
- Investigate trends before capacity becomes critical.

Do not remove production data without owner approval and a retention review.
