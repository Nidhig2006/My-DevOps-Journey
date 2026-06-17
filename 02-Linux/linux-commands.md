#  50 Linux Commands 


---




# Navigation Commands

## Print Current Working Directory

```bash
pwd
```

Displays the full path of the current directory.

Example:

```bash
/home/nidhi/projects
```

---

## List Files and Directories

```bash
ls
```

Displays files and folders in the current directory.

### Detailed Listing

```bash
ls -l
```

Shows permissions, owner, size, and modification date.

### Show Hidden Files

```bash
ls -la
```

Displays hidden files such as `.bashrc`.

---

## Change Directory

```bash
cd directory_name
```

Example:

```bash
cd Documents
```

Move to the Documents directory.

### Move to Home Directory

```bash
cd
```

### Move One Directory Back

```bash
cd ..
```

---

# File and Directory Commands

## Create a Directory

```bash
mkdir project
```

Creates a new directory named `project`.

---

## Create Nested Directories

```bash
mkdir -p projects/devops/linux
```

Creates multiple directories at once.

---

## Remove Empty Directory

```bash
rmdir project
```

Deletes an empty directory.

---

## Create a File

```bash
touch notes.txt
```

Creates an empty file.

---

## Copy Files

```bash
cp file.txt backup/
```

Copies a file to another location.

---

## Copy Directory

```bash
cp -r project backup/
```

Copies a directory recursively.

---

## Move or Rename Files

```bash
mv old.txt new.txt
```

Renames a file.

Example:

```bash
mv notes.txt linux-notes.txt
```

---

## Remove File

```bash
rm file.txt
```

Deletes a file.

---

## Remove Directory Recursively

```bash
rm -r project
```

Deletes a directory and its contents.

---

# File Viewing Commands

## Display File Contents

```bash
cat file.txt
```

Displays the contents of a file.

---

## Display First 10 Lines

```bash
head file.txt
```

Example:

```bash
head -5 file.txt
```

Displays the first 5 lines.

---

## Display Last 10 Lines

```bash
tail file.txt
```

Example:

```bash
tail -20 log.txt
```

Displays the last 20 lines.

---

## View Large Files

```bash
less file.txt
```

Allows scrolling through large files.

Press:

* `q` → Quit
* `/text` → Search text

---

# Permission Commands

Linux permissions are represented as:

```text
r = Read (4)
w = Write (2)
x = Execute (1)
```

Example:

```text
755
```

Means:

```text
Owner: Read + Write + Execute
Group: Read + Execute
Others: Read + Execute
```

---

## Change Permissions

```bash
chmod 755 script.sh
```

Makes the script executable.

---

## Change Owner

```bash
sudo chown user file.txt
```

Changes ownership of a file.

Example:

```bash
sudo chown nidhi project.txt
```

---

# Compression Commands

## Create Tar Archive

```bash
tar -cf archive.tar files/
```

Creates a tar archive.

---

## Extract Tar Archive

```bash
tar -xf archive.tar
```

Extracts files.

---

## Create Compressed Archive

```bash
tar -czf backup.tar.gz project/
```

Creates a compressed archive.

---

## Extract Compressed Archive

```bash
tar -xzf backup.tar.gz
```

Extracts compressed files.

---

## Compress File

```bash
gzip file.txt
```

Creates:

```text
file.txt.gz
```

---

## Decompress File

```bash
gunzip file.txt.gz
```

---

# User Management Commands

## Add User

```bash
sudo useradd harry
```

Creates a new user.

---

## Set Password

```bash
sudo passwd harry
```

Assigns or changes a password.

---

## Delete User

```bash
sudo userdel harry
```

Deletes a user account.

---

## Switch User

```bash
su username
```

Example:

```bash
su root
```

---

## Execute as Super User

```bash
sudo command
```

Example:

```bash
sudo apt update
```

---

# Process Management Commands

## View Running Processes

```bash
ps aux
```

Shows all running processes.

---

## Real-Time Process Monitor

```bash
top
```

Displays CPU and memory usage.

---

## Interactive System Monitor

```bash
htop
```

Improved version of `top`.

---

## Kill Process

```bash
kill PID
```

Example:

```bash
kill 1234
```

Terminates process 1234.

---

## Force Kill Process

```bash
kill -9 PID
```

Forcefully terminates a process.

---

# System Information Commands

## Show Operating System Information

```bash
uname -a
```

Displays kernel and system information.

---

## Show Current User

```bash
whoami
```

Displays logged-in user.

---

## Show Date and Time

```bash
date
```

Displays system date and time.

---

## Show System Uptime

```bash
uptime
```

Displays how long the system has been running.

---

## View Command History

```bash
history
```

Displays previously executed commands.

---

# Disk Management Commands

## Display Disk Space Usage

```bash
df -h
```

Shows available disk space in human-readable format.

---

## Display Directory Size

```bash
du -sh folder/
```

Shows total size of a directory.

---

## Mount File System

```bash
sudo mount /dev/sdb1 /mnt/usb
```

Mounts a device.

---

## Unmount File System

```bash
sudo umount /mnt/usb
```

Unmounts a device.

---

# Networking Commands

## Check Network Connectivity

```bash
ping google.com
```

Tests network connection.

---

## View IP Address

```bash
ip addr
```

Modern replacement for `ifconfig`.

---

## View Network Connections

```bash
netstat -tuln
```

Displays active network connections.

---

## Display Routing Table

```bash
route
```

Shows network routing information.

---

# SSH and Remote Access Commands

## Connect to Remote Server

```bash
ssh username@server-ip
```

Example:

```bash
ssh ubuntu@192.168.1.10
```

---

## Securely Copy File

```bash
scp file.txt user@host:/home/user/
```

Transfers files securely between systems.

---

# Service Management Commands

## Start Service

```bash
sudo systemctl start nginx
```

---

## Stop Service

```bash
sudo systemctl stop nginx
```

---

## Restart Service

```bash
sudo systemctl restart nginx
```

---

## Check Service Status

```bash
sudo systemctl status nginx
```

---

## Enable Service at Boot

```bash
sudo systemctl enable nginx
```

---

# Search and Text Processing Commands

## Find Executable Path

```bash
which python
```

Displays the location of a command.

---

## Search Files

```bash
find . -name "*.txt"
```

Finds all text files.

---

## Search Text in Files

```bash
grep "error" logfile.txt
```

Searches for matching text.

---

## Sort Data

```bash
sort file.txt
```

Sorts file contents alphabetically.

---

## Remove Duplicate Lines

```bash
uniq file.txt
```

Removes duplicate entries.

---

## Print Text

```bash
echo "Hello Linux"
```

Displays text on screen.

---

## Write Output to File and Screen

```bash
ls | tee output.txt
```

Saves output while displaying it.

---

# DevOps Commands

These commands are commonly used by DevOps engineers.

## Download Files

```bash
wget https://example.com/file.zip
```

Downloads files from the internet.

---

## Test APIs

```bash
curl https://api.github.com
```

Makes HTTP requests.

---

## Display Memory Usage

```bash
free -h
```

Shows RAM and swap usage.

---

## Display Hostname

```bash
hostname
```

Shows the system hostname.

---

## View Open Ports

```bash
ss -tulnp
```

Displays listening ports and services.

---

## View Logs

```bash
journalctl
```

Displays system logs.

---

## Edit Scheduled Tasks

```bash
crontab -e
```

Creates and manages scheduled jobs.

Example:

```bash
0 2 * * * /home/user/backup.sh
```

Runs a backup script every day at 2:00 AM.

