![hN4lt](https://github.com/user-attachments/assets/8119bca3-ac51-4b90-9b76-397c84a9c4ed)
# 🐧 Ultimate Ubuntu Command Cheat Sheet

A comprehensive list of essential and advanced Ubuntu commands, grouped by category. Perfect for DevOps engineers, sysadmins, and power users.

---

## 📦 APT Package Management

| Command | Description |
|---------|-------------|
| `sudo apt update` | Refresh package index. |
| `sudo apt upgrade` | Upgrade installed packages. |
| `sudo apt full-upgrade` | Upgrade including package removals. |
| `sudo apt install <pkg>` | Install a package. |
| `sudo apt remove <pkg>` | Remove a package. |
| `sudo apt autoremove` | Remove unused dependencies. |
| `sudo apt clean` | Clear downloaded package cache. |
| `apt search <term>` | Search for packages. |

---

## 📂 Files & Directories

| Command | Description |
|---------|-------------|
| `tree` | Display directory structure (install with `sudo apt install tree`). |
| `lsblk` | List block devices. |
| `mount /dev/sdX /mnt` | Mount a device. |
| `umount /mnt` | Unmount device. |
| `file <filename>` | Determine file type. |
| `stat <file>` | Detailed file metadata. |

---

## 🛠️ System & Hardware Info

| Command | Description |
|---------|-------------|
| `hostnamectl` | View and set hostname. |
| `uptime` | Show system uptime. |
| `whoami` | Print current username. |
| `id` | Show user UID, GID, groups. |
| `lscpu` | Display CPU info. |
| `lsblk` | List all storage devices. |
| `lshw -short` | Hardware summary. |
| `lsusb` | List USB devices. |
| `lspci` | List PCI devices. |
| `dmidecode` | Low-level hardware info (run as root). |

---

## 🧠 Memory & Performance

| Command | Description |
|---------|-------------|
| `top` / `htop` | System monitor (install htop). |
| `vmstat 1` | Real-time memory stats. |
| `iotop` | Show I/O usage by processes (install with `sudo apt install iotop`). |
| `watch -n 1 free -h` | Live memory monitoring. |

---

## 🧑‍💻 Users & Groups

| Command | Description |
|---------|-------------|
| `adduser <name>` | Add new user. |
| `usermod -aG sudo <user>` | Add user to sudo group. |
| `deluser <name>` | Delete a user. |
| `groupadd <group>` | Create group. |
| `passwd <user>` | Set/change user password. |
| `who` | Who's logged in. |
| `w` | Show logged in users and activity. |

---

## 🔐 Permissions & Ownership

| Command | Description |
|---------|-------------|
| `chmod 644 <file>` | rw-r--r-- (owner can read/write). |
| `chmod 755 <dir>` | rwxr-xr-x (for executable files/dirs). |
| `chown user:group <file>` | Change owner and group. |
| `umask` | Show default permission mask. |

---

## 🌐 Networking & Internet

| Command | Description |
|---------|-------------|
| `ip a` / `ifconfig` | Show IP and interfaces (`ifconfig` via `net-tools`). |
| `ip r` | Routing table. |
| `ping <host>` | ICMP test. |
| `traceroute <host>` | Show route to host (install with `sudo apt install traceroute`). |
| `dig <domain>` | DNS lookup (install with `dnsutils`). |
| `nslookup <domain>` | Another DNS tool. |
| `netstat -tulnp` | Listening ports (`net-tools`). |
| `ss -tulnp` | Faster port/status display. |

---

## 📡 SSH & Remote

| Command | Description |
|---------|-------------|
| `ssh user@host` | SSH into remote server. |
| `scp file user@host:/path/` | Copy file to remote server. |
| `rsync -avz source/ user@host:/dest/` | Sync files efficiently. |
| `ssh-keygen` | Generate SSH key pair. |
| `ssh-copy-id user@host` | Install public key on server. |

---

## 🗄️ Disk & Storage

| Command | Description |
|---------|-------------|
| `df -h` | Show disk usage. |
| `du -sh *` | Show size of folders. |
| `lsblk` | List block devices. |
| `mount` / `umount` | Mount/unmount storage. |
| `blkid` | Identify block device UUIDs. |
| `parted -l` / `fdisk -l` | Partition listing. |

---

## 🛠️ System Services (Systemd)

| Command | Description |
|---------|-------------|
| `systemctl status <service>` | Check service status. |
| `systemctl start/stop/restart <service>` | Control service. |
| `systemctl enable/disable <service>` | Auto-start on boot. |
| `journalctl -u <service>` | View service logs. |
| `journalctl -xe` | View detailed error logs. |

---

## 📅 Scheduling & Automation

| Command | Description |
|---------|-------------|
| `crontab -e` | Edit user's cron jobs. |
| `crontab -l` | List user's cron jobs. |
| `systemctl list-timers` | List all active timers. |
| `at now + 1 hour` | One-time tasks (install `at`). |

---

## 🔒 Firewall & Security

| Command | Description |
|---------|-------------|
| `ufw enable` | Enable uncomplicated firewall. |
| `ufw allow <port>` | Allow port through firewall. |
| `ufw status` | Show firewall status. |
| `sudo fail2ban-client status` | Check Fail2Ban status (if installed). |

---

## 🧹 Maintenance

| Command | Description |
|---------|-------------|
| `sudo apt autoremove` | Remove unused packages. |
| `sudo apt clean` | Remove old cache. |
| `journalctl --vacuum-time=7d` | Clean logs older than 7 days. |
| `ncdu /` | Disk usage viewer (install with `sudo apt install ncdu`). |

---

## 🧪 Debugging Tips

```bash
# Redirect stdout and stderr
some-command > output.log 2>&1

# Monitor file live
tail -f /var/log/syslog

# Check if a binary exists
which docker
