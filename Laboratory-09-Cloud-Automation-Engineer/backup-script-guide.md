# Backup Script Guide

## The Script (backup.sh)

```bash
#!/bin/bash
# Automated Backup Script for CloudNova Technologies

SOURCE_DIR="app-data"
BACKUP_DIR="backups"
TIMESTAMP=$(date +"%Y%m%d_%H%M%S")

echo "Initiating automated backup..."

# Create the backup directory if it does not exist
mkdir -p $BACKUP_DIR

# Compress the source directory into a tarball (.tar.gz)
tar -czf $BACKUP_DIR/backup_$TIMESTAMP.tar.gz $SOURCE_DIR

echo "Backup completed successfully at $TIMESTAMP!"
```

## What `chmod +x` Does

The `chmod +x` command gives permission to execute a file. At first, I received a Permission denied error when I tried to run my backup script. After using `chmod +x backup.sh`, I was able to execute the script successfully and create a backup file.

## The Cron Expression

```bash
0 2 * * * /root/backup.sh
```

| Field | Value | Meaning |
|---|---|---|
| Minute | 0 | At minute 0 of the hour |
| Hour | 2 | At 2 AM (24-hour clock) |
| Day of Month | * | Every day of the month |
| Month | * | Every month |
| Day of Week | * | Every day of the week |

Together, this cron expression runs `/root/backup.sh` every day at 2:00 AM.

## Backup Verification

I used the following command to check if the backup file was successfully created:

```bash
ls -l backups/
```

The terminal displayed the backup file:

```text
-rw-r--r-- 1 root root 177 Nov 6 03:37 backup_20261106_033732.tar.gz
```

This confirms that the backup script successfully compressed the `app-data` folder into a `.tar.gz` file.

## Cron Job Configuration

I used the following commands to check and configure the cron job:

```bash
crontab -l
env EDITOR=nano crontab -e
crontab -l
```

The cron job was configured to execute the backup script every day at 2:00 AM. The `crontab -l` command was used to verify the scheduled task.
