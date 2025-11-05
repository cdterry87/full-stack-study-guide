# Linux Study Guide

## 🧩 Beginner Level

- **Q:** What is Linux?  
  **A:** An open-source, Unix-like operating system kernel used in many server environments.

- **Q:** What are some popular Linux distributions?  
  **A:** Ubuntu, Debian, CentOS, Fedora, Rocky Linux, and Arch.

- **Q:** How do you check your current directory?  
  **A:** `pwd` (Print Working Directory)

- **Q:** How do you list files in a directory?  
  **A:** `ls` — use `ls -la` to show hidden files and details.

- **Q:** How do you navigate between directories?  
  **A:** `cd <path>` — use `cd ..` to move up one level.

- **Q:** How do you create and remove directories?  
  **A:** `mkdir <dir>` and `rmdir <dir>` (empty dirs only).

- **Q:** How do you create or edit files?  
  **A:** `touch <file>`, `nano <file>`, or `vim <file>`.

- **Q:** How do you copy or move files?  
  **A:**

  - Copy: `cp source dest`
  - Move/Rename: `mv source dest`

- **Q:** How do you delete files?  
  **A:** `rm <file>` — use `rm -r <dir>` for recursive delete.

- **Q:** How do you view file contents?  
  **A:** `cat`, `less`, `head`, or `tail`.

- **Q:** How do you check your current user?  
  **A:** `whoami`

- **Q:** How do you see system date and uptime?  
  **A:** `date` and `uptime`

- **Q:** How do you get help for a command?  
  **A:** `man <command>` or `<command> --help`

- **Q:** What is the root user?  
  **A:** The superuser account with full system permissions.

- **Q:** How do you run commands as root?  
  **A:** Use `sudo <command>` (if you have permissions).

---

## ⚙️ Intermediate Level

- **Q:** How do file permissions work in Linux?  
  **A:** Three sets (user, group, others), each with read (`r`), write (`w`), and execute (`x`) permissions.

- **Q:** How do you view permissions?  
  **A:** `ls -l` shows permission bits (e.g. `-rw-r--r--`).

- **Q:** How do you change permissions?  
  **A:** `chmod 755 <file>` or symbolic: `chmod u+x <file>`.

- **Q:** How do you change file ownership?  
  **A:** `chown user:group <file>`

- **Q:** What is the purpose of `/etc/passwd` and `/etc/shadow`?  
  **A:** They store user account and password hash info.

- **Q:** How do you view running processes?  
  **A:** `ps aux` or `top`/`htop` (interactive view).

- **Q:** How do you kill a process?  
  **A:** `kill <pid>` or `kill -9 <pid>` (force).

- **Q:** How do you find a process using a port?  
  **A:** `sudo lsof -i :<port>` or `netstat -tuln | grep <port>`

- **Q:** How do you check disk usage?  
  **A:** `df -h` (filesystem) or `du -sh <dir>` (directory).

- **Q:** How do you check memory and CPU usage?  
  **A:** `free -h` and `top` or `htop`.

- **Q:** How do you search for text in files?  
  **A:** `grep "pattern" <file>` or `grep -r "pattern" .` for recursive search.

- **Q:** How do you search for files?  
  **A:** `find /path -name "filename"` or `locate <name>`.

- **Q:** How do you download a file from the internet?  
  **A:** `wget <url>` or `curl -O <url>`.

- **Q:** How do you view network configuration?  
  **A:** `ifconfig` or `ip addr show`.

- **Q:** How do you restart a service?  
  **A:** `sudo systemctl restart <service>`.

- **Q:** How do you check service status?  
  **A:** `sudo systemctl status <service>`.

- **Q:** How do you enable a service to start on boot?  
  **A:** `sudo systemctl enable <service>`.

- **Q:** How do you update and upgrade packages?  
  **A:**

  - Debian/Ubuntu: `sudo apt update && sudo apt upgrade`
  - CentOS/RHEL: `sudo yum update`

- **Q:** How do you install and remove packages?  
  **A:**

  - Install: `sudo apt install <package>`
  - Remove: `sudo apt remove <package>`

- **Q:** How do you view open ports?  
  **A:** `sudo netstat -tulpn` or `ss -tulpn`.

---

## 🧠 Advanced Level

- **Q:** What is the difference between hard and soft links?  
  **A:**

  - **Hard link:** Another pointer to the same file data.
  - **Soft link (symlink):** Shortcut referencing another file’s path.

- **Q:** How do you create a symbolic link?  
  **A:** `ln -s target linkname`

- **Q:** What is the difference between absolute and relative paths?  
  **A:** Absolute starts from root `/`, relative is from current directory.

- **Q:** How do environment variables work?  
  **A:** Store key-value pairs accessible by processes (e.g. `export APP_ENV=production`).

- **Q:** How do you make environment variables persistent?  
  **A:** Add `export VAR=value` to `~/.bashrc` or `~/.profile`.

- **Q:** How do you check which ports are listening?  
  **A:** `sudo lsof -nP -iTCP -sTCP:LISTEN`.

- **Q:** What is cron used for?  
  **A:** Scheduling recurring tasks via `crontab -e`.

- **Q:** What is the crontab syntax?  
  **A:** `minute hour day month weekday command` (e.g., `0 3 * * * /backup.sh` runs daily at 3 AM).

- **Q:** How do you monitor log files?  
  **A:** `tail -f /var/log/syslog` or specific app logs.

- **Q:** How do you check which users are logged in?  
  **A:** `who` or `w`.

- **Q:** How do you create a new user?  
  **A:** `sudo adduser <username>`.

- **Q:** How do you add a user to a group?  
  **A:** `sudo usermod -aG <group> <user>`.

- **Q:** How do you switch users?  
  **A:** `su <user>` or `sudo -u <user> -i`.

- **Q:** How do you change a user’s password?  
  **A:** `passwd <username>`.

- **Q:** What is SSH and how do you connect?  
  **A:** Secure Shell for remote access: `ssh user@host`.

- **Q:** How do you copy files between machines via SSH?  
  **A:** `scp file user@host:/path/`.

- **Q:** What is public key authentication?  
  **A:** Logging in via key pairs (`~/.ssh/id_rsa` and `authorized_keys`) instead of passwords.

- **Q:** How do you change SSH port for security?  
  **A:** Edit `/etc/ssh/sshd_config`, update `Port`, then `sudo systemctl restart sshd`.

- **Q:** What is `chmod 644` vs `chmod 755`?  
  **A:**

  - `644`: Read/write for owner, read for others (files).
  - `755`: Read/execute for all, write for owner (directories/scripts).

- **Q:** How do you compress and extract files?  
  **A:**

  - `.tar.gz`: `tar -czvf archive.tar.gz folder/`
  - Extract: `tar -xzvf archive.tar.gz`.

- **Q:** How do you check system resource usage in real-time?  
  **A:** `htop`, `vmstat`, or `iotop`.

- **Q:** How do you check which process is using the most CPU or memory?  
  **A:** `top` or `htop` sorted by usage.

- **Q:** What is the purpose of `/var/www`?  
  **A:** Default directory for web server files (Apache/Nginx).

- **Q:** What is SELinux or AppArmor?  
  **A:** Security modules enforcing mandatory access control policies.

- **Q:** How do you test network connectivity?  
  **A:** `ping`, `curl`, `traceroute`, or `nc` (netcat).

- **Q:** How do you start a simple HTTP server for testing?  
  **A:** `python3 -m http.server 8080`.

- **Q:** How do you check which command binary will run?  
  **A:** `which <command>` or `type <command>`.

- **Q:** How do you display all environment variables?  
  **A:** `printenv` or `env`.

- **Q:** How do you check system logs for a specific service?  
  **A:** `journalctl -u <service>`.

- **Q:** How do you set file limits for processes?  
  **A:** Edit `/etc/security/limits.conf` or use `ulimit`.
