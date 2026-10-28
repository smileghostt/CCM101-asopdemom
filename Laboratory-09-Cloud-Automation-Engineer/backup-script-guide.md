# Script used in `backup.sh`
```
 #!/bin/bash\
 \# Automated Backup Script for CloudNova Technologies\
 SOURCE_DIR="app-data"\
 BACKUP_DIR="backups"\
 TIMESTAMP=$(date +"%Y%m%d_%H%M%S")\
 echo "Initiating automated backup..."\
 \# Create the backup directory if it does not exist\
 mkdir -p $BACKUP_DIR\
 \# Compress the source directory into a tarball (.tar.gz)\
 tar -czf $BACKUP_DIR/backup_$TIMESTAMP.tar.gz $SOURCE_DIR\
 echo "Backup completed successfully at $TIMESTAMP!"
 ```

The following is the automatic script used for backups within CloudNova Technologies.

> ### REMEMBER TO USE `chmod -x` ON THE SCRIPT AFTER CREATION
> This ensures that the script is executable. Without this, permission to execute the script is denied. This is a vital step in order to create a running script.

# Cron Expression

`0 2 * * * /root/backup.sh`

This expression points towards the `backup.sh` script used. The first segment of the entire expression before the path actually points to the time.

- The first number, 0 in this case, is actually the minute field. Within this script for example, this means that the script will start in the very start of an hour.

- The second number in the field, which is 2, is the hour field. Since it is set to 2, it means that the script will start at 2 in the morning.

- The third part of the field, AKA the first asterisk, is the day of the month. Since it is set to *, this means its every day in the month.
    - If it were a number, it'd be the day of the month. For example, if it was 5, it'd always start at the fifth of the month.
- The fourth part of the field, the second asterisk, is the month field. Since it is an asterisk as well, this means its every month.
    - If it were a number, it'd be the specific month of the year. For example, if it was 10, it'd be every October.
- The final field, the third asterisk, is the day of the week. Since it is an asterisk, this means it is every week.
    - If it were a number, it'd be a specific day of the week from Monday (which is 1) to Sunday (which is either 0 or 7). So if it was 4, it would mean the script runs every Thursday.

> ### REMEMBER!
> The asterisk (*) always means any within a cron expression. Hence why when applied, it applies to every day/month/etc..