# ═══════════════════════════════════════════════════════════════
#  C A T A L O G   O F   U S E F U L   C O M M A N D S
# ═══════════════════════════════════════════════════════════════
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
#  7. System Information (All Platforms)
#  8. Network Commands (All Platforms)
#  9. File Operations (All Platforms)
#  10. Process Management (All Platforms)
#  11. User Management (All Platforms)
#  12. Disk & Storage (All Platforms)
#  13. Date & Time (All Platforms)
#  14. Text Processing (All Platforms)
#  15. Compression & Archiving (All Platforms)
#  16. Package Management (All Platforms)
#  17. Environment Variables (All Platforms)
#  18. System Monitoring (All Platforms)
#  19. Remote Connections (All Platforms)
#  20. System Recovery (All Platforms)
#  21. CMD Shortcuts & Tips
#  22. Batch File Commands
#  23. Registry Commands
#  24. Windows Management Instrumentation (WMI)
#  25. Networking Advanced
#  26. Disk Management Advanced
#  27. User Management Advanced
#  28. Security Commands
#  29. System Utilities
#  30. Troubleshooting Commands
#  31. PowerShell Advanced
#  32. Linux Advanced
#  33. Quick Reference
#
# ═══════════════════════════════════════════════════════════════

# ================================================================
# 1. LINUX COMMANDS (BASH/ZSH)
# ================================================================

# ---- FILE OPERATIONS ----

ls -la                    # List all files with permissions
ls -lh                    # List with human-readable sizes
ls -lt                    # List sorted by modification time
ls -ltr                   # List sorted by time (newest last)
ls -R                     # List recursively
ls -S                     # Sort by size

cat file.txt              # Display full file
less file.txt             # View file page by page
head -n 20 file.txt       # Show first 20 lines
tail -n 50 file.txt       # Show last 50 lines
tail -f file.txt          # Follow file updates in real-time

find / -name "*.txt"      # Find files by name
find / -type f -size +100M # Find files larger than 100MB
find . -mtime -7          # Files modified in last 7 days
find . -mtime +30         # Files modified more than 30 days ago
find . -cmin -60          # Files changed in last 60 minutes

grep "pattern" file.txt   # Search pattern in file
grep -r "pattern" ./      # Recursive search in directory
grep -i "pattern" file    # Case-insensitive search
grep -v "pattern" file    # Exclude pattern
grep -l "pattern" *       # List files containing pattern
grep -n "pattern" file    # Show line numbers

chmod 755 file            # rwxr-xr-x
chmod 644 file            # rw-r--r--
chmod -R 755 directory    # Recursive permission change
chown user:group file     # Change owner and group
chown -R user:group dir   # Recursive owner change

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

# ---- LINUX ADVANCED ----

# Process priority
nice -n 10 command        # Run with low priority
renice -n 10 -p PID       # Change priority of running process
taskset -c 0-3 command    # Pin process to specific CPU cores

# System calls tracing
strace -p PID             # Trace system calls of process
ltrace -p PID             # Trace library calls of process

# Network advanced
iptables -L -n -v         # List firewall rules
iptables -A INPUT -p tcp --dport 22 -j ACCEPT  # Allow SSH
ufw status                # UFW firewall status
ufw allow 22/tcp          # Allow port 22
nft list ruleset          # nftables rules

# Disk advanced
smartctl -a /dev/sda      # SMART info
badblocks -sv /dev/sda    # Check for bad blocks
fsck -f /dev/sda1         # Filesystem check
blkid                     # Block device UUIDs

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

# ================================================================
# 3. POWERSHELL COMMANDS
# ================================================================

# ---- FILE OPERATIONS ----

Get-ChildItem -Path C:\ -Recurse -Filter *.txt
Get-ChildItem -Recurse -File | Where-Object {$_.Length -gt 100MB}
Get-ChildItem -Recurse -File | Where-Object {$_.LastWriteTime -gt (Get-Date).AddDays(-7)}
Get-ChildItem -Recurse -File | Sort-Object Length -Descending

Copy-Item -Path C:\source -Destination D:\dest -Recurse
Move-Item -Path C:\file.txt -Destination D:\file.txt
Remove-Item -Path C:\file.txt -Force
Remove-Item -Path C:\folder -Recurse -Force
New-Item -Path C:\folder -ItemType Directory

Get-Content -Path C:\file.txt
Get-Content -Path C:\file.txt -Tail 50
Get-Content -Path C:\file.txt -Wait
Select-String -Path *.log -Pattern "ERROR"

# ---- SYSTEM INFORMATION ----

Get-ComputerInfo
Get-WmiObject -Class Win32_ComputerSystem
Get-WmiObject -Class Win32_OperatingSystem
Get-WmiObject -Class Win32_Processor
Get-WmiObject -Class Win32_PhysicalMemory
Get-WmiObject -Class Win32_LogicalDisk
Get-WmiObject -Class Win32_NetworkAdapterConfiguration
Get-HotFix
Get-Service
Get-Process
Get-Process | Sort-Object CPU -Descending

# ---- NETWORK COMMANDS ----

Test-Connection -ComputerName google.com -Count 4
Test-NetConnection -ComputerName google.com -Port 443
Resolve-DnsName google.com
Get-NetIPAddress
Get-NetRoute
Invoke-WebRequest -Uri https://example.com -OutFile file.html

# ---- USER MANAGEMENT ----

Get-LocalUser
Get-LocalUser -Name username
New-LocalUser -Name "username" -Password (Read-Host -AsSecureString)
Remove-LocalUser -Name "username"
Get-LocalGroup
Add-LocalGroupMember -Group "Administrators" -Member "username"
Get-LocalGroupMember -Group "Administrators"

# ---- DISK & STORAGE ----

Get-PSDrive
Get-Disk
Get-Partition
Get-Volume
Optimize-Volume -DriveLetter C -ReTrim -Verbose

# ---- DATE & TIME ----

Get-Date
Get-Date -Format "yyyy-MM-dd HH:mm:ss"
(Get-Date).AddDays(7)
(Get-Date).AddDays(-7)

# ---- TEXT PROCESSING ----

Get-Content file.txt | Select-String "pattern"
Get-Content file.txt | Where-Object {$_ -match "pattern"}
Get-Content file.txt | Sort-Object
Get-Content file.txt | ForEach-Object {$_ -replace "old","new"}
Import-Csv file.csv | Export-Csv new.csv
ConvertTo-Json
ConvertFrom-Json

# ---- COMPRESSION & ARCHIVING ----

Compress-Archive -Path C:\folder -DestinationPath C:\archive.zip
Expand-Archive -Path C:\archive.zip -DestinationPath C:\extract
Compress-Archive -Path *.txt -DestinationPath files.zip

# ---- SYSTEM MONITORING ----

Get-Counter
Get-EventLog -LogName System -Newest 50
Get-EventLog -LogName Application -Newest 50
Get-WinEvent -MaxEvents 50 -FilterHashtable @{LogName='System'; Level=1}
Start-Sleep -Seconds 10

# ---- REMOTE MANAGEMENT ----

Enter-PSSession -ComputerName host
Invoke-Command -ComputerName host -ScriptBlock {Get-Process}
New-PSSession -ComputerName host
Get-PSSession
Remove-PSSession -Session $session

# ---- REGISTRY ----

Get-ItemProperty -Path "HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Run"
Set-ItemProperty -Path "HKLM:\SOFTWARE\..." -Name "Key" -Value "Value"
Remove-ItemProperty -Path "HKLM:\SOFTWARE\..." -Name "Key"

# ---- POWERSHELL ADVANCED ----

# Error handling
try {
    Get-Process -Name nonexistent -ErrorAction Stop
} catch {
    Write-Warning "Process not found: $_"
}

# Functions
function Get-SystemUptime {
    (Get-Date) - (Get-CimInstance Win32_OperatingSystem).LastBootUpTime
}

# Modules
Import-Module ActiveDirectory
Import-Module -Name "C:\Modules\MyModule.psm1"
Get-Module -ListAvailable

# Scheduled tasks in PowerShell
Register-ScheduledTask -TaskName "Backup" -Action (New-ScheduledTaskAction -Execute "cmd.exe" -Argument "/c backup.bat")
Unregister-ScheduledTask -TaskName "Backup" -Confirm:$false
Get-ScheduledTask -TaskName "Backup"

# Advanced filtering
Get-ChildItem -Recurse -File | Where-Object {
    $_.LastWriteTime -gt (Get-Date).AddDays(-7) -and
    $_.Length -gt 100MB -and
    $_.Extension -in '.log','.txt','.tmp'
} | Select-Object Name, Length, LastWriteTime

# ================================================================
# 4. CMD ADVANCED (NETWORKING, SYSTEM, DISK, ETC.)
# ================================================================

# ---- CMD NETWORKING ADVANCED ----

netsh int ip show config
netsh int ip show interfaces
netsh int ip show addresses

netsh advfirewall show allprofiles
netsh advfirewall set allprofiles state off
netsh advfirewall set allprofiles state on
netsh advfirewall firewall add rule name="Allow Port 443" dir=in action=allow protocol=TCP localport=443
netsh advfirewall firewall delete rule name="Allow Port 443"

route print
route add 10.0.0.0 mask 255.255.255.0 192.168.1.1
route delete 10.0.0.0

ipconfig /displaydns
ipconfig /flushdns
nslookup google.com
nslookup -type=MX google.com
nslookup -type=TXT google.com

arp -a
arp -d

nbtstat -n
nbtstat -A 192.168.1.1
nbtstat -c

netstat -ano | findstr :80
netstat -ano | findstr ESTABLISHED
netstat -ano | findstr LISTENING

# ---- CMD SYSTEM ADVANCED ----

systeminfo | findstr /C:"OS Name"
systeminfo | findstr /C:"System Type"
systeminfo | findstr /C:"Total Physical Memory"
wmic cpu get name,numberofcores,numberoflogicalprocessors
wmic memorychip get capacity,speed
wmic diskdrive get model,size

driverquery
driverquery /v
driverquery /si
pnputil /enum-drivers
pnputil /add-driver driver.inf /install

sc query
sc query state= all
sc start ServiceName
sc stop ServiceName
sc delete ServiceName
sc config ServiceName start= auto

wevtutil qe System /c:10 /rd:true /f:text
wevtutil qe Application /c:10 /rd:true /f:text
wevtutil qe Security /c:10 /rd:true /f:text

# ---- CMD DISK ADVANCED ----

diskpart
# Inside diskpart:
# list disk
# select disk 0
# list partition
# select partition 1
# active
# assign letter=E:
# format fs=ntfs quick
# format fs=ntfs
# clean

mountvol
mountvol E: /d

# ---- CMD USER ADVANCED ----

net user
net user username password /add
net user username /active:yes
net user username /active:no
net user username /expires:never
net user username /passwordreq:yes
net user username /comment:"Comment"

net localgroup
net localgroup Administrators
net localgroup Administrators username /add
net localgroup Administrators username /delete

net user username /domain
net group /domain
net group "Domain Admins" /domain

# ---- CMD FILE ADVANCED ----

attrib
attrib +h file.txt
attrib -h file.txt
attrib +s file.txt
attrib -s file.txt
attrib +r file.txt
attrib -r file.txt

takeown /f file.txt
takeown /f C:\Windows
icacls file.txt /grant administrators:F

net share sharename=C:\folder
net share sharename /delete

# ---- CMD DATE/TIME ADVANCED ----

echo %DATE%
echo %TIME%
echo %DATE:/=%
echo %DATE:~0,10%
echo %TIME:~0,2%

# ---- CMD ENVIRONMENT ADVANCED ----

set
set JAVA_HOME
setx VAR "value"
setx VAR "value" /M
setx VAR /M

# ---- CMD TROUBLESHOOTING ----

sfc /scannow
DISM /Online /Cleanup-Image /RestoreHealth
chkdsk /f /r
bootrec /fixmbr
bootrec /fixboot
bootrec /rebuildbcd

mdsched

pathping google.com
tracert -d google.com
netsh int ip reset
netsh winsock reset

# ---- CMD BATCH FILE COMMANDS ----

@echo off
echo Hello World
pause
cls
exit /b 0
goto label
:label

set var=value
%var%
set /p var=Enter name:
set /a var=10+5
set var=

if exist file.txt echo File exists
if not exist file.txt echo File not found
if "%var%"=="value" echo Matched
if ERRORLEVEL 1 echo Error occurred

for %%i in (file1 file2 file3) do echo %%i
for %%i in (*.txt) do echo %%i
for /l %%i in (1,1,10) do echo %%i

%*
%1
%2
%0

# ---- CMD SHORTCUTS & TIPS ----

# Keyboard Shortcuts:
# Tab - Autocomplete
# Ctrl + C - Cancel current command
# Ctrl + Z - Suspend
# Ctrl + A - Go to beginning of line
# Ctrl + E - Go to end of line
# Ctrl + Home - Go to beginning of buffer
# Ctrl + End - Go to end of buffer
# Ctrl + Left Arrow - Move left one word
# Ctrl + Right Arrow - Move right one word
# Ctrl + Up Arrow - Previous command
# Ctrl + Down Arrow - Next command
# F7 - Show command history
# F9 - Run command by number from history
# Ctrl + R - Search command history
# Ctrl + L - Clear screen
# Alt + F7 - Clear command history
# Ctrl + Delete - Delete word after cursor
# Ctrl + Backspace - Delete word before cursor

# Color codes:
# 0 = Black      8 = Gray
# 1 = Blue       9 = Light Blue
# 2 = Green      A = Light Green
# 3 = Aqua       B = Light Aqua
# 4 = Red        C = Light Red
# 5 = Purple     D = Light Purple
# 6 = Yellow     E = Light Yellow
# 7 = White      F = Bright White

color 0a          # Green on black
color 0c          # Red on black
color 0e          # Yellow on black
color 0f          # White on black
color ?           # Show available colors

title "New Window Title"
prompt $P$G       # Show full path
prompt $T         # Show time
prompt $D         # Show date
prompt $V         # Show Windows version
prompt $N$G       # Show drive letter only

cls               # Clear screen

# Command chaining:
command1 & command2      # Run command1 then command2 (always)
command1 && command2     # Run command2 only if command1 succeeds
command1 || command2     # Run command2 only if command1 fails
(command1 & command2)    # Group commands

# Redirection:
command > file.txt       # Redirect stdout (overwrite)
command >> file.txt      # Redirect stdout (append)
command 2> errors.txt    # Redirect stderr
command 2>&1             # Redirect stderr to stdout
command > file.txt 2>&1  # Redirect both
command < file.txt       # Take input from file
command1 | command2      # Pipe to command2

# ---- CMD ENVIRONMENT VARIABLES ----

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
%ComputerName%          # Computer name
%UserName%              # Current username
%UserDomain%            # Domain name
%LogonServer%           # Logon server

# ---- CMD DATE/TIME VARIABLES ----

%DATE%                  # Current date
%TIME%                  # Current time
%DATE:~0,4%%DATE:~5,2%%DATE:~8,2%  # YYYYMMDD
%TIME:~0,2%%TIME:~3,2%%TIME:~6,2%  # HHMMSS

# ================================================================
# 5. WINDOWS EXPLORER SEARCH SYNTAX
# ================================================================

# ---- DATE FILTERS ----

datemodified:today
datemodified:yesterday
datemodified:this week
datemodified:last week
datemodified:this month
datemodified:last month
datemodified:1/1/2024
datemodified:>1/1/2024
datemodified:<1/1/2024
datemodified:..1/1/2024
datemodified:1/1/2024..
datemodified:1/1/2024..1/31/2024

datecreated:today
datecreated:yesterday
datecreated:1/1/2024

# ---- SIZE FILTERS ----

size:empty
size:tiny                 # 0-10 KB
size:small                # 10-100 KB
size:medium               # 100 KB - 1 MB
size:large                # 1-16 MB
size:huge                 # 16-128 MB
size:gigantic             # >128 MB
size:>500MB
size:<100KB
size:1MB..10MB

# ---- FILE TYPE FILTERS ----

ext:.txt
ext:.pdf
ext:.docx
ext:.xlsx
ext:.pptx
ext:.jpg
ext:.png
ext:.gif
ext:.mp4
ext:.mp3
ext:.exe
ext:.msi
ext:.zip
ext:.rar
ext:.7z
ext:.log
ext:.tmp

# ---- ATTRIBUTE FILTERS ----

attributes:H              # Hidden
attributes:S              # System
attributes:R              # Read-only
attributes:A              # Archive
attributes:C              # Compressed
attributes:E              # Encrypted

# ---- NAME FILTERS ----

"filename"
*pattern*
pattern*
*pattern
~="regex"

# ---- CONTENT FILTERS ----

content:"search text"
content:"project report"

# ---- AUTHOR/PROPERTY FILTERS ----

author:"John Doe"
title:"presentation"
subject:"budget"
tags:"important"

# ---- COMBINED SEARCHES ----

datemodified:today ext:.docx author:"John"
size:>50MB datemodified:this week
datemodified:1/1/2024..1/31/2024 ext:.pdf
type:document datemodified:yesterday
kind:music size:>10MB
kind:picture datemodified:this month
kind:video size:gigantic
kind:email from:"john@example.com"

# ---- ADVANCED OPERATORS ----

NOT "keyword"
OR
( )
AND
+
-

# ================================================================
# 6. CROSS-PLATFORM UTILITIES
# ================================================================

nano file.txt             # Terminal editor (Linux/macOS)
vim file.txt              # Vim editor
vi file.txt               # Vi editor
emacs file.txt            # Emacs editor
gedit file.txt            # GUI editor (Linux)
notepad file.txt          # Windows
notepad++ file.txt        # Notepad++ (Windows)
code file.txt             # VS Code (all platforms)

7z a archive.7z folder    # Create 7z archive
7z x archive.7z           # Extract 7z archive
7z l archive.7z           # List contents

tar -czf archive.tar.gz folder/  # Create tar.gz
tar -xzf archive.tar.gz          # Extract tar.gz

zip -r archive.zip folder/       # Create zip
unzip archive.zip                # Extract zip

curl (all platforms)
wget (Linux/macOS, Windows via WSL)
nc (netcat) - Linux/macOS, Windows via WSL
nmap - Network scanner (all platforms)
tcpdump - Packet capture (Linux/macOS)

htop (Linux/macOS)
top (Linux/macOS, Windows via WSL)
nmon (Linux/macOS)
taskmgr (Windows GUI)
Activity Monitor (macOS GUI)

rsync (Linux/macOS, Windows via WSL)
robocopy (Windows)
scp (Linux/macOS/Windows via WSL)

sqlite3 database.db       # SQLite CLI
mysql -u user -p          # MySQL CLI
psql -U user database     # PostgreSQL CLI
mongo                     # MongoDB CLI

# ================================================================
# 7. SYSTEM INFORMATION (ALL PLATFORMS)
# ================================================================

# Linux:
lshw
lscpu
lspci
lsusb
dmidecode
inxi -F
neofetch
screenfetch

# Windows CMD:
systeminfo
wmic cpu get name,numberofcores,numberoflogicalprocessors
wmic memorychip get capacity,speed
wmic diskdrive get model,size
wmic os get version,lastbootuptime
driverquery
msinfo32

# Windows PowerShell:
Get-ComputerInfo
Get-CimInstance -ClassName Win32_ComputerSystem
Get-CimInstance -ClassName Win32_Processor
Get-CimInstance -ClassName Win32_PhysicalMemory
Get-CimInstance -ClassName Win32_DiskDrive
Get-CimInstance -ClassName Win32_OperatingSystem

# ================================================================
# 8. NETWORK COMMANDS (ALL PLATFORMS)
# ================================================================

# Linux:
ip addr
ip route
ip neigh
ss -tulpn
ss -tulpn | grep 443
iptables -L -n -v
ip6tables -L -n -v
ufw status
nft list ruleset

# Windows CMD:
ipconfig /all
ipconfig /displaydns
nbtstat -n
netstat -b
netstat -e
netsh int ip show config
netsh advfirewall show allprofiles
route print

# Windows PowerShell:
Get-NetIPConfiguration
Get-NetAdapter
Get-NetRoute
Get-NetNeighbor
Get-NetFirewallRule
Resolve-DnsName hostname
Test-NetConnection host -Port 443

# ================================================================
# 9. FILE OPERATIONS (ALL PLATFORMS)
# ================================================================

# Linux:
cp -r source/ dest/
mv source/ dest/
rm -rf folder/
rm -f file.txt
mkdir -p path/to/folder
touch file.txt
ln -s target link
stat file.txt
file file.txt

# Windows CMD:
copy /y source dest
xcopy /s /e source dest
robocopy source dest /e
move source dest
del /s *.tmp
rd /s /q folder
mkdir path\to\folder
type nul > file.txt
attrib +h file.txt
attrib -h file.txt

# Windows PowerShell:
Copy-Item -Recurse source dest
Move-Item -Path source -Destination dest
Remove-Item -Recurse -Force path
New-Item -Path path -ItemType Directory
New-Item -Path file.txt -ItemType File
Set-Item -Path file.txt -Value "content"
Add-Content -Path file.txt -Value "append"

# ================================================================
# 10. PROCESS MANAGEMENT (ALL PLATFORMS)
# ================================================================

# Linux:
ps aux | grep processname
killall processname
kill -STOP PID
kill -CONT PID
renice -n 10 -p PID
nice -n 10 command
taskset -c 0-3 command
strace -p PID
ltrace -p PID

# Windows CMD:
tasklist /v
taskkill /PID 1234 /F
start /low program.exe
start /high program.exe
wmic process get name,processid,parentprocessid,priority

# Windows PowerShell:
Get-Process | Sort-Object CPU -Descending
Stop-Process -Name processname
Stop-Process -Id PID -Force
Start-Process -FilePath program.exe
Start-Process -FilePath program.exe -WindowStyle Hidden
Get-Process | Where-Object {$_.CPU -gt 50}

# ================================================================
# 11. USER MANAGEMENT (ALL PLATFORMS)
# ================================================================

# Linux:
sudo adduser username
sudo useradd -m username
sudo passwd username
sudo usermod -aG sudo username
sudo deluser username
sudo userdel -r username
su - username
groups username

# Windows CMD:
net user
net user username
net user username /add
net user username password /add
net localgroup Administrators username /add
net user username /delete
wmic useraccount get name,sid,status

# Windows PowerShell:
Get-LocalUser
Get-LocalUser -Name username
New-LocalUser -Name username -Password (Read-Host -AsSecureString)
Add-LocalGroupMember -Group "Administrators" -Member username
Remove-LocalUser -Name username
Get-LocalGroupMember -Group "Administrators"

# ================================================================
# 12. DISK & STORAGE (ALL PLATFORMS)
# ================================================================

# Linux:
df -h
df -i
du -sh * | sort -h
fdisk -l
parted -l
lsblk -f
mount | grep -E 'ext|btrfs|xfs|ntfs'
blkid
smartctl -a /dev/sda
badblocks -sv /dev/sda
fsck -f /dev/sda1

# Windows CMD:
chkdsk /f
chkdsk /r
diskpart
defrag C: /U /V
compact /c /s
wmic logicaldisk get name,size,freespace

# Windows PowerShell:
Get-PSDrive
Get-Disk
Get-Partition
Get-Volume
Optimize-Volume -DriveLetter C -ReTrim
Get-PhysicalDisk | Select-Object Model,Size,MediaType
Repair-Volume -DriveLetter C -Scan

# ================================================================
# 13. DATE & TIME (ALL PLATFORMS)
# ================================================================

# Linux:
date +%Y-%m-%d
date +%H:%M:%S
date +%s
date -d "@timestamp"
date -d "1 day ago"
date -d "tomorrow"
timedatectl
ntpdate pool.ntp.org

# Windows CMD:
date /t
time /t
echo %DATE%
echo %TIME%

# Windows PowerShell:
Get-Date
Get-Date -Format "yyyy-MM-dd"
Get-Date -UFormat %s
(Get-Date).AddDays(-1)
(Get-Date).AddDays(1)

# ================================================================
# 14. TEXT PROCESSING (ALL PLATFORMS)
# ================================================================

# Linux:
grep, awk, sed
sort, uniq, wc
cut, tr, paste
diff file1 file2
comm file1 file2
join file1 file2
split file

# Windows CMD:
find, findstr
sort
type
more

# Windows PowerShell:
Select-String
Sort-Object
Where-Object
ForEach-Object
Group-Object
Measure-Object

# ================================================================
# 15. COMPRESSION & ARCHIVING (ALL PLATFORMS)
# ================================================================

# Linux:
tar -czf archive.tar.gz folder/
tar -xzf archive.tar.gz
tar -cjf archive.tar.bz2 folder/
tar -xjf archive.tar.bz2
tar -xvf archive.tar
zip -r archive.zip folder/
unzip archive.zip
gzip file.txt
gunzip file.txt.gz
bzip2 file.txt
bunzip2 file.txt.bz2
xz file.txt
unxz file.txt.xz

# Windows CMD:
compact /c file.txt
compact /u file.txt

# Windows PowerShell:
Compress-Archive -Path folder -DestinationPath archive.zip
Expand-Archive -Path archive.zip -DestinationPath folder
Compress-Archive -Path *.txt -DestinationPath textfiles.zip

# ================================================================
# 16. PACKAGE MANAGEMENT (ALL PLATFORMS)
# ================================================================

# APT (Debian/Ubuntu):
apt update
apt upgrade
apt install package
apt remove package
apt purge package
apt autoremove
apt search keyword
apt show package
apt list --installed

# YUM (RHEL/CentOS):
yum install package
yum remove package
yum update
yum list installed
yum search keyword
yum info package

# DNF (Fedora):
dnf install package
dnf remove package
dnf update
dnf list installed
dnf search keyword
dnf info package

# PACMAN (Arch):
pacman -S package
pacman -R package
pacman -Syu
pacman -Q
pacman -Ss keyword
pacman -Qi package

# Windows (PowerShell) - Chocolatey:
choco install package
choco uninstall package
choco search keyword
choco list --local-only

# Windows (PowerShell) - Winget:
winget install package
winget uninstall package
winget search keyword
winget list

# ================================================================
# 17. ENVIRONMENT VARIABLES (ALL PLATFORMS)
# ================================================================

# Linux:
env
echo $PATH
export VAR="value"
unset VAR
echo $HOME
echo $USER
echo $SHELL
echo $PWD
echo $OLDPWD

# Windows CMD:
set
echo %PATH%
set VAR=value
set VAR=
echo %USERNAME%
echo %COMPUTERNAME%
echo %OS%

# Windows PowerShell:
Get-ChildItem env:
$env:PATH
$env:VAR = "value"
$env:VAR = $null

# ================================================================
# 18. SYSTEM MONITORING (ALL PLATFORMS)
# ================================================================

# Linux:
top
htop
iotop
nmon
vmstat 1
iostat -x 1
sar -u 1 5
sar -r 1 5
watch -n 1 command
uptime
dmesg | tail -20
journalctl -f

# Windows CMD:
tasklist /v
systeminfo
wmic process get name,cpu,memory
wmic os get freephysicalmemory

# Windows PowerShell:
Get-Process | Sort-Object CPU -Descending
Get-Process | Sort-Object WS -Descending
Get-Counter -ListSet Processor
Get-Counter "\Processor(_Total)\% Processor Time"
Get-EventLog -LogName System -Newest 50

# ================================================================
# 19. REMOTE CONNECTIONS (ALL PLATFORMS)
# ================================================================

# Linux:
ssh user@host
ssh -p 2222 user@host
ssh -i key.pem user@host
scp file user@host:/path
scp user@host:/path/file .
rsync -avz user@host:/path/ /local/path/
rsync -avz /local/path/ user@host:/path/
sftp user@host
telnet host port
nc -zv host port

# Windows CMD:
mstsc
mstsc /v:host
telnet host port
ftp host
winrs -r:host cmd

# Windows PowerShell:
Enter-PSSession -ComputerName host
Invoke-Command -ComputerName host -ScriptBlock {Get-Process}
Test-WSMan -ComputerName host

# ================================================================
# 20. SYSTEM RECOVERY (ALL PLATFORMS)
# ================================================================

# Linux:
fsck -f /dev/sda1
badblocks -sv /dev/sda
dd if=/dev/sda of=/dev/sdb bs=4M
dd if=/dev/sda of=backup.img bs=4M
dd if=backup.img of=/dev/sda bs=4M
testdisk
photorec
chroot /mnt/sysroot
grub-install /dev/sda
rescue

# Windows:
sfc /scannow
DISM /Online /Cleanup-Image /RestoreHealth
chkdsk /f
chkdsk /r
bootrec /fixmbr
bootrec /fixboot
bootrec /rebuildbcd
systemrestore
systemreset

# ---- Windows Recovery Advanced ----
# Boot into recovery mode:
# Shift + Restart
# Advanced Startup Options
# Command Prompt

# ---- macOS Recovery ----
# Command + R at boot
# Disk Utility
# Terminal in Recovery Mode

# ================================================================
# 21. REGISTRY COMMANDS (WINDOWS)
# ================================================================

# ---- Registry Operations (CMD) ----

reg query "HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Run"
reg add "HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Run" /v "AppName" /t REG_SZ /d "C:\app.exe" /f
reg delete "HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Run" /v "AppName" /f
reg export "HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Run" backup.reg
reg import backup.reg
reg compare "HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Run" "HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Run" /s

# ---- Registry Operations (PowerShell) ----

Get-ItemProperty -Path "HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Run"
Set-ItemProperty -Path "HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Run" -Name "AppName" -Value "C:\app.exe"
Remove-ItemProperty -Path "HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Run" -Name "AppName"
New-Item -Path "HKLM:\SOFTWARE\MyApp" -Force
Remove-Item -Path "HKLM:\SOFTWARE\MyApp" -Recurse

# ---- Common Registry Paths ----

# Run at startup:
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Run
HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Run
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\RunOnce
HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\RunOnce

# File associations:
HKEY_CLASSES_ROOT\.txt
HKEY_CLASSES_ROOT\txtfile\shell\open\command

# Uninstall:
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Uninstall
HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Uninstall

# Network:
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters\Interfaces

# Security:
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Lsa
HKEY_LOCAL_MACHINE\SAM
HKEY_LOCAL_MACHINE\SECURITY

# ================================================================
# 22. WINDOWS MANAGEMENT INSTRUMENTATION (WMI)
# ================================================================

# ---- WMI Commands (CMD) ----

wmic process list brief
wmic process get name,processid,parentprocessid
wmic process where "name like '%explorer%'" get processid
wmic process where "commandline like '%notepad%'" delete

wmic service list brief
wmic service where "name='wuauserv'" get name,startmode,state

wmic product get name,version,vendor
wmic product where "name like '%Office%'" call uninstall

wmic logicaldisk where "drivetype=3" get name,size,freespace
wmic logicaldisk where "freespace<1000000000" get name,freespace

wmic os get caption,version,lastbootuptime
wmic os where "primary=true" get /format:value

wmic cpu get name,numberofcores,numberoflogicalprocessors
wmic memorychip get capacity,speed,manufacturer
wmic diskdrive get model,size

wmic bios get serialnumber,manufacturer,version
wmic baseboard get product,manufacturer,version

# ---- WMI Commands (PowerShell) ----

Get-WmiObject -Class Win32_Process
Get-WmiObject -Class Win32_Process | Select-Object Name, ProcessId, ParentProcessId

Get-WmiObject -Class Win32_Service
Get-WmiObject -Class Win32_Service | Where-Object {$_.State -eq 'Running'}

Get-WmiObject -Class Win32_Product
Get-WmiObject -Class Win32_LogicalDisk -Filter "DriveType=3"
Get-WmiObject -Class Win32_OperatingSystem
Get-WmiObject -Class Win32_Processor
Get-WmiObject -Class Win32_PhysicalMemory
Get-WmiObject -Class Win32_DiskDrive
Get-WmiObject -Class Win32_BIOS
Get-WmiObject -Class Win32_BaseBoard

# ---- WMI Query Examples ----

# Get last boot time
wmic os get lastbootuptime

# Get system uptime
wmic os get lastbootuptime
# PowerShell: (Get-Date) - (Get-CimInstance Win32_OperatingSystem).LastBootUpTime

# Get installed software
wmic product get name,version,vendor
# PowerShell: Get-WmiObject -Class Win32_Product | Select-Object Name, Version

# Get disk space
wmic logicaldisk where "drivetype=3" get name,size,freespace
# PowerShell: Get-WmiObject -Class Win32_LogicalDisk -Filter "DriveType=3"

# Get process information
wmic process where "name like '%explorer%'" get processid
# PowerShell: Get-WmiObject -Class Win32_Process | Where-Object {$_.Name -like "*explorer*"}

# ================================================================
# 23. SECURITY COMMANDS
# ================================================================

# ---- Windows Security ----

# Check Windows Defender status
powershell Get-MpPreference

# Update Windows Defender definitions
powershell Update-MpSignature

# Run quick scan
powershell Start-MpScan -ScanType QuickScan

# Run full scan
powershell Start-MpScan -ScanType FullScan

# Check firewall status
netsh advfirewall show allprofiles

# Enable/disable firewall
netsh advfirewall set allprofiles state on
netsh advfirewall set allprofiles state off

# Add firewall rule
netsh advfirewall firewall add rule name="Allow Port 443" dir=in action=allow protocol=TCP localport=443

# Delete firewall rule
netsh advfirewall firewall delete rule name="Allow Port 443"

# Check user account control
wmic os get caption,version,lastbootuptime
# PowerShell: Get-CimInstance -ClassName Win32_OperatingSystem

# ---- Linux Security ----

# Check firewall status
ufw status
iptables -L -n -v

# Check SELinux status
sestatus
getenforce

# Check AppArmor
aa-status

# Check PAM
cat /etc/pam.d/common-auth

# Check SSH security
cat /etc/ssh/sshd_config | grep -E "PermitRootLogin|PasswordAuthentication"

# Check sudoers
cat /etc/sudoers

# Check system logs
journalctl -xe
tail -f /var/log/auth.log

# ================================================================
# 24. SYSTEM UTILITIES
# ================================================================

# ---- Windows Utilities ----

# Task Manager
taskmgr

# Device Manager
devmgmt.msc

# Disk Management
diskmgmt.msc

# Event Viewer
eventvwr.msc

# Services
services.msc

# Computer Management
compmgmt.msc

# System Configuration
msconfig

# Registry Editor
regedit

# Group Policy Editor
gpedit.msc

# Local Security Policy
secpol.msc

# Performance Monitor
perfmon.msc

# Resource Monitor
resmon

# System Information
msinfo32

# DirectX Diagnostic
dxdiag

# Character Map
charmap

# Calculator
calc

# Command Prompt (Admin)
# Right-click Command Prompt → Run as administrator

# PowerShell (Admin)
# Right-click PowerShell → Run as administrator

# ---- Linux Utilities ----

# System Monitor
gnome-system-monitor

# Disk Usage Analyzer
baobab

# System Log Viewer
gnome-logs

# System Settings
gnome-control-center

# Terminal
gnome-terminal

# File Manager
nautilus

# Text Editor
gedit

# Calculator
gnome-calculator

# Screenshot
gnome-screenshot

# Screenshot (full screen)
gnome-screenshot -f

# Screenshot (window)
gnome-screenshot -w

# Screenshot (area)
gnome-screenshot -a

# ================================================================
# 25. TROUBLESHOOTING COMMANDS
# ================================================================

# ---- Windows Troubleshooting ----

# System File Checker
sfc /scannow

# DISM
DISM /Online /Cleanup-Image /RestoreHealth
DISM /Online /Cleanup-Image /CheckHealth
DISM /Online /Cleanup-Image /ScanHealth

# Check Disk
chkdsk /f
chkdsk /r
chkdsk /f /r

# Boot Recovery
bootrec /fixmbr
bootrec /fixboot
bootrec /rebuildbcd
bootrec /scanos

# Network Troubleshooting
ipconfig /release
ipconfig /renew
ipconfig /flushdns
netsh int ip reset
netsh winsock reset
netsh int ip reset log.txt

# Memory Diagnostic
mdsched

# System Restore
rstrui

# System Reset
systemreset

# ---- Linux Troubleshooting ----

# Check disk
fsck -f /dev/sda1
fsck -y /dev/sda1

# Check filesystem
df -h
df -i

# Check memory
free -h
vmstat 1

# Check processes
ps aux
top
htop

# Check network
ping -c 4 google.com
traceroute google.com
netstat -tulpn
ss -tulpn

# Check logs
dmesg | tail -20
journalctl -xe
tail -f /var/log/syslog

# Check hardware
lshw
lspci
lsusb

# ================================================================
# 26. QUICK REFERENCE
# ================================================================

# ---- Linux Quick Reference ----

# File Management
ls -la          # List all files
cp -r           # Copy recursive
mv              # Move/rename
rm -rf          # Remove recursive force
mkdir -p        # Create nested directories
touch           # Create empty file
cat             # Display file
less            # View file
tail -f         # Follow file

# System
uname -a        # All system info
hostnamectl     # System info
systemctl       # System services
journalctl      # System logs
df -h           # Disk space
du -sh          # Directory size
free -h         # Memory usage
uptime          # System uptime

# Network
ip addr         # IP addresses
ping            # Network test
traceroute      # Network route
netstat -tulpn  # Listening ports
ss -tulpn       # Modern netstat
curl            # HTTP requests
wget            # Download files

# ---- Windows CMD Quick Reference ----

# File Management
dir             # List files
copy            # Copy files
move            # Move/rename
del             # Delete files
mkdir           # Create directory
rmdir           # Remove directory
type            # Display file

# System
systeminfo      # System info
tasklist        # List processes
taskkill        # Kill process
shutdown        # Shutdown/restart
chkdsk          # Check disk
sfc /scannow    # System file check

# Network
ipconfig        # IP configuration
ping            # Network test
tracert         # Network route
netstat -ano    # Connections with PID
nslookup        # DNS lookup

# ---- PowerShell Quick Reference ----

# File Management
Get-ChildItem   # List files
Copy-Item       # Copy files
Move-Item       # Move/rename
Remove-Item     # Delete files
New-Item        # Create directory/file
Get-Content     # Display file

# System
Get-ComputerInfo         # System info
Get-Process              # List processes
Stop-Process             # Kill process
Get-Service              # List services
Restart-Computer         # Restart computer
Shutdown-Computer        # Shutdown computer

# Network
Test-Connection          # Network test
Test-NetConnection       # Advanced network test
Resolve-DnsName          # DNS lookup
Get-NetIPAddress         # IP addresses

# ---- Windows Explorer Search Quick Reference ----

datemodified:today       # Today's files
size:>100MB              # Large files
ext:.txt                 # Text files
attributes:H             # Hidden files
"filename"               # Exact file name
*pattern*                # Wildcard search
content:"text"           # Files containing text
author:"John"            # Files by author
NOT "keyword"            # Exclude keyword
OR                       # OR operator

# ---- Common Keyboard Shortcuts ----

# Linux Terminal:
Ctrl + C        # Cancel command
Ctrl + D        # Exit terminal
Ctrl + Z        # Suspend command
Ctrl + L        # Clear screen
Ctrl + R        # Search history
Ctrl + U        # Delete line
Ctrl + K        # Delete to end
Ctrl + W        # Delete word
Ctrl + A        # Beginning of line
Ctrl + E        # End of line
Tab             # Autocomplete
Alt + F2        # Run command

# Windows CMD:
Ctrl + C        # Cancel command
Ctrl + Z        # Suspend command
Ctrl + L        # Clear screen
Ctrl + R        # Search history
Ctrl + A        # Beginning of line
Ctrl + E        # End of line
F7              # Command history
Tab             # Autocomplete

# PowerShell:
Ctrl + C        # Cancel command
Ctrl + D        # Exit PowerShell
Ctrl + L        # Clear screen
Ctrl + R        # Search history
Ctrl + Space    # Autocomplete
Ctrl + Left     # Jump left word
Ctrl + Right    # Jump right word

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
# ================================================================
