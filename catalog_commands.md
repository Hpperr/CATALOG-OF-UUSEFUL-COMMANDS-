# ═══════════════════════════════════════════════════════════════
#  C A T A L O G   O F   U S E F U L   C O M M A N D S
# ═══════════════════════════════════════════════════════════════
#  Version: 1.0.0
#  Author: F1REW0LF
#  License: MIT - Free for Community
#  Platform: Linux | Windows CMD | PowerShell | GUI Search
# ═══════════════════════════════════════════════════════════════
#
#  CATALOG STRUCTURE:
#  1. Linux Commands (Bash/Zsh)
#  2. Windows CMD Commands (Command Prompt)
#  3. PowerShell Commands
#  4. CMD Advanced (Networking, System, Disk, etc.)
#  5. Windows Explorer Search Syntax
#  6. Cross-Platform Utilities
#  7. Advanced Filters & Search
#  8. System Information
#  9. Network Commands (All Platforms)
#  10. File Operations (All Platforms)
#  11. Process Management
#  12. User Management
#  13. Disk & Storage
#  14. Date & Time
#  15. Text Processing
#  16. Compression & Archiving
#  17. Package Management
#  18. Environment Variables
#  19. System Monitoring
#  20. Remote Connections
#  21. System Recovery
#  22. CMD Shortcuts & Tips
#
# ═══════════════════════════════════════════════════════════════

# ================================================================
# 1. LINUX COMMANDS (BASH/ZSH)
# ================================================================

# ---- FILE OPERATIONS ----

# List files with details
ls -la                    # List all files with permissions
ls -lh                    # List with human-readable sizes
ls -lt                    # List sorted by modification time
ls -ltr                   # List sorted by time (newest last)
ls -R                     # List recursively
ls -S                     # Sort by size

# View file content
cat file.txt              # Display full file
less file.txt             # View file page by page
head -n 20 file.txt       # Show first 20 lines
tail -n 50 file.txt       # Show last 50 lines
tail -f file.txt          # Follow file updates in real-time

# File search
find / -name "*.txt"      # Find files by name
find / -type f -size +100M # Find files larger than 100MB
find . -mtime -7          # Files modified in last 7 days
find . -mtime +30         # Files modified more than 30 days ago
find . -cmin -60          # Files changed in last 60 minutes

# Search within files
grep "pattern" file.txt   # Search pattern in file
grep -r "pattern" ./      # Recursive search in directory
grep -i "pattern" file    # Case-insensitive search
grep -v "pattern" file    # Exclude pattern
grep -l "pattern" *       # List files containing pattern
grep -n "pattern" file    # Show line numbers

# File permissions
chmod 755 file            # rwxr-xr-x
chmod 644 file            # rw-r--r--
chmod -R 755 directory    # Recursive permission change
chown user:group file     # Change owner and group
chown -R user:group dir   # Recursive owner change

# Symbolic links
ln -s target linkname     # Create symbolic link
ls -l                     # View symbolic links

# ---- SYSTEM INFORMATION ----

uname -a                  # All system information
uname -r                  # Kernel version
uname -m                  # Architecture (x86_64, arm64)
hostname                  # System hostname
hostnamectl               # Full system info (systemd)
cat /etc/os-release       # OS distribution info
cat /proc/cpuinfo         # CPU information
cat /proc/meminfo         # Memory information
lscpu                     # CPU architecture info
lsblk                     # Block devices
df -h                     # Disk usage (human-readable)
du -sh directory/         # Size of directory
du -sh *                  # Size of all items in current dir

# ---- PROCESS MANAGEMENT ----

ps aux                    # All running processes
ps -ef                    # Full process list
ps -eo pid,ppid,cmd,%mem,%cpu  # Custom process output
top                       # Interactive process viewer
htop                      # Enhanced process viewer
kill PID                  # Terminate process by ID
kill -9 PID               # Force kill process
pkill process_name        # Kill process by name
pgrep process_name        # Get PID by name
nohup command &           # Run command in background
jobs                      # List background jobs
fg                        # Bring job to foreground
bg                        # Resume job in background

# ---- NETWORK COMMANDS ----

ifconfig                  # Network interfaces (legacy)
ip addr                   # IP addresses (modern)
ip link                   # Network interfaces
ping -c 4 google.com      # Ping with 4 packets
traceroute google.com     # Trace route to host
netstat -tulpn            # Listening ports with processes
ss -tulpn                 # Modern socket statistics
ss -tulpn | grep LISTEN   # Only listening ports
curl ifconfig.me          # Public IP address
wget -O file url          # Download file
scp user@host:file .      # Secure copy from remote
rsync -av source/ dest/   # Sync directories

# ---- USER MANAGEMENT ----

whoami                    # Current username
id                        # User and group IDs
users                     # List logged-in users
who                       # Who is logged in
w                         # Who is logged in and what they're doing
last                      # Last login records
lastlog                   # Last login for all users
sudo useradd username     # Create new user
sudo passwd username      # Change user password
sudo usermod -aG group user # Add user to group
groups username           # Show user's groups
sudo deluser username     # Delete user (Debian)
sudo userdel username     # Delete user (Red Hat)

# ---- DISK & STORAGE ----

df -h                     # Disk space usage
df -i                     # Inode usage
du -sh * | sort -h        # Size of directories sorted
lsblk -f                  # Filesystem info
mount                     # Mounted filesystems
fdisk -l                  # Partition table
parted -l                 # Partition info
dd if=/dev/zero of=file bs=1M count=100  # Create 100MB file
mkfs.ext4 /dev/sdb1       # Format partition as ext4

# ---- DATE & TIME ----

date                      # Current date and time
date +%Y-%m-%d            # Format: 2024-01-01
date +%H:%M:%S            # Format: 14:30:00
date -d "tomorrow"        # Tomorrow's date
date -d "yesterday"       # Yesterday's date
cal                       # Calendar for current month
cal 2024                  # Calendar for year
timedatectl               # System time settings
sleep 10                  # Pause for 10 seconds

# ---- TEXT PROCESSING ----

echo "text" > file        # Write text to file
echo "text" >> file       # Append text to file
cat file1 file2 > merged  # Merge files
sort file                 # Sort file content
sort -n file              # Sort numerically
sort -r file              # Sort reverse
uniq file                 # Remove duplicate lines
wc -l file                # Count lines
wc -w file                # Count words
wc -c file                # Count characters
cut -d',' -f1 file.csv    # Cut first column (CSV)
cut -c1-10 file           # Cut first 10 characters
awk '{print $1}' file     # Print first column
sed 's/old/new/g' file    # Replace text
sed -i 's/old/new/g' file # Replace in-place

# ---- COMPRESSION & ARCHIVING ----

tar -czf archive.tar.gz directory/   # Create tar.gz
tar -xzf archive.tar.gz              # Extract tar.gz
tar -cjf archive.tar.bz2 directory/  # Create tar.bz2
tar -xjf archive.tar.bz2             # Extract tar.bz2
zip -r archive.zip directory/        # Create zip
unzip archive.zip                    # Extract zip
gzip file                            # Compress to .gz
gunzip file.gz                       # Decompress .gz
7z a archive.7z directory/           # Create 7z archive
7z x archive.7z                      # Extract 7z

# ---- PACKAGE MANAGEMENT (APT) ----

apt update                # Update package list
apt upgrade               # Upgrade all packages
apt install package       # Install package
apt remove package        # Remove package
apt purge package         # Remove with config
apt autoremove            # Remove unused packages
apt search keyword        # Search packages
apt show package          # Show package info
apt list --installed      # List installed packages

# ---- PACKAGE MANAGEMENT (YUM/DNF) ----

yum install package       # Install package (RHEL)
yum remove package        # Remove package
yum list installed        # List installed packages
yum search keyword        # Search packages
dnf install package       # Install (Fedora)
dnf update                # Update all (Fedora)

# ---- ENVIRONMENT VARIABLES ----

env                       # Show all environment variables
echo $PATH                # Show PATH variable
export VAR=value          # Set environment variable
unset VAR                 # Unset environment variable
echo $HOME                # Home directory
echo $USER                # Current user
echo $SHELL               # Current shell
echo $PWD                 # Current working directory
echo $OLDPWD              # Previous directory

# ---- SYSTEM MONITORING ----

top                       # Real-time process viewer
htop                      # Enhanced top
iotop                     # I/O monitoring
nmon                      # System monitor
vmstat 1                  # Virtual memory statistics
iostat -x 1               # I/O statistics
sar -u 1 5                # CPU usage
sar -r 1 5                # Memory usage
watch -n 1 command        # Execute command every second
uptime                    # System uptime
dmesg | tail -20          # Recent kernel messages

# ---- REMOTE CONNECTIONS ----

ssh user@host             # SSH connection
ssh -p 2222 user@host     # SSH with custom port
ssh -i key.pem user@host  # SSH with key file
scp file user@host:/path  # Copy file to remote
scp user@host:/path/file . # Copy from remote
rsync -avz user@host:/path/ /local/path/  # Sync from remote
sftp user@host            # Secure FTP
telnet host port          # Telnet connection (insecure)
nc -zv host port          # Netcat port scanning

# ---- SYSTEM RECOVERY ----

fsck -f /dev/sda1         # Check filesystem
badblocks -sv /dev/sda    # Check for bad blocks
dd if=/dev/sda of=/dev/sdb bs=4M  # Clone disk
testdisk                  # Recover partitions
photorec                  # Recover files
chroot /mnt/sysroot       # Change root directory
rescue                    # System rescue mode
grub-install /dev/sda     # Install GRUB bootloader

# ================================================================
# 2. WINDOWS CMD COMMANDS (COMMAND PROMPT)
# ================================================================

# ---- FILE OPERATIONS ----

dir                       # List directory contents
dir /w                    # Wide listing
dir /p                    # Page-by-page
dir /s                    # Recursive listing
dir *.txt /s              # Find all .txt files
dir /b                    # Simple listing (names only)
dir /a                    # Show all files (including hidden)
dir /od                   # Sort by date
dir /os                   # Sort by size

# Create/Delete
mkdir folder              # Create directory
rmdir folder              # Remove empty directory
rmdir /s folder           # Remove directory with contents
del file.txt              # Delete file
del /f file.txt           # Force delete read-only file
del /s *.tmp              # Delete all .tmp files recursively
copy file.txt new.txt     # Copy file
copy /y file.txt dest\    # Copy without confirmation
xcopy source dest /e      # Copy directories and subdirectories
xcopy /h                  # Copy hidden/system files
move file.txt folder\     # Move file
rename old.txt new.txt    # Rename file

# View/Edit Files
type file.txt             # Display file content
more file.txt             # Page-by-page view
find "text" file.txt      # Search within file
findstr "pattern" *.txt   # Search string in files
findstr /s "pattern" *.*  # Recursive search
edit file.txt             # Edit file (old editor)

# ---- SYSTEM INFORMATION ----

systeminfo                # Full system information
ver                       # Windows version
hostname                  # Computer name
whoami                    # Current user
set                       # Environment variables
echo %PATH%               # Show PATH variable
echo %USERNAME%           # Current username
echo %COMPUTERNAME%       # Computer name
echo %OS%                 # Operating system

# ---- PROCESS MANAGEMENT ----

tasklist                  # List processes
tasklist /v               # Verbose process list
tasklist /fi "memusage gt 50000"  # Processes using >50MB
taskkill /PID 1234        # Kill process by PID
taskkill /IM process.exe  # Kill process by name
taskkill /F /PID 1234     # Force kill
start program.exe         # Start program
start /min program.exe    # Start minimized
start /max program.exe    # Start maximized

# ---- NETWORK COMMANDS ----

ipconfig                  # IP configuration
ipconfig /all             # Detailed IP config
ipconfig /release         # Release DHCP lease
ipconfig /renew           # Renew DHCP lease
ipconfig /flushdns        # Flush DNS cache
ping host                 # Ping host
ping -t host              # Continuous ping
ping -n 4 host            # Ping 4 times
tracert host              # Trace route
nslookup host             # DNS lookup
netstat -a                # All connections
netstat -ano              # All connections with PIDs
netstat -r                # Routing table
net view                  # View network computers
net use Z: \\server\share # Map network drive
net use /delete Z:        # Disconnect network drive

# ---- USER MANAGEMENT ----

net user                  # List local users
net user username         # User details
net user username password /add  # Add user
net user username /delete # Delete user
net localgroup            # List local groups
net localgroup Administrators username /add  # Add to admin
whoami                    # Current user
whoami /all               # All user info
wmic useraccount get name  # List users (advanced)

# ---- DISK & STORAGE ----

chkdsk                    # Check disk
chkdsk /f                 # Fix disk errors
chkdsk /r                 # Find bad sectors
diskpart                  # Disk partition tool
list disk                 # List disks (inside diskpart)
select disk 0             # Select disk
list partition            # List partitions
clean                     # Clean disk (WARNING!)
format D: /fs:NTFS        # Format drive
defrag C:                 # Defragment drive
wmic diskdrive get model,size  # Disk info

# ---- DATE & TIME ----

date                      # Display/set date
time                      # Display/set time
time /t                   # Display time only
date /t                   # Display date only

# ---- TEXT PROCESSING ----

type file.txt | find "text"      # Search in file
type file.txt | find /v "text"   # Exclude lines
type file.txt | more             # Page view
sort file.txt                    # Sort lines
sort /r file.txt                 # Sort reverse
sort /+n file.txt                # Sort by column n

# ---- COMPRESSION & ARCHIVING ----

# Windows has built-in compression:
compact /c file.txt       # Compress file
compact /u file.txt       # Uncompress file
compact /c /s:folder      # Compress entire folder
compact /u /s:folder      # Uncompress entire folder

# ---- SYSTEM UTILITIES ----

shutdown /s /t 60         # Shutdown in 60 seconds
shutdown /r /t 60         # Reboot in 60 seconds
shutdown /a               # Abort shutdown
shutdown /h               # Hibernate
shutdown /l               # Log off
sfc /scannow              # System File Checker
sfc /verifyonly           # Verify system files
powercfg /energy          # Power efficiency report
powercfg -h off           # Disable hibernation
powercfg -h on            # Enable hibernation

# ---- SCHEDULED TASKS ----

schtasks /create /tn "TaskName" /tr "command" /sc daily /st 09:00
schtasks /delete /tn "TaskName" /f
schtasks /query /tn "TaskName"  # View task
schtasks /run /tn "TaskName"    # Run task now

# ---- SYSTEM RESTORE ----

rstrui                    # System restore GUI
wmic os get lastbootuptime  # Last boot time
wmic os get freephysicalmemory  # Free memory

# ================================================================
# 3. POWERSHELL COMMANDS
# ================================================================

# ---- FILE OPERATIONS ----

Get-ChildItem -Path C:\ -Recurse -Filter *.txt  # Find all .txt
Get-ChildItem -Recurse -File | Where-Object {$_.Length -gt 100MB}  # Files >100MB
Get-ChildItem -Recurse -File | Where-Object {$_.LastWriteTime -gt (Get-Date).AddDays(-7)}  # Files modified last 7 days
Get-ChildItem -Recurse -File | Sort-Object Length -Descending  # Sort by size

# Copy/Move/Delete
Copy-Item -Path C:\source -Destination D:\dest -Recurse
Move-Item -Path C:\file.txt -Destination D:\file.txt
Remove-Item -Path C:\file.txt -Force
Remove-Item -Path C:\folder -Recurse -Force
New-Item -Path C:\folder -ItemType Directory

# View File Content
Get-Content -Path C:\file.txt
Get-Content -Path C:\file.txt -Tail 50  # Last 50 lines
Get-Content -Path C:\file.txt -Wait  # Follow updates
Select-String -Path *.log -Pattern "ERROR"  # Search in files

# ---- SYSTEM INFORMATION ----

Get-ComputerInfo          # Full system info
Get-WmiObject -Class Win32_ComputerSystem  # System info
Get-WmiObject -Class Win32_OperatingSystem  # OS info
Get-WmiObject -Class Win32_Processor  # CPU info
Get-WmiObject -Class Win32_PhysicalMemory  # Memory info
Get-WmiObject -Class Win32_LogicalDisk  # Disk info
Get-WmiObject -Class Win32_NetworkAdapterConfiguration  # Network info
Get-HotFix                 # Installed updates
Get-Service                # All services
Get-Process                # Running processes
Get-Process | Sort-Object CPU -Descending  # Processes by CPU

# ---- NETWORK COMMANDS ----

Test-Connection -ComputerName google.com -Count 4  # Ping
Test-NetConnection -ComputerName google.com -Port 443  # Test port
Resolve-DnsName google.com  # DNS lookup
Get-NetIPAddress          # IP addresses
Get-NetRoute              # Routing table
Invoke-WebRequest -Uri https://example.com -OutFile file.html  # Download

# ---- USER MANAGEMENT ----

Get-LocalUser             # List local users
Get-LocalUser -Name username  # User details
New-LocalUser -Name "username" -Password (Read-Host -AsSecureString)  # Create user
Remove-LocalUser -Name "username"  # Delete user
Get-LocalGroup            # List groups
Add-LocalGroupMember -Group "Administrators" -Member "username"  # Add to admin
Get-LocalGroupMember -Group "Administrators"  # List admin members

# ---- DISK & STORAGE ----

Get-PSDrive               # List drives
Get-Disk                  # List disks
Get-Partition             # List partitions
Get-Volume                # List volumes
Optimize-Volume -DriveLetter C -ReTrim -Verbose  # Trim SSD

# ---- DATE & TIME ----

Get-Date                  # Current date/time
Get-Date -Format "yyyy-MM-dd HH:mm:ss"  # Custom format
(Get-Date).AddDays(7)     # Date 7 days from now
(Get-Date).AddDays(-7)    # Date 7 days ago

# ---- TEXT PROCESSING ----

Get-Content file.txt | Select-String "pattern"  # Search
Get-Content file.txt | Where-Object {$_ -match "pattern"}  # Filter
Get-Content file.txt | Sort-Object  # Sort
Get-Content file.txt | ForEach-Object {$_ -replace "old","new"}  # Replace
Import-Csv file.csv | Export-Csv new.csv  # CSV processing
ConvertTo-Json            # Convert to JSON
ConvertFrom-Json          # Parse JSON

# ---- COMPRESSION & ARCHIVING ----

Compress-Archive -Path C:\folder -DestinationPath C:\archive.zip
Expand-Archive -Path C:\archive.zip -DestinationPath C:\extract
Compress-Archive -Path *.txt -DestinationPath files.zip

# ---- SYSTEM MONITORING ----

Get-Counter                # Performance counters
Get-EventLog -LogName System -Newest 50  # System events
Get-EventLog -LogName Application -Newest 50  # App events
Get-WinEvent -MaxEvents 50 -FilterHashtable @{LogName='System'; Level=1}  # Errors only
Start-Sleep -Seconds 10   # Sleep

# ---- REMOTE MANAGEMENT ----

Enter-PSSession -ComputerName host  # Remote PowerShell
Invoke-Command -ComputerName host -ScriptBlock {Get-Process}  # Remote command
New-PSSession -ComputerName host  # New session
Get-PSSession             # List sessions
Remove-PSSession -Session $session  # Remove session

# ---- REGISTRY ----

Get-ItemProperty -Path "HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Run"  # Get registry
Set-ItemProperty -Path "HKLM:\SOFTWARE\..." -Name "Key" -Value "Value"  # Set registry
Remove-ItemProperty -Path "HKLM:\SOFTWARE\..." -Name "Key"  # Remove registry

# ================================================================
# 4. CMD ADVANCED (NETWORKING, SYSTEM, DISK, ETC.)
# ================================================================

# ---- CMD NETWORKING ADVANCED ----

# Advanced IP configuration
netsh int ip show config   # IP config
netsh int ip show interfaces  # Network interfaces
netsh int ip show addresses  # IP addresses

# Firewall management
netsh advfirewall show allprofiles  # Show firewall rules
netsh advfirewall set allprofiles state off  # Disable firewall
netsh advfirewall set allprofiles state on  # Enable firewall
netsh advfirewall firewall add rule name="Allow Port 443" dir=in action=allow protocol=TCP localport=443
netsh advfirewall firewall delete rule name="Allow Port 443"

# Routing
route print               # Show routing table
route add 10.0.0.0 mask 255.255.255.0 192.168.1.1  # Add route
route delete 10.0.0.0     # Delete route

# DNS
ipconfig /displaydns      # Show DNS cache
ipconfig /flushdns        # Clear DNS cache
nslookup google.com       # DNS lookup
nslookup -type=MX google.com  # MX record lookup
nslookup -type=TXT google.com  # TXT record lookup

# ARP
arp -a                    # Show ARP table
arp -d                    # Clear ARP cache

# NetBIOS
nbtstat -n                # NetBIOS names
nbtstat -A 192.168.1.1    # NetBIOS by IP
nbtstat -c                # NetBIOS cache

# Port scanning (basic)
netstat -ano | findstr :80   # Find port 80
netstat -ano | findstr ESTABLISHED  # Established connections
netstat -ano | findstr LISTENING  # Listening ports

# ---- CMD SYSTEM ADVANCED ----

# System information
systeminfo | findstr /C:"OS Name"  # OS name
systeminfo | findstr /C:"System Type"  # 32/64 bit
systeminfo | findstr /C:"Total Physical Memory"  # Total RAM
wmic cpu get name,numberofcores,numberoflogicalprocessors  # CPU info
wmic memorychip get capacity,speed  # Memory info
wmic diskdrive get model,size  # Disk info

# Driver management
driverquery                # List drivers
driverquery /v             # Verbose driver list
driverquery /si            # Signed drivers
pnputil /enum-drivers     # List installed drivers
pnputil /add-driver driver.inf /install  # Install driver

# Service management
sc query                  # List services
sc query state= all      # All services
sc start ServiceName     # Start service
sc stop ServiceName      # Stop service
sc delete ServiceName    # Delete service
sc config ServiceName start= auto  # Auto start

# Event logs
wevtutil qe System /c:10 /rd:true /f:text  # Last 10 system events
wevtutil qe Application /c:10 /rd:true /f:text  # Last 10 app events
wevtutil qe Security /c:10 /rd:true /f:text  # Security events

# ---- CMD DISK ADVANCED ----

# Disk management (inside diskpart)
diskpart                  # Enter diskpart
# Inside diskpart:
list disk
select disk 0
list partition
select partition 1
active                    # Mark partition as active
assign letter=E:          # Assign drive letter
format fs=ntfs quick      # Quick format
format fs=ntfs            # Full format
clean                     # Clean disk (WARNING - deletes all data)

# Volume management
mountvol                 # Show mount points
mountvol E: /d           # Delete mount point

# ---- CMD USER ADVANCED ----

# User management with net
net user                 # List users
net user username password /add  # Add user with password
net user username /active:yes  # Enable user
net user username /active:no  # Disable user
net user username /expires:never  # Account never expires
net user username /passwordreq:yes  # Password required
net user username /comment:"Comment"  # Add comment

# Group management
net localgroup           # List groups
net localgroup Administrators  # List admin members
net localgroup Administrators username /add  # Add to admin
net localgroup Administrators username /delete  # Remove from admin

# Domain user (if on domain)
net user username /domain  # Domain user info
net group /domain        # Domain groups
net group "Domain Admins" /domain  # Domain admins

# ---- CMD FILE ADVANCED ----

# Advanced file attributes
attrib                    # Show attributes
attrib +h file.txt       # Hide file
attrib -h file.txt       # Unhide file
attrib +s file.txt       # Mark as system
attrib -s file.txt       # Remove system
attrib +r file.txt       # Read-only
attrib -r file.txt       # Remove read-only

# File ownership
takeown /f file.txt      # Take ownership (administrator)
takeown /f C:\Windows    # Take ownership of directory
icacls file.txt /grant administrators:F  # Full control

# File sharing
net share sharename=C:\folder  # Share folder
net share sharename /delete  # Delete share

# ---- CMD DATE/TIME ADVANCED ----

# Date/time formatting
echo %DATE%              # Current date (format depends on locale)
echo %TIME%              # Current time
echo %DATE:/=%           # Remove slashes from date
echo %DATE:~0,10%        # First 10 chars of date
echo %TIME:~0,2%         # First 2 chars of time (hour)

# ---- CMD ENVIRONMENT ADVANCED ----

# Environment variables
set                       # All variables
set JAVA_HOME            # Show specific variable
setx VAR "value"         # Set permanent variable
setx VAR "value" /M      # Set system variable (admin)
setx VAR /M              # Delete system variable

# ---- CMD TROUBLESHOOTING ----

# System diagnostics
sfc /scannow             # System file checker
DISM /Online /Cleanup-Image /RestoreHealth  # DISM
chkdsk /f /r             # Check disk with repair
bootrec /fixmbr          # Fix MBR
bootrec /fixboot         # Fix boot sector
bootrec /rebuildbcd      # Rebuild BCD

# Memory diagnostics
mdsched                  # Memory diagnostic tool

# Network diagnostics
pathping google.com      # Traceroute with packet loss analysis
tracert -d google.com    # Traceroute without DNS
netsh int ip reset       # Reset IP stack
netsh winsock reset      # Reset Winsock

# ---- CMD SHORTCUTS & TIPS ----

# CMD Shortcuts
Tab                       # Autocomplete
Ctrl + C                  # Cancel current command
Ctrl + Z                  # Suspend
Ctrl + A                  # Go to beginning of line
Ctrl + E                  # Go to end of line
F7                        # Command history
F9                        # Run command by number from history
Ctrl + R                  # Search command history
Ctrl + Left/Right         # Jump words
Ctrl + Up/Down            # Previous/next command

# CMD Tips
cls                       # Clear screen
color 0a                 # Change color (green on black)
color ?                  # Show available colors
title "New Title"        # Change window title
prompt $P$G              # Show path in prompt
prompt $T                 # Show time in prompt
prompt $D                 # Show date in prompt

# Multiple commands
command1 & command2      # Run command1 then command2
command1 && command2     # Run command2 only if command1 succeeds
command1 || command2     # Run command2 only if command1 fails

# ---- CMD BATCH FILE COMMANDS ----

# Batch file commands
echo off                 # Turn off echo
@echo off                # Turn off echo (including command)
echo Hello World         # Print text
pause                    # Wait for keypress
cls                      # Clear screen
exit /b 0                # Exit with code 0
goto label               # Jump to label
:label                   # Define label
if condition command    # Conditional execution
for %%i in (list) do command  # Loop
set var=value           # Set variable
%var%                   # Use variable
%*                      # All parameters
%1                      # First parameter
%2                      # Second parameter

# ---- CMD REDIRECTION ----

command > file.txt       # Redirect output to file
command >> file.txt      # Append output to file
command 2> errors.txt    # Redirect errors to file
command > file.txt 2>&1  # Redirect both stdout and stderr
command < file.txt       # Take input from file
command | command2       # Pipe output to another command

# ================================================================
# 5. WINDOWS EXPLORER SEARCH SYNTAX
# ================================================================

# ---- DATE FILTERS ----

datemodified:today        # Files modified today
datemodified:yesterday    # Files modified yesterday
datemodified:this week    # This week
datemodified:last week    # Last week
datemodified:this month   # This month
datemodified:last month   # Last month
datemodified:1/1/2024     # Specific date
datemodified:>1/1/2024    # After date
datemodified:<1/1/2024    # Before date
datemodified:..1/1/2024   # Up to date
datemodified:1/1/2024..   # From date
datemodified:1/1/2024..1/31/2024  # Date range

# File created filters
datecreated:today         # Files created today
datecreated:yesterday     # Files created yesterday
datecreated:1/1/2024      # Specific creation date

# ---- SIZE FILTERS ----

size:empty                # Empty files (0 bytes)
size:tiny                 # 0-10 KB
size:small                # 10-100 KB
size:medium               # 100 KB - 1 MB
size:large                # 1-16 MB
size:huge                 # 16-128 MB
size:gigantic             # >128 MB
size:>500MB               # Larger than 500MB
size:<100KB               # Smaller than 100KB
size:1MB..10MB            # Size range

# ---- FILE TYPE FILTERS ----

ext:.txt                  # Text files
ext:.pdf                  # PDF files
ext:.docx                 # Word documents
ext:.xlsx                 # Excel files
ext:.pptx                 # PowerPoint files
ext:.jpg                  # JPEG images
ext:.png                  # PNG images
ext:.gif                  # GIF images
ext:.mp4                  # MP4 videos
ext:.mp3                  # MP3 audio
ext:.exe                  # Executable files
ext:.msi                  # Installer files
ext:.zip                  # ZIP archives
ext:.rar                  # RAR archives
ext:.7z                   # 7-Zip archives
ext:.log                  # Log files
ext:.tmp                  # Temporary files

# ---- ATTRIBUTE FILTERS ----

attributes:H              # Hidden files
attributes:S              # System files
attributes:R              # Read-only files
attributes:A              # Archive files
attributes:C              # Compressed files
attributes:E              # Encrypted files

# ---- NAME FILTERS ----

"filename"                # Exact file name
*pattern*                 # Wildcard search
pattern*                  # Starts with pattern
*pattern                  # Ends with pattern
~="regex"                 # Regular expression search

# ---- CONTENT FILTERS ----

content:"search text"     # Files containing text
content:"project report"  # Files with specific text

# ---- AUTHOR/PROPERTY FILTERS ----

author:"John Doe"         # Files by author
title:"presentation"      # Files with title
subject:"budget"          # Files with subject
tags:"important"          # Files with tags

# ---- COMBINED SEARCHES ----

datemodified:today ext:.docx author:"John"  # Today's Word docs by John
size:>50MB datemodified:this week  # Large files modified this week
datemodified:1/1/2024..1/31/2024 ext:.pdf  # PDFs from January 2024
type:document datemodified:yesterday  # Documents modified yesterday
kind:music size:>10MB     # Music files >10MB
kind:picture datemodified:this month  # Pictures from this month
kind:video size:gigantic  # Large video files
kind:email from:"john@example.com"  # Emails from specific sender

# ---- ADVANCED OPERATORS ----

NOT "keyword"             # Exclude keyword
OR                        # OR operator
( )                       # Group search terms
AND                       # AND operator (implied by space)
+                         # Must include term
-                         # Must exclude term

# ================================================================
# 6. CROSS-PLATFORM UTILITIES
# ================================================================

# ---- TEXT EDITORS ----

nano file.txt             # Simple terminal editor (Linux/macOS)
vim file.txt              # Vim editor
vi file.txt               # Vi editor
emacs file.txt            # Emacs editor
gedit file.txt            # GUI editor (Linux)
notepad file.txt          # Windows
notepad++ file.txt        # Notepad++ (Windows)
code file.txt             # VS Code (all platforms)

# ---- COMPRESSION (Cross-Platform) ----

# 7-Zip (available on all platforms)
7z a archive.7z folder    # Create
7z x archive.7z           # Extract
7z l archive.7z           # List contents

# tar (Linux/macOS/Windows with WSL)
tar -czf archive.tar.gz folder/
tar -xzf archive.tar.gz

# zip/unzip (all platforms)
zip -r archive.zip folder/
unzip archive.zip

# ---- NETWORK TOOLS ----

curl (all platforms)
wget (Linux/macOS, Windows via WSL)
nc (netcat) - Linux/macOS, Windows via WSL
nmap - Network scanner (all platforms)
tcpdump - Packet capture (Linux/macOS)

# ---- SYSTEM MONITORING ----

htop (Linux/macOS)
top (Linux/macOS, Windows via WSL)
nmon (Linux/macOS)
taskmgr (Windows GUI)
Activity Monitor (macOS GUI)

# ---- FILE SYNCHRONIZATION ----

rsync (Linux/macOS, Windows via WSL)
robocopy (Windows)
scp (Linux/macOS/Windows via WSL)

# ---- DATABASE TOOLS ----

sqlite3 database.db       # SQLite CLI
mysql -u user -p          # MySQL CLI
psql -U user database     # PostgreSQL CLI
mongo                     # MongoDB CLI

# ================================================================
# 7. ADVANCED FILTERS & SEARCH
# ================================================================

# ---- LINUX ADVANCED FIND ----

find . -type f -name "*.log" -exec grep -l "ERROR" {} \;  # Find error logs
find . -type f -mtime -1 -exec ls -l {} \;  # Files modified today
find . -type f -size +1G -exec du -h {} \;  # Files >1GB
find . -type f -perm 777 -exec ls -l {} \;  # Files with full permissions
find . -type d -empty      # Empty directories
find . -type f -name "*.tmp" -delete  # Delete all .tmp files

# ---- GREP ADVANCED ----

grep -r --include="*.py" "function" ./  # Search Python files only
grep -r --exclude="*.log" "pattern" ./  # Exclude log files
grep -B5 -A5 "error" file.log  # Show context
grep -l "pattern" * | xargs rm  # Delete files containing pattern
grep -L "pattern" *        # Files NOT containing pattern

# ---- AWK ADVANCED ----

awk '{print $1, $3}' file  # Print columns 1 and 3
awk 'NR>1 {print}' file    # Skip header row
awk '{sum+=$1} END {print sum}' file  # Sum column
awk -F',' '{print $2}' file.csv  # CSV delimiter
awk '/pattern/ {print}' file  # Lines matching pattern

# ---- SED ADVANCED ----

sed -n '10,20p' file      # Print lines 10-20
sed '/pattern/d' file     # Delete lines with pattern
sed -i.bak 's/old/new/g' file  # Replace with backup
sed '/^$/d' file          # Remove empty lines

# ---- POWERSHELL ADVANCED FILTERING ----

Get-ChildItem -Recurse -File | Where-Object {
    $_.LastWriteTime -gt (Get-Date).AddDays(-7) -and
    $_.Length -gt 100MB
} | Select-Object Name, Length, LastWriteTime

Get-Content file.log | Select-String "ERROR" -Context 2,2  # Context lines
Get-Process | Where-Object {$_.CPU -gt 50} | Sort-Object CPU -Descending
Get-Service | Where-Object {$_.Status -eq 'Stopped'}

# ================================================================
# 8. SYSTEM INFORMATION
# ================================================================

# ---- LINUX SYSTEM INFO ----

lshw                      # Hardware information
lscpu                     # CPU information
lspci                     # PCI devices
lsusb                     # USB devices
dmidecode                 # DMI/SMBIOS info
inxi -F                   # Full system info
neofetch                  # System info with logo
screenfetch               # System info

# ---- WINDOWS SYSTEM INFO (CMD) ----

systeminfo                # Full system info
wmic cpu get name,numberofcores,numberoflogicalprocessors  # CPU info
wmic memorychip get capacity,speed  # Memory info
wmic diskdrive get model,size  # Disk info
wmic os get version,lastbootuptime  # OS info
driverquery               # List drivers
msinfo32                  # System Information GUI

# ---- WINDOWS SYSTEM INFO (PowerShell) ----

Get-ComputerInfo
Get-CimInstance -ClassName Win32_ComputerSystem
Get-CimInstance -ClassName Win32_Processor
Get-CimInstance -ClassName Win32_PhysicalMemory
Get-CimInstance -ClassName Win32_DiskDrive
Get-CimInstance -ClassName Win32_OperatingSystem

# ================================================================
# 9. NETWORK COMMANDS (ALL PLATFORMS)
# ================================================================

# ---- LINUX NETWORK ----

ip addr                   # IP addresses
ip route                  # Routing table
ip neigh                  # ARP table
ss -tulpn                 # Listening ports
ss -tulpn | grep 443      # Check port 443
iptables -L -n -v         # Firewall rules (IPv4)
ip6tables -L -n -v        # Firewall rules (IPv6)
ufw status                # UFW firewall status
nft list ruleset          # nftables rules

# ---- WINDOWS NETWORK (CMD) ----

ipconfig /all             # All IP config
ipconfig /displaydns      # DNS cache
nbtstat -n                # NetBIOS names
netstat -b                # Processes using connections
netstat -e                # Ethernet statistics
netsh int ip show config  # IP config
netsh advfirewall show allprofiles  # Firewall rules
route print               # Routing table

# ---- WINDOWS NETWORK (PowerShell) ----

Get-NetIPConfiguration    # IP config
Get-NetAdapter            # Network adapters
Get-NetRoute              # Routing table
Get-NetNeighbor           # ARP table
Get-NetFirewallRule       # Firewall rules
Resolve-DnsName hostname  # DNS lookup
Test-NetConnection host -Port 443  # Test connection

# ================================================================
# 10. FILE OPERATIONS (ALL PLATFORMS)
# ================================================================

# ---- LINUX FILE OPS ----

cp -r source/ dest/       # Copy directory recursively
mv source/ dest/          # Move/rename
rm -rf folder/            # Remove directory and contents
rm -f file.txt            # Remove file (force)
mkdir -p path/to/folder   # Create nested directories
touch file.txt            # Create empty file / update timestamp
ln -s target link         # Symbolic link
ln target link            # Hard link
stat file.txt             # File statistics
file file.txt             # Determine file type

# ---- WINDOWS FILE OPS (CMD) ----

copy /y source dest       # Copy without confirmation
xcopy /s /e source dest   # Copy directories and subdirectories
robocopy source dest /e   # Robust copy (advanced)
move source dest          # Move/rename
del /s *.tmp              # Delete .tmp files recursively
rd /s /q folder           # Remove directory and contents
mkdir path\to\folder      # Create directory (nested)
type nul > file.txt       # Create empty file
attrib +h file.txt        # Hide file
attrib -h file.txt        # Unhide file

# ---- WINDOWS FILE OPS (PowerShell) ----

Copy-Item -Recurse source dest
Move-Item -Path source -Destination dest
Remove-Item -Recurse -Force path
New-Item -Path path -ItemType Directory
New-Item -Path file.txt -ItemType File
Set-Item -Path file.txt -Value "content"  # Write content
Add-Content -Path file.txt -Value "append"  # Append

# ================================================================
# 11. PROCESS MANAGEMENT
# ================================================================

# ---- LINUX PROCESS ----

ps aux | grep processname # Find process
killall processname      # Kill all processes by name
kill -STOP PID           # Pause process
kill -CONT PID           # Resume process
renice -n 10 -p PID      # Change process priority
nice -n 10 command       # Run with low priority
taskset -c 0-3 command   # Pin process to CPU cores
strace -p PID            # Trace system calls
ltrace -p PID            # Trace library calls

# ---- WINDOWS PROCESS (CMD) ----

tasklist /v              # Verbose process list
taskkill /PID 1234 /F    # Force kill process
start /low program.exe   # Low priority
start /high program.exe  # High priority
wmic process get name,processid,parentprocessid,priority

# ---- WINDOWS PROCESS (PowerShell) ----

Get-Process | Sort-Object CPU -Descending
Stop-Process -Name processname
Stop-Process -Id PID -Force
Start-Process -FilePath program.exe
Start-Process -FilePath program.exe -WindowStyle Hidden
Get-Process | Where-Object {$_.CPU -gt 50}

# ================================================================
# 12. USER MANAGEMENT
# ================================================================

# ---- LINUX USER ----

sudo adduser username    # Create user (Debian)
sudo useradd -m username # Create user (Red Hat)
sudo passwd username     # Change password
sudo usermod -aG sudo username  # Add to sudo group
sudo deluser username    # Delete user (Debian)
sudo userdel -r username # Delete user with home (Red Hat)
su - username            # Switch user
groups username          # Show user groups

# ---- WINDOWS USER (CMD) ----

net user                 # List users
net user username        # User details
net user username /add   # Create user
net user username password /add  # Create with password
net localgroup Administrators username /add  # Add to admin
net user username /delete  # Delete user
wmic useraccount get name,sid,status

# ---- WINDOWS USER (PowerShell) ----

Get-LocalUser
Get-LocalUser -Name username
New-LocalUser -Name username -Password (Read-Host -AsSecureString)
Add-LocalGroupMember -Group "Administrators" -Member username
Remove-LocalUser -Name username
Get-LocalGroupMember -Group "Administrators"

# ================================================================
# 13. DISK & STORAGE
# ================================================================

# ---- LINUX DISK ----

df -h                     # Disk usage
df -i                     # Inode usage
du -sh * | sort -h        # Directory sizes
fdisk -l                  # Partition table
parted -l                 # Partition info
lsblk -f                  # Filesystem info
mount | grep -E 'ext|btrfs|xfs|ntfs'  # Mounted filesystems
blkid                     # Block device UUIDs
smartctl -a /dev/sda      # SMART info
badblocks -sv /dev/sda    # Bad blocks check
fsck -f /dev/sda1         # Filesystem check

# ---- WINDOWS DISK (CMD) ----

chkdsk /f                 # Fix disk errors
chkdsk /r                 # Find bad sectors
diskpart                  # Disk partition tool
defrag C: /U /V           # Defragment and report
compact /c /s             # Compress files
wmic logicaldisk get name,size,freespace

# ---- WINDOWS DISK (PowerShell) ----

Get-PSDrive               # List drives
Get-Disk                  # List physical disks
Get-Partition             # List partitions
Get-Volume                # List volumes
Optimize-Volume -DriveLetter C -ReTrim  # Trim SSD
Get-PhysicalDisk | Select-Object Model,Size,MediaType
Repair-Volume -DriveLetter C -Scan  # Check volume health

# ================================================================
# 14. DATE & TIME
# ================================================================

# ---- LINUX DATE ----

date +%Y-%m-%d            # 2024-01-01
date +%H:%M:%S            # 14:30:00
date +%s                  # Unix timestamp
date -d "@timestamp"      # Convert timestamp
date -d "1 day ago"       # Yesterday
date -d "tomorrow"        # Tomorrow
timedatectl               # System time
ntpdate pool.ntp.org      # Sync time

# ---- WINDOWS DATE (CMD) ----

date /t                  # Show date
time /t                  # Show time
echo %DATE%              # Current date
echo %TIME%              # Current time

# ---- WINDOWS DATE (PowerShell) ----

Get-Date
Get-Date -Format "yyyy-MM-dd"
Get-Date -UFormat %s     # Unix timestamp
(Get-Date).AddDays(-1)   # Yesterday
(Get-Date).AddDays(1)    # Tomorrow

# ================================================================
# 15. TEXT PROCESSING
# ================================================================

# ---- LINUX TEXT ----

grep, awk, sed           # Powerful text tools
sort, uniq, wc           # Sorting and counting
cut, tr, paste           # Column operations
diff file1 file2         # Compare files
comm file1 file2         # Common lines
join file1 file2         # Join files
split file               # Split file

# ---- WINDOWS TEXT (CMD) ----

find, findstr            # Search text
sort                     # Sort text
type                     # Display text
more                     # Page view

# ---- WINDOWS TEXT (PowerShell) ----

Select-String            # Search text
Sort-Object              # Sort text
Where-Object             # Filter text
ForEach-Object           # Transform text
Group-Object             # Group text
Measure-Object           # Count text

# ================================================================
# 16. COMPRESSION & ARCHIVING
# ================================================================

# ---- LINUX COMPRESSION ----

tar -czf archive.tar.gz folder/    # Create .tar.gz
tar -xzf archive.tar.gz            # Extract .tar.gz
tar -cjf archive.tar.bz2 folder/   # Create .tar.bz2
tar -xjf archive.tar.bz2           # Extract .tar.bz2
tar -xvf archive.tar               # Extract .tar
zip -r archive.zip folder/         # Create .zip
unzip archive.zip                  # Extract .zip
gzip file.txt                      # Compress to .gz
gunzip file.txt.gz                 # Decompress .gz
bzip2 file.txt                     # Compress to .bz2
bunzip2 file.txt.bz2               # Decompress .bz2
xz file.txt                        # Compress to .xz
unxz file.txt.xz                   # Decompress .xz

# ---- WINDOWS COMPRESSION (CMD) ----

compact /c file.txt       # Compress
compact /u file.txt       # Uncompress

# ---- WINDOWS COMPRESSION (PowerShell) ----

Compress-Archive -Path folder -DestinationPath archive.zip
Expand-Archive -Path archive.zip -DestinationPath folder
Compress-Archive -Path *.txt -DestinationPath textfiles.zip

# ================================================================
# 17. PACKAGE MANAGEMENT
# ================================================================

# ---- APT (Debian/Ubuntu) ----

apt update               # Update package list
apt upgrade              # Upgrade all packages
apt install package      # Install package
apt remove package       # Remove package
apt purge package        # Remove with config
apt autoremove           # Remove unused dependencies
apt search keyword       # Search packages
apt show package         # Show package info
apt list --installed     # List installed packages

# ---- YUM (RHEL/CentOS) ----

yum install package      # Install package
yum remove package       # Remove package
yum update               # Update all
yum list installed       # List installed
yum search keyword       # Search packages
yum info package         # Package info

# ---- DNF (Fedora) ----

dnf install package      # Install package
dnf remove package       # Remove package
dnf update               # Update all
dnf list installed       # List installed
dnf search keyword       # Search packages
dnf info package         # Package info

# ---- PACMAN (Arch) ----

pacman -S package        # Install package
pacman -R package        # Remove package
pacman -Syu              # Update system
pacman -Q                # List installed
pacman -Ss keyword       # Search packages
pacman -Qi package       # Package info

# ---- WINDOWS (PowerShell) ----

# Choco (requires chocolatey)
choco install package
choco uninstall package
choco search keyword
choco list --local-only

# Winget (Windows 11)
winget install package
winget uninstall package
winget search keyword
winget list

# ================================================================
# 18. ENVIRONMENT VARIABLES
# ================================================================

# ---- LINUX ----

env                       # All environment variables
echo $PATH                # PATH variable
export VAR="value"        # Set variable
unset VAR                 # Unset variable
echo $HOME                # Home directory
echo $USER                # Current user
echo $SHELL               # Current shell
echo $PWD                 # Current directory
echo $OLDPWD              # Previous directory

# ---- WINDOWS (CMD) ----

set                       # All environment variables
echo %PATH%               # PATH variable
set VAR=value             # Set variable
set VAR=                  # Unset variable
echo %USERNAME%           # Current user
echo %COMPUTERNAME%       # Computer name
echo %OS%                 # Operating system

# ---- WINDOWS (PowerShell) ----

Get-ChildItem env:        # All environment variables
$env:PATH                 # PATH variable
$env:VAR = "value"        # Set variable
$env:VAR = $null          # Unset variable

# ================================================================
# 19. SYSTEM MONITORING
# ================================================================

# ---- LINUX MONITORING ----

top                       # Interactive process viewer
htop                      # Enhanced top
iotop                     # I/O monitoring
nmon                      # System monitor
vmstat 1                  # Virtual memory
iostat -x 1               # I/O statistics
sar -u 1 5                # CPU usage
sar -r 1 5                # Memory usage
watch -n 1 command        # Execute command every second
uptime                    # System uptime
dmesg | tail -20          # Kernel messages
journalctl -f             # System logs (systemd)

# ---- WINDOWS MONITORING (CMD) ----

tasklist /v               # Process list
systeminfo                # System info
wmic process get name,cpu,memory  # Process info
wmic os get freephysicalmemory  # Free memory

# ---- WINDOWS MONITORING (PowerShell) ----

Get-Process | Sort-Object CPU -Descending
Get-Process | Sort-Object WS -Descending  # Memory usage
Get-Counter -ListSet Processor  # Performance counters
Get-Counter "\Processor(_Total)\% Processor Time"
Get-EventLog -LogName System -Newest 50

# ================================================================
# 20. REMOTE CONNECTIONS
# ================================================================

# ---- LINUX REMOTE ----

ssh user@host             # SSH connection
ssh -p 2222 user@host     # SSH custom port
ssh -i key.pem user@host  # SSH with key
scp file user@host:/path  # Copy to remote
scp user@host:/path/file . # Copy from remote
rsync -avz user@host:/path/ /local/path/  # Sync from remote
rsync -avz /local/path/ user@host:/path/  # Sync to remote
sftp user@host            # Secure FTP
telnet host port          # Telnet (insecure)
nc -zv host port          # Netcat port scan

# ---- WINDOWS REMOTE (CMD) ----

mstsc                     # RDP client
mstsc /v:host             # RDP to host
telnet host port          # Telnet
ftp host                  # FTP client
winrs -r:host cmd         # Windows Remote Shell

# ---- WINDOWS REMOTE (PowerShell) ----

Enter-PSSession -ComputerName host  # PowerShell remote
Invoke-Command -ComputerName host -ScriptBlock {Get-Process}
Test-WSMan -ComputerName host  # Test WinRM

# ================================================================
# 21. SYSTEM RECOVERY
# ================================================================

# ---- LINUX RECOVERY ----

fsck -f /dev/sda1         # Check filesystem
badblocks -sv /dev/sda    # Check for bad blocks
dd if=/dev/sda of=/dev/sdb bs=4M  # Clone disk
dd if=/dev/sda of=backup.img bs=4M  # Create disk image
dd if=backup.img of=/dev/sda bs=4M  # Restore disk image
testdisk                  # Recover partitions
photorec                  # Recover files
chroot /mnt/sysroot       # Change root directory
grub-install /dev/sda     # Install GRUB
rescue                    # System rescue mode

# ---- WINDOWS RECOVERY ----

sfc /scannow              # System File Checker
DISM /Online /Cleanup-Image /RestoreHealth  # DISM
chkdsk /f                 # Check disk
chkdsk /r                 # Check disk with bad sector recovery
bootrec /fixmbr           # Fix MBR
bootrec /fixboot          # Fix boot sector
bootrec /rebuildbcd       # Rebuild BCD
systemrestore             # System restore
systemreset               # Reset PC (Windows 10/11)

# ---- WINDOWS RECOVERY (Advanced) ----

# Boot into recovery mode:
# Shift + Restart
# Advanced Startup Options
# Command Prompt

# ---- MACOS RECOVERY ----

# Command + R at boot
# Disk Utility
# Terminal in Recovery Mode

# ================================================================
# 22. CMD SHORTCUTS & TIPS
# ================================================================

# ---- CMD KEYBOARD SHORTCUTS ----

Tab                       # Autocomplete filenames/commands
Ctrl + C                  # Cancel current command
Ctrl + Z                  # Suspend current command
Ctrl + A                  # Go to beginning of line
Ctrl + E                  # Go to end of line
Ctrl + Home               # Go to beginning of buffer
Ctrl + End                # Go to end of buffer
Ctrl + Left Arrow         # Move left one word
Ctrl + Right Arrow        # Move right one word
Ctrl + Up Arrow           # Previous command in history
Ctrl + Down Arrow         # Next command in history
F7                        # Show command history
F9                        # Run command by number from history
Ctrl + R                  # Search command history
Ctrl + L                  # Clear screen (like cls)
Alt + F7                  # Clear command history
Ctrl + Delete             # Delete word after cursor
Ctrl + Backspace          # Delete word before cursor

# ---- CMD TIPS ----

cls                       # Clear screen
color 0a                 # Change text color (green on black)
color ?                  # Show available color codes
color 0c                 # Red on black
color 0e                 # Yellow on black
color 0f                 # White on black
title "New Window Title"  # Change window title
prompt $P$G              # Show full path in prompt
prompt $T                 # Show time in prompt
prompt $D                 # Show date in prompt
prompt $V                 # Show Windows version
prompt $N$G              # Show drive letter only
prompt $_                 # New line in prompt

# ---- CMD MULTIPLE COMMANDS ----

command1 & command2      # Run command1 then command2 (always)
command1 && command2     # Run command2 only if command1 succeeds
command1 || command2     # Run command2 only if command1 fails
(command1 & command2)    # Group commands

# ---- CMD REDIRECTION ----

command > file.txt       # Redirect stdout to file (overwrite)
command >> file.txt      # Redirect stdout to file (append)
command 2> errors.txt    # Redirect stderr to file
command 2>&1             # Redirect stderr to stdout
command > file.txt 2>&1  # Redirect both to file
command < file.txt       # Take input from file
command1 | command2      # Pipe stdout to stdin of command2

# ---- CMD BATCH FILE ----

# Basic batch file commands
@echo off                # Turn off command echoing (including this line)
echo Hello World         # Display text
pause                    # Pause and wait for keypress
cls                      # Clear screen
exit /b 0                # Exit with code 0
goto label               # Jump to label
:label                   # Define label

# Variables
set var=value           # Set variable
%var%                   # Use variable value
set /p var=Enter name:  # Get user input
set /a var=10+5         # Arithmetic
set var=                 # Clear variable

# Conditional execution
if exist file.txt echo File exists
if not exist file.txt echo File not found
if "%var%"=="value" echo Matched
if ERRORLEVEL 1 echo Error occurred

# Loops
for %%i in (file1 file2 file3) do echo %%i
for %%i in (*.txt) do echo %%i
for /l %%i in (1,1,10) do echo %%i

# Parameters
%*                      # All parameters
%1                      # First parameter
%2                      # Second parameter
%0                      # Script name

# ---- CMD ENVIRONMENT ----

# System environment
%SystemRoot%            # Windows directory
%ProgramFiles%          # Program Files directory
%CommonProgramFiles%    # Common Files directory
%AppData%               # AppData directory
%LocalAppData%          # Local AppData directory
%UserProfile%           # User profile directory
%AllUsersProfile%       # All users profile
%ProgramData%           # ProgramData directory
%Temp%                  # Temp directory
%Tmp%                   # Tmp directory
%Path%                  # PATH variable
%ComSpec%               # Command interpreter path
%OS%                    # Operating system
%Processor_Architecture% # CPU architecture

# ---- CMD NETWORK ENVIRONMENT ----

%ComputerName%          # Computer name
%UserName%              # Current username
%UserDomain%            # Domain name
%LogonServer%           # Logon server

# ---- CMD DATE/TIME VARIABLES ----

%DATE%                  # Current date (format depends on locale)
%TIME%                  # Current time (format depends on locale)
%DATE:~0,4%%DATE:~5,2%%DATE:~8,2%  # YYYYMMDD format
%TIME:~0,2%%TIME:~3,2%%TIME:~6,2%  # HHMMSS format

# ---- CMD COMMAND HISTORY ----

# View history
# Press F7 to show history dialog
# Use doskey /history to list history

# ---- CMD DOSKEY MACROS ----

doskey /macros          # List all macros
doskey ls=dir /b        # Create 'ls' alias
doskey ll=dir /w        # Create 'll' alias
doskey cls=cls          # Create 'cls' alias
doskey /exename=cmd.exe  # Set macro for specific executable

# Save/load macros
doskey /macros > macros.txt
doskey /macrofile=macros.txt

# ---- CMD QUICK REFERENCE ----

# Most common commands:
dir                     # List directory
cd                      # Change directory
cls                     # Clear screen
type                    # Display file
copy                    # Copy file
move                    # Move/rename file
del                     # Delete file
mkdir                   # Create directory
rmdir                   # Remove directory
ren                     # Rename file
find                    # Find text in file
findstr                 # Find string in files
ping                    # Test network connectivity
ipconfig                # IP configuration
netstat                 # Network statistics
tasklist                # List processes
taskkill                # Kill process
shutdown                # Shutdown/restart system
systeminfo              # System information

# ================================================================
# END OF CATALOG
# ================================================================
# 
# This catalog is a comprehensive reference of useful commands.
# It includes Linux, Windows CMD, PowerShell, and GUI search syntax.
# All commands are for legitimate system administration and use.
# 
# ---
# Author: F1REW0LF
# License: MIT - Free for Community
# Version: 1.0.0
# ================================================================
