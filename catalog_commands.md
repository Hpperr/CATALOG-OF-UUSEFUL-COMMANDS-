#!/bin/bash
# ═══════════════════════════════════════════════════════════════════
#  C A T A L O G   O F   U S E F U L   C O M M A N D S
#  U L T I M A T E   E D I T I O N   v 3 . 0
# ═══════════════════════════════════════════════════════════════════
#  Author: F1REW0LF
#  License: MIT - Free for Community
#  Platform: Linux | Windows CMD | PowerShell | GUI Search
#  ═══════════════════════════════════════════════════════════════════
#
#  📚 COMPLETE CATALOG STRUCTURE:
#  ──────────────────────────────────────────────────────────────────
#  1.   Linux Commands (Bash/Zsh)
#  2.   Windows CMD Commands
#  3.   PowerShell Commands
#  4.   Network Commands (All Platforms)
#  5.   System Information (All Platforms)
#  6.   File Operations (All Platforms)
#  7.   Process Management (All Platforms)
#  8.   User Management (All Platforms)
#  9.   Disk & Storage (All Platforms)
#  10.  Security & Firewall Commands
#  11.  Docker & Container Commands
#  12.  Kubernetes Commands
#  13.  Git Commands
#  14.  Database Commands (MySQL, PostgreSQL, MongoDB, Redis)
#  15.  Cloud CLI Commands (AWS, Azure, GCP)
#  16.  Monitoring & Logging
#  17.  Automation & Scripting (Ansible, Terraform, Jenkins)
#  18.  Performance Tuning
#  19.  Troubleshooting Commands
#  20.  Backup & Recovery Commands
#  21.  Registry Commands (Windows)
#  22.  Windows Management Instrumentation (WMI)
#  23.  Network Advanced (Routing, VPN, DNS, Load Balancing)
#  24.  System Utilities & Tools
#  25.  Web & API Testing
#  26.  Data Processing (jq, yq, csv, JSON, XML)
#  27.  SSH & Remote Access Advanced
#  28.  Cron & Scheduled Tasks
#  29.  Encryption & Hashing
#  30.  Package Management (All Platforms)
#  31.  Text Processing Mastery
#  32.  System Recovery & Rescue
#  33.  Quick Reference & Cheatsheets
#  34.  Real-World Scenarios & Command Combinations
#  35.  Pro Tips & Hidden Gems
#
# ═══════════════════════════════════════════════════════════════════

# ================================================================
# 1. LINUX COMMANDS (BASH/ZSH) - COMPLETE
# ================================================================

# ─── FILE OPERATIONS ──────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `ls -la` | List all files with permissions |
| `ls -lh` | List with human-readable sizes |
| `ls -lt` | List sorted by modification time |
| `ls -ltr` | List sorted by time (newest last) |
| `ls -R` | List recursively |
| `ls -S` | Sort by size |
| `ls -X` | Sort by extension |
| `ls -d */` | List only directories |
| `ls -l \| grep ^d` | List only directories with details |
| `ls -l \| grep ^-` | List only files |
| `ls -l \| sort -k5 -rn` | Sort by size descending |
| `ls -l \| awk '{print $5, $9}' \| sort -rn` | Show size and name sorted |
| `ls -l --time-style=+%Y-%m-%d` | Custom date format |
| `cat file.txt` | Display full file |
| `tac file.txt` | Display file in reverse |
| `less file.txt` | View file page by page |
| `more file.txt` | View file page by page |
| `head -n 20 file.txt` | Show first 20 lines |
| `tail -n 50 file.txt` | Show last 50 lines |
| `tail -f file.txt` | Follow file updates in real-time |
| `tail -F file.txt` | Follow even if file is rotated |
| `find / -name "*.txt"` | Find files by name |
| `find / -type f -size +100M` | Find files larger than 100MB |
| `find . -mtime -7` | Files modified in last 7 days |
| `find . -mtime +30` | Files modified more than 30 days ago |
| `find . -cmin -60` | Files changed in last 60 minutes |
| `find . -type f -empty` | Find empty files |
| `find . -type d -empty` | Find empty directories |
| `find . -type f -perm 644` | Find files with specific permissions |
| `find . -type f -user username` | Find files owned by user |
| `find . -type f -exec chmod 644 {} \;` | Change permissions on found files |
| `find . -type f -exec grep -l "pattern" {} \;` | Find files containing pattern |
| `find . -type f -exec rm {} \;` | Delete found files |
| `find . -type f -name "*.log" -delete` | Delete all .log files |
| `find . -type f -name "*.tmp" -mtime +7 -delete` | Delete .tmp files older than 7 days |
| `grep "pattern" file.txt` | Search pattern in file |
| `grep -r "pattern" ./` | Recursive search in directory |
| `grep -i "pattern" file` | Case-insensitive search |
| `grep -v "pattern" file` | Exclude pattern |
| `grep -l "pattern" *` | List files containing pattern |
| `grep -n "pattern" file` | Show line numbers |
| `grep -A 5 "pattern" file` | Show 5 lines after match |
| `grep -B 5 "pattern" file` | Show 5 lines before match |
| `grep -C 5 "pattern" file` | Show 5 lines before and after |
| `grep -e "pattern1" -e "pattern2" file` | Multiple patterns |
| `grep -f patterns.txt file` | Use pattern file |
| `grep -c "pattern" file` | Count matches |
| `grep -o "pattern" file` | Only matching part |
| `grep -E "pattern" file` | Extended regex |
| `grep -P "pattern" file` | Perl regex |
| `grep --color=auto "pattern" file` | Highlight matches |
| `chmod 755 file` | rwxr-xr-x |
| `chmod 644 file` | rw-r--r-- |
| `chmod -R 755 directory` | Recursive permission change |
| `chmod +x file` | Make executable |
| `chmod -x file` | Remove executable |
| `chmod u+x file` | User execute |
| `chmod g+x file` | Group execute |
| `chmod o+x file` | Others execute |
| `chown user:group file` | Change owner and group |
| `chown -R user:group dir` | Recursive owner change |
| `chown user file` | Change owner only |
| `chgrp group file` | Change group only |
| `ln -s target linkname` | Create symbolic link |
| `ln target linkname` | Create hard link |
| `stat file.txt` | File statistics |
| `file file.txt` | Determine file type |
| `touch file.txt` | Create empty file or update timestamp |
| `touch -t 202401011200 file.txt` | Set specific timestamp |
| `mkdir dir` | Create directory |
| `mkdir -p path/to/dir` | Create nested directories |
| `mkdir -m 755 dir` | Create with permissions |
| `rmdir dir` | Remove empty directory |
| `rm -rf dir` | Remove directory with contents |
| `rm -i file` | Interactive delete |
| `rm -f file` | Force delete |
| `cp file1 file2` | Copy file |
| `cp -r dir1 dir2` | Copy directory recursively |
| `cp -a dir1 dir2` | Archive copy (preserve attributes) |
| `cp -u file1 file2` | Copy only if newer |
| `cp -i file1 file2` | Interactive copy |
| `cp -v file1 file2` | Verbose copy |
| `mv file1 file2` | Move/rename |
| `mv -i file1 file2` | Interactive move |
| `mv -u file1 file2` | Move only if newer |
| `rsync -av src/ dest/` | Sync directories |
| `rsync -avz src/ user@host:/dest/` | Sync with compression |
| `rsync -av --delete src/ dest/` | Delete extra files |
| `rsync -av --exclude='*.tmp' src/ dest/` | Exclude pattern |
| `rsync -av --progress src/ dest/` | Show progress |
| `scp file user@host:/path` | Secure copy to remote |
| `scp user@host:/path/file .` | Secure copy from remote |
| `scp -P 2222 file user@host:/path` | With custom port |
| `scp -r dir user@host:/path` | Recursive copy |

# ─── SYSTEM INFORMATION ──────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `uname -a` | All system information |
| `uname -r` | Kernel version |
| `uname -m` | Architecture (x86_64, arm64) |
| `uname -s` | Kernel name |
| `uname -n` | Network hostname |
| `hostname` | System hostname |
| `hostnamectl` | Full system info (systemd) |
| `cat /etc/os-release` | OS distribution info |
| `cat /etc/*-release` | OS release info |
| `lsb_release -a` | LSB distribution info (if installed) |
| `cat /proc/cpuinfo` | CPU information |
| `cat /proc/meminfo` | Memory information |
| `cat /proc/version` | Kernel version info |
| `cat /proc/uptime` | System uptime |
| `cat /proc/loadavg` | System load average |
| `cat /proc/mounts` | Mounted filesystems |
| `cat /proc/partitions` | Partition information |
| `cat /proc/interrupts` | Interrupt information |
| `cat /proc/swaps` | Swap information |
| `lscpu` | CPU architecture info |
| `lsblk` | Block devices |
| `lsblk -f` | Filesystem info |
| `lspci` | PCI devices |
| `lspci -v` | Verbose PCI info |
| `lspci -k` | Kernel drivers |
| `lsusb` | USB devices |
| `lsusb -v` | Verbose USB info |
| `lshw` | Hardware information |
| `lshw -short` | Summary hardware info |
| `dmidecode` | Hardware info from BIOS |
| `dmidecode -t system` | System information |
| `dmidecode -t memory` | Memory information |
| `dmidecode -t processor` | Processor information |
| `inxi -F` | Full system info |
| `inxi -Fxz` | Full system info (hide sensitive) |
| `inxi -c` | Color output |
| `neofetch` | System info with ASCII art |
| `screenfetch` | System info with ASCII art |
| `hardinfo` | GUI system info |
| `hwinfo --short` | Hardware information summary |

# ─── PROCESS MANAGEMENT ──────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `ps aux` | All running processes |
| `ps -ef` | Full process list |
| `ps -eo pid,ppid,cmd,%mem,%cpu` | Custom process output |
| `ps -eo pid,ppid,cmd,%mem,%cpu --sort=-%cpu` | Sort by CPU usage |
| `ps -eo pid,ppid,cmd,%mem,%cpu --sort=-%mem` | Sort by memory usage |
| `ps -ef \| grep process` | Find process |
| `ps -C process_name -o pid,cmd` | Process by name |
| `ps -u username` | Processes by user |
| `ps -p PID` | Specific process |
| `ps -axjf` | Process tree |
| `pstree` | Process tree |
| `pstree -p` | Process tree with PIDs |
| `pstree -u` | Process tree with users |
| `top` | Interactive process viewer |
| `htop` | Enhanced process viewer |
| `btop` | Modern process viewer |
| `atop` | Advanced system monitor |
| `glances` | System monitoring tool |
| `nmon` | System performance monitor |
| `kill PID` | Terminate process by ID |
| `kill -9 PID` | Force kill process |
| `kill -15 PID` | Graceful termination |
| `kill -1 PID` | SIGHUP (reload config) |
| `kill -2 PID` | SIGINT (interrupt) |
| `kill -3 PID` | SIGQUIT (core dump) |
| `pkill process_name` | Kill process by name |
| `pkill -9 process_name` | Force kill by name |
| `pkill -f "pattern"` | Kill by full command |
| `pkill -u username process` | Kill by user |
| `killall process_name` | Kill all processes by name |
| `killall -9 process_name` | Force kill all |
| `pgrep process_name` | Get PID by name |
| `pgrep -f "pattern"` | Get PID by full command |
| `pgrep -u username` | Get PIDs by user |
| `pidof process_name` | Get PID by name |
| `nohup command &` | Run command in background |
| `command &` | Run in background |
| `jobs` | List background jobs |
| `jobs -l` | List with PIDs |
| `fg` | Bring job to foreground |
| `fg %1` | Bring specific job |
| `bg` | Resume job in background |
| `bg %1` | Resume specific job |
| `disown` | Remove job from shell's job table |
| `disown %1` | Remove specific job |
| `disown -h %1` | Keep job after shell exit |
| `nice -n 10 command` | Run with low priority |
| `nice -n -20 command` | Run with high priority |
| `renice -n 10 -p PID` | Change priority of running process |
| `renice -n 10 -u user` | Change priority by user |
| `taskset -c 0-3 command` | Pin process to specific CPU cores |
| `taskset -p 0x01 PID` | Pin existing process |
| `time command` | Measure execution time |
| `/usr/bin/time -v command` | Detailed timing |
| `watch -n 1 command` | Execute command every second |
| `watch -d command` | Highlight differences |
| `watch -n 5 "ps aux \| grep process"` | Monitor process |
| `strace -p PID` | Trace system calls |
| `strace -o output.txt command` | Save trace to file |
| `strace -e open command` | Trace only open calls |
| `strace -f command` | Trace child processes |
| `ltrace -p PID` | Trace library calls |
| `lsof` | List open files |
| `lsof -i :80` | Processes using port 80 |
| `lsof -u username` | Files opened by user |
| `lsof -p PID` | Files opened by process |
| `lsof +D /path` | Files in directory |
| `fuser -v /path` | Processes using file |
| `fuser -k /path` | Kill processes using file |
| `fuser -n tcp 80` | Process using port |
| `systemctl` | Systemd service management |
| `systemctl status service` | Service status |
| `systemctl start service` | Start service |
| `systemctl stop service` | Stop service |
| `systemctl restart service` | Restart service |
| `systemctl reload service` | Reload service config |
| `systemctl enable service` | Enable service at boot |
| `systemctl disable service` | Disable service |
| `systemctl mask service` | Prevent service from starting |
| `systemctl unmask service` | Unmask service |
| `systemctl list-units` | List active units |
| `systemctl list-units --all` | List all units |
| `systemctl list-unit-files` | List unit files |
| `systemctl list-dependencies service` | Dependencies |
| `systemctl is-active service` | Check if active |
| `systemctl is-enabled service` | Check if enabled |
| `service service start` | SysV init start |
| `service service stop` | SysV init stop |
| `service service status` | SysV init status |
| `service --status-all` | All services status |
| `initctl list` | Upstart services |
| `initctl start service` | Start Upstart service |
| `initctl stop service` | Stop Upstart service |

# ─── NETWORK COMMANDS ────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `ifconfig` | Network interfaces (legacy) |
| `ip addr` | IP addresses (modern) |
| `ip link` | Network interfaces |
| `ip route` | Routing table |
| `ip neigh` | ARP table |
| `ip -br addr` | Brief IP addresses |
| `ip -br link` | Brief link status |
| `ip monitor` | Monitor network changes |
| `ping -c 4 google.com` | Ping with 4 packets |
| `ping -i 0.5 google.com` | Ping with 0.5s interval |
| `ping -s 1024 google.com` | Ping with packet size |
| `ping -W 2 google.com` | Set timeout |
| `ping -f google.com` | Flood ping (requires root) |
| `traceroute google.com` | Trace route to host |
| `traceroute -n google.com` | Without DNS resolution |
| `traceroute -m 30 google.com` | Set max hops |
| `tracepath google.com` | Trace route (no root needed) |
| `mtr google.com` | My TraceRoute (combines ping/traceroute) |
| `mtr -r google.com` | Report mode |
| `mtr -c 10 google.com` | 10 iterations |
| `netstat -tulpn` | Listening ports with processes |
| `netstat -a` | All connections |
| `netstat -an` | All with numeric addresses |
| `netstat -r` | Routing table |
| `netstat -i` | Interface statistics |
| `netstat -s` | Protocol statistics |
| `ss -tulpn` | Modern socket statistics |
| `ss -tulpn \| grep LISTEN` | Only listening ports |
| `ss -tup` | Show process using sockets |
| `ss -t -a` | All TCP sockets |
| `ss -u -a` | All UDP sockets |
| `ss -x` | Unix domain sockets |
| `ss -m` | Socket memory usage |
| `curl ifconfig.me` | Public IP address |
| `curl icanhazip.com` | Public IP (alternative) |
| `curl ipinfo.io` | Public IP with location |
| `curl -I example.com` | Get HTTP headers |
| `curl -L example.com` | Follow redirects |
| `curl -o file url` | Download file |
| `curl -O url` | Save with original name |
| `curl -v url` | Verbose output |
| `curl -k https://self-signed.com` | Ignore SSL errors |
| `curl -H "Header: value" url` | Custom headers |
| `curl -d "data" url` | POST request |
| `curl -X POST -d "data" url` | Explicit POST |
| `curl -F "file=@file.txt" url` | File upload |
| `curl -u user:pass url` | Basic authentication |
| `curl --limit-rate 100K url` | Rate limit download |
| `curl --max-time 30 url` | Maximum time |
| `wget -O file url` | Download file |
| `wget -c url` | Resume download |
| `wget -r -l 2 url` | Recursive download (2 levels) |
| `wget -np url` | No parent |
| `wget -nd url` | No directories |
| `wget -q url` | Quiet mode |
| `wget --limit-rate=100k url` | Rate limit |
| `wget -T 30 url` | Timeout |
| `wget --user-agent="Mozilla/5.0" url` | Custom user agent |
| `nc -zv host port` | Netcat port scanning |
| `nc -l -p 1234` | Listen on port |
| `nc host 1234` | Connect to host |
| `nc -u host 1234` | UDP connection |
| `nmap host` | Port scanning |
| `nmap -sV host` | Service version scanning |
| `nmap -p- host` | Scan all ports |
| `nmap -p 80,443,8080 host` | Specific ports |
| `nmap -sS host` | SYN scan |
| `nmap -sU host` | UDP scan |
| `nmap -O host` | OS detection |
| `nmap -A host` | Aggressive scan |
| `nmap -sn 192.168.1.0/24` | Ping scan |
| `nmap -sL 192.168.1.0/24` | DNS scan |
| `tcpdump -i eth0` | Capture packets |
| `tcpdump -i eth0 port 80` | Capture HTTP traffic |
| `tcpdump -i eth0 -w capture.pcap` | Save capture to file |
| `tcpdump -r capture.pcap` | Read capture file |
| `tcpdump -n -i eth0` | No DNS resolution |
| `tcpdump -v -i eth0` | Verbose output |
| `tcpdump 'tcp[tcpflags] & (tcp-syn) != 0'` | Capture SYN packets |
| `tcpdump 'udp port 53'` | Capture DNS traffic |
| `tcpdump 'ip src 192.168.1.100'` | Filter by source IP |
| `tcpdump 'ip dst 192.168.1.100'` | Filter by dest IP |
| `tcpdump -A -i eth0` | ASCII output |
| `tcpdump -X -i eth0` | Hex output |
| `arp -a` | ARP table |
| `arp -d IP` | Delete ARP entry |
| `arp -s IP MAC` | Add static ARP |
| `nslookup domain.com` | DNS lookup |
| `nslookup -type=MX domain.com` | MX record |
| `nslookup -type=TXT domain.com` | TXT record |
| `nslookup -type=NS domain.com` | NS record |
| `nslookup -type=CNAME domain.com` | CNAME record |
| `dig domain.com` | DNS query |
| `dig domain.com MX` | MX record |
| `dig domain.com TXT` | TXT record |
| `dig domain.com ANY` | Any record |
| `dig +trace domain.com` | Trace DNS resolution |
| `dig +short domain.com` | Short output |
| `dig -x 8.8.8.8` | Reverse DNS |
| `whois domain.com` | Domain information |
| `whois IP` | IP information |
| `host domain.com` | DNS lookup (simple) |
| `host -t MX domain.com` | MX record |
| `host -t NS domain.com` | NS record |
| `host -a domain.com` | All records |
| `host IP` | Reverse DNS |

# ─── USER MANAGEMENT ─────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `whoami` | Current username |
| `id` | User and group IDs |
| `id username` | User info |
| `users` | List logged-in users |
| `who` | Who is logged in |
| `w` | Who is logged in and what they're doing |
| `last` | Last login records |
| `last -n 10` | Last 10 logins |
| `lastb` | Bad login attempts |
| `lastlog` | Last login for all users |
| `lastlog -u username` | Last login for user |
| `logname` | Login name |
| `groups` | Current user's groups |
| `groups username` | Show user's groups |
| `sudo useradd username` | Create new user |
| `sudo adduser username` | Create new user (Debian) |
| `sudo useradd -m username` | Create with home directory |
| `sudo useradd -c "Comment" username` | With comment |
| `sudo useradd -s /bin/bash username` | Set shell |
| `sudo useradd -g group username` | Set primary group |
| `sudo useradd -G group1,group2 username` | Additional groups |
| `sudo useradd -d /home/username username` | Custom home |
| `sudo useradd -e 2024-12-31 username` | Expiration date |
| `sudo passwd username` | Change user password |
| `sudo passwd -l username` | Lock user |
| `sudo passwd -u username` | Unlock user |
| `sudo passwd -d username` | Remove password |
| `sudo passwd -e username` | Force password change |
| `sudo usermod -aG group user` | Add user to group |
| `sudo usermod -g group user` | Change primary group |
| `sudo usermod -G group1,group2 user` | Set additional groups |
| `sudo usermod -l newname oldname` | Rename user |
| `sudo usermod -d /home/new home user` | Change home directory |
| `sudo usermod -s /bin/bash user` | Change shell |
| `sudo usermod -L user` | Lock user |
| `sudo usermod -U user` | Unlock user |
| `sudo deluser username` | Delete user (Debian) |
| `sudo userdel username` | Delete user (Red Hat) |
| `sudo userdel -r username` | Delete user with home directory |
| `sudo groupadd groupname` | Create group |
| `sudo groupdel groupname` | Delete group |
| `sudo groupmod -n newname oldname` | Rename group |
| `su - username` | Switch user |
| `su -` | Switch to root |
| `sudo -i` | Switch to root (full environment) |
| `sudo -s` | Switch to root (current environment) |
| `sudo -u username command` | Run command as another user |
| `sudo -l` | List sudo privileges |
| `sudo -k` | Invalidate sudo cache |
| `sudo !!` | Run previous command with sudo |
| `visudo` | Edit sudoers file |
| `chage -l username` | Password aging info |
| `chage -M 30 username` | Set max days |
| `chage -m 7 username` | Set min days |
| `chage -W 7 username` | Set warning days |
| `chage -E 2024-12-31 username` | Set expiration |

# ─── DISK & STORAGE ──────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `df -h` | Disk space usage |
| `df -i` | Inode usage |
| `df -h --total` | Total disk usage |
| `df -T` | Filesystem type |
| `df -x tmpfs` | Exclude tmpfs |
| `du -sh *` | Size of all items in current dir |
| `du -sh * \| sort -h` | Size of directories sorted |
| `du -h --max-depth=1` | Size with depth limit |
| `du -a` | All files |
| `du -c` | Total at end |
| `du -b` | Bytes |
| `du --exclude='*.tmp'` | Exclude pattern |
| `lsblk` | Block devices |
| `lsblk -f` | Filesystem info |
| `lsblk -m` | Mount points |
| `blkid` | Block device UUIDs |
| `mount` | Mounted filesystems |
| `mount /dev/sdb1 /mnt` | Mount device |
| `mount -o rw,noatime /dev/sdb1 /mnt` | Mount with options |
| `mount -t ntfs /dev/sdb1 /mnt` | Mount NTFS |
| `umount /mnt` | Unmount filesystem |
| `umount -l /mnt` | Lazy unmount |
| `umount -f /mnt` | Force unmount |
| `fdisk -l` | Partition table |
| `fdisk /dev/sda` | Interactive partition tool |
| `parted -l` | Partition info |
| `parted /dev/sda` | Interactive partition tool |
| `parted -s /dev/sda mklabel gpt` | Create GPT label |
| `parted -s /dev/sda mkpart primary ext4 0% 100%` | Create partition |
| `parted -s /dev/sda rm 1` | Remove partition |
| `gdisk /dev/sda` | GPT partition tool |
| `sfdisk -d /dev/sda > partitions.txt` | Backup partition table |
| `sfdisk /dev/sda < partitions.txt` | Restore partition table |
| `dd if=/dev/zero of=file bs=1M count=100` | Create 100MB file |
| `dd if=/dev/sda of=backup.img bs=4M` | Create disk image |
| `dd if=backup.img of=/dev/sda bs=4M` | Restore disk image |
| `dd if=/dev/sda of=/dev/sdb bs=4M` | Clone disk |
| `dd if=/dev/zero of=/dev/sda bs=1M count=1` | Destroy partition table |
| `dd if=/dev/urandom of=/dev/sda bs=1M` | Secure wipe disk |
| `dd status=progress if=/dev/sda of=backup.img` | Show progress |
| `mkfs.ext4 /dev/sdb1` | Format partition as ext4 |
| `mkfs.ntfs /dev/sdb1` | Format partition as NTFS |
| `mkfs.fat -F32 /dev/sdb1` | Format partition as FAT32 |
| `mkfs.xfs /dev/sdb1` | Format as XFS |
| `mkfs.btrfs /dev/sdb1` | Format as BTRFS |
| `mkfs -t ext4 /dev/sdb1` | Format with type |
| `mkswap /dev/sdb1` | Create swap |
| `swapon /dev/sdb1` | Enable swap |
| `swapoff /dev/sdb1` | Disable swap |
| `swapon -s` | Show swap usage |
| `smartctl -a /dev/sda` | SMART info |
| `smartctl -H /dev/sda` | Health status |
| `smartctl -t short /dev/sda` | Short test |
| `smartctl -t long /dev/sda` | Long test |
| `smartctl -l selftest /dev/sda` | Test results |
| `badblocks -sv /dev/sda` | Check for bad blocks |
| `badblocks -sv -o badblocks.txt /dev/sda` | Save bad blocks |
| `fsck -f /dev/sda1` | Filesystem check |
| `fsck -y /dev/sda1` | Auto-repair |
| `fsck -n /dev/sda1` | Dry run |
| `fsck -C /dev/sda1` | Show progress |
| `e2fsck -f /dev/sda1` | ext filesystem check |
| `tune2fs -l /dev/sda1` | ext filesystem info |
| `tune2fs -c 30 /dev/sda1` | Set mount count |
| `tune2fs -i 30d /dev/sda1` | Set check interval |
| `tune2fs -m 5 /dev/sda1` | Set reserved blocks |
| `xfs_repair /dev/sda1` | XFS repair |
| `xfs_info /dev/sda1` | XFS info |
| `btrfs check /dev/sda1` | BTRFS check |
| `btrfs filesystem show` | BTRFS info |
| `sync` | Flush filesystem buffers |
| `resize2fs /dev/sda1` | Resize ext filesystem |
| `xfs_growfs /mnt` | Grow XFS filesystem |

# ─── DATE & TIME ──────────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `date` | Current date and time |
| `date +%Y-%m-%d` | Format: 2024-01-01 |
| `date +%H:%M:%S` | Format: 14:30:00 |
| `date +%s` | Unix timestamp |
| `date +%A` | Full weekday name |
| `date +%B` | Full month name |
| `date +%j` | Day of year |
| `date +%W` | Week number |
| `date -d "@timestamp"` | Convert timestamp to date |
| `date -d "tomorrow"` | Tomorrow's date |
| `date -d "yesterday"` | Yesterday's date |
| `date -d "1 day ago"` | One day ago |
| `date -d "1 week ago"` | One week ago |
| `date -d "1 month ago"` | One month ago |
| `date -d "next Monday"` | Next Monday |
| `date -d "last Friday"` | Last Friday |
| `date -d "2024-01-01 + 2 days"` | Date calculation |
| `cal` | Calendar for current month |
| `cal -y` | Calendar for year |
| `cal 2024` | Calendar for year |
| `cal -3` | Previous, current, next month |
| `timedatectl` | System time settings |
| `timedatectl status` | Current status |
| `timedatectl list-timezones` | List timezones |
| `timedatectl set-timezone Asia/Ho_Chi_Minh` | Set timezone |
| `timedatectl set-time "2024-01-01 12:00:00"` | Set time |
| `timedatectl set-ntp true` | Enable NTP |
| `ntpdate pool.ntp.org` | Sync time with NTP |
| `ntpdate -u pool.ntp.org` | Sync with unprivileged port |
| `chronyc tracking` | Chrony NTP status |
| `chronyc sources` | Chrony NTP sources |
| `sleep 10` | Pause for 10 seconds |
| `sleep 1m` | Pause for 1 minute |
| `sleep 1h` | Pause for 1 hour |
| `timeout 10 command` | Run command with timeout |
| `watch -n 1 date` | Watch date update |

# ─── TEXT PROCESSING ─────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `echo "text" > file` | Write text to file |
| `echo "text" >> file` | Append text to file |
| `cat file1 file2 > merged` | Merge files |
| `sort file` | Sort file content |
| `sort -n file` | Sort numerically |
| `sort -r file` | Sort reverse |
| `sort -k2 file` | Sort by column 2 |
| `sort -t',' -k2 file.csv` | Sort CSV by column 2 |
| `sort -u file` | Sort and remove duplicates |
| `uniq file` | Remove duplicate lines |
| `uniq -c file` | Count duplicates |
| `uniq -d file` | Show duplicates only |
| `uniq -u file` | Show unique only |
| `wc -l file` | Count lines |
| `wc -w file` | Count words |
| `wc -c file` | Count characters |
| `wc -m file` | Count characters (multibyte) |
| `cut -d',' -f1 file.csv` | Cut first column (CSV) |
| `cut -c1-10 file` | Cut first 10 characters |
| `cut -f1-3 file` | Cut fields (tab separated) |
| `cut --complement -f2 file` | Exclude field 2 |
| `awk '{print $1}' file` | Print first column |
| `awk '{print $NF}' file` | Print last column |
| `awk '/pattern/ {print}' file` | Print lines with pattern |
| `awk '{print NR, $0}' file` | Print line numbers |
| `awk '{sum+=$1} END {print sum}' file` | Sum column 1 |
| `awk '{sum+=$1; count++} END {print sum/count}' file` | Average of column 1 |
| `awk '{print $1, $3}' file` | Print columns 1 and 3 |
| `awk -F, '{print $1}' file.csv` | CSV with comma delimiter |
| `awk 'NF > 5' file` | Print lines with >5 fields |
| `awk '!seen[$0]++' file` | Remove duplicates |
| `sed 's/old/new/g' file` | Replace text |
| `sed -i 's/old/new/g' file` | Replace in-place |
| `sed '/pattern/d' file` | Delete lines with pattern |
| `sed -n '1,10p' file` | Print lines 1-10 |
| `sed -n '/start/,/end/p' file` | Print range |
| `sed -i.bak 's/old/new/g' file` | In-place with backup |
| `sed 's/\bword\b/replacement/g' file` | Replace whole word |
| `sed 's/^/prefix/' file` | Add prefix |
| `sed 's/$/suffix/' file` | Add suffix |
| `sed 's/pattern/&/g' file` | Replace with match |
| `sed 's/\(pattern\)/\1/g' file` | Use backreferences |
| `sed '/pattern/ i text' file` | Insert before pattern |
| `sed '/pattern/ a text' file` | Append after pattern |
| `sed '/pattern/ c text' file` | Replace line with pattern |
| `sed 's/^[ \t]*//' file` | Remove leading whitespace |
| `sed 's/[ \t]*$//' file` | Remove trailing whitespace |
| `sed 's/^[ \t]*//;s/[ \t]*$//' file` | Trim whitespace |
| `diff file1 file2` | Compare files |
| `diff -u file1 file2` | Unified diff |
| `diff -y file1 file2` | Side by side |
| `diff -w file1 file2` | Ignore whitespace |
| `diff -r dir1 dir2` | Compare directories |
| `comm file1 file2` | Common lines between files |
| `comm -12 file1 file2` | Lines in both |
| `comm -13 file1 file2` | Lines only in file2 |
| `comm -23 file1 file2` | Lines only in file1 |
| `join file1 file2` | Join files on common field |
| `join -t',' file1.csv file2.csv` | Join CSV files |
| `split -l 1000 file` | Split file into 1000-line chunks |
| `split -b 100M file` | Split by size |
| `split -d file` | Split with numeric suffixes |
| `tr 'a-z' 'A-Z' < file` | Convert to uppercase |
| `tr -d '\n' < file` | Remove newlines |
| `tr -s ' ' < file` | Squeeze spaces |
| `tr -d '[:punct:]' < file` | Remove punctuation |
| `paste file1 file2` | Merge files line by line |
| `paste -d',' file1 file2` | Merge with comma delimiter |
| `paste -s file` | Merge all lines into one |
| `rev file` | Reverse lines |
| `tac file` | Reverse file lines |
| `shuf file` | Randomize lines |
| `shuf -n 10 file` | Random 10 lines |
| `yes "text"` | Repeat output |
| `yes \| head -n 100` | Repeat 100 times |
| `factor number` | Factor number |
| `seq 1 10` | Generate number sequence |
| `printf "format" args` | Formatted output |

# ─── COMPRESSION & ARCHIVING ─────────────────────────────────────

| Command | Description |
|---------|-------------|
| `tar -czf archive.tar.gz directory/` | Create tar.gz |
| `tar -xzf archive.tar.gz` | Extract tar.gz |
| `tar -cjf archive.tar.bz2 directory/` | Create tar.bz2 |
| `tar -xjf archive.tar.bz2` | Extract tar.bz2 |
| `tar -cJf archive.tar.xz directory/` | Create tar.xz |
| `tar -xJf archive.tar.xz` | Extract tar.xz |
| `tar -cvf archive.tar directory/` | Create tar |
| `tar -xvf archive.tar` | Extract tar |
| `tar -tf archive.tar.gz` | List contents |
| `tar -tvf archive.tar.gz` | Verbose list |
| `tar -czf - directory/ \| ssh user@host "cat > archive.tar.gz"` | Remote archive |
| `tar -xzf archive.tar.gz -C /target` | Extract to target |
| `tar --exclude='*.tmp' -czf archive.tar.gz dir/` | Exclude files |
| `tar -czf archive.tar.gz dir/ --exclude-from=exclude.txt` | Exclude list |
| `zip -r archive.zip directory/` | Create zip |
| `unzip archive.zip` | Extract zip |
| `unzip -l archive.zip` | List contents |
| `unzip -d /target archive.zip` | Extract to target |
| `zip -e archive.zip file.txt` | Encrypt zip |
| `zip -r -9 archive.zip dir/` | Maximum compression |
| `unzip -o archive.zip` | Overwrite files |
| `gzip file` | Compress to .gz |
| `gunzip file.gz` | Decompress .gz |
| `gzip -9 file` | Maximum compression |
| `gzip -d file.gz` | Decompress |
| `bzip2 file` | Compress to .bz2 |
| `bunzip2 file.bz2` | Decompress .bz2 |
| `bzip2 -9 file` | Maximum compression |
| `xz file` | Compress to .xz |
| `unxz file.xz` | Decompress .xz |
| `xz -9 file` | Maximum compression |
| `xz -d file.xz` | Decompress |
| `zcat file.gz` | View compressed file |
| `zless file.gz` | View compressed file page by page |
| `zgrep pattern file.gz` | Search in compressed file |
| `7z a archive.7z directory/` | Create 7z archive |
| `7z x archive.7z` | Extract 7z |
| `7z l archive.7z` | List contents |
| `7z a -mx=9 archive.7z dir/` | Maximum compression |
| `7z a -p password archive.7z dir/` | Password protected |
| `7z a -tzip archive.zip dir/` | Create zip with 7z |
| `rar a archive.rar dir/` | Create rar |
| `unrar x archive.rar` | Extract rar |
| `unrar l archive.rar` | List contents |
| `file archive.tar.gz` | Determine archive type |

# ─── PACKAGE MANAGEMENT ──────────────────────────────────────────

## APT (Debian/Ubuntu)

| Command | Description |
|---------|-------------|
| `apt update` | Update package list |
| `apt upgrade` | Upgrade all packages |
| `apt full-upgrade` | Full upgrade with dependencies |
| `apt install package` | Install package |
| `apt install package1 package2` | Install multiple |
| `apt remove package` | Remove package |
| `apt purge package` | Remove with config |
| `apt autoremove` | Remove unused packages |
| `apt autoclean` | Clean package cache |
| `apt clean` | Clean entire cache |
| `apt search keyword` | Search packages |
| `apt show package` | Show package info |
| `apt list --installed` | List installed packages |
| `apt list --upgradable` | List upgradable packages |
| `apt depends package` | Show dependencies |
| `apt rdepends package` | Show reverse dependencies |
| `apt cache policy package` | Show package policy |
| `apt source package` | Download source |
| `apt build-dep package` | Install build dependencies |
| `dpkg -i package.deb` | Install .deb file |
| `dpkg -r package` | Remove package |
| `dpkg -l` | List packages |
| `dpkg -l \| grep package` | Find package |
| `dpkg -s package` | Package status |
| `dpkg -S file` | Find package owning file |
| `dpkg -L package` | List files in package |
| `dpkg --configure -a` | Configure all packages |
| `dpkg-reconfigure package` | Reconfigure package |
| `apt-get update` | Legacy update |
| `apt-get upgrade` | Legacy upgrade |
| `apt-get install package` | Legacy install |
| `apt-get remove package` | Legacy remove |
| `apt-get autoremove` | Legacy autoremove |
| `aptitude` | Interactive package manager |

## YUM/DNF (RHEL/Fedora)

| Command | Description |
|---------|-------------|
| `yum install package` | Install package (RHEL) |
| `yum install package1 package2` | Install multiple |
| `yum remove package` | Remove package |
| `yum update` | Update all packages |
| `yum update package` | Update specific package |
| `yum list installed` | List installed packages |
| `yum list available` | List available |
| `yum search keyword` | Search packages |
| `yum info package` | Package info |
| `yum groupinstall "Group Name"` | Install group |
| `yum groupremove "Group Name"` | Remove group |
| `yum groupinfo "Group Name"` | Group info |
| `yum repolist` | List repositories |
| `yum clean all` | Clean cache |
| `yum history` | Transaction history |
| `yum history undo ID` | Undo transaction |
| `yum provides /path/file` | Find file owner |
| `dnf install package` | Install (Fedora) |
| `dnf remove package` | Remove (Fedora) |
| `dnf update` | Update all (Fedora) |
| `dnf list installed` | List installed (Fedora) |
| `dnf search keyword` | Search (Fedora) |
| `dnf info package` | Package info (Fedora) |
| `dnf groupinstall "Group Name"` | Install group (Fedora) |
| `dnf repolist` | Repositories (Fedora) |
| `dnf clean all` | Clean cache (Fedora) |
| `rpm -i package.rpm` | Install .rpm file |
| `rpm -e package` | Remove package |
| `rpm -qa` | List all RPMs |
| `rpm -qa \| grep package` | Find RPM |
| `rpm -qi package` | RPM info |
| `rpm -ql package` | List files in RPM |
| `rpm -qf /path/file` | Find RPM owning file |

## PACMAN (Arch)

| Command | Description |
|---------|-------------|
| `pacman -S package` | Install package |
| `pacman -S package1 package2` | Install multiple |
| `pacman -R package` | Remove package |
| `pacman -Rns package` | Remove with dependencies |
| `pacman -Syu` | Update system |
| `pacman -Syyu` | Force update |
| `pacman -Q` | List installed packages |
| `pacman -Qt` | List installed packages (not needed by others) |
| `pacman -Ss keyword` | Search packages |
| `pacman -Qi package` | Show package info |
| `pacman -Ql package` | List files in package |
| `pacman -Qo /path/file` | Find package owning file |
| `pacman -Sc` | Remove unused packages |
| `pacman -Scc` | Remove all cache |
| `pacman -Sg` | List groups |
| `pacman -Sg group` | List packages in group |
| `pacman -U package.pkg.tar.xz` | Install local package |
| `pamac` | GUI package manager |
| `yay -S package` | AUR helper install |
| `yay -R package` | AUR helper remove |
| `yay -Syu` | AUR helper update |
| `paru -S package` | Alternative AUR helper |

## Snap & Flatpak

| Command | Description |
|---------|-------------|
| `snap install package` | Install snap package |
| `snap remove package` | Remove snap package |
| `snap list` | List installed snaps |
| `snap find keyword` | Search snaps |
| `snap info package` | Snap info |
| `snap refresh` | Update snaps |
| `snap changes` | Snap changes |
| `snap connections` | Snap connections |
| `snap revert package` | Revert snap |
| `snap disable package` | Disable snap |
| `snap enable package` | Enable snap |
| `flatpak install flathub package` | Install flatpak |
| `flatpak uninstall package` | Remove flatpak |
| `flatpak list` | List installed flatpaks |
| `flatpak search keyword` | Search flatpaks |
| `flatpak info package` | Flatpak info |
| `flatpak update` | Update flatpaks |
| `flatpak run package` | Run flatpak |
| `flatpak override package` | Override permissions |

# ─── ENVIRONMENT VARIABLES ───────────────────────────────────────

| Command | Description |
|---------|-------------|
| `env` | Show all environment variables |
| `printenv` | Show all environment variables |
| `printenv VAR` | Show specific variable |
| `echo $PATH` | Show PATH variable |
| `echo $HOME` | Home directory |
| `echo $USER` | Current user |
| `echo $SHELL` | Current shell |
| `echo $PWD` | Current working directory |
| `echo $OLDPWD` | Previous directory |
| `echo $TERM` | Terminal type |
| `echo $LANG` | Language setting |
| `echo $EDITOR` | Default editor |
| `echo $DISPLAY` | X display |
| `echo $HOSTNAME` | Hostname |
| `echo $RANDOM` | Random number |
| `export VAR=value` | Set environment variable |
| `export VAR=value; command` | Set variable for command only |
| `unset VAR` | Unset environment variable |
| `set` | Show all variables (shell) |
| `shopt` | Show shell options |
| `alias` | List aliases |
| `alias ll='ls -la'` | Create alias |
| `unalias ll` | Remove alias |
| `source file` | Source script file |
| `. file` | Source script file (alternative) |

# ─── SYSTEM MONITORING ───────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `top` | Real-time process viewer |
| `htop` | Enhanced top |
| `btop` | Modern process viewer |
| `atop` | Advanced system monitor |
| `glances` | System monitoring tool |
| `nmon` | System performance monitor |
| `iotop` | I/O monitoring |
| `iotop -o` | Only processes with I/O |
| `vmstat 1` | Virtual memory statistics |
| `vmstat 1 5` | VM stats every second, 5 times |
| `vmstat -s` | Summary stats |
| `iostat -x 1` | I/O statistics |
| `iostat -x 1 5` | I/O stats every second, 5 times |
| `mpstat 1` | CPU stats per core |
| `mpstat -P ALL 1` | All CPU cores |
| `sar -u 1 5` | CPU usage |
| `sar -r 1 5` | Memory usage |
| `sar -b 1 5` | I/O statistics |
| `sar -n DEV 1 5` | Network statistics |
| `sar -q` | System load |
| `sar -B` | Paging statistics |
| `watch -n 1 command` | Execute command every second |
| `watch -d command` | Highlight differences |
| `watch -t command` | Hide header |
| `uptime` | System uptime |
| `dmesg` | Kernel ring buffer |
| `dmesg -T` | With timestamps |
| `dmesg \| tail -20` | Recent kernel messages |
| `dmesg -w` | Watch kernel messages |
| `journalctl -f` | Follow system logs |
| `journalctl -u service` | Logs for specific service |
| `journalctl -u service -f` | Follow service logs |
| `journalctl --since "1 hour ago"` | Logs from last hour |
| `journalctl --since "today"` | Today's logs |
| `journalctl --until "yesterday"` | Until yesterday |
| `journalctl -p err` | Error level logs |
| `journalctl -p info` | Info level logs |
| `journalctl -k` | Kernel logs |
| `journalctl -b` | Current boot logs |
| `journalctl -b -1` | Previous boot logs |
| `journalctl --list-boots` | List boots |
| `journalctl --verify` | Verify journal |
| `systemd-analyze` | Boot performance |
| `systemd-analyze blame` | Boot time per service |
| `systemd-analyze critical-chain` | Critical chain |
| `systemd-analyze plot > boot.svg` | Create SVG plot |

# ─── REMOTE CONNECTIONS ──────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `ssh user@host` | SSH connection |
| `ssh -p 2222 user@host` | SSH with custom port |
| `ssh -i key.pem user@host` | SSH with key file |
| `ssh -v user@host` | Verbose SSH |
| `ssh -vvv user@host` | Very verbose |
| `ssh -J user@jump-host user@host` | SSH via jump host |
| `ssh -L 8080:localhost:80 user@host` | Port forwarding (local) |
| `ssh -R 8080:localhost:80 user@host` | Port forwarding (remote) |
| `ssh -D 1080 user@host` | Dynamic port forwarding |
| `ssh -N -L 8080:localhost:80 user@host` | Forward without command |
| `ssh -f -N -L 8080:localhost:80 user@host` | Background forward |
| `ssh -o "StrictHostKeyChecking=no" host` | Skip host key check |
| `ssh-copy-id user@host` | Copy SSH key to server |
| `ssh-agent` | SSH agent |
| `ssh-add` | Add key to agent |
| `ssh-add -l` | List agent keys |
| `ssh-add -D` | Remove all keys |
| `ssh-keygen -t rsa -b 4096` | Generate SSH key |
| `ssh-keygen -t ed25519` | Generate ED25519 key |
| `ssh-keygen -f ~/.ssh/id_rsa -p` | Change passphrase |
| `scp file user@host:/path` | Copy file to remote |
| `scp user@host:/path/file .` | Copy from remote |
| `scp -P 2222 file user@host:/path` | With custom port |
| `scp -r dir user@host:/path` | Recursive copy |
| `scp -3 host1:/file host2:/file` | Copy between hosts |
| `rsync -avz user@host:/path/ /local/path/` | Sync from remote |
| `rsync -avz /local/path/ user@host:/path/` | Sync to remote |
| `rsync -avz --delete user@host:/path/ /local/path/` | Delete extra files |
| `rsync -avz --exclude='*.tmp' user@host:/path/ /local/path/` | Exclude pattern |
| `rsync -avz --progress user@host:/path/ /local/path/` | Show progress |
| `rsync -e "ssh -p 2222" -avz user@host:/path/ /local/path/` | Custom SSH port |
| `sftp user@host` | Secure FTP |
| `sftp -P 2222 user@host` | SFTP with custom port |
| `telnet host port` | Telnet connection (insecure) |
| `nc -zv host port` | Netcat port scanning |
| `nc -l -p 1234` | Netcat listen |
| `nc host 1234` | Netcat connect |
| `ncat host port` | Ncat (modern netcat) |
| `screen` | Terminal multiplexer |
| `screen -S session` | Named session |
| `screen -r session` | Resume session |
| `screen -ls` | List sessions |
| `tmux` | Terminal multiplexer |
| `tmux new -s session` | Named session |
| `tmux attach -t session` | Attach session |
| `tmux ls` | List sessions |
| `tmux kill-session -t session` | Kill session |

# ─── SYSTEM RECOVERY ─────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `fsck -f /dev/sda1` | Check filesystem |
| `fsck -y /dev/sda1` | Auto-repair filesystem |
| `fsck -n /dev/sda1` | Dry run |
| `fsck -C /dev/sda1` | Show progress |
| `badblocks -sv /dev/sda` | Check for bad blocks |
| `badblocks -sv -o badblocks.txt /dev/sda` | Save bad blocks |
| `dd if=/dev/sda of=/dev/sdb bs=4M` | Clone disk |
| `dd if=/dev/sda of=backup.img bs=4M` | Create disk image |
| `dd if=backup.img of=/dev/sda bs=4M` | Restore disk image |
| `dd if=/dev/zero of=/dev/sda bs=1M count=1` | Destroy partition table |
| `dd if=/dev/urandom of=/dev/sda bs=1M` | Secure wipe disk |
| `testdisk` | Recover partitions |
| `photorec` | Recover files |
| `chroot /mnt/sysroot` | Change root directory |
| `chroot /mnt/sysroot /bin/bash` | Chroot with shell |
| `rescue` | System rescue mode |
| `grub-install /dev/sda` | Install GRUB bootloader |
| `grub-install --root-directory=/mnt /dev/sda` | Install to custom root |
| `update-grub` | Update GRUB configuration |
| `grub-mkconfig -o /boot/grub/grub.cfg` | Generate GRUB config |
| `grub-mkrescue` | Create rescue ISO |
| `grub-reboot` | Reboot into GRUB menu |
| `boot-repair` | Boot repair tool |
| `systemctl rescue` | Enter rescue mode |
| `systemctl emergency` | Enter emergency mode |
| `systemctl reboot` | Reboot system |
| `systemctl poweroff` | Power off |
| `systemctl halt` | Halt |
| `reboot` | Reboot |
| `shutdown -h now` | Power off now |
| `shutdown -r now` | Reboot now |
| `shutdown -h +10` | Power off in 10 minutes |
| `shutdown -c` | Cancel shutdown |
| `init 0` | Power off |
| `init 6` | Reboot |
| `telinit` | Change runlevel |

# ─── LINUX ADVANCED ──────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `strace -p PID` | Trace system calls |
| `strace -o output.txt command` | Save trace to file |
| `strace -e open command` | Trace only open calls |
| `strace -f command` | Trace child processes |
| `strace -c command` | Summary of calls |
| `ltrace -p PID` | Trace library calls |
| `ltrace -c command` | Summary of library calls |
| `lsof` | List open files |
| `lsof -i :80` | Processes using port 80 |
| `lsof -u username` | Files opened by user |
| `lsof -p PID` | Files opened by process |
| `lsof +D /path` | Files in directory |
| `lsof -n` | No DNS resolution |
| `lsof -P` | No port translation |
| `fuser -v /path` | Processes using file |
| `fuser -k /path` | Kill processes using file |
| `fuser -n tcp 80` | Process using port |
| `ldd /bin/ls` | Show shared libraries |
| `objdump -d binary` | Disassemble binary |
| `objdump -h binary` | Section headers |
| `nm binary` | List symbols |
| `readelf -h binary` | ELF header info |
| `readelf -l binary` | Program headers |
| `readelf -S binary` | Section headers |
| `strings binary` | Print readable strings |
| `xxd file` | Hex dump |
| `xxd -r file` | Reverse hex dump |
| `hexdump -C file` | Hex dump with ASCII |
| `od -x file` | Octal dump |
| `od -c file` | Character dump |
| `ulimit -a` | Show limits |
| `ulimit -n 65536` | Increase file descriptor limit |
| `ulimit -u unlimited` | Unlimited processes |
| `ulimit -c unlimited` | Unlimited core dump size |
| `sysctl -a` | Show kernel parameters |
| `sysctl -w net.ipv4.ip_forward=1` | Enable IP forwarding |
| `sysctl -w vm.swappiness=10` | Set swappiness |
| `sysctl -p` | Load settings from sysctl.conf |
| `modprobe module` | Load kernel module |
| `lsmod` | List loaded modules |
| `rmmod module` | Remove kernel module |
| `insmod module.ko` | Insert module (manual) |
| `modinfo module` | Module information |
| `depmod -a` | Generate module dependencies |
| `dmesg -c` | Clear kernel ring buffer |
| `logger "message"` | Add to system log |
| `logrotate` | Log rotation utility |
| `logrotate -f /etc/logrotate.conf` | Force logrotate |
| `logrotate -d /etc/logrotate.conf` | Debug mode |

# ================================================================
# 2. WINDOWS CMD COMMANDS - COMPLETE
# ================================================================

# ─── FILE OPERATIONS ──────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `dir` | List directory contents |
| `dir /w` | Wide listing |
| `dir /p` | Page-by-page |
| `dir /s` | Recursive listing |
| `dir /b` | Simple listing (names only) |
| `dir /a` | Show all files (including hidden) |
| `dir /od` | Sort by date |
| `dir /os` | Sort by size |
| `dir /tc` | Show creation time |
| `dir /tw` | Show last write time |
| `dir /ta` | Show last access time |
| `dir /o-n` | Sort by name descending |
| `dir /o-g` | Sort by type |
| `dir /x` | Show short names |
| `dir *.txt /s` | Find all .txt files |
| `dir /b /s *.txt` | Simple recursive find |
| `mkdir folder` | Create directory |
| `md folder` | Create directory (short) |
| `rmdir folder` | Remove empty directory |
| `rd folder` | Remove empty directory (short) |
| `rmdir /s folder` | Remove directory with contents |
| `rmdir /s /q folder` | Remove without confirmation |
| `del file.txt` | Delete file |
| `erase file.txt` | Delete file (alternative) |
| `del /f file.txt` | Force delete read-only file |
| `del /s *.tmp` | Delete all .tmp files recursively |
| `del /q *.tmp` | Delete without confirmation |
| `del /a:h file.txt` | Delete hidden file |
| `copy file.txt new.txt` | Copy file |
| `copy /y file.txt dest\` | Copy without confirmation |
| `copy /v file.txt dest\` | Verify after copy |
| `xcopy source dest /e` | Copy directories and subdirectories |
| `xcopy /h` | Copy hidden/system files |
| `xcopy /c` | Continue even if errors |
| `xcopy /i` | Assume destination is directory |
| `xcopy /f` | Show full source/dest names |
| `xcopy /l` | List files without copying |
| `xcopy /d:01-01-2024` | Copy files modified after date |
| `xcopy /u` | Update files (copy only newer) |
| `robocopy source dest /e` | Robust copy |
| `robocopy source dest /mir` | Mirror directory |
| `robocopy source dest /mt:8` | Multi-threaded copy |
| `robocopy source dest /r:3 /w:5` | Retry 3 times with 5s wait |
| `robocopy source dest /zb` | Use backup mode |
| `robocopy source dest /ndl` | No directory logging |
| `move file.txt folder\` | Move file |
| `move /y file.txt folder\` | Move without confirmation |
| `rename old.txt new.txt` | Rename file |
| `ren old.txt new.txt` | Rename file (short) |
| `type file.txt` | Display file content |
| `more file.txt` | Page-by-page view |
| `find "text" file.txt` | Search within file |
| `find /c "text" file.txt` | Count matches |
| `find /n "text" file.txt` | Show line numbers |
| `findstr "pattern" *.txt` | Search string in files |
| `findstr /s "pattern" *.*` | Recursive search |
| `findstr /i "pattern" file` | Case-insensitive search |
| `findstr /v "pattern" file` | Exclude pattern |
| `findstr /c:"exact phrase" file` | Search exact phrase |
| `findstr /r "regex" file` | Use regex |
| `findstr /m "pattern" *.txt` | List files containing pattern |
| `edit file.txt` | Edit file (old editor) |

# ─── SYSTEM INFORMATION ──────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `systeminfo` | Full system information |
| `systeminfo \| findstr /C:"OS Name"` | Show OS name only |
| `systeminfo \| findstr /C:"Total Physical Memory"` | Show total memory |
| `systeminfo \| findstr /C:"System Type"` | Show system type |
| `ver` | Windows version |
| `hostname` | Computer name |
| `whoami` | Current user |
| `whoami /all` | Detailed user info |
| `set` | Environment variables |
| `echo %PATH%` | Show PATH variable |
| `echo %USERNAME%` | Current username |
| `echo %COMPUTERNAME%` | Computer name |
| `echo %OS%` | Operating system |
| `echo %PROCESSOR_ARCHITECTURE%` | CPU architecture |
| `echo %NUMBER_OF_PROCESSORS%` | Number of processors |
| `echo %USERPROFILE%` | User profile path |
| `echo %APPDATA%` | AppData path |
| `echo %TEMP%` | Temporary folder path |

# ─── PROCESS MANAGEMENT ──────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `tasklist` | List processes |
| `tasklist /v` | Verbose process list |
| `tasklist /fi "memusage gt 50000"` | Processes using >50MB |
| `tasklist /fi "status eq running"` | Running processes |
| `tasklist /svc` | Processes with services |
| `tasklist /m` | List DLLs loaded |
| `tasklist /s host /u user /p pass` | Remote process list |
| `taskkill /PID 1234` | Kill process by PID |
| `taskkill /IM process.exe` | Kill process by name |
| `taskkill /F /PID 1234` | Force kill |
| `taskkill /F /IM process.exe` | Force kill by name |
| `taskkill /T /PID 1234` | Kill process tree |
| `taskkill /S host /U user /P pass /PID 1234` | Remote kill |
| `start program.exe` | Start program |
| `start /min program.exe` | Start minimized |
| `start /max program.exe` | Start maximized |
| `start /b program.exe` | Start without window |
| `start /wait program.exe` | Start and wait for exit |
| `start "" "C:\Program Files\app.exe"` | Start with spaces in path |
| `start explorer.exe` | Start Explorer |
| `start cmd.exe` | Open new command prompt |
| `start www.google.com` | Open in browser |

# ─── NETWORK COMMANDS ────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `ipconfig` | IP configuration |
| `ipconfig /all` | Detailed IP config |
| `ipconfig /release` | Release DHCP lease |
| `ipconfig /renew` | Renew DHCP lease |
| `ipconfig /flushdns` | Flush DNS cache |
| `ipconfig /displaydns` | Show DNS cache |
| `ipconfig /registerdns` | Register DNS |
| `ping host` | Ping host |
| `ping -t host` | Continuous ping |
| `ping -n 4 host` | Ping 4 times |
| `ping -l 1024 host` | Ping with packet size |
| `ping -w 2000 host` | Set timeout (ms) |
| `ping -4 host` | IPv4 only |
| `ping -6 host` | IPv6 only |
| `tracert host` | Trace route |
| `tracert -d host` | Trace without resolving |
| `tracert -h 30 host` | Max hops |
| `pathping host` | Route with packet loss info |
| `pathping -n host` | Without DNS resolution |
| `nslookup host` | DNS lookup |
| `nslookup -type=MX google.com` | MX record lookup |
| `nslookup -type=TXT google.com` | TXT record lookup |
| `nslookup -type=NS google.com` | NS record lookup |
| `nslookup -type=CNAME google.com` | CNAME record lookup |
| `nslookup -type=ANY google.com` | ANY record lookup |
| `nslookup -querytype=MX google.com` | Alternative query |
| `nslookup -d host` | Debug mode |
| `nslookup -set debug` | Set debug mode |
| `netstat -a` | All connections |
| `netstat -ano` | All connections with PIDs |
| `netstat -b` | Show executable for connections |
| `netstat -r` | Routing table |
| `netstat -e` | Ethernet statistics |
| `netstat -s` | Protocol statistics |
| `netstat -p tcp` | TCP connections only |
| `netstat -p udp` | UDP connections only |
| `net view` | View network computers |
| `net view \\computer` | View shares on computer |
| `net use Z: \\server\share` | Map network drive |
| `net use /delete Z:` | Disconnect network drive |
| `net use * /delete` | Disconnect all network drives |
| `net use Z: \\server\share /persistent:yes` | Persistent mapping |
| `net use Z: \\server\share password /user:username` | With credentials |
| `arp -a` | ARP table |
| `arp -d` | Clear ARP cache |
| `arp -s IP MAC` | Add static ARP |
| `route print` | Routing table |
| `route add 10.0.0.0 mask 255.255.255.0 192.168.1.1` | Add route |
| `route delete 10.0.0.0` | Delete route |
| `route add 0.0.0.0 mask 0.0.0.0 192.168.1.1` | Add default gateway |
| `route -p add 10.0.0.0 mask 255.255.255.0 192.168.1.1` | Persistent route |
| `netsh int ip show config` | IP config details |
| `netsh int ip show interfaces` | Interface list |
| `netsh int ip show addresses` | IP addresses |
| `netsh int ip reset` | Reset IP stack |
| `netsh winsock reset` | Reset Winsock |
| `netsh int ip reset log.txt` | Reset with log |
| `netsh int ip set dns "Ethernet" static 8.8.8.8` | Set DNS |
| `netsh int ip add dns "Ethernet" 8.8.4.4` | Add DNS |
| `netsh int ip set address "Ethernet" static 192.168.1.100 255.255.255.0 192.168.1.1 1` | Set static IP |
| `netsh int ip set address "Ethernet" dhcp` | Set DHCP |
| `netsh wlan show networks` | Show WiFi networks |
| `netsh wlan show profile name="SSID" key=clear` | Show WiFi password |
| `netsh wlan connect name="SSID"` | Connect to WiFi |
| `netsh wlan disconnect` | Disconnect WiFi |
| `netsh wlan show drivers` | WiFi driver info |
| `netsh advfirewall show allprofiles` | Firewall status |
| `netsh advfirewall set allprofiles state off` | Disable firewall |
| `netsh advfirewall set allprofiles state on` | Enable firewall |
| `netsh advfirewall firewall add rule name="Allow 443" dir=in action=allow protocol=TCP localport=443` | Add rule |
| `netsh advfirewall firewall add rule name="Allow 443" dir=in action=allow protocol=TCP localport=443 remoteip=any` | With remote IP |
| `netsh advfirewall firewall add rule name="Allow SSH" dir=in action=allow protocol=TCP localport=22` | Allow SSH |
| `netsh advfirewall firewall delete rule name="Allow 443"` | Delete rule |
| `netsh advfirewall firewall set rule group="Remote Desktop" new enable=Yes` | Enable RDP |
| `netsh advfirewall firewall set rule group="Remote Desktop" new enable=No` | Disable RDP |

# ─── USER MANAGEMENT ─────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `net user` | List local users |
| `net user username` | User details |
| `net user username password /add` | Add user |
| `net user username /delete` | Delete user |
| `net user username /active:yes` | Enable user |
| `net user username /active:no` | Disable user |
| `net user username /expires:never` | User never expires |
| `net user username /expires:01/01/2025` | Set expiration |
| `net user username /comment:"Comment"` | Add comment |
| `net user username /fullname:"Full Name"` | Set full name |
| `net user username /passwordreq:yes` | Require password |
| `net user username /passwordreq:no` | No password required |
| `net localgroup` | List local groups |
| `net localgroup Administrators` | List admin members |
| `net localgroup Administrators username /add` | Add to admin |
| `net localgroup Administrators username /delete` | Remove from admin |
| `net group /domain` | List domain groups |
| `net group "Domain Admins" /domain` | List domain admins |
| `net user username /domain` | Domain user info |
| `net user username * /domain` | Change domain password |
| `net accounts` | Account settings |
| `net accounts /maxpwage:30` | Set max password age |
| `net accounts /minpwage:7` | Set min password age |
| `net accounts /minpwlen:8` | Set min password length |
| `wmic useraccount get name,disabled,status` | List user accounts |
| `wmic useraccount where "name='username'" get name,sid` | Get user SID |
| `wmic useraccount where "name='username'" call Rename "newname"` | Rename user |
| `wmic useraccount where "name='username'" call SetPassword "newpass"` | Set password |
| `wmic group get name` | List groups |
| `wmic group where "name='Administrators'" get name,status` | Group info |

# ─── DISK & STORAGE ──────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `chkdsk` | Check disk |
| `chkdsk /f` | Fix disk errors |
| `chkdsk /r` | Find bad sectors |
| `chkdsk /x` | Force volume dismount |
| `chkdsk /scan` | Online scan |
| `chkdsk /perf` | Use maximum performance |
| `chkdsk /spotfix` | Spot fix errors |
| `diskpart` | Disk partition tool |
| `list disk` | List disks (inside diskpart) |
| `select disk 0` | Select disk |
| `list partition` | List partitions |
| `select partition 1` | Select partition |
| `clean` | Clean disk (WARNING!) |
| `create partition primary` | Create primary partition |
| `create partition extended` | Create extended partition |
| `create partition logical` | Create logical partition |
| `format fs=ntfs quick` | Quick format NTFS |
| `format fs=ntfs` | Full format NTFS |
| `format fs=fat32 quick` | Quick format FAT32 |
| `assign letter=E:` | Assign drive letter |
| `remove letter=E:` | Remove drive letter |
| `active` | Mark partition as active |
| `convert gpt` | Convert to GPT |
| `convert mbr` | Convert to MBR |
| `list volume` | List volumes |
| `select volume 0` | Select volume |
| `extend` | Extend volume |
| `shrink desired=1000` | Shrink volume by 1GB |
| `mountvol` | Mount point management |
| `mountvol E: /d` | Delete mount point |
| `mountvol E: \\?\Volume{...}\` | Mount volume |
| `defrag C:` | Defragment drive |
| `defrag C: /U /V` | Verbose defrag |
| `defrag C: /O` | Optimize |
| `defrag C: /D` | Traditional defrag |
| `defrag C: /L` | Retrim |
| `compact /c file.txt` | Compress file |
| `compact /u file.txt` | Uncompress file |
| `compact /c /s:folder` | Compress entire folder |
| `compact /u /s:folder` | Uncompress entire folder |
| `compact /q file.txt` | Query compression |
| `compact /exe` | Compress with EXE algorithm |
| `wmic diskdrive get model,size,interfacetype` | Disk info |
| `wmic logicaldisk get name,size,freespace,filesystem` | Volume info |
| `wmic volume get driveletter,size,freespace` | Volume details |
| `fsutil volume diskfree C:` | Disk free space |
| `fsutil fsinfo drives` | List drives |
| `fsutil fsinfo driveinfo C:` | Drive info |
| `fsutil fsinfo ntfsinfo C:` | NTFS info |
| `fsutil volume defect C:` | Bad sectors |
| `powershell Get-PSDrive` | List drives (PowerShell) |

# ─── DATE & TIME ──────────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `date` | Display/set date |
| `time` | Display/set time |
| `time /t` | Display time only |
| `date /t` | Display date only |
| `echo %DATE%` | Current date variable |
| `echo %TIME%` | Current time variable |
| `echo %DATE:~0,4%%DATE:~5,2%%DATE:~8,2%` | YYYYMMDD format |
| `echo %TIME:~0,2%%TIME:~3,2%%TIME:~6,2%` | HHMMSS format |
| `wmic os get lastbootuptime` | Last boot time |
| `wmic os get localdatetime` | Current system time |
| `systeminfo \| findstr "Boot Time"` | Boot time |
| `powercfg /energy` | Power efficiency report |
| `powercfg /sleepstudy` | Sleep study report |
| `powercfg /batteryreport` | Battery report |
| `powercfg -h off` | Disable hibernation |
| `powercfg -h on` | Enable hibernation |
| `powercfg /setactive scheme_guid` | Set power scheme |
| `powercfg /list` | List power schemes |
| `powercfg /query` | Query power settings |
| `wmic path Win32_TimeZone` | Timezone info |
| `tzutil /g` | Current timezone |
| `tzutil /l` | List timezones |
| `tzutil /s "Asia/Bangkok"` | Set timezone |

# ─── SYSTEM UTILITIES ────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `shutdown /s /t 60` | Shutdown in 60 seconds |
| `shutdown /r /t 60` | Reboot in 60 seconds |
| `shutdown /a` | Abort shutdown |
| `shutdown /h` | Hibernate |
| `shutdown /l` | Log off |
| `shutdown /p` | Turn off local computer |
| `shutdown /s /t 0` | Shutdown immediately |
| `shutdown /r /t 0` | Reboot immediately |
| `shutdown /s /c "Message"` | Custom message |
| `shutdown /s /t 60 /c "System will shutdown in 1 minute"` | With message |
| `sfc /scannow` | System File Checker |
| `sfc /verifyonly` | Verify system files |
| `sfc /scanfile=file.dll` | Scan specific file |
| `sfc /verifyfile=file.dll` | Verify specific file |
| `DISM /Online /Cleanup-Image /RestoreHealth` | Fix system image |
| `DISM /Online /Cleanup-Image /CheckHealth` | Check system image |
| `DISM /Online /Cleanup-Image /ScanHealth` | Scan system image |
| `DISM /Online /Cleanup-Image /RestoreHealth /Source:source.wim` | Custom source |
| `DISM /Online /Cleanup-Image /RestoreHealth /LimitAccess` | No Windows Update |
| `DISM /Image:C:\ /Cleanup-Image /RestoreHealth` | Offline image |
| `msconfig` | System Configuration |
| `msinfo32` | System Information |
| `taskmgr` | Task Manager |
| `devmgmt.msc` | Device Manager |
| `diskmgmt.msc` | Disk Management |
| `eventvwr.msc` | Event Viewer |
| `services.msc` | Services |
| `compmgmt.msc` | Computer Management |
| `perfmon.msc` | Performance Monitor |
| `resmon` | Resource Monitor |
| `regedit` | Registry Editor |
| `gpedit.msc` | Group Policy Editor |
| `secpol.msc` | Local Security Policy |
| `certlm.msc` | Certificate Manager |
| `certmgr.msc` | User Certificate Manager |
| `mmc` | Microsoft Management Console |
| `dxdiag` | DirectX Diagnostic |
| `charmap` | Character Map |
| `calc` | Calculator |
| `notepad` | Notepad |
| `mspaint` | Paint |
| `snippingtool` | Snipping Tool |
| `explorer` | File Explorer |
| `control` | Control Panel |
| `control printers` | Printers |
| `control admintools` | Administrative Tools |
| `ncpa.cpl` | Network Connections |
| `inetcpl.cpl` | Internet Options |
| `appwiz.cpl` | Programs and Features |
| `firewall.cpl` | Windows Firewall |
| `sysdm.cpl` | System Properties |
| `powercfg.cpl` | Power Options |
| `timedate.cpl` | Date and Time |
| `desk.cpl` | Display Settings |
| `mmsys.cpl` | Sound |
| `main.cpl` | Mouse Properties |
| `access.cpl` | Accessibility Options |
| `intl.cpl` | Region and Language |
| `ms-settings:` | Windows Settings (Win10/11) |

# ─── SCHEDULED TASKS ─────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `schtasks /create /tn "TaskName" /tr "command" /sc daily /st 09:00` | Create daily task |
| `schtasks /create /tn "TaskName" /tr "command" /sc hourly` | Create hourly task |
| `schtasks /create /tn "TaskName" /tr "command" /sc onstart` | Run at startup |
| `schtasks /create /tn "TaskName" /tr "command" /sc onlogon` | Run at logon |
| `schtasks /create /tn "TaskName" /tr "command" /sc weekly /d MON /st 09:00` | Weekly task |
| `schtasks /create /tn "TaskName" /tr "command" /sc monthly /d 1 /st 09:00` | Monthly task |
| `schtasks /create /tn "TaskName" /tr "command" /sc once /st 09:00 /sd 01/01/2025` | One-time task |
| `schtasks /create /tn "TaskName" /tr "command" /sc minute /mo 30` | Every 30 minutes |
| `schtasks /create /tn "TaskName" /tr "command" /ru username /rp password` | Run as user |
| `schtasks /create /tn "TaskName" /tr "command" /ru SYSTEM` | Run as SYSTEM |
| `schtasks /create /tn "TaskName" /tr "command" /sc daily /st 09:00 /it` | Interactive task |
| `schtasks /delete /tn "TaskName" /f` | Delete task |
| `schtasks /query /tn "TaskName"` | View task |
| `schtasks /query /fo LIST /v` | Verbose list |
| `schtasks /query /fo CSV` | CSV format |
| `schtasks /run /tn "TaskName"` | Run task now |
| `schtasks /end /tn "TaskName"` | Stop task |
| `schtasks /change /tn "TaskName" /st 10:00` | Change start time |
| `schtasks /change /tn "TaskName" /disable` | Disable task |
| `schtasks /change /tn "TaskName" /enable` | Enable task |
| `schtasks /change /tn "TaskName" /ru newuser` | Change user |
| `schtasks /change /tn "TaskName" /rp newpass` | Change password |

# ─── CMD BATCH FILE COMMANDS ─────────────────────────────────────

| Command | Description |
|---------|-------------|
| `@echo off` | Hide commands |
| `echo Hello World` | Display text |
| `pause` | Pause execution |
| `cls` | Clear screen |
| `exit /b 0` | Exit with code 0 |
| `goto label` | Jump to label |
| `:label` | Define label |
| `set var=value` | Set variable |
| `%var%` | Use variable |
| `set /p var=Enter name:` | Get user input |
| `set /a var=10+5` | Arithmetic |
| `set var=` | Clear variable |
| `if exist file.txt echo File exists` | Conditional |
| `if not exist file.txt echo File not found` | Not exists |
| `if "%var%"=="value" echo Matched` | String comparison |
| `if ERRORLEVEL 1 echo Error occurred` | Error check |
| `for %%i in (file1 file2 file3) do echo %%i` | Loop list |
| `for %%i in (*.txt) do echo %%i` | Loop files |
| `for /l %%i in (1,1,10) do echo %%i` | Loop numbers |
| `for /f "delims=" %%i in (file.txt) do echo %%i` | Read file line |
| `%*` | All arguments |
| `%1` | First argument |
| `%2` | Second argument |
| `%0` | Script name |
| `shift` | Shift arguments |
| `call script.bat` | Call another batch |
| `start program.exe` | Start program |
| `timeout /t 10 /nobreak` | Wait 10 seconds |
| `choice /c YN /t 10 /d N` | Choice prompt |
| `color 0a` | Set colors |
| `title "My Script"` | Set window title |
| `prompt $P$G` | Set prompt |
| `pushd path` | Save directory and change |
| `popd` | Return to saved directory |
| `cd /d "C:\Program Files"` | Change drive and directory |
| `where program.exe` | Find program in PATH |
| `where /r C:\ file.txt` | Find file recursively |

# ─── CMD SHORTCUTS & TIPS ────────────────────────────────────────

| Shortcut | Description |
|----------|-------------|
| `Tab` | Autocomplete |
| `Ctrl + C` | Cancel current command |
| `Ctrl + Z` | Suspend |
| `Ctrl + A` | Go to beginning of line |
| `Ctrl + E` | Go to end of line |
| `Ctrl + Home` | Go to beginning of buffer |
| `Ctrl + End` | Go to end of buffer |
| `Ctrl + Left Arrow` | Move left one word |
| `Ctrl + Right Arrow` | Move right one word |
| `Ctrl + Up Arrow` | Previous command |
| `Ctrl + Down Arrow` | Next command |
| `F7` | Show command history |
| `F9` | Run command by number from history |
| `Ctrl + R` | Search command history |
| `Ctrl + L` | Clear screen |
| `Alt + F7` | Clear command history |
| `Ctrl + Delete` | Delete word after cursor |
| `Ctrl + Backspace` | Delete word before cursor |
| `Insert` | Toggle insert/overwrite |
| `Alt + Enter` | Toggle fullscreen |
| `Home` | Beginning of line |
| `End` | End of line |
| `Page Up` | Scroll up |
| `Page Down` | Scroll down |
| `Esc` | Clear line |

# ─── CMD COLOR CODES ─────────────────────────────────────────────

| Color | Code |
|-------|------|
| Black | 0 |
| Blue | 1 |
| Green | 2 |
| Aqua | 3 |
| Red | 4 |
| Purple | 5 |
| Yellow | 6 |
| White | 7 |
| Gray | 8 |
| Light Blue | 9 |
| Light Green | A |
| Light Aqua | B |
| Light Red | C |
| Light Purple | D |
| Light Yellow | E |
| Bright White | F |

# ─── COMMAND CHAINING ────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `command1 & command2` | Run command1 then command2 (always) |
| `command1 && command2` | Run command2 only if command1 succeeds |
| `command1 \|\| command2` | Run command2 only if command1 fails |
| `(command1 & command2)` | Group commands |
| `command1 \| command2` | Pipe output to command2 |

# ─── REDIRECTION ──────────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `command > file.txt` | Redirect stdout (overwrite) |
| `command >> file.txt` | Redirect stdout (append) |
| `command 2> errors.txt` | Redirect stderr |
| `command 2>&1` | Redirect stderr to stdout |
| `command > file.txt 2>&1` | Redirect both |
| `command < file.txt` | Take input from file |
| `command1 \| command2` | Pipe to command2 |
| `command 2> nul` | Suppress errors |
| `command > nul 2>&1` | Suppress all output |
| `command > file.txt & type file.txt` | Write and display |

# ================================================================
# 3. POWERSHELL COMMANDS - COMPLETE
# ================================================================

# ─── FILE OPERATIONS ──────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `Get-ChildItem -Path C:\ -Recurse -Filter *.txt` | Find all .txt files |
| `Get-ChildItem -Recurse -File \| Where-Object {$_.Length -gt 100MB}` | Files >100MB |
| `Get-ChildItem -Recurse -File \| Where-Object {$_.LastWriteTime -gt (Get-Date).AddDays(-7)}` | Files from last 7 days |
| `Get-ChildItem -Recurse -File \| Sort-Object Length -Descending` | Sort files by size |
| `Get-ChildItem -Hidden` | Show hidden files |
| `Get-ChildItem -Force` | Show all files |
| `Get-ChildItem -Directory` | List directories only |
| `Get-ChildItem -File` | List files only |
| `Copy-Item -Path C:\source -Destination D:\dest -Recurse` | Copy recursively |
| `Copy-Item -Path C:\source -Destination D:\dest -Container` | Copy with structure |
| `Copy-Item -Path C:\source -Destination D:\dest -Force` | Force copy |
| `Move-Item -Path C:\file.txt -Destination D:\file.txt` | Move file |
| `Move-Item -Path C:\folder -Destination D:\folder` | Move folder |
| `Remove-Item -Path C:\file.txt -Force` | Remove file |
| `Remove-Item -Path C:\folder -Recurse -Force` | Remove folder |
| `Remove-Item -Path C:\folder -Recurse -Confirm:$false` | Remove without confirmation |
| `New-Item -Path C:\folder -ItemType Directory` | Create directory |
| `New-Item -Path C:\folder -ItemType Directory -Force` | Create directory (force) |
| `New-Item -Path file.txt -ItemType File` | Create empty file |
| `New-Item -Path file.txt -ItemType File -Value "content"` | Create with content |
| `New-Item -Path C:\folder -ItemType SymbolicLink -Target C:\target` | Create symbolic link |
| `Get-Content -Path C:\file.txt` | Display content |
| `Get-Content -Path C:\file.txt -Tail 50` | Show last 50 lines |
| `Get-Content -Path C:\file.txt -Wait` | Follow file updates |
| `Get-Content -Path C:\file.txt -Head 10` | Show first 10 lines |
| `Select-String -Path *.log -Pattern "ERROR"` | Search in log files |
| `Select-String -Path *.log -Pattern "ERROR" -CaseSensitive` | Case-sensitive |
| `Select-String -Path *.log -Pattern "ERROR" -NotMatch` | Exclude pattern |
| `Select-String -Path *.log -Pattern "ERROR" -SimpleMatch` | Simple match |
| `Set-Content -Path file.txt -Value "content"` | Write to file |
| `Add-Content -Path file.txt -Value "append"` | Append to file |
| `Clear-Content -Path file.txt` | Clear file content |
| `Get-FileHash -Path file.txt` | Get file hash |
| `Get-FileHash -Path file.txt -Algorithm SHA256` | SHA256 hash |
| `Compare-Object (Get-Content file1.txt) (Get-Content file2.txt)` | Compare files |

# ─── SYSTEM INFORMATION ──────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `Get-ComputerInfo` | Full computer info |
| `Get-CimInstance -Class Win32_ComputerSystem` | System info |
| `Get-CimInstance -Class Win32_OperatingSystem` | OS info |
| `Get-CimInstance -Class Win32_Processor` | CPU info |
| `Get-CimInstance -Class Win32_PhysicalMemory` | Memory info |
| `Get-CimInstance -Class Win32_LogicalDisk` | Disk info |
| `Get-CimInstance -Class Win32_NetworkAdapterConfiguration` | Network info |
| `Get-CimInstance -Class Win32_Bios` | BIOS info |
| `Get-CimInstance -Class Win32_BaseBoard` | Motherboard info |
| `Get-CimInstance -Class Win32_TimeZone` | Timezone info |
| `Get-CimInstance -Class Win32_UserAccount` | User accounts |
| `Get-CimInstance -Class Win32_Group` | Groups |
| `Get-CimInstance -Class Win32_Service` | Services |
| `Get-CimInstance -Class Win32_Process` | Processes |
| `Get-CimInstance -Class Win32_Product` | Installed products |
| `Get-CimInstance -Class Win32_QuickFixEngineering` | Hotfixes |
| `Get-HotFix` | Installed updates |
| `Get-Service` | List services |
| `Get-Service \| Where-Object {$_.Status -eq 'Running'}` | Running services |
| `Get-Service \| Where-Object {$_.Status -eq 'Stopped'}` | Stopped services |
| `Get-Process` | List processes |
| `Get-Process \| Sort-Object CPU -Descending` | Sort by CPU |
| `Get-Process \| Sort-Object WS -Descending` | Sort by memory |
| `Get-Process -Name notepad` | Process by name |
| `Get-Process -Id 1234` | Process by ID |
| `Get-PSDrive` | List drives |
| `Get-Disk` | List disks |
| `Get-Partition` | List partitions |
| `Get-Volume` | List volumes |
| `Get-History` | Command history |
| `Get-PSProvider` | Providers |
| `Get-PSRepository` | Repositories |

# ─── NETWORK COMMANDS ────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `Test-Connection -ComputerName google.com -Count 4` | Ping test |
| `Test-Connection -ComputerName google.com -Count 4 -Delay 2` | With delay |
| `Test-NetConnection -ComputerName google.com -Port 443` | Test connection on port |
| `Test-NetConnection -ComputerName google.com -Port 443 -InformationLevel Detailed` | Detailed |
| `Test-NetConnection -ComputerName google.com -TraceRoute` | Trace route |
| `Resolve-DnsName google.com` | DNS lookup |
| `Resolve-DnsName google.com -Type MX` | MX record |
| `Resolve-DnsName google.com -Type TXT` | TXT record |
| `Resolve-DnsName google.com -Type NS` | NS record |
| `Resolve-DnsName google.com -Type CNAME` | CNAME record |
| `Get-NetIPAddress` | IP addresses |
| `Get-NetIPConfiguration` | IP configuration |
| `Get-NetRoute` | Routing table |
| `Get-NetNeighbor` | ARP table |
| `Get-NetAdapter` | Network adapters |
| `Get-NetAdapter -Name "Ethernet" -IncludeHidden` | Specific adapter |
| `Invoke-WebRequest -Uri https://example.com -OutFile file.html` | Download file |
| `Invoke-WebRequest -Uri https://example.com -UseBasicParsing` | Basic parsing |
| `Invoke-WebRequest -Uri https://example.com -Headers @{Header="Value"}` | Custom headers |
| `Invoke-RestMethod -Uri https://api.github.com` | REST API call |
| `Invoke-RestMethod -Uri https://api.github.com -Method POST -Body $body` | POST request |
| `Get-NetFirewallRule` | List firewall rules |
| `Get-NetFirewallRule -DisplayName "Allow 443"` | Specific rule |
| `New-NetFirewallRule -DisplayName "Allow 443" -Direction Inbound -LocalPort 443 -Protocol TCP -Action Allow` | Create rule |
| `New-NetFirewallRule -DisplayName "Allow 443" -Direction Inbound -LocalPort 443 -Protocol TCP -Action Allow -RemoteAddress 192.168.1.0/24` | With remote IP |
| `Remove-NetFirewallRule -DisplayName "Allow 443"` | Remove rule |
| `Get-NetFirewallProfile` | Firewall profiles |
| `Set-NetFirewallProfile -Profile Domain,Public,Private -Enabled False` | Disable firewall |
| `Set-NetFirewallProfile -Profile Domain,Public,Private -Enabled True` | Enable firewall |
| `Set-NetFirewallRule -DisplayName "Remote Desktop" -Enabled True` | Enable RDP |
| `Get-NetTCPConnection` | TCP connections |
| `Get-NetUDPEndpoint` | UDP endpoints |
| `Get-NetTcpSetting` | TCP settings |
| `New-NetLbfoTeam` | Create NIC team |
| `Set-NetLbfoTeam` | Configure NIC team |
| `Get-NetLbfoTeam` | Get NIC teams |

# ─── USER MANAGEMENT ─────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `Get-LocalUser` | List local users |
| `Get-LocalUser -Name username` | User details |
| `Get-LocalUser -Name username -SID` | User SID |
| `New-LocalUser -Name "username" -Password (Read-Host -AsSecureString)` | Create user |
| `New-LocalUser -Name "username" -Password (Read-Host -AsSecureString) -FullName "Full Name"` | With full name |
| `New-LocalUser -Name "username" -Password (Read-Host -AsSecureString) -Description "Description"` | With description |
| `Remove-LocalUser -Name "username"` | Delete user |
| `Set-LocalUser -Name "username" -Password (Read-Host -AsSecureString)` | Change password |
| `Set-LocalUser -Name "username" -Enabled $true` | Enable user |
| `Set-LocalUser -Name "username" -Enabled $false` | Disable user |
| `Set-LocalUser -Name "username" -FullName "New Name"` | Change full name |
| `Set-LocalUser -Name "username" -Description "New Description"` | Change description |
| `Get-LocalGroup` | List local groups |
| `Get-LocalGroup -Name "Administrators"` | Group info |
| `Add-LocalGroupMember -Group "Administrators" -Member "username"` | Add to admin |
| `Remove-LocalGroupMember -Group "Administrators" -Member "username"` | Remove from admin |
| `Get-LocalGroupMember -Group "Administrators"` | List admin members |
| `Get-LocalGroupMember -Group "Users"` | List users group members |
| `Get-WmiObject -Class Win32_UserAccount` | All user accounts |
| `Get-WmiObject -Class Win32_UserAccount -Filter "Name='username'"` | Specific user |
| `Get-WmiObject -Class Win32_UserAccount -Filter "Disabled='True'"` | Disabled users |
| `Get-WmiObject -Class Win32_Group` | All groups |
| `Add-Computer -DomainName domain.com -Credential domain\user` | Join domain |
| `Remove-Computer -UnjoinDomainCredential domain\user -Restart` | Leave domain |
| `Rename-Computer -NewName "NewName"` | Rename computer |
| `Restart-Computer` | Restart computer |
| `Restart-Computer -Force` | Force restart |
| `Stop-Computer` | Shutdown computer |
| `Stop-Computer -Force` | Force shutdown |

# ─── DISK & STORAGE ──────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `Get-PSDrive` | List drives |
| `Get-PSDrive -Name C` | Specific drive |
| `Get-Disk` | List disks |
| `Get-Disk -Number 0` | Specific disk |
| `Get-Disk \| Where-Object {$_.OperationalStatus -eq 'Online'}` | Online disks |
| `Get-Partition` | List partitions |
| `Get-Partition -DriveLetter C` | Specific partition |
| `Get-Volume` | List volumes |
| `Get-Volume -DriveLetter C` | Specific volume |
| `Optimize-Volume -DriveLetter C -ReTrim -Verbose` | Optimize drive |
| `Optimize-Volume -DriveLetter C -Defrag -Verbose` | Defrag |
| `Optimize-Volume -DriveLetter C -Analyze -Verbose` | Analyze |
| `Get-PhysicalDisk \| Select-Object Model,Size,MediaType` | Physical disk info |
| `Get-PhysicalDisk \| Where-Object {$_.MediaType -eq 'SSD'}` | SSD drives |
| `Repair-Volume -DriveLetter C -Scan` | Scan volume |
| `Repair-Volume -DriveLetter C -OfflineScanAndFix` | Fix volume |
| `Set-Partition -DriveLetter C -IsActive $true` | Set partition active |
| `Set-Partition -DriveLetter C -IsHidden $true` | Hide partition |
| `New-Partition -DiskNumber 0 -UseMaximumSize -AssignDriveLetter` | Create partition |
| `New-Partition -DiskNumber 0 -Size 100GB -DriveLetter D` | Create partition with size |
| `Remove-Partition -DriveLetter D -Confirm:$false` | Remove partition |
| `Format-Volume -DriveLetter D -FileSystem NTFS -NewFileSystemLabel "Data"` | Format volume |
| `Format-Volume -DriveLetter D -FileSystem NTFS -FileSystemLabel "Data" -Quick` | Quick format |
| `Resize-Partition -DriveLetter C -Size 100GB` | Resize partition |
| `Get-Disk \| Initialize-Disk -PartitionStyle GPT` | Initialize disk |
| `Get-Disk \| Set-Disk -IsReadOnly $true` | Make disk read-only |
| `Get-Disk \| Set-Disk -IsReadOnly $false` | Make disk writable |
| `Get-Disk \| Clear-Disk -RemoveData -Confirm:$false` | Clear disk |
| `Set-StorageSetting -NewDiskPolicy OfflineShared` | Disk policy |

# ─── DATE & TIME ──────────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `Get-Date` | Current date/time |
| `Get-Date -Format "yyyy-MM-dd HH:mm:ss"` | Custom format |
| `Get-Date -UFormat %s` | Unix timestamp |
| `Get-Date -Format "dddd, MMMM d, yyyy"` | Long format |
| `(Get-Date).AddDays(7)` | 7 days from now |
| `(Get-Date).AddDays(-7)` | 7 days ago |
| `(Get-Date).AddHours(-1)` | 1 hour ago |
| `(Get-Date).AddMonths(1)` | 1 month from now |
| `(Get-Date).AddYears(1)` | 1 year from now |
| `(Get-Date).DayOfWeek` | Day of week |
| `(Get-Date).ToString("MM/dd/yyyy")` | Format as string |
| `New-TimeSpan -Start (Get-Date) -End (Get-Date).AddDays(7)` | Time span |
| `Get-TimeZone` | Timezone info |
| `Set-TimeZone -Name "Asia/Bangkok"` | Set timezone |
| `Set-Date -Date "2024-01-01 12:00:00"` | Set system date/time |
| `Get-CimInstance -Class Win32_LocalTime` | System time |

# ─── TEXT PROCESSING ─────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `Get-Content file.txt \| Select-String "pattern"` | Search in file |
| `Get-Content file.txt \| Where-Object {$_ -match "pattern"}` | Filter lines |
| `Get-Content file.txt \| Sort-Object` | Sort lines |
| `Get-Content file.txt \| Sort-Object -Unique` | Sort and unique |
| `Get-Content file.txt \| ForEach-Object {$_ -replace "old","new"}` | Replace text |
| `Get-Content file.txt \| Select-Object -First 10` | First 10 lines |
| `Get-Content file.txt \| Select-Object -Last 10` | Last 10 lines |
| `Get-Content file.txt \| Measure-Object -Line` | Count lines |
| `Get-Content file.txt \| Measure-Object -Word` | Count words |
| `Get-Content file.txt \| Measure-Object -Character` | Count characters |
| `Get-Content file.txt \| Group-Object` | Group lines |
| `Get-Content file.txt \| Where-Object {$_ -match "pattern"} \| ForEach-Object {$_ -replace "old","new"}` | Chain operations |
| `Import-Csv file.csv \| Export-Csv new.csv` | CSV import/export |
| `Import-Csv file.csv \| Where-Object {$_.Column -eq "Value"}` | Filter CSV |
| `Import-Csv file.csv \| Group-Object Column` | Group by column |
| `Import-Csv file.csv \| Export-Csv new.csv -NoTypeInformation` | Export without type |
| `Import-Csv file.csv \| ConvertTo-Json \| Out-File file.json` | CSV to JSON |
| `ConvertTo-Json` | Convert to JSON |
| `ConvertFrom-Json` | Convert from JSON |
| `ConvertTo-Csv` | Convert to CSV |
| `ConvertFrom-Csv` | Convert from CSV |
| `ConvertTo-Html` | Convert to HTML |
| `Export-Csv -Path file.csv -NoTypeInformation` | Export to CSV |
| `Export-CliXml -Path file.xml` | Export to XML |
| `Import-CliXml -Path file.xml` | Import from XML |
| `Out-File -FilePath file.txt` | Output to file |
| `Out-Null` | Suppress output |
| `Out-Host` | Output to host |

# ─── COMPRESSION & ARCHIVING ─────────────────────────────────────

| Command | Description |
|---------|-------------|
| `Compress-Archive -Path C:\folder -DestinationPath C:\archive.zip` | Create zip |
| `Compress-Archive -Path C:\folder -DestinationPath C:\archive.zip -CompressionLevel Optimal` | Optimal compression |
| `Compress-Archive -Path *.txt -DestinationPath files.zip` | Zip files |
| `Compress-Archive -Path C:\folder -DestinationPath C:\archive.zip -Force` | Overwrite if exists |
| `Expand-Archive -Path C:\archive.zip -DestinationPath C:\extract` | Extract zip |
| `Expand-Archive -Path C:\archive.zip -DestinationPath C:\extract -Force` | Overwrite |
| `Expand-Archive -Path C:\archive.zip -DestinationPath C:\extract -PassThru` | Show extracted files |

# ─── SYSTEM MONITORING ───────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `Get-Counter "\Processor(_Total)\% Processor Time"` | CPU usage |
| `Get-Counter "\Memory\Available MBytes"` | Available memory |
| `Get-Counter "\PhysicalDisk(_Total)\% Disk Time"` | Disk usage |
| `Get-Counter "\Network Interface(*)\Bytes Total/sec"` | Network usage |
| `Get-Counter -ListSet Processor` | Available processor counters |
| `Get-Counter -ListSet Memory` | Available memory counters |
| `Get-Counter -ListSet PhysicalDisk` | Available disk counters |
| `Get-Counter -ListSet Network Interface` | Available network counters |
| `Get-EventLog -LogName System -Newest 50` | Recent system events |
| `Get-EventLog -LogName Application -Newest 50` | Recent application events |
| `Get-EventLog -LogName Security -Newest 50` | Recent security events |
| `Get-WinEvent -MaxEvents 50 -FilterHashtable @{LogName='System'; Level=1}` | Critical events |
| `Get-WinEvent -MaxEvents 50 -FilterHashtable @{LogName='Application'; ProviderName='Application Error'}` | Application errors |
| `Start-Sleep -Seconds 10` | Pause |
| `Start-Sleep -Milliseconds 500` | Pause 500ms |
| `Measure-Command { command }` | Measure command time |
| `Get-CimInstance -Class Win32_PerfFormattedData_PerfOS_System` | System performance |
| `Get-CimInstance -Class Win32_PerfFormattedData_PerfOS_Processor` | Processor performance |
| `Get-CimInstance -Class Win32_PerfFormattedData_PerfOS_Memory` | Memory performance |
| `Get-CimInstance -Class Win32_PerfFormattedData_PerfOS_PhysicalDisk` | Disk performance |

# ─── REGISTRY OPERATIONS ─────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `Get-ItemProperty -Path "HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Run"` | Read registry |
| `Get-ItemProperty -Path "HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Run" -Name "App"` | Specific value |
| `Get-ChildItem -Path "HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Run"` | List keys |
| `Set-ItemProperty -Path "HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Run" -Name "App" -Value "C:\app.exe"` | Set value |
| `Set-ItemProperty -Path "HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Run" -Name "App" -Value "C:\app.exe" -Type String` | With type |
| `Remove-ItemProperty -Path "HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Run" -Name "App"` | Remove value |
| `New-Item -Path "HKLM:\SOFTWARE\MyApp" -Force` | Create key |
| `New-Item -Path "HKLM:\SOFTWARE\MyApp\SubKey" -Force` | Create subkey |
| `Remove-Item -Path "HKLM:\SOFTWARE\MyApp" -Recurse` | Delete key |
| `Get-ItemProperty -Path "HKCU:\Software\Microsoft\Notepad"` | HKCU example |
| `Get-ItemProperty -Path "HKCR:\txtfile\shell\open\command"` | File association |
| `Get-ChildItem -Path "HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Uninstall"` | Installed apps |
| `Get-ItemProperty -Path "HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Uninstall\*" \| Select-Object DisplayName` | App names |
| `Get-ChildItem -Path "HKLM:\SYSTEM\CurrentControlSet\Services"` | Services |
| `Get-ItemProperty -Path "HKLM:\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters"` | TCP/IP settings |

# ─── POWERSHELL ADVANCED ─────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `try { command } catch { Write-Warning "Error: $_" }` | Error handling |
| `try { command } catch [System.Exception] { Write-Host "Error: $_" }` | Specific error |
| `function Get-SystemUptime { (Get-Date) - (Get-CimInstance Win32_OperatingSystem).LastBootUpTime }` | Define function |
| `function Get-SystemUptime { param($Computer) Invoke-Command -ComputerName $Computer -ScriptBlock { (Get-Date) - (Get-CimInstance Win32_OperatingSystem).LastBootUpTime } }` | Function with param |
| `Import-Module ActiveDirectory` | Import module |
| `Import-Module -Name "C:\Modules\MyModule.psm1"` | Import custom module |
| `Get-Module -ListAvailable` | List available modules |
| `Get-Module -ListAvailable \| Where-Object {$_.Name -like "*AD*"}` | Find AD module |
| `Install-Module -Name ModuleName` | Install module |
| `Update-Module -Name ModuleName` | Update module |
| `Remove-Module -Name ModuleName` | Remove module |
| `Uninstall-Module -Name ModuleName` | Uninstall module |
| `Get-Command -Module ModuleName` | Commands in module |
| `Get-Help Get-Process` | Help for command |
| `Get-Help Get-Process -Detailed` | Detailed help |
| `Get-Help Get-Process -Examples` | Examples |
| `Get-Member -InputObject (Get-Process)` | Get object members |
| `Get-TypeData` | Type data |
| `Get-PSDrive` | PS drives |
| `New-PSDrive -Name "Data" -PSProvider FileSystem -Root "C:\Data"` | New PS drive |
| `Remove-PSDrive -Name "Data"` | Remove PS drive |
| `Get-PSProvider` | PS providers |
| `New-Item -Path "Data:\file.txt" -ItemType File` | Use PS drive |
| `$PSVersionTable` | PowerShell version |
| `$Error` | Error variable |
| `$Error.Clear()` | Clear errors |
| `$VerbosePreference = "Continue"` | Verbose output |
| `$DebugPreference = "Continue"` | Debug output |

# ─── POWERSHELL ADVANCED FILTERING ──────────────────────────────

| Command | Description |
|---------|-------------|
| `Get-ChildItem -Recurse -File \| Where-Object { $_.LastWriteTime -gt (Get-Date).AddDays(-7) -and $_.Length -gt 100MB -and $_.Extension -in '.log','.txt','.tmp' }` | Complex filtering |
| `Get-ChildItem -Recurse -File \| Where-Object { $_.Extension -eq ".txt" -or $_.Extension -eq ".log" }` | Multiple extensions |
| `Get-ChildItem -Recurse -File \| Where-Object { $_.Name -like "*backup*" }` | Name wildcard |
| `Get-Process \| Where-Object { $_.CPU -gt 50 -and $_.WorkingSet -gt 100MB }` | Process filtering |
| `Get-Process \| Where-Object { $_.ProcessName -like "*chrome*" }` | Process name filter |
| `Get-Service \| Where-Object { $_.Status -eq "Running" -and $_.Name -like "*win*" }` | Service filtering |
| `Get-EventLog -LogName System -Newest 100 \| Where-Object { $_.EntryType -eq "Error" }` | Error log filtering |
| `Get-ChildItem -Recurse -File \| Select-Object Name, Length, LastWriteTime, Extension` | Select properties |
| `Get-ChildItem -Recurse -File \| Select-Object Name, @{N="SizeMB";E={[math]::Round($_.Length/1MB,2)}}` | Custom property |

# ─── POWERSHELL REMOTE MANAGEMENT ────────────────────────────────

| Command | Description |
|---------|-------------|
| `Enter-PSSession -ComputerName host` | Enter remote session |
| `Enter-PSSession -ComputerName host -Credential domain\user` | With credentials |
| `Exit-PSSession` | Exit session |
| `Invoke-Command -ComputerName host -ScriptBlock {Get-Process}` | Run command remotely |
| `Invoke-Command -ComputerName host -ScriptBlock {Get-Process} -Credential domain\user` | With credentials |
| `New-PSSession -ComputerName host` | Create session |
| `New-PSSession -ComputerName host -SessionName "Remote"` | Named session |
| `Get-PSSession` | List sessions |
| `Remove-PSSession -Session $session` | Remove session |
| `Test-WSMan -ComputerName host` | Test WinRM connectivity |
| `Enable-PSRemoting -Force` | Enable PowerShell remoting |
| `Disable-PSRemoting -Force` | Disable PowerShell remoting |
| `Set-Item WSMan:\localhost\Client\TrustedHosts -Value "host"` | Add trusted host |
| `Set-Item WSMan:\localhost\Client\TrustedHosts -Value "host" -Force` | Without confirmation |
| `Clear-Item WSMan:\localhost\Client\TrustedHosts` | Clear trusted hosts |
| `Get-WSManInstance -ResourceURI winrm/config/listener` | WinRM listeners |
| `Set-WSManQuickConfig` | Quick WinRM config |

# ─── POWERSHELL SCHEDULED TASKS ──────────────────────────────────

| Command | Description |
|---------|-------------|
| `Register-ScheduledTask -TaskName "Backup" -Action (New-ScheduledTaskAction -Execute "cmd.exe" -Argument "/c backup.bat")` | Create task |
| `Register-ScheduledTask -TaskName "Backup" -Action (New-ScheduledTaskAction -Execute "cmd.exe" -Argument "/c backup.bat") -Trigger (New-ScheduledTaskTrigger -Daily -At 9am)` | With trigger |
| `Register-ScheduledTask -TaskName "Backup" -Action (New-ScheduledTaskAction -Execute "cmd.exe" -Argument "/c backup.bat") -User "username" -Password "password"` | Run as user |
| `Register-ScheduledTask -TaskName "Backup" -Action (New-ScheduledTaskAction -Execute "cmd.exe" -Argument "/c backup.bat") -User "SYSTEM"` | Run as SYSTEM |
| `Unregister-ScheduledTask -TaskName "Backup" -Confirm:$false` | Remove task |
| `Get-ScheduledTask -TaskName "Backup"` | Get task info |
| `Get-ScheduledTask \| Where-Object {$_.State -eq "Ready"}` | Ready tasks |
| `Start-ScheduledTask -TaskName "Backup"` | Run task now |
| `Stop-ScheduledTask -TaskName "Backup"` | Stop task |
| `Enable-ScheduledTask -TaskName "Backup"` | Enable task |
| `Disable-ScheduledTask -TaskName "Backup"` | Disable task |
| `Update-ScheduledTask -TaskName "Backup" -Action (New-ScheduledTaskAction -Execute "cmd.exe" -Argument "/c newbackup.bat")` | Update task |
| `Export-ScheduledTask -TaskName "Backup" \| Out-File backup.xml` | Export task |
| `Import-ScheduledTask -Xml (Get-Content backup.xml) \| Register-ScheduledTask -TaskName "Backup"` | Import task |

# ================================================================
# 4. DOCKER & CONTAINER COMMANDS - COMPLETE
# ================================================================

# ─── DOCKER BASIC ─────────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `docker --version` | Docker version |
| `docker info` | Docker system info |
| `docker system df` | Docker disk usage |
| `docker system prune` | Remove unused data |
| `docker system prune -a` | Remove all unused data |
| `docker system prune -f` | Force prune |
| `docker login` | Login to registry |
| `docker login -u username -p password registry` | Login with credentials |
| `docker logout` | Logout from registry |

# ─── DOCKER CONTAINER MANAGEMENT ─────────────────────────────────

| Command | Description |
|---------|-------------|
| `docker run -d --name nginx -p 80:80 nginx` | Run container |
| `docker run -it --name ubuntu ubuntu /bin/bash` | Interactive container |
| `docker run --rm -it ubuntu /bin/bash` | Remove after exit |
| `docker run -v /host/path:/container/path ubuntu` | Mount volume |
| `docker run -e ENV_VAR=value ubuntu` | Set environment variable |
| `docker run --network host ubuntu` | Use host network |
| `docker run --restart=always nginx` | Auto-restart |
| `docker run --memory=512m nginx` | Memory limit |
| `docker run --cpus=0.5 nginx` | CPU limit |
| `docker ps` | List running containers |
| `docker ps -a` | List all containers |
| `docker ps -q` | Quiet mode (IDs only) |
| `docker ps -a -q` | All container IDs |
| `docker ps -a --filter "status=exited"` | Exited containers |
| `docker stop container_name` | Stop container |
| `docker stop -t 30 container_name` | Stop with timeout |
| `docker start container_name` | Start container |
| `docker restart container_name` | Restart container |
| `docker pause container_name` | Pause container |
| `docker unpause container_name` | Unpause container |
| `docker rm container_name` | Remove container |
| `docker rm -f container_name` | Force remove |
| `docker rm -v container_name` | Remove volumes |
| `docker rm $(docker ps -a -q)` | Remove all containers |
| `docker exec -it container_name /bin/bash` | Execute in container |
| `docker exec -it container_name sh` | Execute with sh |
| `docker exec container_name command` | Run command |
| `docker exec -e VAR=value container_name command` | With env vars |
| `docker logs container_name` | Show logs |
| `docker logs -f container_name` | Follow logs |
| `docker logs --tail 100 container_name` | Last 100 lines |
| `docker logs --since "1 hour ago" container_name` | Since time |
| `docker logs --until "1 hour ago" container_name` | Until time |
| `docker cp container_name:/path/file .` | Copy from container |
| `docker cp file container_name:/path/` | Copy to container |
| `docker port container_name` | Port mappings |
| `docker top container_name` | Processes in container |
| `docker stats` | Container stats |
| `docker stats container_name` | Specific container |
| `docker inspect container_name` | Container details |
| `docker inspect -f '{{.State.Status}}' container_name` | Specific field |
| `docker rename old_name new_name` | Rename container |
| `docker update --memory=1g container_name` | Update resources |

# ─── DOCKER IMAGE MANAGEMENT ─────────────────────────────────────

| Command | Description |
|---------|-------------|
| `docker images` | List images |
| `docker images -a` | All images |
| `docker images -q` | Quiet mode (IDs only) |
| `docker images --filter "dangling=true"` | Dangling images |
| `docker pull ubuntu:latest` | Pull image |
| `docker pull ubuntu:20.04` | Pull specific tag |
| `docker pull registry/image:tag` | Pull from registry |
| `docker build -t myapp:latest .` | Build image |
| `docker build -t myapp:latest -f Dockerfile .` | Custom Dockerfile |
| `docker build --no-cache -t myapp:latest .` | No cache |
| `docker build --build-arg VERSION=1.0 -t myapp:latest .` | Build arguments |
| `docker tag myapp:latest myregistry/myapp:v1` | Tag image |
| `docker tag myapp:latest myregistry/myapp:v1.0` | Multiple tags |
| `docker push myregistry/myapp:v1` | Push to registry |
| `docker push myregistry/myapp:latest` | Push latest |
| `docker rmi image_id` | Remove image |
| `docker rmi -f image_id` | Force remove |
| `docker rmi $(docker images -q)` | Remove all images |
| `docker rmi $(docker images -f "dangling=true" -q)` | Remove dangling images |
| `docker save -o image.tar image_name` | Save image to tar |
| `docker save image_name \| gzip > image.tar.gz` | Save compressed |
| `docker load -i image.tar` | Load image from tar |
| `docker load < image.tar.gz` | Load compressed |
| `docker history image_name` | Image history |
| `docker image inspect image_name` | Image details |

# ─── DOCKER COMPOSE ──────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `docker-compose up -d` | Start services in background |
| `docker-compose up -d --build` | Build and start |
| `docker-compose up -d --scale web=3` | Scale services |
| `docker-compose down` | Stop and remove containers |
| `docker-compose down -v` | Remove volumes |
| `docker-compose down --rmi all` | Remove images |
| `docker-compose ps` | List services |
| `docker-compose ps -a` | All containers |
| `docker-compose logs -f` | Follow logs |
| `docker-compose logs service` | Service logs |
| `docker-compose logs --tail 100` | Last 100 lines |
| `docker-compose exec service /bin/bash` | Execute in service |
| `docker-compose exec service command` | Run command |
| `docker-compose exec -e VAR=value service command` | With env vars |
| `docker-compose run service command` | Run one-off command |
| `docker-compose build` | Build/rebuild services |
| `docker-compose build --no-cache` | Build without cache |
| `docker-compose restart service` | Restart service |
| `docker-compose stop service` | Stop service |
| `docker-compose start service` | Start service |
| `docker-compose pause` | Pause services |
| `docker-compose unpause` | Unpause services |
| `docker-compose config` | Validate config |
| `docker-compose config -q` | Quiet validation |
| `docker-compose top` | Processes in services |
| `docker-compose port service 80` | Port mapping |
| `docker-compose images` | Images used |
| `docker-compose events` | Stream events |
| `docker-compose version` | Compose version |

# ─── DOCKER NETWORK ──────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `docker network ls` | List networks |
| `docker network create mynet` | Create network |
| `docker network create -d bridge mynet` | Bridge network |
| `docker network create -d overlay mynet` | Overlay network |
| `docker network create --subnet=10.0.0.0/24 mynet` | With subnet |
| `docker network create --driver=macvlan --subnet=192.168.1.0/24 -o parent=eth0 mynet` | Macvlan network |
| `docker network connect mynet container_name` | Connect container to network |
| `docker network disconnect mynet container_name` | Disconnect container |
| `docker network inspect mynet` | Inspect network |
| `docker network rm mynet` | Remove network |
| `docker network prune` | Remove unused networks |
| `docker network prune -f` | Force prune |

# ─── DOCKER VOLUMES ──────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `docker volume ls` | List volumes |
| `docker volume create myvolume` | Create volume |
| `docker volume create -d local myvolume` | With driver |
| `docker volume inspect myvolume` | Inspect volume |
| `docker volume rm myvolume` | Remove volume |
| `docker volume rm $(docker volume ls -q)` | Remove all volumes |
| `docker volume prune` | Remove unused volumes |
| `docker volume prune -f` | Force prune |
| `docker run -v myvolume:/data nginx` | Mount volume |
| `docker run -v /host/path:/container/path nginx` | Bind mount |
| `docker run --mount type=volume,source=myvolume,target=/data nginx` | Mount with options |
| `docker run --mount type=bind,source=/host/path,target=/container/path nginx` | Bind mount with options |
| `docker run --mount type=tmpfs,target=/tmp nginx` | Tmpfs mount |

# ─── KUBERNETES COMMANDS ─────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `kubectl get pods` | List pods |
| `kubectl get pods -n namespace` | Specific namespace |
| `kubectl get pods -A` | All namespaces |
| `kubectl get pods -w` | Watch pods |
| `kubectl get pods -o wide` | Detailed output |
| `kubectl get pods -o json` | JSON output |
| `kubectl get pods -o yaml` | YAML output |
| `kubectl get services` | List services |
| `kubectl get deployments` | List deployments |
| `kubectl get nodes` | List nodes |
| `kubectl get nodes -o wide` | Detailed nodes |
| `kubectl get namespaces` | List namespaces |
| `kubectl get configmaps` | List config maps |
| `kubectl get secrets` | List secrets |
| `kubectl get ingresses` | List ingresses |
| `kubectl get persistentvolumes` | List PVs |
| `kubectl get persistentvolumeclaims` | List PVCs |
| `kubectl get events --sort-by='.lastTimestamp'` | Events sorted |
| `kubectl create -f deployment.yaml` | Create resource |
| `kubectl apply -f deployment.yaml` | Apply/update resource |
| `kubectl apply -f directory/` | Apply all in directory |
| `kubectl apply -k directory/` | Apply kustomization |
| `kubectl delete -f deployment.yaml` | Delete resource |
| `kubectl delete pod pod_name` | Delete pod |
| `kubectl delete deployment deployment_name` | Delete deployment |
| `kubectl delete service service_name` | Delete service |
| `kubectl logs pod_name` | Pod logs |
| `kubectl logs -f pod_name` | Follow logs |
| `kubectl logs pod_name -c container_name` | Specific container |
| `kubectl logs --since=1h pod_name` | Since time |
| `kubectl logs --tail=100 pod_name` | Last 100 lines |
| `kubectl exec -it pod_name -- /bin/bash` | Execute in pod |
| `kubectl exec -it pod_name -c container_name -- /bin/bash` | Specific container |
| `kubectl exec pod_name -- command` | Run command |
| `kubectl describe pod pod_name` | Describe pod |
| `kubectl describe deployment deployment_name` | Describe deployment |
| `kubectl describe node node_name` | Describe node |
| `kubectl port-forward pod_name 8080:80` | Port forward |
| `kubectl port-forward service/service_name 8080:80` | Service port forward |
| `kubectl scale deployment myapp --replicas=3` | Scale deployment |
| `kubectl scale --replicas=3 deployment/myapp` | Alternative |
| `kubectl rollout status deployment myapp` | Check rollout status |
| `kubectl rollout history deployment myapp` | Rollout history |
| `kubectl rollout undo deployment myapp` | Rollback |
| `kubectl rollout undo deployment myapp --to-revision=2` | Specific revision |
| `kubectl autoscale deployment myapp --min=2 --max=10 --cpu-percent=80` | Autoscale |
| `kubectl edit deployment myapp` | Edit deployment |
| `kubectl edit service myapp` | Edit service |
| `kubectl patch deployment myapp -p '{"spec":{"replicas":3}}'` | Patch deployment |
| `kubectl set image deployment/myapp myapp=image:new` | Update image |
| `kubectl set env deployment/myapp ENV_VAR=value` | Set env var |
| `kubectl label pod pod_name key=value` | Add label |
| `kubectl annotate pod pod_name annotation=value` | Add annotation |
| `kubectl top node` | Node metrics |
| `kubectl top pod` | Pod metrics |
| `kubectl top pod -n namespace` | Namespace metrics |
| `kubectl api-resources` | API resources |
| `kubectl explain pod` | Explain resource |
| `kubectl version` | Kubernetes version |
| `kubectl cluster-info` | Cluster info |
| `kubectl config view` | Kubeconfig view |
| `kubectl config use-context context` | Change context |
| `kubectl config set-context context --namespace=namespace` | Set namespace |

# ─── KUBERNETES ADVANCED ─────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `kubectl get pods --field-selector=status.phase=Running` | Filter by phase |
| `kubectl get pods -l app=myapp` | Label selector |
| `kubectl get pods -l app=myapp -l env=prod` | Multiple labels |
| `kubectl get pods -l 'app in (myapp,yourapp)'` | Set-based selector |
| `kubectl get pods --show-labels` | Show labels |
| `kubectl get pods --namespace=namespace` | Namespace |
| `kubectl get pods --all-namespaces` | All namespaces |
| `kubectl get pods --watch` | Watch changes |
| `kubectl get pods --sort-by='.metadata.creationTimestamp'` | Sort by creation |
| `kubectl get pods --sort-by='.status.phase'` | Sort by phase |
| `kubectl get nodes --sort-by='.status.capacity.cpu'` | Sort nodes by CPU |
| `kubectl delete pods --all` | Delete all pods |
| `kubectl delete pods --field-selector=status.phase=Failed` | Delete failed pods |
| `kubectl delete pods -l app=myapp` | Delete by label |
| `kubectl delete all --all -n namespace` | Delete all resources |
| `kubectl run nginx --image=nginx` | Run pod |
| `kubectl expose deployment nginx --port=80 --type=LoadBalancer` | Expose service |
| `kubectl create secret generic mysecret --from-literal=key=value` | Create secret |
| `kubectl create configmap myconfig --from-literal=key=value` | Create configmap |
| `kubectl create serviceaccount myuser` | Create service account |
| `kubectl create rolebinding myrolebinding --role=myrole --serviceaccount=namespace:myuser` | Role binding |
| `kubectl create clusterrolebinding myclusterrolebinding --clusterrole=cluster-admin --serviceaccount=namespace:myuser` | Cluster role binding |
| `kubectl taint nodes node_name key=value:NoSchedule` | Taint node |
| `kubectl taint nodes node_name key:NoSchedule-` | Remove taint |
| `kubectl cordon node_name` | Mark node unschedulable |
| `kubectl uncordon node_name` | Mark node schedulable |
| `kubectl drain node_name --ignore-daemonsets` | Drain node |
| `kubectl cert-manager` | Certificate management |
| `kubectl kustomize` | Kustomize commands |

# ================================================================
# 5. GIT COMMANDS - COMPLETE
# ================================================================

# ─── GIT BASIC ────────────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `git init` | Initialize repository |
| `git init --bare` | Initialize bare repository |
| `git clone https://github.com/user/repo.git` | Clone repository |
| `git clone -b branch_name https://github.com/user/repo.git` | Clone specific branch |
| `git clone --depth 1 https://github.com/user/repo.git` | Shallow clone |
| `git clone --recursive https://github.com/user/repo.git` | Clone with submodules |
| `git status` | Check status |
| `git status -s` | Short status |
| `git add .` | Stage all changes |
| `git add file.txt` | Stage specific file |
| `git add -p file.txt` | Interactive staging |
| `git add -A` | Stage all (including deletions) |
| `git add -u` | Stage tracked files |
| `git commit -m "message"` | Commit changes |
| `git commit -am "message"` | Add and commit all |
| `git commit -m "message" -m "body"` | Multi-line commit |
| `git commit --amend -m "new message"` | Amend last commit |
| `git commit --amend --no-edit` | Amend without changing message |
| `git push origin main` | Push to remote |
| `git push -u origin main` | Push and set upstream |
| `git push origin --tags` | Push tags |
| `git push origin main --force` | Force push |
| `git push --force-with-lease` | Force push (safe) |
| `git pull origin main` | Pull from remote |
| `git pull --rebase origin main` | Pull with rebase |
| `git fetch origin` | Fetch from remote |
| `git fetch --all` | Fetch all remotes |
| `git fetch --prune` | Fetch and prune |
| `git log` | View commit history |
| `git log --oneline` | Compact history |
| `git log --graph` | Visual history |
| `git log --graph --oneline --decorate` | Nice visual |
| `git log -p` | Show changes |
| `git log --since="2 days ago"` | Since time |
| `git log --until="yesterday"` | Until time |
| `git log --author="name"` | By author |
| `git log --grep="pattern"` | By message |
| `git log file.txt` | File history |
| `git log -L 10,20:file.txt` | Line range history |
| `git diff` | Show changes |
| `git diff --staged` | Show staged changes |
| `git diff HEAD` | Show changes since last commit |
| `git diff commit1..commit2` | Compare commits |
| `git diff branch1..branch2` | Compare branches |
| `git diff --stat` | Summary diff |
| `git diff --name-only` | Only changed files |
| `git show commit_hash` | Show commit details |
| `git show commit_hash:file.txt` | Show file at commit |
| `git blame file.txt` | Blame file |
| `git blame -L 10,20 file.txt` | Blame lines |
| `git shortlog` | Shortlog |
| `git shortlog -sn` | Count commits per author |

# ─── GIT BRANCHES ─────────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `git branch` | List branches |
| `git branch -a` | List all branches (including remote) |
| `git branch -r` | List remote branches |
| `git branch -vv` | Show tracking branches |
| `git checkout branch_name` | Switch branch |
| `git checkout -b new_branch` | Create and switch branch |
| `git checkout -b new_branch origin/remote_branch` | Track remote branch |
| `git switch branch_name` | Switch branch (modern) |
| `git switch -c new_branch` | Create and switch (modern) |
| `git merge branch_name` | Merge branch |
| `git merge --no-ff branch_name` | Merge with no fast-forward |
| `git merge --squash branch_name` | Squash merge |
| `git merge --abort` | Abort merge |
| `git branch -d branch_name` | Delete branch |
| `git branch -D branch_name` | Force delete branch |
| `git push origin --delete branch_name` | Delete remote branch |
| `git branch -m old_name new_name` | Rename branch |
| `git branch -m new_name` | Rename current branch |
| `git cherry-pick commit_hash` | Apply specific commit |
| `git cherry-pick -n commit_hash` | Cherry-pick without commit |
| `git cherry-pick --abort` | Abort cherry-pick |
| `git rebase branch_name` | Rebase current branch |
| `git rebase -i HEAD~10` | Interactive rebase |
| `git rebase --continue` | Continue rebase |
| `git rebase --abort` | Abort rebase |
| `git rebase --skip` | Skip commit |
| `git rebase --onto newbase oldbase branch` | Advanced rebase |
| `git tag` | List tags |
| `git tag v1.0.0` | Create tag |
| `git tag -a v1.0.0 -m "Version 1.0.0"` | Annotated tag |
| `git tag -d v1.0.0` | Delete tag |
| `git push origin v1.0.0` | Push tag |
| `git push origin --tags` | Push all tags |
| `git fetch --tags` | Fetch tags |
| `git checkout tags/v1.0.0` | Checkout tag |

# ─── GIT UNDO ─────────────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `git reset HEAD file.txt` | Unstage file |
| `git restore --staged file.txt` | Unstage file (modern) |
| `git reset --soft HEAD~1` | Undo commit (keep changes) |
| `git reset --mixed HEAD~1` | Undo commit (unstage changes) |
| `git reset --hard HEAD~1` | Undo commit (discard changes) |
| `git reset --hard origin/main` | Reset to remote |
| `git revert commit_hash` | Revert commit |
| `git revert HEAD` | Revert last commit |
| `git revert -n commit_hash` | Revert without commit |
| `git restore file.txt` | Discard changes to file |
| `git checkout -- file.txt` | Discard changes (legacy) |
| `git clean -fd` | Remove untracked files |
| `git clean -fd -n` | Dry run |
| `git clean -fdx` | Remove ignored files too |
| `git stash` | Stash changes |
| `git stash push -m "message"` | Stash with message |
| `git stash pop` | Apply and drop latest stash |
| `git stash apply` | Apply stashed changes |
| `git stash list` | List stashes |
| `git stash show stash@{0}` | Show stash |
| `git stash show -p stash@{0}` | Show stash diff |
| `git stash drop stash@{0}` | Drop stash |
| `git stash clear` | Clear all stashes |
| `git stash branch branch_name stash@{0}` | Create branch from stash |

# ─── GIT REMOTE ───────────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `git remote -v` | Show remotes |
| `git remote add origin https://github.com/user/repo.git` | Add remote |
| `git remote add upstream https://github.com/original/repo.git` | Add upstream |
| `git remote set-url origin https://github.com/user/repo.git` | Change URL |
| `git remote remove origin` | Remove remote |
| `git remote rename old new` | Rename remote |
| `git remote show origin` | Show remote info |
| `git remote prune origin` | Remove stale remote branches |
| `git fetch origin` | Fetch from remote |
| `git fetch upstream` | Fetch from upstream |
| `git pull upstream main` | Pull from upstream |
| `git push origin main` | Push to origin |
| `git push upstream main` | Push to upstream |
| `git push -u origin main` | Push and set upstream |
| `git push origin --force` | Force push (not recommended) |
| `git push --force-with-lease` | Safe force push |

# ─── GIT WORKFLOW ─────────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `git worktree add ../project-branch branch` | Add worktree |
| `git worktree list` | List worktrees |
| `git worktree remove ../project-branch` | Remove worktree |
| `git submodule add https://github.com/user/submodule.git` | Add submodule |
| `git submodule update --init` | Init submodules |
| `git submodule update --recursive` | Update submodules |
| `git submodule foreach git pull origin main` | Pull in submodules |
| `git bisect start` | Start bisect |
| `git bisect bad` | Mark as bad |
| `git bisect good commit_hash` | Mark as good |
| `git bisect reset` | End bisect |
| `git grep "pattern"` | Search in repo |
| `git grep -n "pattern"` | Show line numbers |
| `git grep "pattern" $(git rev-list --all)` | Search all history |
| `git ls-files` | List tracked files |
| `git ls-tree -r main --name-only` | List files in tree |
| `git cat-file -p commit_hash` | Show object |
| `git rev-parse HEAD` | Get current commit hash |
| `git describe` | Describe commit |
| `git cherry -v` | List commits not merged upstream |

# ─── GIT CONFIGURATION ────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `git config --list` | List config |
| `git config --global user.name "Your Name"` | Set user name |
| `git config --global user.email "email@example.com"` | Set user email |
| `git config --global core.editor "vim"` | Set editor |
| `git config --global color.ui auto` | Enable colors |
| `git config --global alias.co checkout` | Create alias |
| `git config --global alias.br branch` | Branch alias |
| `git config --global alias.st status` | Status alias |
| `git config --global alias.lg "log --oneline --graph --decorate"` | Log alias |
| `git config --global init.defaultBranch main` | Default branch |
| `git config --global core.autocrlf false` | Line endings |
| `git config --global credential.helper cache` | Cache credentials |
| `git config --global credential.helper 'cache --timeout=3600'` | Cache for 1 hour |
| `git config --global core.excludesfile ~/.gitignore_global` | Global ignore |
| `git config --global diff.tool meld` | Diff tool |
| `git config --global merge.tool meld` | Merge tool |
| `git config --global pull.rebase false` | Pull behavior |
| `git config --global rebase.autoStash true` | Auto stash on rebase |

# ─── GITIGNORE ────────────────────────────────────────────────────

| File | Description |
|------|-------------|
| `.gitignore` | Ignore patterns |
| `*.log` | Ignore log files |
| `*.tmp` | Ignore temp files |
| `node_modules/` | Ignore node_modules |
| `vendor/` | Ignore vendor |
| `*.pyc` | Ignore Python cache |
| `.env` | Ignore env files |
| `*.swp` | Ignore vim swap |
| `*.swo` | Ignore vim swap |
| `.idea/` | Ignore IDE |
| `.vscode/` | Ignore VS Code |
| `*.iml` | Ignore IntelliJ |
| `*.class` | Ignore Java class files |
| `*.jar` | Ignore Java JAR |
| `*.war` | Ignore Java WAR |
| `*.ear` | Ignore Java EAR |
| `*.exe` | Ignore Windows executables |
| `*.dll` | Ignore Windows DLL |
| `*.so` | Ignore Linux shared objects |
| `*.dylib` | Ignore Mac libraries |
| `*.DS_Store` | Ignore Mac files |
| `Thumbs.db` | Ignore Windows thumbnails |
| `*.bak` | Ignore backup files |
| `*.orig` | Ignore original files |

# ─── GIT HOOKS ────────────────────────────────────────────────────

| Hook | Description |
|------|-------------|
| `pre-commit` | Before commit |
| `commit-msg` | Before commit message |
| `post-commit` | After commit |
| `pre-rebase` | Before rebase |
| `post-rebase` | After rebase |
| `pre-push` | Before push |
| `post-update` | After update |
| `pre-merge-commit` | Before merge commit |
| `pre-receive` | Before receive (server) |
| `update` | During receive (server) |
| `post-receive` | After receive (server) |
| `post-checkout` | After checkout |

# ================================================================
# 6. DATABASE COMMANDS - COMPLETE
# ================================================================

# ─── MYSQL ────────────────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `mysql -u root -p` | Connect to MySQL |
| `mysql -u root -p -h host` | Connect to remote MySQL |
| `mysql -u root -p -h host -P 3306` | Custom port |
| `mysql -u root -p -h host -D dbname` | Connect to specific DB |
| `mysql -u root -p -e "SHOW DATABASES;"` | Run query from CLI |
| `mysql -u root -p < backup.sql` | Run SQL script |
| `mysql -u root -p -e "SELECT * FROM table" dbname` | Query specific DB |
| `SHOW DATABASES;` | List databases |
| `CREATE DATABASE dbname;` | Create database |
| `CREATE DATABASE dbname CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;` | With charset |
| `DROP DATABASE dbname;` | Drop database |
| `USE dbname;` | Use database |
| `SHOW TABLES;` | List tables |
| `DESCRIBE table_name;` | Describe table |
| `SHOW CREATE TABLE table_name;` | Show create table |
| `SHOW INDEX FROM table_name;` | Show indexes |
| `SELECT * FROM table_name;` | Query table |
| `SELECT * FROM table_name WHERE id=1;` | Filter query |
| `SELECT col1, col2 FROM table_name ORDER BY col1 DESC;` | Order by |
| `SELECT COUNT(*) FROM table_name;` | Count rows |
| `SELECT DISTINCT col FROM table_name;` | Distinct values |
| `INSERT INTO table_name (col1, col2) VALUES ('val1', 'val2');` | Insert row |
| `INSERT INTO table_name (col1, col2) VALUES ('val1', 'val2'), ('val3', 'val4');` | Multiple rows |
| `REPLACE INTO table_name (col1, col2) VALUES ('val1', 'val2');` | Replace row |
| `UPDATE table_name SET col1='val1' WHERE id=1;` | Update row |
| `DELETE FROM table_name WHERE id=1;` | Delete row |
| `TRUNCATE TABLE table_name;` | Delete all rows |
| `ALTER TABLE table_name ADD COLUMN col DATATYPE;` | Add column |
| `ALTER TABLE table_name DROP COLUMN col;` | Drop column |
| `ALTER TABLE table_name RENAME COLUMN old TO new;` | Rename column |
| `ALTER TABLE table_name MODIFY COLUMN col DATATYPE;` | Modify column |
| `CREATE INDEX idx_name ON table_name (col);` | Create index |
| `DROP INDEX idx_name ON table_name;` | Drop index |
| `CREATE TABLE new_table LIKE old_table;` | Copy table structure |
| `INSERT INTO new_table SELECT * FROM old_table;` | Copy data |
| `EXPLAIN SELECT * FROM table_name;` | Query plan |
| `OPTIMIZE TABLE table_name;` | Optimize table |
| `ANALYZE TABLE table_name;` | Analyze table |
| `FLUSH PRIVILEGES;` | Reload privileges |
| `GRANT ALL PRIVILEGES ON dbname.* TO 'user'@'localhost' IDENTIFIED BY 'password';` | Grant privileges |
| `GRANT SELECT, INSERT ON dbname.* TO 'user'@'localhost';` | Specific privileges |
| `REVOKE ALL PRIVILEGES ON dbname.* FROM 'user'@'localhost';` | Revoke privileges |
| `SHOW GRANTS FOR 'user'@'localhost';` | Show grants |
| `CREATE USER 'user'@'localhost' IDENTIFIED BY 'password';` | Create user |
| `ALTER USER 'user'@'localhost' IDENTIFIED BY 'newpassword';` | Change password |
| `DROP USER 'user'@'localhost';` | Drop user |
| `SHOW PROCESSLIST;` | Show processes |
| `KILL process_id;` | Kill process |
| `SHOW STATUS;` | Show status |
| `SHOW VARIABLES;` | Show variables |
| `SHOW VARIABLES LIKE 'character_set%';` | Show charset |
| `SHOW ENGINE INNODB STATUS\G` | InnoDB status |
| `mysqldump -u root -p dbname > backup.sql` | Backup database |
| `mysqldump -u root -p --all-databases > all.sql` | Backup all databases |
| `mysqldump -u root -p --no-data dbname > structure.sql` | Backup structure only |
| `mysqldump -u root -p --no-create-info dbname > data.sql` | Backup data only |
| `mysqldump -u root -p --where="id>100" dbname table > partial.sql` | Backup with condition |
| `mysqldump -u root -p --single-transaction dbname > backup.sql` | Backup without locks |
| `mysql -u root -p dbname < backup.sql` | Restore database |
| `mysql -u root -p -e "source /path/backup.sql"` | Restore (alternative) |
| `mysqlcheck -u root -p --auto-repair --optimize dbname` | Check and optimize |
| `mysqlcheck -u root -p --check dbname` | Check database |
| `mysqlcheck -u root -p --repair dbname` | Repair database |
| `mysqladmin -u root -p status` | MySQL status |
| `mysqladmin -u root -p processlist` | Process list |
| `mysqladmin -u root -p shutdown` | Shutdown MySQL |
| `mysqladmin -u root -p reload` | Reload config |
| `mysqladmin -u root -p flush-hosts` | Flush hosts |
| `mysqladmin -u root -p flush-tables` | Flush tables |
| `mysqladmin -u root -p flush-logs` | Flush logs |

# ─── POSTGRESQL ──────────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `psql -U username -d dbname` | Connect to PostgreSQL |
| `psql -U username -h host -d dbname` | Remote connection |
| `psql -U username -h host -p 5432 -d dbname` | Custom port |
| `psql -U username -d dbname -c "SELECT * FROM table"` | Run query |
| `psql -U username -d dbname -f script.sql` | Run script |
| `\l` | List databases |
| `\c dbname` | Connect to database |
| `\dt` | List tables |
| `\dt schema.*` | Tables in schema |
| `\d table_name` | Describe table |
| `\d+ table_name` | Detailed describe |
| `\di` | List indexes |
| `\dv` | List views |
| `\ds` | List sequences |
| `\df` | List functions |
| `\du` | List users |
| `\dn` | List schemas |
| `\db` | List tablespaces |
| `\x` | Toggle expanded output |
| `\q` | Quit psql |
| `\?` | Help |
| `\h` | SQL command help |
| `\h SELECT` | Help for SELECT |
| `\timing` | Toggle timing |
| `\echo text` | Echo text |
| `\i file.sql` | Include file |
| `\o file.txt` | Output to file |
| `\copy table_name TO '/path/file.csv' CSV HEADER;` | Export CSV |
| `\copy table_name FROM '/path/file.csv' CSV HEADER;` | Import CSV |
| `SELECT * FROM table_name;` | Query table |
| `SELECT * FROM table_name WHERE id=1;` | Filter query |
| `SELECT col1, col2 FROM table_name ORDER BY col1 DESC;` | Order by |
| `SELECT COUNT(*) FROM table_name;` | Count rows |
| `SELECT DISTINCT col FROM table_name;` | Distinct values |
| `INSERT INTO table_name (col1, col2) VALUES ('val1', 'val2');` | Insert row |
| `INSERT INTO table_name (col1, col2) VALUES ('val1', 'val2'), ('val3', 'val4');` | Multiple rows |
| `UPDATE table_name SET col1='val1' WHERE id=1;` | Update row |
| `DELETE FROM table_name WHERE id=1;` | Delete row |
| `TRUNCATE TABLE table_name;` | Delete all rows |
| `ALTER TABLE table_name ADD COLUMN col DATATYPE;` | Add column |
| `ALTER TABLE table_name DROP COLUMN col;` | Drop column |
| `ALTER TABLE table_name RENAME COLUMN old TO new;` | Rename column |
| `ALTER TABLE table_name ALTER COLUMN col TYPE DATATYPE;` | Change column type |
| `CREATE INDEX idx_name ON table_name (col);` | Create index |
| `DROP INDEX idx_name;` | Drop index |
| `CREATE TABLE new_table AS SELECT * FROM old_table;` | Copy table |
| `EXPLAIN SELECT * FROM table_name;` | Query plan |
| `EXPLAIN ANALYZE SELECT * FROM table_name;` | Analyze query |
| `VACUUM table_name;` | Vacuum table |
| `VACUUM ANALYZE table_name;` | Vacuum and analyze |
| `ANALYZE table_name;` | Analyze table |
| `REINDEX INDEX idx_name;` | Reindex index |
| `REINDEX TABLE table_name;` | Reindex table |
| `CREATE USER username WITH PASSWORD 'password';` | Create user |
| `ALTER USER username WITH PASSWORD 'newpassword';` | Change password |
| `DROP USER username;` | Drop user |
| `GRANT ALL PRIVILEGES ON DATABASE dbname TO username;` | Grant privileges |
| `GRANT SELECT ON table_name TO username;` | Specific privileges |
| `REVOKE ALL PRIVILEGES ON DATABASE dbname FROM username;` | Revoke privileges |
| `pg_dump -U username dbname > backup.sql` | Backup database |
| `pg_dump -U username -F c dbname > backup.dump` | Custom format backup |
| `pg_dump -U username -F t dbname > backup.tar` | Tar format backup |
| `pg_dump -U username --schema-only dbname > structure.sql` | Structure only |
| `pg_dump -U username --data-only dbname > data.sql` | Data only |
| `pg_dump -U username -t table_name dbname > backup.sql` | Specific table |
| `pg_dump -U username --exclude-table=table_name dbname > backup.sql` | Exclude table |
| `pg_dumpall -U username > all.sql` | Backup all databases |
| `psql -U username -d dbname < backup.sql` | Restore database |
| `pg_restore -U username -d dbname backup.dump` | Restore custom format |
| `pg_restore -U username -d dbname -t table_name backup.dump` | Specific table |
| `pg_ctl status` | PostgreSQL status |
| `pg_ctl start` | Start PostgreSQL |
| `pg_ctl stop` | Stop PostgreSQL |
| `pg_ctl restart` | Restart PostgreSQL |
| `pg_ctl reload` | Reload config |
| `pg_lsclusters` | List clusters |
| `psql -U username -d dbname -c "SELECT version();"` | Version info |

# ─── MONGODB ──────────────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `mongosh` | Connect to MongoDB (MongoDB 6.0+) |
| `mongosh --host host --port 27017` | Connect with host/port |
| `mongosh -u username -p password` | Connect with authentication |
| `mongosh --authenticationDatabase admin` | Auth database |
| `mongo` | Connect to MongoDB (legacy) |
| `show dbs` | List databases |
| `use dbname` | Use database |
| `show collections` | List collections |
| `show users` | List users |
| `show roles` | List roles |
| `db` | Show current database |
| `db.stats()` | Database stats |
| `db.collection.find()` | Query collection |
| `db.collection.find().pretty()` | Pretty output |
| `db.collection.find({field: "value"})` | Filter query |
| `db.collection.find({field: {$gt: 10}})` | Comparison operators |
| `db.collection.find({}).sort({field: 1})` | Sort ascending |
| `db.collection.find({}).sort({field: -1})` | Sort descending |
| `db.collection.find({}).limit(10)` | Limit results |
| `db.collection.find({}).skip(10)` | Skip results |
| `db.collection.findOne()` | Find one document |
| `db.collection.countDocuments()` | Count documents |
| `db.collection.distinct("field")` | Distinct values |
| `db.collection.insertOne({field: "value"})` | Insert one document |
| `db.collection.insertMany([{field1: "value1"}, {field2: "value2"}])` | Insert many |
| `db.collection.updateOne({_id: id}, {$set: {field: "value"}})` | Update one |
| `db.collection.updateMany({field: "value"}, {$set: {field2: "value2"}})` | Update many |
| `db.collection.replaceOne({_id: id}, {newField: "value"})` | Replace one |
| `db.collection.deleteOne({_id: id})` | Delete one |
| `db.collection.deleteMany({field: "value"})` | Delete many |
| `db.collection.drop()` | Drop collection |
| `db.dropDatabase()` | Drop database |
| `db.collection.createIndex({field: 1})` | Create index |
| `db.collection.createIndex({field: 1}, {unique: true})` | Unique index |
| `db.collection.createIndex({field: "text"})` | Text index |
| `db.collection.getIndexes()` | List indexes |
| `db.collection.dropIndex("index_name")` | Drop index |
| `db.collection.dropIndexes()` | Drop all indexes |
| `db.collection.aggregate([ { $match: { field: "value" } }, { $group: { _id: "$field2", count: { $sum: 1 } } } ])` | Aggregate |
| `db.collection.aggregate([ { $lookup: { from: "other", localField: "field", foreignField: "field", as: "result" } } ])` | Lookup (join) |
| `db.collection.aggregate([ { $unwind: "$array_field" } ])` | Unwind array |
| `db.collection.aggregate([ { $project: { field: 1, computed: { $add: ["$field", 10] } } } ])` | Project |
| `db.collection.aggregate([ { $sort: { field: -1 } }, { $limit: 10 } ])` | Sort and limit |
| `db.createUser({user: "username", pwd: "password", roles: [{role: "readWrite", db: "dbname"}]})` | Create user |
| `db.createUser({user: "username", pwd: "password", roles: [{role: "clusterAdmin", db: "admin"}]})` | Admin user |
| `db.dropUser("username")` | Drop user |
| `db.grantRolesToUser("username", [{role: "read", db: "dbname"}])` | Grant role |
| `db.revokeRolesFromUser("username", [{role: "read", db: "dbname"}])` | Revoke role |
| `db.getUsers()` | List users |
| `db.version()` | MongoDB version |
| `db.serverStatus()` | Server status |
| `db.currentOp()` | Current operations |
| `db.killOp(opid)` | Kill operation |
| `mongodump --db dbname --out backup` | Backup database |
| `mongodump --db dbname --collection collection --out backup` | Backup collection |
| `mongodump --uri "mongodb://user:pass@host:port/db" --out backup` | Backup with URI |
| `mongorestore --db dbname backup/dbname` | Restore database |
| `mongorestore --db dbname --collection collection backup/dbname/collection.bson` | Restore collection |
| `mongorestore --uri "mongodb://user:pass@host:port/db" backup/dbname` | Restore with URI |
| `mongostat` | Database stats |
| `mongotop` | Collection usage stats |
| `mongoexport --db dbname --collection collection --out data.json` | Export JSON |
| `mongoexport --db dbname --collection collection --out data.csv --type=csv --fields=field1,field2` | Export CSV |
| `mongoimport --db dbname --collection collection --file data.json` | Import JSON |
| `mongoimport --db dbname --collection collection --type=csv --headerline --file data.csv` | Import CSV |

# ─── REDIS ────────────────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `redis-cli` | Connect to Redis |
| `redis-cli -h host -p 6379` | Connect with host/port |
| `redis-cli -a password` | Connect with password |
| `redis-cli ping` | Ping Redis |
| `redis-cli info` | Server info |
| `redis-cli monitor` | Monitor commands |
| `redis-cli --stat` | Statistics |
| `redis-cli --latency` | Latency |
| `redis-cli --intrinsic-latency 100` | Intrinsic latency |
| `redis-cli --bigkeys` | Find big keys |
| `redis-cli --scan` | Scan keys |
| `redis-cli --scan --pattern "user:*"` | Pattern scan |
| `SET key "value"` | Set string |
| `GET key` | Get string |
| `DEL key` | Delete key |
| `EXISTS key` | Check key exists |
| `EXPIRE key 60` | Set expiration |
| `TTL key` | Get TTL |
| `PERSIST key` | Remove expiration |
| `TYPE key` | Get key type |
| `KEYS *` | List all keys |
| `KEYS pattern*` | Pattern keys |
| `SCAN 0` | Scan keys (cursor) |
| `SCAN 0 MATCH pattern*` | Pattern scan |
| `HSET hash field value` | Set hash field |
| `HGET hash field` | Get hash field |
| `HGETALL hash` | Get all hash fields |
| `HDEL hash field` | Delete hash field |
| `HLEN hash` | Hash length |
| `HEXISTS hash field` | Check field exists |
| `HKEYS hash` | Get hash keys |
| `HVALS hash` | Get hash values |
| `LPUSH list value` | Push to list (left) |
| `RPUSH list value` | Push to list (right) |
| `LPOP list` | Pop from list (left) |
| `RPOP list` | Pop from list (right) |
| `LRANGE list 0 -1` | Get all list elements |
| `LLEN list` | List length |
| `LINDEX list index` | Get element at index |
| `LREM list count value` | Remove elements |
| `SADD set value` | Add to set |
| `SMEMBERS set` | Get set members |
| `SREM set value` | Remove from set |
| `SISMEMBER set value` | Check membership |
| `SCARD set` | Set cardinality |
| `SUNION set1 set2` | Set union |
| `SINTER set1 set2` | Set intersection |
| `SDIFF set1 set2` | Set difference |
| `ZADD zset score member` | Add to sorted set |
| `ZRANGE zset 0 -1` | Get sorted set |
| `ZREVRANGE zset 0 -1` | Reverse sorted set |
| `ZREM zset member` | Remove from sorted set |
| `ZCARD zset` | Sorted set cardinality |
| `ZSCORE zset member` | Get score |
| `ZRANK zset member` | Get rank |
| `FLUSHDB` | Clear current database |
| `FLUSHALL` | Clear all databases |
| `SELECT dbindex` | Select database |
| `DBSIZE` | Database size |
| `INFO` | Server info |
| `INFO memory` | Memory info |
| `INFO stats` | Stats info |
| `INFO clients` | Client info |
| `CONFIG GET *` | Get config |
| `CONFIG SET parameter value` | Set config |
| `CONFIG REWRITE` | Persist config |
| `SAVE` | Save snapshot |
| `BGSAVE` | Background save |
| `LASTSAVE` | Last save time |
| `SHUTDOWN` | Shutdown Redis |
| `SHUTDOWN SAVE` | Save and shutdown |
| `SHUTDOWN NOSAVE` | Shutdown without save |
| `AUTH password` | Authenticate |
| `PING` | Ping |
| `ECHO message` | Echo |
| `COMMAND` | List commands |
| `COMMAND INFO command` | Command info |

# ================================================================
# 7. GIT COMMANDS - ADVANCED
# ================================================================

# ─── GIT REBASE ADVANCED ──────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `git rebase -i HEAD~10` | Interactive rebase last 10 commits |
| `git rebase -i --root` | Rebase from root |
| `git rebase --onto newbase oldbase branch` | Advanced rebase |
| `git rebase --continue` | Continue after resolving |
| `git rebase --abort` | Abort rebase |
| `git rebase --skip` | Skip current commit |
| `git rebase --update-refs` | Update references |
| `git rebase --autosquash` | Autosquash fixup commits |
| `git rebase --committer-date-is-author-date` | Keep dates |

# ─── GIT CHERRY-PICK ADVANCED ────────────────────────────────────

| Command | Description |
|---------|-------------|
| `git cherry-pick commit1 commit2 commit3` | Multiple commits |
| `git cherry-pick commit1..commit2` | Range of commits |
| `git cherry-pick --no-commit commit` | Cherry-pick without commit |
| `git cherry-pick --signoff commit` | Signed-off-by |
| `git cherry-pick --strategy=recursive -X theirs commit` | Conflict resolution |
| `git cherry-pick --continue` | Continue after conflict |
| `git cherry-pick --abort` | Abort cherry-pick |

# ─── GIT BISECT ───────────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `git bisect start` | Start bisect |
| `git bisect bad` | Mark current as bad |
| `git bisect good commit_hash` | Mark commit as good |
| `git bisect bad HEAD~10` | Mark older as bad |
| `git bisect reset` | End bisect |
| `git bisect log` | Show bisect log |
| `git bisect run script.sh` | Automate bisect |

# ─── GIT FILTER-BRANCH ───────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `git filter-branch --tree-filter 'rm -f file.txt' HEAD` | Remove file from history |
| `git filter-branch --commit-filter 'git commit-tree "$@"' HEAD` | Filter commits |
| `git filter-branch --env-filter 'export GIT_AUTHOR_EMAIL=new@email.com' HEAD` | Change email |
| `git filter-repo --path file.txt --invert-paths` | Modern filter-repo |
| `git filter-repo --email-callback 'return email.replace("@old", "@new")'` | Rename email |

# ─── GIT SUBMODULE ADVANCED ──────────────────────────────────────

| Command | Description |
|---------|-------------|
| `git submodule add https://github.com/user/submodule.git path` | Add submodule |
| `git submodule update --init --recursive` | Init and update |
| `git submodule update --remote` | Update submodule to remote |
| `git submodule sync` | Sync submodule URLs |
| `git submodule foreach 'git checkout main'` | Command on all submodules |
| `git submodule deinit -f submodule` | Deinit submodule |
| `git submodule summary` | Summary of submodule changes |
| `git submodule status` | Submodule status |

# ─── GIT WORKTREE ─────────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `git worktree add ../project-branch branch` | Add worktree |
| `git worktree add ../project-branch -b new-branch` | Create branch |
| `git worktree list` | List worktrees |
| `git worktree remove ../project-branch` | Remove worktree |
| `git worktree lock ../project-branch` | Lock worktree |
| `git worktree unlock ../project-branch` | Unlock worktree |
| `git worktree prune` | Prune worktrees |

# ─── GIT REBASE -I COMMANDS ──────────────────────────────────────

| Command | Description |
|---------|-------------|
| `pick` | Use commit |
| `reword` | Change commit message |
| `edit` | Stop and edit |
| `squash` | Merge with previous |
| `fixup` | Merge with previous (discard message) |
| `drop` | Remove commit |
| `exec` | Run command |

# ================================================================
# 8. DOCKER ADVANCED COMMANDS
# ================================================================

# ─── DOCKER BUILD OPTIONS ────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `docker build --no-cache -t image .` | Build without cache |
| `docker build --pull -t image .` | Pull base image |
| `docker build --build-arg VAR=value -t image .` | Build arguments |
| `docker build -t image -f Dockerfile.prod .` | Custom Dockerfile |
| `docker build --target stage -t image .` | Multi-stage target |
| `docker build --squash -t image .` | Squash layers |
| `docker build --compress -t image .` | Compress build context |
| `docker build --rm -t image .` | Remove intermediate containers |
| `docker build --force-rm -t image .` | Force remove |

# ─── DOCKER RUN OPTIONS ──────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `docker run -d --restart=always nginx` | Auto-restart |
| `docker run -d --restart=unless-stopped nginx` | Restart unless stopped |
| `docker run -d --restart=on-failure:5 nginx` | Restart on failure |
| `docker run -d --health-cmd="curl -f http://localhost/" --health-interval=30s nginx` | Healthcheck |
| `docker run -d --security-opt=no-new-privileges nginx` | Security options |
| `docker run -d --cap-add=NET_ADMIN nginx` | Add capabilities |
| `docker run -d --cap-drop=ALL nginx` | Drop capabilities |
| `docker run -d --read-only nginx` | Read-only rootfs |
| `docker run -d --tmpfs=/tmp nginx` | Tmpfs mount |
| `docker run -d --shm-size=256m nginx` | Shared memory size |
| `docker run -d --ulimit nofile=65536:65536 nginx` | ulimit settings |
| `docker run -d --entrypoint /bin/bash nginx` | Override entrypoint |
| `docker run -d --user 1000:1000 nginx` | Run as user |
| `docker run -d --group-add=1000 nginx` | Additional groups |

# ─── DOCKER COMPOSE ADVANCED ─────────────────────────────────────

| Command | Description |
|---------|-------------|
| `docker-compose up -d --scale web=3` | Scale services |
| `docker-compose up -d --remove-orphans` | Remove orphan containers |
| `docker-compose down -v --remove-orphans` | Down with volumes |
| `docker-compose config --services` | List services |
| `docker-compose config --volumes` | List volumes |
| `docker-compose config --images` | List images |
| `docker-compose config --hash-service` | Service hash |
| `docker-compose events --json` | Events in JSON |
| `docker-compose exec -T service command` | Disable TTY |
| `docker-compose run --rm service command` | Run and remove |
| `docker-compose run --service-ports service` | Use service ports |
| `docker-compose up --abort-on-container-exit` | Abort on exit |
| `docker-compose up --exit-code-from service` | Exit code from service |
| `docker-compose logs --no-color` | No color output |
| `docker-compose port service 80 --protocol=udp` | Protocol |

# ─── DOCKERFILE BEST PRACTICES ──────────────────────────────────

| Instruction | Description |
|-------------|-------------|
| `FROM base:latest` | Base image |
| `ARG VERSION=latest` | Build arguments |
| `ENV VAR=value` | Environment variables |
| `WORKDIR /app` | Working directory |
| `RUN apt-get update && apt-get install -y package` | Run commands |
| `COPY . .` | Copy files |
| `ADD archive.tar.gz /` | Add files (with extraction) |
| `USER 1000:1000` | Set user |
| `EXPOSE 80` | Expose port |
| `CMD ["cmd", "arg"]` | Default command |
| `ENTRYPOINT ["cmd"]` | Entrypoint |
| `VOLUME ["/data"]` | Volume declaration |
| `HEALTHCHECK --interval=30s CMD curl -f http://localhost/` | Healthcheck |
| `LABEL version="1.0"` | Labels |

# ─── DOCKER SECURITY ─────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `docker scan image` | Scan for vulnerabilities |
| `docker scan --file Dockerfile image` | Scan with Dockerfile |
| `docker trust inspect image` | Trust inspection |
| `docker trust sign image` | Sign image |
| `docker trust revoke image` | Revoke signature |
| `docker secret create secret value` | Create secret |
| `docker secret ls` | List secrets |
| `docker secret inspect secret` | Inspect secret |
| `docker secret rm secret` | Remove secret |
| `docker config create config value` | Create config |
| `docker config ls` | List configs |
| `docker config inspect config` | Inspect config |
| `docker config rm config` | Remove config |

# ================================================================
# 9. KUBERNETES ADVANCED COMMANDS
# ================================================================

# ─── KUBECTL CONTEXT ──────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `kubectl config get-contexts` | List contexts |
| `kubectl config current-context` | Current context |
| `kubectl config use-context context` | Switch context |
| `kubectl config set-context context --namespace=namespace` | Set namespace |
| `kubectl config set-context context --cluster=cluster --user=user` | Set cluster/user |
| `kubectl config set-cluster cluster --server=server` | Set cluster |
| `kubectl config set-credentials user --token=token` | Set credentials |
| `kubectl config view` | View config |
| `kubectl config view --minify` | Minified view |
| `kubectl config view -o json` | JSON output |

# ─── KUBECTL NAMESPACE ───────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `kubectl get ns` | List namespaces |
| `kubectl create ns namespace` | Create namespace |
| `kubectl delete ns namespace` | Delete namespace |
| `kubectl get pods -n namespace` | Pods in namespace |
| `kubectl get all -n namespace` | All resources in namespace |
| `kubectl delete all --all -n namespace` | Delete all in namespace |

# ─── KUBECTL LABELS AND SELECTORS ───────────────────────────────

| Command | Description |
|---------|-------------|
| `kubectl label pod pod_name key=value` | Add label |
| `kubectl label pod pod_name key-` | Remove label |
| `kubectl label pod pod_name key=value --overwrite` | Overwrite label |
| `kubectl get pods -l app=myapp` | Label selector |
| `kubectl get pods -l app=myapp,env=prod` | Multiple labels |
| `kubectl get pods -l 'app in (myapp,yourapp)'` | Set selector |
| `kubectl get pods -l '!app'` | App label absent |
| `kubectl annotate pod pod_name annotation=value` | Add annotation |
| `kubectl annotate pod pod_name annotation-` | Remove annotation |

# ─── KUBECTL TROUBLESHOOTING ─────────────────────────────────────

| Command | Description |
|---------|-------------|
| `kubectl describe pod pod_name` | Describe pod |
| `kubectl describe node node_name` | Describe node |
| `kubectl logs pod_name -p` | Previous container logs |
| `kubectl logs pod_name --tail=100` | Last 100 lines |
| `kubectl logs pod_name --since=1h` | Since time |
| `kubectl logs pod_name --timestamps` | Add timestamps |
| `kubectl logs pod_name --prefix` | Add pod prefix |
| `kubectl logs -l app=myapp` | Logs by label |
| `kubectl exec -it pod_name -- /bin/bash` | Execute in pod |
| `kubectl exec -it pod_name -- sh` | With sh |
| `kubectl exec -it pod_name -c container_name -- /bin/bash` | Specific container |
| `kubectl exec pod_name -- command` | Run command |
| `kubectl cp pod_name:/path/file /local/path` | Copy from pod |
| `kubectl cp /local/path pod_name:/path/file` | Copy to pod |
| `kubectl port-forward pod_name 8080:80` | Port forward |
| `kubectl port-forward svc/service_name 8080:80` | Service port forward |
| `kubectl port-forward deployment/deployment_name 8080:80` | Deployment port forward |
| `kubectl attach pod_name` | Attach to pod |
| `kubectl run debug-pod --image=busybox -it --rm -- /bin/sh` | Debug pod |

# ─── KUBECTL ROLLOUT ─────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `kubectl rollout status deployment/deployment_name` | Status |
| `kubectl rollout history deployment/deployment_name` | History |
| `kubectl rollout history deployment/deployment_name --revision=2` | Specific revision |
| `kubectl rollout undo deployment/deployment_name` | Rollback |
| `kubectl rollout undo deployment/deployment_name --to-revision=2` | Specific revision |
| `kubectl rollout restart deployment/deployment_name` | Restart |
| `kubectl rollout pause deployment/deployment_name` | Pause |
| `kubectl rollout resume deployment/deployment_name` | Resume |

# ─── KUBECTL PATCH ───────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `kubectl patch deployment deployment_name -p '{"spec":{"replicas":3}}'` | Patch JSON |
| `kubectl patch service service_name -p '{"spec":{"type":"LoadBalancer"}}'` | Patch service |
| `kubectl patch deployment deployment_name --type='json' -p='[{"op": "replace", "path": "/spec/replicas", "value": 3}]'` | JSON patch |
| `kubectl patch deployment deployment_name --type='strategic' -p='{"spec":{"template":{"spec":{"containers":[{"name":"container","image":"new-image"}]}}}}'` | Strategic merge |
| `kubectl patch deployment deployment_name --patch-file patch.yaml` | Patch from file |

# ─── KUBECTL KUSTOMIZE ───────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `kubectl kustomize ./kustomize` | Build kustomization |
| `kubectl apply -k ./kustomize` | Apply kustomization |
| `kubectl diff -k ./kustomize` | Diff kustomization |
| `kubectl delete -k ./kustomize` | Delete kustomization |

# ─── HELM COMMANDS ────────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `helm version` | Helm version |
| `helm repo add stable https://charts.helm.sh/stable` | Add repo |
| `helm repo update` | Update repos |
| `helm repo list` | List repos |
| `helm search repo keyword` | Search repos |
| `helm search hub keyword` | Search hub |
| `helm install release-name chart` | Install chart |
| `helm install release-name chart --namespace namespace` | With namespace |
| `helm install release-name chart --values values.yaml` | With values file |
| `helm install release-name chart --set key=value` | Set value |
| `helm upgrade release-name chart` | Upgrade release |
| `helm upgrade release-name chart --values new-values.yaml` | With new values |
| `helm upgrade release-name chart --set key=newvalue` | Set new value |
| `helm rollback release-name revision` | Rollback |
| `helm history release-name` | History |
| `helm list` | List releases |
| `helm list --all` | All releases |
| `helm list --namespace namespace` | Specific namespace |
| `helm uninstall release-name` | Uninstall |
| `helm status release-name` | Status |
| `helm get values release-name` | Get values |
| `helm get manifest release-name` | Get manifest |
| `helm get notes release-name` | Get notes |
| `helm template chart` | Render template |
| `helm lint chart` | Lint chart |
| `helm package chart` | Package chart |
| `helm push chart.tgz repo` | Push chart |
| `helm dependency build chart` | Build dependencies |
| `helm dependency update chart` | Update dependencies |

# ================================================================
# 10. TERRAFORM COMMANDS - COMPLETE
# ================================================================

| Command | Description |
|---------|-------------|
| `terraform init` | Initialize |
| `terraform init -upgrade` | Upgrade modules |
| `terraform init -reconfigure` | Reconfigure backend |
| `terraform plan` | Plan changes |
| `terraform plan -out plan.tfplan` | Save plan |
| `terraform plan -var="key=value"` | With variables |
| `terraform plan -var-file="prod.tfvars"` | Var file |
| `terraform apply` | Apply changes |
| `terraform apply -auto-approve` | Apply without confirmation |
| `terraform apply plan.tfplan` | Apply saved plan |
| `terraform destroy` | Destroy resources |
| `terraform destroy -auto-approve` | Destroy without confirmation |
| `terraform validate` | Validate config |
| `terraform fmt` | Format config |
| `terraform fmt -recursive` | Recursive format |
| `terraform fmt -check` | Check format |
| `terraform state list` | List state resources |
| `terraform state show resource` | Show resource state |
| `terraform state pull` | Pull state |
| `terraform state push` | Push state |
| `terraform state mv source destination` | Move resource |
| `terraform state rm resource` | Remove resource |
| `terraform state replace-provider` | Replace provider |
| `terraform output` | Show outputs |
| `terraform output -json` | JSON output |
| `terraform output -raw output_name` | Raw output |
| `terraform import resource id` | Import resource |
| `terraform import -var-file=prod.tfvars resource id` | With vars |
| `terraform graph` | Dependency graph |
| `terraform graph -draw-cycles` | Show cycles |
| `terraform providers` | Provider info |
| `terraform providers schema` | Provider schema |
| `terraform version` | Version |
| `terraform console` | Interactive console |
| `terraform force-unlock lock-id` | Force unlock |
| `terraform refresh` | Refresh state |
| `terraform taint resource` | Taint resource |
| `terraform untaint resource` | Untaint resource |
| `terraform workspace list` | List workspaces |
| `terraform workspace new workspace` | Create workspace |
| `terraform workspace select workspace` | Select workspace |
| `terraform workspace delete workspace` | Delete workspace |
| `terraform apply -var-file="test.tfvars" -state=terraform-test.tfstate` | Custom state file |
| `terraform plan -out=plan.tfplan -var-file="prod.tfvars" -state=terraform-prod.tfstate` | Complete plan |

# ================================================================
# 11. ANSIBLE COMMANDS - COMPLETE
# ================================================================

| Command | Description |
|---------|-------------|
| `ansible --version` | Ansible version |
| `ansible all -m ping` | Ping all hosts |
| `ansible hostname -m ping` | Ping specific host |
| `ansible all -m ping -i inventory` | Custom inventory |
| `ansible all -m ping -u username` | With user |
| `ansible all -m ping -k` | Ask for password |
| `ansible all -m ping -K` | Ask for sudo password |
| `ansible-playbook playbook.yml` | Run playbook |
| `ansible-playbook playbook.yml -i inventory` | Custom inventory |
| `ansible-playbook playbook.yml -u username` | With user |
| `ansible-playbook playbook.yml -k -K` | Ask passwords |
| `ansible-playbook playbook.yml --check` | Dry run |
| `ansible-playbook playbook.yml --diff` | Show changes |
| `ansible-playbook playbook.yml --syntax-check` | Syntax check |
| `ansible-playbook playbook.yml --extra-vars "key=value"` | Extra vars |
| `ansible-playbook playbook.yml -e "@vars.yaml"` | Vars file |
| `ansible-playbook playbook.yml -vvv` | Verbose output |
| `ansible-playbook playbook.yml --step` | Step mode |
| `ansible-playbook playbook.yml --limit hostname` | Limit hosts |
| `ansible-inventory --list` | List inventory |
| `ansible-inventory --host hostname` | Host info |
| `ansible-inventory -i inventory --graph` | Inventory graph |
| `ansible-doc -l` | List modules |
| `ansible-doc module_name` | Module documentation |
| `ansible-doc -s module_name` | Short module doc |
| `ansible-galaxy init role_name` | Create role |
| `ansible-galaxy install role_name` | Install role |
| `ansible-galaxy remove role_name` | Remove role |
| `ansible-galaxy list` | List roles |
| `ansible-galaxy search keyword` | Search roles |
| `ansible-galaxy install -r requirements.yml` | Install from file |
| `ansible-config list` | List config options |
| `ansible-config view` | View config |
| `ansible-config dump` | Dump config |
| `ansible-vault encrypt file.yml` | Encrypt file |
| `ansible-vault decrypt file.yml` | Decrypt file |
| `ansible-vault view file.yml` | View encrypted file |
| `ansible-vault edit file.yml` | Edit encrypted file |
| `ansible-vault rekey file.yml` | Change password |
| `ansible-vault create file.yml` | Create encrypted file |
| `ansible-console` | Interactive console |
| `ansible-console -i inventory` | With inventory |
| `ansible-connection` | Connection info |

# ================================================================
# 12. PERFORMANCE TUNING COMMANDS
# ================================================================

# ─── LINUX PERFORMANCE ───────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `sysctl -a \| grep vm` | VM parameters |
| `sysctl -w vm.swappiness=10` | Set swappiness |
| `sysctl -w vm.vfs_cache_pressure=50` | Cache pressure |
| `sysctl -w vm.dirty_ratio=20` | Dirty ratio |
| `sysctl -w vm.dirty_background_ratio=10` | Dirty background |
| `sysctl -w vm.dirty_expire_centisecs=3000` | Dirty expire |
| `sysctl -w kernel.numa_balancing=0` | NUMA balancing |
| `echo 3 > /proc/sys/vm/drop_caches` | Clear caches |
| `echo 1 > /proc/sys/vm/drop_caches` | Clear pagecache |
| `echo 2 > /proc/sys/vm/drop_caches` | Clear dentries/inodes |
| `sysctl -w net.ipv4.tcp_tw_reuse=1` | Reuse TIME_WAIT |
| `sysctl -w net.ipv4.tcp_tw_recycle=1` | Recycle TIME_WAIT |
| `sysctl -w net.ipv4.tcp_fin_timeout=30` | FIN timeout |
| `sysctl -w net.ipv4.tcp_keepalive_time=7200` | Keepalive time |
| `sysctl -w net.ipv4.tcp_keepalive_probes=9` | Keepalive probes |
| `sysctl -w net.ipv4.tcp_keepalive_intvl=75` | Keepalive interval |
| `sysctl -w net.core.rmem_max=16777216` | Receive buffer |
| `sysctl -w net.core.wmem_max=16777216` | Send buffer |
| `sysctl -w net.ipv4.tcp_rmem='4096 87380 16777216'` | TCP read buffer |
| `sysctl -w net.ipv4.tcp_wmem='4096 65536 16777216'` | TCP write buffer |
| `sysctl -w net.core.somaxconn=65535` | Listen backlog |
| `sysctl -w net.ipv4.ip_local_port_range='1024 65000'` | Port range |
| `sysctl -w fs.file-max=2097152` | File max |
| `sysctl -w fs.nr_open=1048576` | NR open |
| `ulimit -n 65536` | Increase file descriptors |
| `ulimit -u unlimited` | Unlimited processes |
| `ulimit -c unlimited` | Unlimited core dump |
| `ulimit -s unlimited` | Unlimited stack |

# ─── NETWORK PERFORMANCE ─────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `ethtool -k eth0` | Offloading info |
| `ethtool -K eth0 tx off rx off` | Disable offloading |
| `ethtool -K eth0 tx on rx on` | Enable offloading |
| `ethtool -G eth0 rx 4096 tx 4096` | Ring buffer size |
| `ethtool -l eth0` | Channel info |
| `ethtool -L eth0 combined 4` | Set channels |
| `ethtool -S eth0` | Statistics |
| `ethtool -p eth0 10` | Blink LED |
| `ethtool -i eth0` | Driver info |
| `ethtool -m eth0` | Module info |
| `tc qdisc show` | Traffic control |
| `tc qdisc add dev eth0 root handle 1: htb default 30` | HTB scheduler |
| `tc class add dev eth0 parent 1: classid 1:1 htb rate 100mbit` | Rate limit |
| `tc filter add dev eth0 parent 1: protocol ip u32 match ip dst 192.168.1.0/24 flowid 1:1` | Filter |
| `tc qdisc del dev eth0 root` | Remove scheduler |
| `tuned-adm list` | Tuning profiles |
| `tuned-adm active` | Active profile |
| `tuned-adm profile profile` | Set profile |
| `tuned-adm recommend` | Recommended profile |
| `tuned-adm verify` | Verify config |

# ─── STORAGE PERFORMANCE ─────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `blockdev --setra 8192 /dev/sda` | Read-ahead |
| `blockdev --getra /dev/sda` | Get read-ahead |
| `blockdev --setra 0 /dev/sda` | Disable read-ahead |
| `echo deadline > /sys/block/sda/queue/scheduler` | Set I/O scheduler |
| `echo noop > /sys/block/sda/queue/scheduler` | Noop scheduler |
| `echo cfq > /sys/block/sda/queue/scheduler` | CFQ scheduler |
| `echo mq-deadline > /sys/block/sda/queue/scheduler` | MQ deadline |
| `echo 512 > /sys/block/sda/queue/nr_requests` | Requests |
| `echo 0 > /sys/block/sda/queue/add_random` | Disable random |
| `echo 1 > /sys/block/sda/queue/rq_affinity` | Request affinity |
| `echo 1 > /sys/block/sda/queue/nomerges` | Disable merges |
| `echo 2 > /sys/block/sda/queue/nomerges` | Aggressive merges |
| `hdparm -Tt /dev/sda` | Disk speed test |
| `hdparm -I /dev/sda` | Disk info |
| `hdparm -c1 /dev/sda` | Enable 32-bit I/O |
| `hdparm -m16 /dev/sda` | Multi-sector I/O |
| `hdparm -u1 /dev/sda` | Unmask IRQ |
| `fio --randrepeat=1 --ioengine=libaio --direct=1 --gtod_reduce=1 --name=test --bs=4k --iodepth=64 --size=1G --readwrite=randrw --rwmixread=75` | Disk benchmark |

# ─── MYSQL PERFORMANCE ───────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `SHOW STATUS LIKE 'Queries';` | Query count |
| `SHOW STATUS LIKE 'Slow_queries';` | Slow queries |
| `SHOW VARIABLES LIKE 'slow_query_log';` | Slow log status |
| `SET GLOBAL slow_query_log = 'ON';` | Enable slow log |
| `SET GLOBAL long_query_time = 2;` | Set slow threshold |
| `SHOW STATUS LIKE 'Innodb_rows_read';` | InnoDB reads |
| `SHOW ENGINE INNODB STATUS\G` | InnoDB status |
| `SHOW PROCESSLIST;` | Current queries |
| `SHOW FULL PROCESSLIST;` | Full processlist |
| `EXPLAIN SELECT * FROM table;` | Query plan |
| `ANALYZE TABLE table;` | Analyze table |
| `OPTIMIZE TABLE table;` | Optimize table |
| `SHOW INDEX FROM table;` | Show indexes |
| `CREATE INDEX idx ON table (col);` | Create index |
| `DROP INDEX idx ON table;` | Drop index |
| `SET profiling = 1;` | Enable profiling |
| `SHOW PROFILES;` | Show profiles |
| `SHOW PROFILE FOR QUERY 1;` | Profile details |
| `FLUSH LOGS;` | Flush logs |
| `FLUSH STATUS;` | Flush status |

# ================================================================
# 13. TROUBLESHOOTING MASTERY
# ================================================================

# ─── SYSTEM TROUBLESHOOTING ──────────────────────────────────────

| Command | Description |
|---------|-------------|
| `dmesg -T \| tail -50` | Recent kernel messages |
| `dmesg -T \| grep -i error` | Kernel errors |
| `dmesg -T \| grep -i fail` | Kernel failures |
| `journalctl -xe` | System logs with details |
| `journalctl -b -1` | Previous boot logs |
| `journalctl -p err` | Error level logs |
| `journalctl -p err -b` | Errors from current boot |
| `journalctl -u service -p err` | Service errors |
| `journalctl -f -u service` | Follow service logs |
| `systemctl list-units --failed` | Failed units |
| `systemctl status unit` | Unit status |
| `systemctl is-active service` | Check if active |
| `systemctl is-enabled service` | Check if enabled |
| `systemctl is-failed service` | Check if failed |
| `systemd-analyze blame` | Boot time by service |
| `systemd-analyze critical-chain` | Critical chain |
| `systemd-analyze plot > boot.svg` | Boot analysis |

# ─── NETWORK TROUBLESHOOTING ─────────────────────────────────────

| Command | Description |
|---------|-------------|
| `ping -c 10 -i 0.5 host` | Detailed ping test |
| `ping -s 1024 host` | Large packet ping |
| `ping -M do -s 1472 host` | MTU test |
| `traceroute -n host` | Trace without DNS |
| `traceroute -m 30 host` | Max hops |
| `mtr -r -c 10 host` | Report mode |
| `mtr -r -c 10 -n host` | No DNS |
| `dig +trace host` | Trace DNS resolution |
| `dig +nslookup host` | DNS lookup |
| `dig +tcp host` | TCP DNS |
| `nslookup -debug host` | Debug mode |
| `whois domain.com` | Domain info |
| `curl -v https://host` | Verbose HTTP request |
| `curl -w "@format" -o /dev/null -s https://host` | HTTP timing |
| `curl --max-time 10 -I https://host` | Timeout headers |
| `openssl s_client -connect host:443 -servername host` | SSL/TLS handshake |
| `openssl s_client -connect host:443 -tls1_2` | TLS 1.2 |
| `openssl s_client -showcerts` | Show certificates |
| `openssl x509 -in cert.pem -text -noout` | Certificate details |
| `openssl verify -CAfile ca.pem cert.pem` | Verify certificate |
| `ss -tulpn -i` | Socket info |
| `ss -tup -o state established` | Established connections |
| `ss -tup -i state time-wait` | TIME_WAIT connections |
| `netstat -i` | Interface stats |
| `netstat -s` | Protocol stats |
| `netstat -rn` | Routing table |
| `ip -s link` | Interface stats |
| `ip -s -s link` | Detailed stats |
| `ip route show cache` | Routing cache |
| `ip neigh show` | ARP table |
| `arp -a -n` | ARP with numeric |
| `tcpdump -i any -n -c 100` | Capture 100 packets |
| `tcpdump -i any -n port 80` | HTTP traffic |
| `tcpdump -i any -n not port 22` | Exclude SSH |
| `tcpdump -i any -n 'tcp[tcpflags] & (tcp-syn) != 0'` | SYN packets |
| `tcpdump -i any -n 'udp port 53'` | DNS traffic |
| `tcpdump -i any -n 'ip src 192.168.1.100'` | Source IP |
| `tcpdump -i any -n 'ip dst 192.168.1.100'` | Dest IP |
| `tcpdump -i any -n -A -s 0 port 80` | Full HTTP payload |
| `tcpdump -i any -n -w capture.pcap` | Save capture |
| `tcpdump -r capture.pcap -n -A` | Read capture |
| `tcpdump -r capture.pcap -n 'tcp port 80'` | Filter capture |
| `nmap -sV -A host` | Service detection |
| `nmap -p- -T4 host` | Fast all ports |
| `nmap -sS -sV -O host` | SYN scan with OS |
| `nmap -sn 192.168.1.0/24` | Ping sweep |
| `nmap -p 80,443 --script http-headers host` | HTTP headers |

# ─── APPLICATION TROUBLESHOOTING ────────────────────────────────

| Command | Description |
|---------|-------------|
| `tail -f /var/log/application.log` | Follow app logs |
| `tail -f /var/log/application.log \| grep -i error` | Filter errors |
| `grep "ERROR" /var/log/application.log` | Find errors |
| `grep "ERROR" -A 5 -B 5 /var/log/application.log` | Context |
| `grep "ERROR" -c /var/log/application.log` | Count errors |
| `netstat -ano \| grep PORT` | Process on port |
| `ss -tulpn \| grep PORT` | Socket on port |
| `lsof -i :PORT` | Process on port |
| `fuser -n tcp PORT` | Process on port |
| `pgrep -f "process_name"` | Find process by name |
| `ps aux \| grep process_name` | Process details |
| `ps -ef \| grep process_name` | Full details |
| `pstree -p PID` | Process tree |
| `strace -p PID -e trace=network` | Network syscalls |
| `strace -p PID -e trace=file` | File syscalls |
| `strace -p PID -e trace=process` | Process syscalls |
| `strace -p PID -e trace=signal` | Signal tracing |
| `strace -p PID -c` | Call summary |
| `ltrace -p PID` | Library calls |
| `lsof -p PID` | Open files |
| `lsof -p PID -i` | Network connections |
| `cat /proc/PID/status` | Process status |
| `cat /proc/PID/environ \| tr '\0' '\n'` | Environment |
| `cat /proc/PID/limits` | Process limits |
| `cat /proc/PID/cmdline \| tr '\0' ' '` | Command line |
| `cat /proc/PID/fd/*` | Open file descriptors |
| `ls -l /proc/PID/fd/` | List file descriptors |

# ─── MEMORY TROUBLESHOOTING ─────────────────────────────────────

| Command | Description |
|---------|-------------|
| `free -h` | Memory usage |
| `free -m` | Memory in MB |
| `cat /proc/meminfo` | Detailed memory |
| `vmstat 1 5` | Virtual memory stats |
| `vmstat -s` | Summary |
| `top -o %MEM` | Sort by memory |
| `ps aux --sort=-%mem` | Memory sort |
| `ps -eo pid,ppid,cmd,%mem,%cpu --sort=-%mem` | Custom sort |
| `smem -rs` | Memory report |
| `smem -t` | Total memory |
| `smem -p` | Pie chart |
| `pmap -x PID` | Process memory map |
| `pmap -d PID` | Detailed map |
| `cat /proc/PID/maps` | Memory maps |
| `cat /proc/PID/smaps` | Detailed maps |
| `echo 3 > /proc/sys/vm/drop_caches` | Clear caches |
| `echo 1 > /proc/sys/vm/drop_caches` | Clear pagecache |
| `echo 2 > /proc/sys/vm/drop_caches` | Clear dentries/inodes |
| `sysctl -w vm.swappiness=10` | Reduce swappiness |
| `sysctl -w vm.vfs_cache_pressure=50` | Reduce cache |

# ─── CPU TROUBLESHOOTING ─────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `top -o %CPU` | Sort by CPU |
| `ps aux --sort=-%cpu` | CPU sort |
| `ps -eo pid,ppid,cmd,%mem,%cpu --sort=-%cpu` | Custom sort |
| `mpstat -P ALL 1` | CPU per core |
| `mpstat 1 5` | Summary |
| `sar -u 1 5` | CPU usage |
| `sar -q 1 5` | Load average |
| `cat /proc/cpuinfo` | CPU info |
| `lscpu` | CPU architecture |
| `taskset -cp 0-3 PID` | Pin process to cores |
| `taskset -cp PID` | Current affinity |
| `nice -n -10 command` | High priority |
| `renice -n -10 -p PID` | Change priority |
| `renice -n -10 -u user` | All user processes |
| `chrt -p PID` | Scheduling policy |
| `chrt -f -p 99 PID` | Real-time priority |
| `irqtop` | IRQ statistics |
| `watch -n 1 'cat /proc/interrupts'` | Watch IRQs |
| `perf top` | Performance monitoring |
| `perf record -g` | Record perf data |
| `perf report` | Report perf data |
| `perf stat command` | Command statistics |

# ─── DISK I/O TROUBLESHOOTING ───────────────────────────────────

| Command | Description |
|---------|-------------|
| `iostat -x 1` | I/O statistics |
| `iostat -x 1 5` | Every second, 5 times |
| `iostat -m` | Megabytes |
| `iostat -d -x -k 1` | Disk stats |
| `iotop -o` | I/O processes |
| `iotop -a` | Accumulated I/O |
| `iotop -d 2` | Update every 2s |
| `df -h` | Disk space |
| `df -i` | Inode usage |
| `du -sh /* \| sort -h` | Root sizes |
| `du -sh * \| sort -h` | Current dir sizes |
| `du -h --max-depth=1` | Depth limit |
| `lsof \| grep deleted` | Deleted files still open |
| `lsof +L1` | Open files with size 0 |
| `lsblk -f` | Filesystem info |
| `blkid` | UUIDs |
| `smartctl -a /dev/sda` | SMART info |
| `smartctl -H /dev/sda` | Health status |
| `smartctl -t short /dev/sda` | Short test |
| `smartctl -l selftest /dev/sda` | Test results |
| `badblocks -sv /dev/sda` | Bad blocks |
| `badblocks -sv -o badblocks.txt /dev/sda` | Save bad blocks |
| `fsck -f /dev/sda1` | Filesystem check |
| `fsck -y /dev/sda1` | Auto-repair |
| `fsck -n /dev/sda1` | Dry run |
| `tune2fs -l /dev/sda1` | ext filesystem info |
| `tune2fs -c 30 /dev/sda1` | Set mount count |
| `tune2fs -i 30d /dev/sda1` | Set check interval |
| `xfs_repair /dev/sda1` | XFS repair |
| `xfs_info /dev/sda1` | XFS info |
| `btrfs check /dev/sda1` | BTRFS check |
| `btrfs filesystem show` | BTRFS info |
| `ls -laR \| wc -l` | Count files |
| `find / -type f -size +100M -exec ls -lh {} \;` | Large files |
| `find / -type f -empty` | Empty files |
| `find / -type d -empty` | Empty directories |
| `find / -name "*.log" -size +100M` | Large logs |
| `find / -type f -perm 777` | World writable |

# ─── PROCESS TROUBLESHOOTING ─────────────────────────────────────

| Command | Description |
|---------|-------------|
| `ps auxf` | Process tree |
| `ps -ef --forest` | Forest view |
| `pstree -p -a` | Tree with args |
| `ps aux \| grep -E "Z|D"` | Zombie/Uninterruptible |
| `ps -eo pid,stat,comm \| grep '^[0-9]* D'` | Uninterruptible |
| `ps -eo pid,stat,comm \| grep '^[0-9]* Z'` | Zombie processes |
| `ps -eo pid,ppid,cmd,state,time` | Process states |
| `top -p PID` | Specific process |
| `top -n 1 -b \| grep process` | Batch mode |
| `htop -p PID` | Specific process |
| `lsof \| grep process_name` | Files used |
| `strace -p PID -e trace=open` | Open calls |
| `strace -p PID -e trace=read,write` | Read/write calls |
| `strace -p PID -e trace=connect,accept` | Network calls |
| `ltrace -p PID -e strcmp,strcpy` | String functions |
| `gdb -p PID` | Debug process |
| `gdb -p PID -ex "thread apply all bt" -ex "detach" -ex "quit"` | Backtrace all threads |
| `pmap -x PID` | Memory map |
| `pstack PID` | Stack trace |
| `pstree -p PID` | Process tree |
| `ls -l /proc/PID/fd/` | File descriptors |
| `cat /proc/PID/status` | Status info |
| `cat /proc/PID/stack` | Kernel stack |
| `cat /proc/PID/wchan` | Waiting channel |
| `cat /proc/PID/oom_score` | OOM score |
| `cat /proc/PID/oom_adj` | OOM adjustment |
| `echo -17 > /proc/PID/oom_adj` | OOM protection |

# ================================================================
# 14. ENCRYPTION & HASHING
# ================================================================

# ─── OpenSSL ──────────────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `openssl version` | OpenSSL version |
| `openssl genrsa -out private.pem 2048` | Generate RSA private key |
| `openssl genrsa -des3 -out private.pem 2048` | With password |
| `openssl rsa -in private.pem -pubout -out public.pem` | Extract public key |
| `openssl rsa -in private.pem -text -noout` | View RSA key |
| `openssl req -new -key private.pem -out request.csr` | Generate CSR |
| `openssl req -new -x509 -key private.pem -out cert.pem -days 365` | Self-signed cert |
| `openssl req -x509 -newkey rsa:4096 -keyout key.pem -out cert.pem -days 365` | Key and cert |
| `openssl req -text -noout -in request.csr` | View CSR |
| `openssl x509 -in cert.pem -text -noout` | View certificate |
| `openssl x509 -in cert.pem -fingerprint -noout` | Certificate fingerprint |
| `openssl x509 -in cert.pem -issuer -noout` | Certificate issuer |
| `openssl x509 -in cert.pem -subject -noout` | Certificate subject |
| `openssl x509 -in cert.pem -dates -noout` | Validity dates |
| `openssl verify -CAfile ca.pem cert.pem` | Verify certificate |
| `openssl pkcs12 -export -in cert.pem -inkey private.pem -out bundle.p12` | Create PKCS12 |
| `openssl pkcs12 -in bundle.p12 -out client.pem -clcerts -nokeys` | Extract cert |
| `openssl pkcs12 -in bundle.p12 -out client.key -nocerts` | Extract key |
| `openssl enc -aes-256-cbc -salt -in file.txt -out file.enc` | Encrypt file |
| `openssl enc -aes-256-cbc -d -in file.enc -out file.txt` | Decrypt file |
| `openssl enc -aes-256-cbc -a -in file.txt -out file.enc` | Base64 encode |
| `openssl enc -aes-256-cbc -a -d -in file.enc -out file.txt` | Base64 decode |
| `openssl dgst -sha256 file.txt` | SHA256 hash |
| `openssl dgst -sha512 file.txt` | SHA512 hash |
| `openssl dgst -md5 file.txt` | MD5 hash |
| `openssl sha256 -hmac "key" file.txt` | HMAC-SHA256 |
| `openssl rand -hex 32` | Generate random hex |
| `openssl rand -base64 32` | Generate random base64 |
| `openssl s_client -connect host:443` | SSL/TLS connection |
| `openssl s_client -connect host:443 -servername host` | With SNI |
| `openssl s_client -showcerts -connect host:443` | Show certificates |
| `openssl s_time -connect host:443` | SSL/TLS timing |

# ─── GPG ──────────────────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `gpg --version` | GPG version |
| `gpg --gen-key` | Generate key |
| `gpg --full-generate-key` | Full key generation |
| `gpg --list-keys` | List keys |
| `gpg --list-secret-keys` | List secret keys |
| `gpg --export -a "name" > public.asc` | Export public key |
| `gpg --export-secret-keys -a "name" > private.asc` | Export private key |
| `gpg --import public.asc` | Import public key |
| `gpg --import private.asc` | Import private key |
| `gpg --delete-key "name"` | Delete public key |
| `gpg --delete-secret-key "name"` | Delete secret key |
| `gpg --encrypt -r "name" file.txt` | Encrypt file |
| `gpg --decrypt file.gpg` | Decrypt file |
| `gpg --sign file.txt` | Sign file |
| `gpg --clearsign file.txt` | Clear sign |
| `gpg --verify file.sig file.txt` | Verify signature |
| `gpg --detach-sign file.txt` | Detached signature |
| `gpg --export-ownertrust` | Export trust |
| `gpg --import-ownertrust` | Import trust |
| `gpg --refresh-keys` | Refresh keys |
| `gpg --search-keys "name"` | Search keys |
| `gpg --send-keys key-id` | Send to keyserver |
| `gpg --recv-keys key-id` | Receive from keyserver |
| `gpg --fingerprint` | Key fingerprints |

# ─── HASHING ──────────────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `md5sum file.txt` | MD5 hash |
| `sha1sum file.txt` | SHA1 hash |
| `sha224sum file.txt` | SHA224 hash |
| `sha256sum file.txt` | SHA256 hash |
| `sha384sum file.txt` | SHA384 hash |
| `sha512sum file.txt` | SHA512 hash |
| `b2sum file.txt` | BLAKE2 hash |
| `cksum file.txt` | CRC checksum |
| `sum file.txt` | Checksum |
| `echo -n "text" \| md5sum` | String MD5 |
| `echo -n "text" \| sha256sum` | String SHA256 |
| `sha256sum -c checksums.txt` | Verify checksums |
| `sha512sum -c checksums.txt --quiet` | Quiet verify |
| `find . -type f -exec sha256sum {} \; > checksums.txt` | Generate checksums |

# ================================================================
# 15. WEB & API TESTING
# ================================================================

# ─── CURL ADVANCED ───────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `curl -I https://example.com` | Headers only |
| `curl -v https://example.com` | Verbose output |
| `curl -vvv https://example.com` | Very verbose |
| `curl -k https://self-signed.com` | Ignore SSL |
| `curl -L https://example.com` | Follow redirects |
| `curl -o file https://example.com` | Save output |
| `curl -O https://example.com/file.txt` | Save with name |
| `curl -C - -O https://example.com/file.txt` | Resume download |
| `curl --limit-rate 100K https://example.com` | Rate limit |
| `curl --max-time 30 https://example.com` | Timeout |
| `curl --connect-timeout 5 https://example.com` | Connect timeout |
| `curl -H "Header: value" https://example.com` | Custom header |
| `curl -H "Accept: application/json" https://example.com` | JSON accept |
| `curl -H "User-Agent: Mozilla/5.0" https://example.com` | User agent |
| `curl -u user:pass https://example.com` | Basic auth |
| `curl -X POST -d "data=value" https://example.com` | POST request |
| `curl -X POST -d @file.json -H "Content-Type: application/json" https://example.com` | JSON POST |
| `curl -X PUT -d @file.json https://example.com` | PUT request |
| `curl -X DELETE https://example.com` | DELETE request |
| `curl -F "file=@file.txt" https://example.com` | File upload |
| `curl -F "file=@file.txt;type=image/png" https://example.com` | With MIME type |
| `curl --data-urlencode "name=value" https://example.com` | URL encoded |
| `curl -b cookies.txt https://example.com` | Send cookies |
| `curl -c cookies.txt https://example.com` | Save cookies |
| `curl --referer https://example.com https://other.com` | Referer |
| `curl -A "Mozilla/5.0" https://example.com` | User agent (alt) |
| `curl -e https://example.com https://other.com` | Referer (alt) |
| `curl --compressed https://example.com` | Accept compression |
| `curl --no-keepalive https://example.com` | Disable keepalive |
| `curl --tlsv1.2 https://example.com` | TLS version |
| `curl --ciphers ECDHE-RSA-AES128-GCM-SHA256 https://example.com` | Cipher suite |
| `curl -w "%{time_total}\n" -o /dev/null -s https://example.com` | Total time |
| `curl -w "@format.txt" -o /dev/null -s https://example.com` | Custom format |

# ─── HTTPie ───────────────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `http https://example.com` | GET request |
| `http -v https://example.com` | Verbose |
| `http -h https://example.com` | Headers only |
| `http -b https://example.com` | Body only |
| `http https://example.com Accept:application/json` | Custom header |
| `http POST https://example.com key=value` | POST request |
| `http POST https://example.com key=value key2=value2` | Multiple fields |
| `http POST https://example.com < file.json` | Upload JSON |
| `http PUT https://example.com key=value` | PUT request |
| `http DELETE https://example.com` | DELETE request |
| `http -f POST https://example.com key=value` | Form data |
| `http -a user:pass https://example.com` | Basic auth |
| `http --session=name https://example.com` | Session |
| `http --download https://example.com/file` | Download |
| `http --stream https://example.com` | Stream response |
| `http --check-status https://example.com` | Check status |
| `http --timeout=30 https://example.com` | Timeout |
| `http --follow https://example.com` | Follow redirects |
| `http --print Hh https://example.com` | Print headers |
| `http --pretty=all https://example.com` | Pretty output |

# ─── POSTMAN CLI ─────────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `newman run collection.json` | Run collection |
| `newman run collection.json -e environment.json` | With environment |
| `newman run collection.json -g globals.json` | Globals |
| `newman run collection.json --folder "folder"` | Specific folder |
| `newman run collection.json -d data.csv` | Data file |
| `newman run collection.json -n 10` | Iterations |
| `newman run collection.json --delay-request 1000` | Delay (ms) |
| `newman run collection.json --reporters cli,json` | Reporters |
| `newman run collection.json --reporter-json-export output.json` | JSON output |
| `newman run collection.json --bail` | Stop on failure |
| `newman run collection.json --insecure` | Ignore SSL |
| `newman run collection.json --disable-unicode` | Disable unicode |
| `newman run collection.json --timeout 30000` | Timeout (ms) |

# ─── API TESTING ─────────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `curl -X GET "https://api.example.com/users" -H "Authorization: Bearer token"` | API GET |
| `curl -X POST "https://api.example.com/users" -H "Authorization: Bearer token" -H "Content-Type: application/json" -d '{"name":"John","email":"john@example.com"}'` | API POST |
| `curl -X PUT "https://api.example.com/users/1" -H "Authorization: Bearer token" -H "Content-Type: application/json" -d '{"name":"John Updated"}'` | API PUT |
| `curl -X DELETE "https://api.example.com/users/1" -H "Authorization: Bearer token"` | API DELETE |
| `curl -X GET "https://api.example.com/users?page=1&limit=10" -H "Authorization: Bearer token"` | Query params |
| `curl -X POST "https://api.example.com/login" -d '{"username":"user","password":"pass"}' -H "Content-Type: application/json" -c cookies.txt` | Login and save cookies |
| `curl -X GET "https://api.example.com/profile" -b cookies.txt` | Use cookies |
| `jq '.' response.json` | Pretty JSON |
| `jq '.data[].name' response.json` | Extract data |
| `jq '.[] \| select(.id==1)' response.json` | Filter data |
| `jq '. \| length' response.json` | Count items |
| `http -v https://api.example.com/users Authorization:"Bearer token"` | API request with httpie |
| `grpcurl -plaintext host:port package.service/method` | gRPC request |
| `grpcurl -d '{"key":"value"}' -plaintext host:port package.service/method` | gRPC with data |
| `grpcurl list host:port` | List gRPC services |
| `grpcurl describe host:port package.service` | Describe service |

# ================================================================
# 16. DATA PROCESSING - jq, yq, csv
# ================================================================

# ─── jq (JSON) ────────────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `jq '.' file.json` | Pretty print JSON |
| `jq -c '.' file.json` | Compact output |
| `jq -r '.' file.json` | Raw output |
| `jq '.key' file.json` | Get value |
| `jq '.object.key' file.json` | Nested value |
| `jq '.[0]' file.json` | Array index |
| `jq '.[]' file.json` | Array values |
| `jq '.[] \| .key' file.json` | Array values |
| `jq '.[] \| select(.key=="value")' file.json` | Filter |
| `jq '.[] \| select(.key > 10)' file.json` | Numeric filter |
| `jq '.[] \| select(.key \| contains("pattern"))' file.json` | Contains filter |
| `jq '.[] \| {name: .name, value: .value}' file.json` | Select fields |
| `jq '.[] \| map(.key)' file.json` | Map operation |
| `jq '.[] \| group_by(.key)' file.json` | Group by |
| `jq '.[] \| sort_by(.key)' file.json` | Sort |
| `jq '.[] \| length' file.json` | Length |
| `jq '.[] \| keys' file.json` | Keys |
| `jq '.[] \| has("key")' file.json` | Has key |
| `jq '.[] \| del(.key)' file.json` | Delete key |
| `jq '.[] \| .newkey = "value"' file.json` | Add key |
| `jq '.[] \| .key = "newvalue"' file.json` | Update key |
| `jq '.[] \| .key += 1' file.json` | Increment |
| `jq '.[] \| .key? // "default"' file.json` | Default value |
| `jq '.[] \| if .key > 10 then "large" else "small" end' file.json` | Conditional |
| `jq 'def add: . + 1; . \| add' file.json` | Custom function |
| `jq -s 'add' file1.json file2.json` | Merge files |
| `jq -n '{key: "value"}'` | Create JSON |
| `jq -n '[range(10)]'` | Generate range |
| `jq '. \| fromjson' file.json` | Parse JSON string |

# ─── yq (YAML/JSON) ──────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `yq eval file.yaml` | View YAML |
| `yq eval '.key' file.yaml` | Get value |
| `yq eval '.object.key' file.yaml` | Nested value |
| `yq eval '.[0]' file.yaml` | Array index |
| `yq eval '.[]' file.yaml` | Array values |
| `yq eval '.[] \| .key' file.yaml` | Array values |
| `yq eval '.[] \| select(.key=="value")' file.yaml` | Filter |
| `yq eval '.[] \| {name: .name, value: .value}' file.yaml` | Select fields |
| `yq eval '.[] \| sort_by(.key)' file.yaml` | Sort |
| `yq eval '.key = "newvalue"' file.yaml` | Update value |
| `yq eval '.newkey = "value"' file.yaml` | Add key |
| `yq eval 'del(.key)' file.yaml` | Delete key |
| `yq eval -i '.key = "newvalue"' file.yaml` | In-place update |
| `yq eval file.yaml -o=json` | YAML to JSON |
| `yq eval file.json -o=yaml` | JSON to YAML |
| `yq eval --prettyPrint file.yaml` | Pretty print |
| `yq eval --inplace file.yaml` | In-place edit |
| `yq eval --split-exp '.key' file.yaml` | Split files |
| `yq eval --merge file1.yaml file2.yaml` | Merge files |
| `yq eval --merge --inplace file1.yaml file2.yaml` | Merge and save |

# ─── CSV Processing ──────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `csvtool col 1 file.csv` | Get column 1 |
| `csvtool col 1,3 file.csv` | Columns 1 and 3 |
| `csvtool -t ',' col 1 file.csv` | Custom delimiter |
| `csvtool -u ',' drop 1 file.csv` | Drop column |
| `csvtool transpose file.csv` | Transpose |
| `csvtool sort 1 file.csv` | Sort by column 1 |
| `csvtool sort 1n file.csv` | Numeric sort |
| `csvtool dedup 1 file.csv` | Unique by column |
| `csvtool count file.csv` | Count rows |
| `csvcut -c 1,3 file.csv` | Cut columns |
| `csvgrep -c 1 -m value file.csv` | Grep column |
| `csvstat file.csv` | Statistics |
| `csvsql --query "SELECT * FROM file WHERE col1='value'" file.csv` | SQL query |
| `csvjoin file1.csv file2.csv -c id` | Join files |
| `csvmerge file1.csv file2.csv` | Merge files |
| `csvstack file1.csv file2.csv` | Stack files |
| `in2csv file.xlsx > file.csv` | Excel to CSV |
| `csv2json file.csv` | CSV to JSON |
| `json2csv file.json` | JSON to CSV |
| `sed 's/,/\t/g' file.csv` | CSV to TSV |
| `awk -F',' '{print $1, $3}' file.csv` | CSV columns |
| `awk -F',' '{sum+=$1} END {print sum}' file.csv` | Sum column |
| `awk -F',' 'NR>1 {print}' file.csv` | Skip header |
| `sort -t',' -k2n file.csv` | Sort by column 2 |

# ─── XML Processing ──────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `xmllint file.xml` | Validate XML |
| `xmllint --format file.xml` | Pretty print |
| `xmllint --xpath '//tag' file.xml` | XPath query |
| `xmllint --xpath '//tag/text()' file.xml` | Text only |
| `xmllint --xpath '//tag/@attribute' file.xml` | Attribute |
| `xmllint --xpath 'count(//tag)' file.xml` | Count |
| `xmllint --xpath '//tag[@attr="value"]' file.xml` | Filter |
| `xmlstarlet el file.xml` | List elements |
| `xmlstarlet sel -t -v "//tag" file.xml` | Select value |
| `xmlstarlet sel -t -m "//tag" -v "." -n file.xml` | Multiple values |
| `xmlstarlet ed -u "//tag" -v "newvalue" file.xml` | Update value |
| `xmlstarlet ed -a "//tag" -t elem -n "newtag" -v "value" file.xml` | Add element |
| `xmlstarlet ed -d "//tag" file.xml` | Delete element |
| `xmlstarlet tr transform.xsl file.xml` | Apply XSLT |

# ================================================================
# 17. CRON & SCHEDULED TASKS - LINUX
# ================================================================

# ─── CRON SYNTAX ──────────────────────────────────────────────────

| Field | Description | Values |
|-------|-------------|--------|
| Minute | 0-59 | * (any), */5 (every 5) |
| Hour | 0-23 | * (any), */2 (every 2) |
| Day of Month | 1-31 | * (any) |
| Month | 1-12 | * (any) |
| Day of Week | 0-6 (0=Sun) | * (any) |

# ─── CRON EXAMPLES ────────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `crontab -e` | Edit crontab |
| `crontab -l` | List crontab |
| `crontab -r` | Remove crontab |
| `crontab -u user -l` | List user's crontab |
| `crontab -u user -e` | Edit user's crontab |
| `crontab -u user -r` | Remove user's crontab |
| `* * * * * command` | Every minute |
| `*/5 * * * * command` | Every 5 minutes |
| `0 * * * * command` | Every hour |
| `0 0 * * * command` | Every day at midnight |
| `0 9 * * 1-5 command` | Weekdays at 9am |
| `0 0 * * 0 command` | Sunday at midnight |
| `0 0 1 * * command` | 1st of every month |
| `0 0 1 1 * command` | January 1st |
| `@reboot command` | At reboot |
| `@daily command` | Daily |
| `@weekly command` | Weekly |
| `@monthly command` | Monthly |
| `@yearly command` | Yearly |
| `@hourly command` | Hourly |
| `MAILTO=user@example.com` | Email output |
| `PATH=/usr/local/bin:/usr/bin:/bin` | Set PATH |
| `SHELL=/bin/bash` | Set shell |

# ─── CRON LOGGING ─────────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `grep CRON /var/log/syslog` | Cron logs |
| `grep CRON /var/log/cron` | Cron logs (RHEL) |
| `grep -i error /var/log/syslog \| grep CRON` | Cron errors |
| `journalctl -u cron` | Cron journal logs |
| `journalctl -u cron -f` | Follow cron logs |
| `systemctl status cron` | Cron service status |
| `systemctl start cron` | Start cron |
| `systemctl stop cron` | Stop cron |
| `systemctl enable cron` | Enable cron |
| `systemctl disable cron` | Disable cron |

# ─── ANACRON ──────────────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `anacron -f` | Run anacron now |
| `anacron -u` | Update timestamps |
| `anacron -s` | Run sequentially |
| `anacron -d` | Debug mode |
| `cat /etc/anacrontab` | View anacrontab |

# ─── AT COMMAND ──────────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `at now + 5 minutes` | Run in 5 minutes |
| `at now + 1 hour` | Run in 1 hour |
| `at now + 1 day` | Run in 1 day |
| `at tomorrow 09:00` | Run tomorrow at 9am |
| `at 2024-01-01 00:00` | Run at specific date/time |
| `atq` | List pending jobs |
| `atrm job_id` | Remove job |
| `at -c job_id` | Show job command |
| `at -l` | List jobs (alternative) |
| `at -d job_id` | Delete job (alternative) |
| `batch` | Run when system load low |

# ================================================================
# 18. SSH & REMOTE ACCESS ADVANCED
# ================================================================

# ─── SSH CONFIGURATION ───────────────────────────────────────────

| File | Description |
|------|-------------|
| `~/.ssh/config` | SSH client config |
| `~/.ssh/id_rsa` | Private key |
| `~/.ssh/id_rsa.pub` | Public key |
| `~/.ssh/known_hosts` | Known hosts |
| `~/.ssh/authorized_keys` | Authorized keys |
| `/etc/ssh/sshd_config` | Server config |
| `/etc/ssh/ssh_config` | Global client config |

# ─── SSH CONFIG EXAMPLES ─────────────────────────────────────────

| Config | Description |
|--------|-------------|
| `Host myserver` | Host alias |
| `HostName 192.168.1.100` | Host IP |
| `Port 2222` | Custom port |
| `User username` | Username |
| `IdentityFile ~/.ssh/id_rsa` | Key file |
| `ForwardAgent yes` | Agent forwarding |
| `ForwardX11 yes` | X11 forwarding |
| `StrictHostKeyChecking no` | Skip host key check |
| `UserKnownHostsFile /dev/null` | Don't save host key |
| `LogLevel DEBUG` | Debug logging |
| `Compression yes` | Enable compression |
| `ServerAliveInterval 60` | Keep alive |
| `ServerAliveCountMax 3` | Max alive count |
| `TCPKeepAlive yes` | TCP keepalive |
| `ControlMaster auto` | Connection sharing |
| `ControlPath /tmp/ssh-mux-%r@%h:%p` | Control path |
| `ControlPersist 10m` | Persistent connection |

# ─── SSH TUNNELING ───────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `ssh -L 8080:localhost:80 user@host` | Local port forwarding |
| `ssh -L 8080:remote-host:80 user@host` | Forward to remote host |
| `ssh -R 8080:localhost:80 user@host` | Remote port forwarding |
| `ssh -R 8080:remote-host:80 user@host` | Remote to remote |
| `ssh -D 1080 user@host` | Dynamic SOCKS5 proxy |
| `ssh -f -N -L 8080:localhost:80 user@host` | Background forwarding |
| `ssh -f -N -R 8080:localhost:80 user@host` | Background remote |
| `ssh -L 5432:localhost:5432 db-host -N` | Database tunnel |
| `ssh -L 3306:localhost:3306 db-host -N` | MySQL tunnel |
| `ssh -L 27017:localhost:27017 db-host -N` | MongoDB tunnel |
| `ssh -L 6379:localhost:6379 redis-host -N` | Redis tunnel |
| `ssh -L 9200:localhost:9200 elastic-host -N` | Elasticsearch tunnel |
| `ssh -L 8080:localhost:80 -L 8443:localhost:443 user@host` | Multiple forwards |
| `ssh -R 8080:localhost:80 -R 8443:localhost:443 user@host` | Multiple remote |
| `ssh -L 8080:localhost:80 user@host -v` | Verbose tunnel |
| `ssh -L 8080:localhost:80 user@host -Nf` | Daemon mode |

# ─── SSH KEY MANAGEMENT ──────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `ssh-keygen -t rsa -b 4096 -C "comment"` | Generate RSA key |
| `ssh-keygen -t ed25519 -C "comment"` | Generate ED25519 key |
| `ssh-keygen -t ecdsa -b 521` | Generate ECDSA key |
| `ssh-keygen -f ~/.ssh/id_rsa -p` | Change passphrase |
| `ssh-keygen -y -f ~/.ssh/id_rsa` | Extract public key |
| `ssh-keygen -R hostname` | Remove host from known_hosts |
| `ssh-keygen -F hostname` | Find host in known_hosts |
| `ssh-keygen -l -f ~/.ssh/id_rsa.pub` | Key fingerprint |
| `ssh-keygen -H -f known_hosts` | Hash known_hosts |
| `ssh-copy-id user@host` | Copy public key to server |
| `ssh-copy-id -i ~/.ssh/id_rsa.pub user@host` | Specific key |
| `ssh-copy-id -p 2222 user@host` | Custom port |
| `ssh-agent -s` | Start SSH agent |
| `ssh-agent -k` | Kill SSH agent |
| `ssh-add ~/.ssh/id_rsa` | Add key to agent |
| `ssh-add -l` | List agent keys |
| `ssh-add -D` | Remove all keys |
| `ssh-add -t 3600 ~/.ssh/id_rsa` | Add with timeout |

# ─── SCREEN COMMANDS ─────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `screen` | Start screen |
| `screen -S session` | Named session |
| `screen -r session` | Resume session |
| `screen -r` | Resume first session |
| `screen -ls` | List sessions |
| `screen -d` | Detach session |
| `screen -D` | Force detach |
| `screen -X -S session quit` | Kill session |
| `screen -dmS session command` | Start in detached mode |
| `screen -S session -X log` | Start logging |
| `screen -S session -X logfile file` | Set log file |
| `screen -S session -X hardcopy` | Screenshot |
| `Ctrl+a c` | Create new window |
| `Ctrl+a n` | Next window |
| `Ctrl+a p` | Previous window |
| `Ctrl+a "` | List windows |
| `Ctrl+a d` | Detach |
| `Ctrl+a k` | Kill window |
| `Ctrl+a A` | Rename window |
| `Ctrl+a [ ` | Copy mode |
| `Ctrl+a ] ` | Paste |
| `Ctrl+a ?` | Help |

# ─── TMUX COMMANDS ───────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `tmux` | Start tmux |
| `tmux new -s session` | Named session |
| `tmux attach -t session` | Attach session |
| `tmux detach` | Detach session |
| `tmux ls` | List sessions |
| `tmux kill-session -t session` | Kill session |
| `tmux kill-session -a` | Kill all sessions |
| `tmux list-windows` | List windows |
| `tmux list-panes` | List panes |
| `tmux new-window` | New window |
| `tmux new-window -n name` | Named window |
| `tmux split-window` | Split horizontally |
| `tmux split-window -h` | Split vertically |
| `tmux select-pane -t 0` | Select pane |
| `tmux swap-pane -s 0 -t 1` | Swap panes |
| `tmux resize-pane -D 10` | Resize down |
| `tmux resize-pane -U 10` | Resize up |
| `tmux set-option -g prefix C-a` | Change prefix |
| `tmux source-file ~/.tmux.conf` | Reload config |
| `Ctrl+b c` | Create window |
| `Ctrl+b n` | Next window |
| `Ctrl+b p` | Previous window |
| `Ctrl+b 0-9` | Switch window |
| `Ctrl+b d` | Detach |
| `Ctrl+b %` | Split vertical |
| `Ctrl+b "` | Split horizontal |
| `Ctrl+b arrow` | Switch pane |
| `Ctrl+b x` | Kill pane |
| `Ctrl+b [ ` | Copy mode |
| `Ctrl+b ] ` | Paste |

# ================================================================
# 19. WINDOWS EXPLORER SEARCH SYNTAX
# ================================================================

# ─── DATE FILTERS ─────────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `datemodified:today` | Today |
| `datemodified:yesterday` | Yesterday |
| `datemodified:this week` | This week |
| `datemodified:last week` | Last week |
| `datemodified:this month` | This month |
| `datemodified:last month` | Last month |
| `datemodified:1/1/2024` | Specific date |
| `datemodified:>1/1/2024` | After date |
| `datemodified:<1/1/2024` | Before date |
| `datemodified:..1/1/2024` | Up to date |
| `datemodified:1/1/2024..` | From date |
| `datemodified:1/1/2024..1/31/2024` | Date range |
| `datecreated:today` | Created today |

# ─── SIZE FILTERS ─────────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `size:empty` | Empty files |
| `size:tiny` | 0-10 KB |
| `size:small` | 10-100 KB |
| `size:medium` | 100 KB - 1 MB |
| `size:large` | 1-16 MB |
| `size:huge` | 16-128 MB |
| `size:gigantic` | >128 MB |
| `size:>500MB` | Greater than 500MB |
| `size:<100KB` | Less than 100KB |
| `size:1MB..10MB` | Range |

# ─── FILE TYPE FILTERS ───────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `ext:.txt` | Text files |
| `ext:.pdf` | PDF files |
| `ext:.docx` | Word files |
| `ext:.xlsx` | Excel files |
| `ext:.pptx` | PowerPoint files |
| `ext:.jpg` | JPG images |
| `ext:.png` | PNG images |
| `ext:.gif` | GIF images |
| `ext:.mp4` | MP4 videos |
| `ext:.mp3` | MP3 audio |
| `ext:.exe` | Executables |
| `ext:.msi` | Installers |
| `ext:.zip` | ZIP archives |
| `ext:.rar` | RAR archives |
| `ext:.7z` | 7Z archives |
| `ext:.log` | Log files |
| `ext:.tmp` | Temp files |
| `ext:.html` | HTML files |
| `ext:.js` | JavaScript |
| `ext:.css` | CSS files |
| `ext:.xml` | XML files |
| `ext:.json` | JSON files |
| `ext:.yaml` | YAML files |
| `ext:.yml` | YAML files |

# ─── ATTRIBUTE FILTERS ───────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `attributes:H` | Hidden files |
| `attributes:S` | System files |
| `attributes:R` | Read-only files |
| `attributes:A` | Archive files |
| `attributes:C` | Compressed files |
| `attributes:E` | Encrypted files |

# ─── NAME FILTERS ────────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `"filename"` | Exact name |
| `*pattern*` | Contains pattern |
| `pattern*` | Starts with pattern |
| `*pattern` | Ends with pattern |
| `~="regex"` | Regex pattern |

# ─── CONTENT FILTERS ─────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `content:"search text"` | Contains text |
| `content:"project report"` | Phrase search |

# ─── PROPERTY FILTERS ────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `author:"John Doe"` | Author |
| `title:"presentation"` | Title |
| `subject:"budget"` | Subject |
| `tags:"important"` | Tags |
| `company:"Microsoft"` | Company |
| `category:"financial"` | Category |
| `comment:"review"` | Comments |

# ─── COMBINED SEARCHES ───────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `datemodified:today ext:.docx author:"John"` | Combined filters |
| `size:>50MB datemodified:this week` | Size and date |
| `datemodified:1/1/2024..1/31/2024 ext:.pdf` | Date and extension |
| `type:document datemodified:yesterday` | Type and date |
| `kind:music size:>10MB` | Kind and size |
| `kind:picture datemodified:this month` | Kind and date |
| `kind:video size:gigantic` | Kind and size |
| `kind:email from:"john@example.com"` | Email search |

# ─── ADVANCED OPERATORS ──────────────────────────────────────────

| Operator | Description |
|----------|-------------|
| `NOT "keyword"` | Exclude keyword |
| `OR` | OR operator |
| `( )` | Grouping |
| `AND` | AND operator |
| `+` | Must include |
| `-` | Must exclude |
| `>` | Greater than |
| `<` | Less than |
| `..` | Range |

# ================================================================
# 20. PRO TIPS & HIDDEN GEMS
# ================================================================

# ─── LINUX PRO TIPS ──────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `!!` | Repeat last command |
| `!$` | Last argument of previous command |
| `!*` | All arguments of previous command |
| `!command` | Repeat command from history |
| `Ctrl+r` | Reverse search |
| `Ctrl+g` | Cancel search |
| `Alt+., Alt+_` | Last argument (repeatable) |
| `cd -` | Go to previous directory |
| `cd ~` | Go to home directory |
| `cd /` | Go to root |
| `pushd .` | Save current directory |
| `popd` | Go to saved directory |
| `dirs` | List directory stack |
| `fc -l` | List command history |
| `history` | Show history |
| `history -c` | Clear history |
| `history -d 100` | Delete command 100 |
| `export HISTSIZE=10000` | Larger history |
| `export HISTFILESIZE=20000` | Larger history file |
| `export HISTCONTROL=ignoredups` | Ignore duplicates |
| `export HISTTIMEFORMAT="%F %T "` | Timestamp in history |
| `touch -t 202401011200 file` | Set timestamp |
| `watch -n 1 -d 'command'` | Watch with highlighting |
| `time command` | Timing |
| `/usr/bin/time -v command` | Detailed timing |
| `yes \| command` | Auto-confirm |
| `command 2>&1 \| tee file.log` | Output to file and terminal |
| `command \| tee >(grep error > errors.log)` | Multiple outputs |
| `command \| less -S` | Horizontal scrolling |
| `command \| column -t -s,` | Pretty CSV |
| `command \| fold -w 80` | Wrap to 80 chars |
| `command \| tr -d '\r'` | Remove Windows CR |
| `command \| sponge file` | Write output to file (moreutils) |
| `command \| tee /dev/tty \| command2` | Pipe to terminal and command |

# ─── WINDOWS PRO TIPS ────────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `echo %cd%` | Current directory |
| `echo %date%` | Current date |
| `echo %time%` | Current time |
| `echo %random%` | Random number |
| `echo %errorlevel%` | Last error code |
| `echo %cmdcmdline%` | Command line |
| `%userprofile%\Desktop` | Desktop path |
| `%userprofile%\Documents` | Documents path |
| `%userprofile%\Downloads` | Downloads path |
| `%programfiles%` | Program Files |
| `%programfiles(x86)%` | Program Files x86 |
| `%appdata%` | AppData Roaming |
| `%localappdata%` | AppData Local |
| `%temp%` | Temp folder |
| `doskey /history` | Command history |
| `doskey ls=dir $*` | Create alias |
| `doskey /macros` | List aliases |
| `doskey /reinstall` | Reload doskey |
| `start .` | Open current folder |
| `start explorer` | Open Explorer |
| `start notepad file.txt` | Open with default |
| `start www.google.com` | Open URL |
| `clip < file.txt` | Copy to clipboard |
| `echo text \| clip` | Copy to clipboard |
| `dir \| find "pattern"` | Filter output |
| `type file.txt \| find "pattern"` | Search file |
| `type file.txt \| more` | Page output |
| `tree` | Directory tree |
| `tree /F` | With files |
| `tree /A` | ASCII characters |

# ─── POWERSHELL PRO TIPS ─────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `Get-History` | Command history |
| `Invoke-History 5` | Run command 5 |
| `Get-Command *process*` | Find commands |
| `Get-Alias` | List aliases |
| `Set-Alias ll Get-ChildItem` | Create alias |
| `Get-ChildItem -Recurse \| Format-Table -AutoSize` | Format table |
| `Get-ChildItem \| Out-GridView` | GUI view |
| `Get-ChildItem \| Export-Csv file.csv` | Export CSV |
| `Get-ChildItem \| ConvertTo-Json` | Convert to JSON |
| `Get-ChildItem \| Format-List` | Format list |
| `Get-Process \| Format-Table -AutoSize -Wrap` | Wrap table |
| `Get-Process \| Select-Object -First 10` | Top 10 |
| `Get-Process \| Where-Object {$_.CPU -gt 50}` | Filter |
| `Get-Process \| Group-Object ProcessName` | Group |
| `Get-EventLog -LogName System -Newest 10 \| Format-Table -AutoSize` | Events |
| `Get-EventLog -LogName System -Newest 10 \| Out-GridView` | GUI events |
| `Get-Counter \| Select-Object -ExpandProperty CounterSamples` | Counters |
| `Get-Help command -Examples` | Examples |
| `Get-Help command -Detailed` | Detailed help |
| `command -?` | Quick help |
| `Set-PSReadLineOption -EditMode Emacs` | Emacs mode |
| `Set-PSReadLineOption -Colors @{Command="#ff0000"}` | Colors |
| `$PSVersionTable` | Version info |
| `$?` | Last command success |
| `$Error[0]` | Last error |
| `$Error.Clear()` | Clear errors |
| `$null = command` | Suppress output |
| `command \| Out-Null` | Suppress output |

# ─── TERMINAL MULTIPLEXING ───────────────────────────────────────

| Command | Description |
|---------|-------------|
| `Ctrl+Z` | Suspend command |
| `bg` | Resume in background |
| `fg` | Bring to foreground |
| `jobs` | List jobs |
| `disown` | Remove from job table |
| `nohup command &` | Run in background |
| `command &` | Background job |
| `screen` | Screen session |
| `tmux` | Tmux session |
| `byobu` | Byobu (wrapper) |

# ─── TEXT MANIPULATION ───────────────────────────────────────────

| Command | Description |
|---------|-------------|
| `tr '[:upper:]' '[:lower:]'` | Lowercase |
| `tr '[:lower:]' '[:upper:]'` | Uppercase |
| `tr -d '[:space:]'` | Remove whitespace |
| `tr -s ' '` | Squeeze spaces |
| `tr ',' '\t'` | CSV to TSV |
| `col -b` | Remove backspaces |
| `expand -t 4` | Tabs to spaces |
| `unexpand -t 4` | Spaces to tabs |
| `pr -2 -t` | Two-column output |
| `pr -3 -t -w 80` | Three-column output |
| `fold -w 80` | Wrap at 80 |
| `paste -d, - - < file` | Combine lines |
| `paste -d',' file1 file2` | Combine files |
| `join -t, -1 1 -2 1 file1.csv file2.csv` | Join files |
| `awk '!seen[$0]++'` | Remove duplicates |
| `awk '{print > $2".txt"}'` | Split by field |
| `awk '{a[$1]++;} END{for(i in a) print i, a[i]}'` | Count occurrences |
| `sed '/^$/d'` | Remove empty lines |
| `sed 's/^[ \t]*//;s/[ \t]*$//'` | Trim whitespace |
| `sed 's/^/"/;s/$/"/'` | Add quotes |
| `sed 's/,\s*/,/g'` | Clean CSV |
| `sed -E 's/[0-9]{3}-[0-9]{3}-[0-9]{4}/XXX-XXX-XXXX/g'` | Mask phone numbers |

# ================================================================
# END OF CATALOG
# ═══════════════════════════════════════════════════════════════════
#
# This catalog is a comprehensive reference of useful commands.
# It includes Linux, Windows CMD, PowerShell, Docker, Kubernetes,
# Git, Databases, Cloud CLI, and much more. All commands are for
# legitimate system administration and use.
#
# 📝 HOW TO USE:
# 1. Search for the command you need using Ctrl+F
# 2. Copy and paste into your terminal
# 3. Adjust parameters as needed
# 4. For Windows, use CMD or PowerShell as indicated
#
# 📊 STATISTICS:
# - Over 1,500+ commands
# - 35+ categories
# - 10+ platforms covered
# - Real-world battle-tested commands
#
# 🔧 TIPS:
# - Use Ctrl+F to find commands quickly
# - Bookmark this file for easy access
# - Practice commands in a test environment first
# - Always backup before running destructive commands
#
# ---
# Author: F1REW0LF
# License: MIT - Free for Community
# Version: 3.0 - Ultimate Edition
# ═══════════════════════════════════════════════════════════════════
