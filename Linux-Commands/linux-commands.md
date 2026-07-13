# 🐧 Linux Basic Commands Reference

> A beginner-friendly guide to the 30 most essential Linux commands.  
> Use this as a cheat sheet to navigate, manage files, and control your system from the terminal.

---

## 📋 Table of Contents

1. [Navigation](#-1-navigation)
2. [File & Directory Management](#-2-file--directory-management)
3. [Viewing & Editing Files](#-3-viewing--editing-files)
4. [System Information](#-4-system-information)
5. [Permissions & Ownership](#-5-permissions--ownership)
6. [Networking & Packages](#-6-networking--packages)
7. [Pro Tips](#-pro-tips)

---

## 📁 1. Navigation

> Commands for moving around the file system.

### `pwd` — Print Working Directory
Shows your current location in the file system.
```bash
pwd
# Output: /home/username
```

### `ls` — List Directory Contents
Lists files and folders in the current directory.
```bash
ls
ls -la   # Show all files (including hidden) with detailed info
```

### `cd` — Change Directory
Move into a specified folder.
```bash
cd /var/www        # Go to a specific path
cd ..              # Go up one level
cd ~               # Go to home directory
```

---

## 🗂️ 2. File & Directory Management

> Commands for creating, copying, moving, and deleting files and folders.

### `touch` — Create a File
Creates a new empty file.
```bash
touch index.js
```

### `mkdir` — Make Directory
Creates a new folder.
```bash
mkdir my-project
mkdir -p parent/child/grandchild   # Create nested directories
```

### `cp` — Copy
Copies a file or directory to another location.
```bash
cp file.txt /backup/file.txt
cp -r folder/ /backup/folder/      # Copy a directory recursively
```

### `mv` — Move / Rename
Moves or renames a file or directory.
```bash
mv old-name.txt new-name.txt       # Rename
mv file.txt /another/location/     # Move
```

### `rm` — Remove
Deletes a file or directory.
```bash
rm file.txt
rm -rf folder/    # ⚠️ Force-delete folder and all contents (irreversible)
```

### `find` — Search for Files
Finds files by name or type within a directory.
```bash
find . -name "*.txt"               # Find all .txt files
find /var -name "error.log"
```

---

## 📄 3. Viewing & Editing Files

> Commands for reading and editing file content.

### `cat` — Concatenate / Print File
Prints file contents to the terminal.
```bash
cat README.md
```

### `less` — Paginated File Viewer
Views file content one page at a time. Press `q` to quit.
```bash
less server.log
```

### `head` — Show Top of File
Displays the first 10 lines of a file.
```bash
head app.log
head -n 20 app.log    # Show first 20 lines
```

### `tail` — Show Bottom of File
Displays the last 10 lines of a file. Useful for live logs.
```bash
tail app.log
tail -f app.log       # Follow/stream log in real time
```

### `nano` — Text Editor
Opens a simple in-terminal text editor.
```bash
nano config.env
```

### `grep` — Search Inside Files
Searches for a pattern or keyword within file content.
```bash
grep "error" app.log
grep -r "TODO" ./src/     # Search recursively in a folder
```

---

## 💻 4. System Information

> Commands to inspect system resources and status.

### `top` — Process Monitor
Shows live running processes and CPU/memory usage.
```bash
top
```

### `df` — Disk Free
Shows disk space usage across all mounted drives.
```bash
df -h    # Human-readable sizes (MB, GB)
```

### `du` — Disk Usage
Shows how much space a file or directory is using.
```bash
du -sh ./node_modules
```

### `free` — Memory Usage
Displays total, used, and available RAM.
```bash
free -h
```

### `uname` — System Info
Prints system information like kernel version and architecture.
```bash
uname -a
```

### `whoami` — Current User
Prints the username of the currently logged-in user.
```bash
whoami
```

---

## 🔐 5. Permissions & Ownership

> Commands for managing who can read, write, or execute files.

### `chmod` — Change File Mode/Permissions
Sets read, write, and execute permissions on a file.
```bash
chmod 755 script.sh      # Owner: full | Group & Others: read+execute
chmod +x deploy.sh       # Make a file executable
```

### `chown` — Change Ownership
Changes the owner (and optionally group) of a file.
```bash
chown ubuntu file.txt
chown ubuntu:www-data file.txt
```

### `sudo` — Superuser Do
Runs a command with administrator (root) privileges.
```bash
sudo apt update
sudo nano /etc/hosts
```

---

## 🌐 6. Networking & Packages

> Commands for network checks and installing software.

### `ping` — Test Network Connectivity
Sends packets to a host to check if it's reachable.
```bash
ping google.com
ping -c 4 google.com    # Send only 4 packets
```

### `curl` — Transfer Data via URL
Fetches content from a URL. Great for testing APIs.
```bash
curl https://api.example.com/data
curl -X POST -H "Content-Type: application/json" -d '{"key":"val"}' https://api.example.com
```

### `apt install` — Install Packages
Installs software packages on Debian/Ubuntu systems.
```bash
sudo apt update                  # Refresh package list
sudo apt install nginx           # Install a package
```

---

## 💡 Pro Tips

| Shortcut / Trick | What It Does |
|-----------------|-------------|
| `man <command>` | Open the manual for any command (e.g. `man grep`) |
| `Tab` key | Autocomplete file/directory names |
| `Ctrl + C` | Cancel/stop a running command |
| `Ctrl + L` | Clear the terminal screen |
| `!!` | Repeat the last command |
| `history` | Show list of previously run commands |
| `<command> --help` | Show quick usage info for a command |

> **Tip:** If you get a `Permission denied` error, try prefixing your command with `sudo`.

---

*Happy hacking! 🚀*
