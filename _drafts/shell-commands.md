# Shell commands

## SCP

| Command | Description |
| ------- | ----------- |
| `scp file.txt remote_username@remote_ip:/remote/directory` | secure copy local file.txt to remote computer |

## Network

| Command | Description |
| ------- | ----------- |
| `ip address show` | Show all IP addresses for all network adapters |

## Filesystem

| Command | Description |
| ------- | ----------- |
| `df -h` | check free space on disk |
| `du` | check the size of folders |
| `ls -l [file]` | displays permissions for that file |
| `ls -ld [directory]` | displays the permissions for that directory |
| `rm -r [directoryPath]` | will remove all directory and all files within e.g. rm -r /home/michael/rubbish |
| `rm -r [directoryPath/*]` | will remove all files in that [directoryPath] |
| `touch /home/michael/newFile.txt` | will create a new text file in the /home/michael directory |

## Server management

| Command | Description |
| ------- | ----------- |
| `sudo shutdown -P now` | shutdown server |
| `free -m` | check free and used memory (Displayed in Mb) |
| `sudo apt-get update` | update the APT package index |
| `sudo apt-get upgrade` | upgrades packages or apps currently installed on your system |
| `sudo apt-get dist-upgrade` | will upgrade the actual distribution e.g. 10.10 to 10.11 |
| `crontab -l > ~/Desktop/cron.txt` | will copy your cron jobs to a file on the Desktop called cron.txt |
