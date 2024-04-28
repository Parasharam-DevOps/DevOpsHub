📍Some Important Linux Commands
DevOps Engineer Should Aware Of :

###SYSTEM INFORMATION
uname -a # Display Linux system information
uname -r # Display kernel release information
lsb_release -a # Show which version of ubuntu installed
uptime # Show how long the system has been running the load
hostname # Show system host name
hostname -I # Display the IP addresses of the host
last reboot # Show system reboot history
date # Show the current date and time
cal # Show this month's calendar
w # Display who is online
whoami # Who you are logged in as

###Networking commands-
Ifconfig # To display the system ip address.
Netstat -anlp | grep httpd # To see the apache is running or not.
Ping <hostname> # To display to see the connection remote to available or not.
dig <hostname> # To display the repose time and remote server.
nslookup <hostname> # To display the hostname is dns registered or not.
Telnet <hostname portnum> # To see the remote server and port is available
Nmap <hostname> # It is used for port number scanners.
Traceroute <hostname> -# To reach the website path in 30 hops in display.

###PERFORMANCE MONITORING ANDSTATISTICS
top # Display and manage the top processes
mpstat 1 # Display processor related statistics
vmstat 1 # Display virtual memory statistics
iostat 1 # Display I/O statistics
tcpdump -i eth0 # Capture and display all packets on interface eth0 tcpdump -i eth0 'port 80' # Monitor all traffic on port 80 ( HTTP )
lsof # List all open files on the system
lsof -u user # List files opened by user
free -h # Display free and used memory
watch df -h # Execute "df -h", showing periodic updates

###USER INFORMATION ANDMANAGEMENT
id # Display the user and group ids of your current user.
last # Display the last users who have logged onto the system.
who # Show who is logged into the system.
groupadd test # Create a group named "test".
useradd -c "John Smith" -m john # Create an account named john, with a
comment of "John Smith" and create the user's home directory.
userdel john # Delete the john account.
usermod -aG sales john # Add the john account to the sales group

###FILE AND DIRECTORY COMMANDS
ls -al # List all files in a long listing (detailed) format
pwd # Display the present working directory
mkdir directory # Create a directory
rm file # Remove (delete) file
rm -r directory # Remove the directory and its contents recursively
rm -f file # Force removal of file without prompting for confirmation
rm -rf directory # Forcefully remove directory recursively
rmdir # Delete a file or files
cp file1 file2 # Copy file1 to file2
cp -r source_directory destination # Copy source_directory recursively to destination.
If destination exists, copy source_directory into destination, otherwise create destination with the contents of source_directory.
mv file1 file2 # Rename or move file1 to file2. If file2 is an existing directory, move file1 into directory file2
