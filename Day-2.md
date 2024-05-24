# Day-2 | Linux

#### 1. What’s Linux?
Linux is an open-source operating system that is the foundation of many modern technologies, from servers and mainframes to mobile devices. It is based on the Linux kernel and is known for its robustness, security, and flexibility. Linux distributions, or distros, package the kernel with various software and tools to create a complete operating system. Examples of popular distros include Ubuntu, Fedora, CentOS, and Debian.

#### 2. Ports
In the context of networking, a port is a communication endpoint. Ports allow different applications to communicate over a network using TCP or UDP protocols. Each port is associated with a specific service or application, identified by a port number. Commonly used ports include:
- **80**: HTTP
- **443**: HTTPS
- **22**: SSH
- **21**: FTP

Example:
```bash
# List open ports and services using netstat
netstat -tuln
```

#### 3. SSH-Key Pair to Access Linux
SSH (Secure Shell) is a protocol for securely accessing remote machines. Key-based authentication is a method that uses a pair of cryptographic keys, a private key kept on the client machine, and a public key stored on the server.

Steps to create and use SSH key pairs:
1. Generate an SSH key pair:
   ```bash
   ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
   ```
   This creates a private key (`~/.ssh/id_rsa`) and a public key (`~/.ssh/id_rsa.pub`).

2. Copy the public key to the remote server:
   ```bash
   ssh-copy-id user@remote_host
   ```
   
3. Connect to the remote server:
   ```bash
   ssh user@remote_host
   ```

#### 4. Inbound Rules & Outbound Rules
Inbound and outbound rules control the traffic entering and leaving a system or network. These rules are typically managed through a firewall, such as `iptables` in Linux.

Example: Allow SSH traffic and deny all other incoming traffic.
```bash
# Allow SSH (port 22) traffic
sudo iptables -A INPUT -p tcp --dport 22 -j ACCEPT

# Deny all other incoming traffic
sudo iptables -A INPUT -j DROP
```

#### 5. Basic Commands
Some essential Linux commands:
```bash
# List files in a directory
ls -l

# Change directory
cd /path/to/directory

# Print working directory
pwd

# Copy files
cp source_file destination_file

# Move files
mv source_file destination_file

# Remove files
rm file_name

# Display file contents
cat file_name

# Find manual pages for a command
man command_name
```

#### 6. User Management
Linux allows you to manage users with commands like `adduser`, `usermod`, and `deluser`.

Example:
```bash
# Add a new user
sudo adduser new_user

# Add user to a group
sudo usermod -aG group_name new_user

# Delete a user
sudo deluser user_name
```

#### 7. Files/Folder Permissions
Permissions in Linux determine who can read, write, or execute a file or directory. They are represented by a combination of `r` (read), `w` (write), and `x` (execute).

Example:
```bash
# View permissions
ls -l

# Change permissions (e.g., read/write/execute for owner, read for group and others)
chmod 744 file_name
```

#### 8. File/Folder Ownership
Each file and directory has an owner and a group. The `chown` command changes the ownership.

Example:
```bash
# Change owner
sudo chown new_owner file_name

# Change owner and group
sudo chown new_owner:new_group file_name
```

#### 9. Package Management
Package management is handled by different tools depending on the Linux distribution.

For Debian-based systems (e.g., Ubuntu):
```bash
# Update package list
sudo apt update

# Install a package
sudo apt install package_name

# Remove a package
sudo apt remove package_name
```

For Red Hat-based systems (e.g., CentOS):
```bash
# Install a package
sudo yum install package_name

# Remove a package
sudo yum remove package_name
```

