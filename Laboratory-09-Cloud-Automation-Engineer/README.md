# Laboratory 09 – The Cloud Automation Engineer

## Mission Overview

In this laboratory, I learned how to automate backup tasks using a Bash script. I created a script that automatically compresses important client data into a backup file. I also learned how to use cron to schedule backup tasks and make cloud operations more efficient.

## Objectives

- Understand Bash script syntax, including variables and basic commands
- Use nano to write and save scripts
- Modify file permissions with chmod
- Understand task scheduling and crontab syntax
- Document automation code and cron jobs in Markdown
- Complete the final chapter of my GitHub Cloud Computing Portfolio

## Commands Executed

```bash
mkdir app-data
echo "This is critical client data." > app-data/data.txt
nano backup.sh
./backup.sh
chmod +x backup.sh
./backup.sh
ls -l backups/
crontab -l
env EDITOR=nano crontab -e
crontab -l
```

## Skills Learned

- Creating and running Bash scripts
- Using variables to store folder names and file paths
- Compressing files using the tar command
- Changing file permissions using chmod
- Creating backup files for important data
- Scheduling automated tasks using cron
- Using Linux commands to manage files and directories
- Documenting cloud automation activities using Markdown
- Understanding the importance of automation in cloud computing
