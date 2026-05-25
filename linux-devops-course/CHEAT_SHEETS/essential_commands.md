# Linux Essential Commands - Quick Reference

Print this or bookmark this page!

---

## 📍 Navigation Commands

| Command | Purpose | Example |
|---------|---------|---------|
| `pwd` | Print working directory | `pwd` → `/home/ubuntu` |
| `cd` | Change directory | `cd /var/log` |
| `cd ~` | Go to home | `cd ~` |
| `cd ..` | Go to parent directory | `cd ..` |
| `cd -` | Go to previous directory | `cd -` |
| `cd /` | Go to root | `cd /` |
| `ls` | List files | `ls` |
| `ls -l` | Long listing | `ls -l` |
| `ls -la` | Long listing + hidden files | `ls -la` |
| `ls -lh` | Long listing + human-readable sizes | `ls -lh` |
| `ls -lt` | Sort by modification time | `ls -lt` |

---

## 📁 File and Directory Operations

| Command | Purpose | Example |
|---------|---------|---------|
| `mkdir` | Create directory | `mkdir my_folder` |
| `mkdir -p` | Create nested directories | `mkdir -p path/to/deep/dir` |
| `rmdir` | Remove empty directory | `rmdir my_folder` |
| `touch` | Create empty file or update timestamp | `touch config.txt` |
| `cp` | Copy file | `cp source.txt dest.txt` |
| `cp -r` | Copy directory recursively | `cp -r src_dir dst_dir` |
| `mv` | Move or rename | `mv old_name.txt new_name.txt` |
| `rm` | Remove file | `rm file.txt` |
| `rm -r` | Remove directory recursively | `rm -r my_folder` |
| `rm -i` | Remove with confirmation | `rm -i file.txt` |

---

## 📖 Viewing File Contents

| Command | Purpose | Example |
|---------|---------|---------|
| `cat` | Display entire file | `cat file.txt` |
| `head` | Show first 10 lines | `head file.txt` |
| `head -n 20` | Show first 20 lines | `head -n 20 file.txt` |
| `tail` | Show last 10 lines | `tail file.txt` |
| `tail -n 20` | Show last 20 lines | `tail -n 20 file.txt` |
| `tail -f` | Follow file (real-time) | `tail -f /var/log/syslog` |
| `less` | Page through file | `less file.txt` (press q to exit) |
| `more` | Page through file (older) | `more file.txt` |
| `wc` | Word/line count | `wc -l file.txt` |

---

## ✍️ Text Editing

| Command | Purpose | Example |
|---------|---------|---------|
| `nano` | Simple text editor | `nano config.txt` |
| `vim` | Advanced text editor | `vim script.sh` |
| `vi` | Original vi editor | `vi file.txt` |

**nano shortcuts:**
- Ctrl+X = Exit
- Ctrl+O = Save
- Ctrl+A = Home
- Ctrl+E = End

---

## 🔍 Searching and Finding

| Command | Purpose | Example |
|---------|---------|---------|
| `grep` | Search text | `grep "error" log.txt` |
| `grep -i` | Case-insensitive search | `grep -i "ERROR" file.txt` |
| `grep -r` | Search recursively in directories | `grep -r "config" /etc/` |
| `find` | Find files by name | `find . -name "*.log"` |
| `find -type f` | Find files only | `find . -type f -name "*.txt"` |
| `find -type d` | Find directories only | `find . -type d -name "backup"` |
| `which` | Find command location | `which python3` |
| `whereis` | Find command, source, manual | `whereis ssh` |

---

## 📊 System Information

| Command | Purpose | Example |
|---------|---------|---------|
| `whoami` | Show current user | `whoami` → `ubuntu` |
| `id` | Show user ID and groups | `id` |
| `uname -a` | System information | `uname -a` |
| `hostname` | Show computer name | `hostname` |
| `df -h` | Disk space usage | `df -h` |
| `du -sh` | Directory size | `du -sh /home/` |
| `free -h` | Memory usage | `free -h` |
| `uptime` | System uptime | `uptime` |
| `date` | Current date and time | `date` |
| `cal` | Calendar | `cal` |

---

## 👤 User and Permission Management

| Command | Purpose | Example |
|---------|---------|---------|
| `sudo` | Run as root | `sudo apt install package` |
| `chmod` | Change file permissions | `chmod 755 script.sh` |
| `chown` | Change file owner | `sudo chown ubuntu:ubuntu file.txt` |
| `chgrp` | Change group | `chgrp group_name file.txt` |
| `passwd` | Change password | `passwd` |
| `useradd` | Add user (use with sudo) | `sudo useradd username` |
| `usermod` | Modify user | `sudo usermod -aG sudo username` |
| `userdel` | Delete user | `sudo userdel username` |

---

## 📦 Package Management (Ubuntu/Debian)

| Command | Purpose | Example |
|---------|---------|---------|
| `sudo apt update` | Update package list | `sudo apt update` |
| `sudo apt upgrade` | Upgrade packages | `sudo apt upgrade` |
| `sudo apt install` | Install package | `sudo apt install curl` |
| `sudo apt remove` | Remove package | `sudo apt remove curl` |
| `sudo apt autoremove` | Remove unused packages | `sudo apt autoremove` |
| `apt search` | Search for package | `apt search docker` |
| `dpkg -l` | List installed packages | `dpkg -l` |

---

## 🔧 Service Management

| Command | Purpose | Example |
|---------|---------|---------|
| `sudo systemctl start` | Start service | `sudo systemctl start ssh` |
| `sudo systemctl stop` | Stop service | `sudo systemctl stop ssh` |
| `sudo systemctl restart` | Restart service | `sudo systemctl restart ssh` |
| `sudo systemctl status` | Check service status | `sudo systemctl status ssh` |
| `sudo systemctl enable` | Enable on boot | `sudo systemctl enable ssh` |
| `sudo systemctl disable` | Disable on boot | `sudo systemctl disable ssh` |
| `systemctl list-units --type=service` | List all services | `systemctl list-units --type=service` |

---

## ⚙️ Process Management

| Command | Purpose | Example |
|---------|---------|---------|
| `ps` | Show processes | `ps aux` |
| `ps aux` | Show all processes with details | `ps aux` |
| `top` | Interactive process monitor | `top` |
| `htop` | Better process monitor | `htop` |
| `kill` | Terminate process | `kill PID` |
| `kill -9` | Force kill process | `kill -9 PID` |
| `bg` | Run in background | `bg` |
| `fg` | Bring to foreground | `fg` |
| `jobs` | Show background jobs | `jobs` |

---

## 🌐 Network Commands

| Command | Purpose | Example |
|---------|---------|---------|
| `ifconfig` | Show network interfaces | `ifconfig` |
| `ip a` | Show IP addresses | `ip a` |
| `ping` | Test connectivity | `ping google.com` |
| `netstat` | Network statistics | `netstat -tuln` |
| `ss` | Socket statistics (better than netstat) | `ss -tuln` |
| `curl` | Download/test HTTP | `curl https://example.com` |
| `wget` | Download file | `wget https://example.com/file.zip` |
| `ssh` | Secure shell | `ssh user@host` |
| `scp` | Secure copy | `scp file.txt user@host:/path/` |
| `telnet` | Test port connectivity | `telnet host port` |

---

## 📝 File Permissions Quick Reference

| Permission | Binary | Meaning |
|------------|--------|---------|
| `r` (read) | 4 | Can view/list |
| `w` (write) | 2 | Can modify/create |
| `x` (execute) | 1 | Can run/access |

**Examples:**
```bash
chmod 755 script.sh   # Owner: rwx, Others: r-x
chmod 644 config.txt  # Owner: rw, Others: r--
chmod 700 secret.sh   # Owner: rwx, Others: none
```

---

## 🔗 Path Shortcuts

| Symbol | Means | Example |
|--------|-------|---------|
| `/` | Root directory | `cd /` |
| `~` | Home directory | `cd ~` |
| `.` | Current directory | `ls .` |
| `..` | Parent directory | `cd ..` |
| `-` | Previous directory | `cd -` |

---

## 📚 Getting Help

| Command | Purpose | Example |
|---------|---------|---------|
| `man` | Manual pages | `man ls` (press q to exit) |
| `--help` | Command help | `ls --help` |
| `-h` | Short help flag | `ls -h` |
| `info` | Info pages | `info command` |

---

## 💡 Pro Tips

### Tip 1: Combine Commands with Pipes
```bash
ps aux | grep python   # Show only python processes
cat file.txt | grep "error"  # Search for errors
```

### Tip 2: Redirect Output
```bash
ls > file_list.txt     # Save output to file
cat file.txt >> log.txt  # Append to file
```

### Tip 3: Use Wildcards
```bash
ls *.txt              # List all .txt files
rm file_*.log         # Remove files matching pattern
```

### Tip 4: Tab Completion
```bash
ls /va<TAB>  # Becomes: ls /var/
cd Dow<TAB>  # Becomes: cd Downloads/
```

### Tip 5: Command History
```bash
history              # Show all previous commands
!10                  # Run command #10 from history
Ctrl+R               # Search history
```

---

## 🚨 Dangerous Commands (Use with Caution!)

⚠️ **These can damage your system:**

```bash
rm -rf /           # DO NOT RUN - deletes everything
sudo rm -rf /*     # DO NOT RUN
dd if=/dev/zero of=/dev/sda   # DO NOT RUN - destroys disk
chmod -R 000 /    # DO NOT RUN - removes all permissions
```

**Always verify with `pwd` before running destructive commands!**

---

## 📝 Quick Reference Example Workflow

```bash
# Start at home
cd ~
pwd  # /home/ubuntu

# Create project directory
mkdir my_project
cd my_project

# Create subdirectories
mkdir -p config scripts data

# Create files
touch README.md
echo "# My Project" > README.md

# View structure
ls -la
tree .

# Copy files
cp README.md README.md.bak

# Move around
cd scripts
pwd  # /home/ubuntu/my_project/scripts
cd ..

# Remove backup
rm README.md.bak

# View final structure
ls -la
```

---

## 🎯 Most Important Commands to Remember

If you only remember 10 commands, remember these:

1. `pwd` - Where am I?
2. `cd` - Go there
3. `ls -la` - What's here?
4. `sudo` - Do this as admin
5. `cat` / `less` - Show me the file
6. `nano` - Edit file
7. `man` - Help!
8. `grep` - Find in file
9. `find` - Find file
10. `sudo apt install` - Get software

---

**Last Updated:** 2025-05-25
**Print and Keep Handy!**
