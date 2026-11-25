# Linux Disk Management

## Check Disk Capacity
```bash
df -h
df -i
lsblk
```
- `df -h` shows filesystem space usage.
- `df -i` shows inode usage.
- `lsblk` displays block devices and mount points.

## Find Large Directories
```bash
sudo du -xhd1 /var 2>/dev/null | sort -h
```
Adjust the path to the filesystem being investigated. This command reads directory usage; it does not delete files.

## Identify Large Files
```bash
sudo find /var -xdev -type f -size +500M -print
```

## Troubleshooting Checklist
1. Identify the full filesystem using `df -h`.
2. Check inode usage using `df -i`.
3. Locate large directories and files.
4. Review log retention, application growth, and backup policies.
5. Confirm ownership and business purpose before cleanup.
6. Follow approved retention and change procedures.
7. Recheck capacity after an authorized cleanup.

## Important
Never delete files blindly from `/var`, database directories, application directories, or backup locations. Do not truncate active logs without understanding logging and service requirements.
