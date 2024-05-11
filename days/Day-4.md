# Learned
### Lab-Setup
  - Installing VMware/VirtualBox  
  - Configuring VirtualBox  
  - Installing Kali Linux  

### Intro to Linux
  - [Exploring Kali Linux](#exploring-kali-linux)  
  - [Sudo Overview](#sudo-overview)  
  - [Navigating File System](#navigating-file-system)  
  - [Users and Privileges](#users-and-privileges)  
  - [Common Network Commands](#common-network-commands)  
  - [Viewing, Creating, and Editing Files](#viewing-creating-and-editing-files)  
  - [Starting and Stopping Services](#starting-and-stopping-services)  
  - [Installing and Updating Tools](#installing-and-updating-tools)  

# A Few Details
### Exploring Kali Linux
Kali Linux is a specialized Linux distribution designed for digital forensics, penetration testing, and ethical hacking purposes. It is a powerful and widely used operating system used by cybersecurity professionals, researchers, and enthusiasts.

Kali Linux is based on Debian Linux. It provides a comprehensive set of pre-installed tools and software packages specifically tailored for various security testing and hacking purposes.

The main goal of Kali Linux is to provide a robust and all-in-one platform for performing security assessments, vulnerability analysis, network scanning, password cracking, wireless security testing, and much more. It includes tools for web application testing, reverse engineering, exploit development, and secure communication as well.

Kali Linux is designed with security in mind and comes with features like full disk encryption, secure shell access, and regular updates to ensure a secure and up-to-date environment for its users.

While Kali Linux is a powerful tool for security professionals, it is important to use it responsibly and within legal boundaries. Ethical hacking and security testing should always be performed with proper authorization and adherence to applicable laws and regulations.  

### Sudo Overview  
The `sudo` command in Linux allows a user with appropriate privileges to execute commands as a superuser or another user. It is commonly used to perform administrative tasks that require elevated privileges. Here's an example of how `sudo` is used:

Let's say you want to install a software package using the `apt` package manager, but it requires administrative privileges. You can use `sudo` to execute the `apt` command with elevated privileges. Here's the command:

```bash
sudo apt install <package_name>

```

For instance, if you want to install the package named "nginx" on an Ubuntu system, you can use the following command:

```bash
sudo apt install nginx

```

After running this command, you will be prompted to enter your password. Once you provide the correct password, the command will be executed with superuser privileges, allowing you to install the "nginx" package on the system.

Please note that the availability and configuration of `sudo` can vary depending on the Linux distribution and the user's privileges. Additionally, the `sudo` command can be used for various other administrative tasks, such as editing system files, managing services, and executing critical commands.  

### Navigating File System 
`pwd` (Print Working Directory):

- Explanation: Displays the current working directory. Example: Running `pwd` in the terminal would show the absolute path of the current directory, such as "/home/user/documents".

`cd` (Change Directory):

- Explanation: Allows you to change the current working directory. Example: Running `cd /home/user/documents` would change the directory to "/home/user/documents".

`cd ..` (Change to Parent Directory):

- Explanation: Moves up one level in the directory hierarchy. Example: Running `cd ..` in "/home/user/documents" would move to the "/home/user" directory.

`ls` (List Directory Contents):

- Explanation: Lists the files and directories in the current directory. Example: Running `ls` would display the files and directories in the current directory.

`ls -la` (List Detailed Directory Contents):

- Explanation: Lists detailed information about files and directories, including hidden files. Example: Running `ls -la` would display a detailed list of files and directories, including hidden files, in the current directory.

`mkdir` (Make Directory):

- Explanation: Creates a new directory. Example: Running `mkdir new_folder` would create a new directory named "new_folder" in the current directory.

`rmdir` (Remove Directory):

- Explanation: Removes an empty directory. Example: Running `rmdir empty_folder` would remove the directory named "empty_folder" if it is empty.

`man` (Manual):

- Explanation: Displays the manual pages for a specified command. Example: Running `man ls` would show the manual pages with detailed information about the `ls` command.

`echo`:

- Explanation: Displays text or variables as output. Example: Running `echo "Hello, world!"` would output "Hello, world!" in the terminal.

`>` (Output Redirection):

- Explanation: Redirects the output of a command to a file and overwrites the file if it already exists.Example: Running `echo "Hello" > greeting.txt` would write the text "Hello" to a file named "greeting.txt" or overwrite the file if it exists.

`>>` (Append Output):

- Explanation: Redirects the output of a command and appends it to a file. Example: Running `echo "World!" >> greeting.txt` would append the text "World!" to the end of the "greeting.txt" file.

`rm` (Remove):

- Explanation: Deletes files or directories. Example: Running `rm file.txt` would delete the file named "file.txt" from the current directory.

`mv` (Move):

- Explanation: Moves or renames files and directories. Example: Running `mv file.txt new_directory/file_renamed.txt` would move the file "file.txt" to the "new_directory" and rename it as "file_renamed.txt".

`cp` (Copy):

- Explanation: Copies files and directories. Example: Running `cp file.txt backup/file_copy.txt` would create a copy of "file.txt" named "file_copy.txt" in the "backup" directory.

`locate`:

- Explanation: Searches for files and directories in a prebuilt database. Example: Running `locate myfile.txt` would search for the file named "myfile.txt" in the prebuilt database and display its path if found.

`updatedb`:

- Explanation: Updates the database used by the `locate` command to reflect recent changes in the file system. Example: Running `updatedb` would update the database, allowing the `locate` command to provide up-to-date search results.

`passwd`:

- Explanation: Allows a user to change their password. Example: Running `passwd` would prompt the user to enter their current password and then set a new password.

Remember to exercise caution when using commands like `rm` as they can permanently delete files. It's always a good practice to double-check before executing such commands.

### Users and Privileges
In the `ls -la` output, the "rwx" refers to the permissions associated with a file or directory. The permissions are displayed for three different entities: the owner, the group, and other users. Each entity has three permission categories: read (r), write (w), and execute (x). Here's a breakdown of what each permission category represents:

- Read (r): Allows the entity to read or view the contents of a file or the names of files within a directory.
- Write (w): Enables the entity to modify or write to a file or add, delete, or rename files within a directory.
- Execute (x): Grants the entity the permission to execute a file or enter a directory. For directories, execute permission is required to access its contents.

In the `ls -la` output, the permissions are displayed as a series of nine characters. The first character represents the file type (e.g., `-` for a regular file, `d` for a directory). The next three characters represent the owner's permissions, followed by the group's permissions, and then the permissions for other users.

For example, let's consider an `ls -la` output line:

```
-rwxr-x--- 1 user group 4096 May 10 12:34 myfile.txt

```

In this example, the permissions are broken down as follows:

- `rwxr-x---`: The first character indicates that it is a regular file. The following three characters (`rwx`) represent the owner's permissions (read, write, and execute). The next three characters (`r-x`) represent the group's permissions (read and execute). The last three characters (`--`) represent the permissions for other users (no permissions).
- `1`: Indicates the number of hard links to the file.
- `user`: Refers to the owner of the file.
- `group`: Refers to the group assigned to the file.
- `4096`: Indicates the file size in bytes.
- `May 10 12:34`: Specifies the date and time of the last modification.
- `myfile.txt`: Represents the name of the file.

It's worth noting that if a permission is not granted for a particular entity, a hyphen (`-`) is displayed in its place. Additionally, the output can include additional information such as special permissions, ownership, and timestamps.

Here are explanations and examples of the commands mentioned in this video. Please note, Teachable blocks the mention of some of the sensitive paths shown in the video, so we cannot display them in text format here:

`chmod` (Change Mode):

- Explanation: Changes the permissions of a file or directory. Example: Running `chmod +x script.sh` would add the execute permission to the file "script.sh", allowing it to be executed as a script.

`adduser`:

- Explanation: Creates a new user account. Example: Running `adduser john` would create a new user account with the username "john" and prompt for additional user information.

`su` (Switch User):

- Explanation: Allows a user to switch to another user account. Example: Running `su jane` would switch to the user account "jane" after entering the password for that account.

`/etc/sudoers`:

- Explanation: Displays the content of the "/etc/sudoers" file, which contains configuration information for the `sudo` command. Example: Running `/etc/sudoers` would display the configuration directives for `sudo` access and permissions.

`sudo -l`:

- Explanation: Lists the commands a user is allowed to run with `sudo` privileges. Example: Running `sudo -l` would display the commands and permissions available to the current user with `sudo` access.

Please note that some of these commands require administrative privileges, and caution should be exercised when modifying system files or working with user accounts.  

### Common Network Commands
`ip a`:

- Explanation: Displays the network interfaces and their associated IP addresses.Example: Running `ip a` would show information about network interfaces, including their IP addresses, MAC addresses, and other details.

`ifconfig`:

- Explanation: Displays the configuration and status of network interfaces. Example: Running `ifconfig` would show the configuration details, including IP addresses, MAC addresses, and other information for active network interfaces.

`iwconfig`:

- Explanation: Displays the configuration and status of wireless network interfaces. Example: Running `iwconfig` would show the configuration details, such as wireless signal strength, frequency, and encryption information, for active wireless interfaces.

`ip n`:

- Explanation: Displays the Neighbor Table, which contains the IP-to-MAC address mappings for devices in the local network. Example: Running `ip n` would show the IP and MAC addresses of devices that have recently communicated with the current device.

`arp -a`:

- Explanation: Displays the ARP (Address Resolution Protocol) cache, which maps IP addresses to MAC addresses. Example: Running `arp -a` would show the IP and MAC addresses of devices that have been resolved recently by the ARP protocol.

`ip r`:

- Explanation: Displays the routing table, which contains information about network routes. Example: Running `ip r` would show the routing table, including destination networks, gateway IP addresses, and network interfaces.

`route`:

- Explanation: Displays or manipulates the IP routing table. Example: Running `route` would display the routing table, similar to the `ip r` command.

`ping`:

- Explanation: Sends ICMP echo requests to a specified IP address to check network connectivity and measure round-trip time. Example: Running `ping 8.8.8.8` would send ICMP echo requests to the IP address "8.8.8.8" (Google's DNS server) and display the round-trip time and packet loss statistics.

These commands are commonly used for network troubleshooting, configuration, and gathering network-related information in Linux systems.  

### Viewing, Creating and Editing Files  
`echo "hello" > hey.txt`:

- Explanation: Creates a new file named "hey.txt" with the content "hello" and overwrites the file if it already exists.Example: Running `echo "hello" > hey.txt` would create a file named "hey.txt" and write the word "hello" into it.

`echo "hello again" >> hey.txt`:

- Explanation: Appends the content "hello again" to an existing file named "hey.txt" or creates a new file if it doesn't exist.Example: Running `echo "hello again" >> hey.txt` would append the text "hello again" to the end of the "hey.txt" file.

`touch newfile.txt`:

- Explanation: Creates a new empty file named "newfile.txt" or updates the timestamp of an existing file to the current time.Example: Running `touch newfile.txt` would create an empty file named "newfile.txt" if it doesn't exist or update its timestamp if it already exists.

`nano newfile.txt`:

- Explanation: Opens the text editor Nano and allows you to create or edit the content of a file named "newfile.txt".Example: Running `nano newfile.txt` would open the Nano editor, where you can enter or modify text in the "newfile.txt" file.

`mousepad newfile.txt`:

- Explanation: Opens the Mousepad text editor and allows you to create or edit the content of a file named "newfile.txt".Example: Running `mousepad newfile.txt` would open the Mousepad editor, where you can enter or modify text in the "newfile.txt" file.

These commands are commonly used for file manipulation and editing in Linux systems. The `echo` command is used to print text or variables to the terminal or redirect them to files. The `touch` command is used to create or update file timestamps. The `nano` and `mousepad` commands are text editors that allow you to create and modify files directly from the terminal.  

### Starting and Stopping Services
`sudo service apache2 start`:

- Explanation: Starts the Apache web server service.Example: Running `sudo service apache2 start` would initiate the Apache web server and make it available for serving web pages.

`sudo service apache2 stop`:

- Explanation: Stops the Apache web server service. Example: Running `sudo service apache2 stop` would halt the running Apache web server, shutting down any active web page serving.

`python3 -m http.server 80`:

- Explanation: Starts a simple HTTP server using Python on port 80.Example: Running `python3 -m http.server 80` would start a basic HTTP server on port 80, allowing you to serve files from the current directory.

`sudo systemctl enable ssh`:

- Explanation: Enables the SSH (Secure Shell) service to start automatically on system boot. Example: Running `sudo systemctl enable ssh` would configure the system to start the SSH service during system startup.

`sudo systemctl disable ssh`:

- Explanation: Disables the SSH service from starting automatically on system boot. Example: Running `sudo systemctl disable ssh` would prevent the SSH service from starting automatically during system startup.

These commands are frequently used in Linux systems for managing services, starting and stopping processes, and enabling or disabling specific services at system startup. The `sudo` command is used to execute commands with superuser privileges. The `service` and `systemctl` commands are used to manage system services.  

### Installing and Updating Tools
`sudo apt update && sudo apt upgrade`:

- Explanation: Updates the package lists and upgrades installed packages on a Debian-based Linux system using the APT package manager. Example: Running `sudo apt update && sudo apt upgrade` would update the package lists to retrieve information about available updates, and then upgrade the installed packages to their latest versions.

`sudo apt install cron-daemon-common`:

- Explanation: Installs the "cron-daemon-common" package using APT. Cron is a time-based job scheduler in Linux systems, and the "cron-daemon-common" package provides common files and utilities for the cron daemon. Example: Running `sudo apt install cron-daemon-common` would download and install the "cron-daemon-common" package on the system.

`sudo git clone https://github.com/Dewalt-arch/pimpmykali.git`:

- Explanation: Clones a Git repository from the specified URL using the Git version control system. Example: Running `sudo git clone https://github.com/Dewalt-arch/pimpmykali.git` would clone the repository from the given URL and create a local copy of the repository's files and version history.

These commands are commonly used in Linux systems for updating packages, installing new software, and managing version-controlled repositories. The `sudo` command is used to execute commands with superuser privileges. The `apt` command is used for package management in Debian-based distributions. The `git` command is used for version control and working with Git repositories.  
