
# Wizard Cheat Sheet
#Link: https://wizardbrew.github.io/LinuxCommandsheet/
--
cat << 'EOF' > linux_cheat_sheet.md
# 🐧 Linux Command Cheat Sheet
## 🗂️ File & Directory Commands

| Type         | Command       | Example 1                         | Example 2                            |
|--------------|---------------|-----------------------------------|--------------------------------------|
| 📂 Navigation | `cd`          | `cd /var/log` – Go to system logs | `cd ~/projects` – Jump to projects   |
| 📋 Listing    | `ls`          | `ls -l` – Long format             | `ls -lha /etc` – All files human-readable |
| ➕ Creation    | `mkdir`       | `mkdir newdir` – Create “newdir”  | `mkdir -p a/b/c` – Nested dirs       |
| 📝 Viewing    | `cat`         | `cat README.md` – Dump file       | `cat file1 file2` – Concat & view    |
| 🔍 Searching  | `find`        | `find . -name "*.log"` – Find logs| `find /home -size +1M` – Files >1 MB |
| 📄 Copy       | `cp`          | `cp a.txt b.txt` – Copy file      | `cp -r src/ dest/` – Copy dir        |
| 🚚 Move       | `mv`          | `mv old.txt new.txt` – Rename     | `mv *.log archive/` – Move logs      |
| 🗑️ Deletion    | `rm`          | `rm file.txt` – Delete file       | `rm -rf temp/` – Force delete dir    |
| 📊 Disk Usage | `du`          | `du -h .` – Folder sizes          | `du -sh ~/` – Summarize home         |
| 💾 Disk Free  | `df`          | `df -h` – FS usage                | `df -Th` – Type + human              |
| 🔗 Linking    | `ln`          | `ln -s /usr/bin/python3 python` – Symlink | `ln file.txt hardlink.txt` – Hard link |

---

## 🌐 Network Commands

| Type           | Command       | Example 1                          | Example 2                              |
|----------------|---------------|------------------------------------|----------------------------------------|
| 📶 Connectivity | `ping`        | `ping google.com` – Reachability   | `ping -c3 1.1.1.1` – 3 packets         |
| 🛰️ Trace Route  | `traceroute`  | `traceroute example.com`           | `traceroute -n 8.8.8.8`                |
| 🌐 HTTP Client | `curl`        | `curl https://api.github.com`      | `curl -I https://example.com`          |
| ⬇️ Download     | `wget`        | `wget file.tar.gz`                 | `wget -qO- https://site.com`           |
| 🕵️ DNS Lookup   | `dig`         | `dig +short example.com`           | `dig @8.8.8.8 example.com`             |
| 🔌 Socket Info  | `netstat`     | `netstat -tuln`                    | `netstat -p`                           |
| 🔌 Socket Info  | `ss`          | `ss -tuln`                         | `ss -p`                                |
| ⚙️ IP Config    | `ip`          | `ip addr show`                     | `ip route show`                        |
| 🔍 Port Scan    | `nmap`        | `nmap localhost`                   | `nmap -sS 192.168.1.0/24`              |

---

## 🔐 Permissions Management

| Type           | Command       | Example 1                                     | Example 2                      |
|----------------|---------------|-----------------------------------------------|--------------------------------|
| 🔑 Modify Mode | `chmod`       | `chmod 755 script.sh`                         | `chmod -R u+rwX,g-w,o-rwx dir/` |
| 👤 Change Owner| `chown`       | `chown parvez file.txt`                       | `chown -R user:group dir/`     |
| 🔒 Default Mask| `umask`       | `umask 022`                                   | `umask 077`                    |
| 📜 Get ACL     | `getfacl`     | `getfacl file.txt`                            | `getfacl -R dir/`              |
| 🛠️ Set ACL     | `setfacl`     | `setfacl -m u:alice:rw file.txt`              | `setfacl -x g:staff file.txt`  |

---

## 🔧 systemd (systemctl)

| Type           | Command                     | Example 1                         | Example 2                             |
|----------------|-----------------------------|-----------------------------------|---------------------------------------|
| ℹ️ Status       | `systemctl status`         | `systemctl status sshd`           | `systemctl status nginx.service`      |
| ▶️ Start        | `systemctl start`          | `systemctl start sshd`            | `systemctl start apache2`             |
| ⏹️ Stop         | `systemctl stop`           | `systemctl stop sshd`             | `systemctl stop apache2`              |
| 🔄 Restart     | `systemctl restart`        | `systemctl restart sshd`          | `systemctl restart apache2`           |
| 🛡️ Enable       | `systemctl enable`         | `systemctl enable sshd`           | `systemctl enable nginx`              |
| ❌ Disable      | `systemctl disable`        | `systemctl disable sshd`          | `systemctl disable nginx`             |
| 🔃 Reload       | `systemctl daemon-reload`  | `systemctl daemon-reload`         | `systemctl reload-or-restart sshd`    |
| 📜 List Units  | `systemctl list-unit-files`| `systemctl list-unit-files`       | `systemctl list-units --type=service`|

---

## ⚙️ Service Management (`service`)

| Type           | Command                    | Example 1              | Example 2               |
|----------------|----------------------------|------------------------|-------------------------|
| ℹ️ Status       | `service <name> status`    | `service sshd status`  | `service apache2 status`|
| ▶️ Start        | `service <name> start`     | `service sshd start`   | `service apache2 start` |
| ⏹️ Stop         | `service <name> stop`      | `service sshd stop`    | `service apache2 stop`  |
| 🔄 Restart     | `service <name> restart`   | `service sshd restart` | `service apache2 restart`|
| 🔃 Reload       | `service <name> reload`    | `service sshd reload`  | `service apache2 reload`|

---

## 📝 .bashrc Snippets

| Type              | Snippet                                             | Example 1                    | Example 2                              |
|-------------------|-----------------------------------------------------|------------------------------|----------------------------------------|
| 🔗 Alias           | `alias`                                            | `alias ll='ls -la'`          | `alias gs='git status'`                |
| 🌿 Export          | `export`                                           | `export PATH=$PATH:/opt/bin` | `export EDITOR=vim`                    |
| 🎨 PS1 Prompt      | `PS1`                                              | `PS1="\u@\h:\w\$ "`         | `PS1="

\[\e[32m\]

\u@\h

\[\e[m\]

:\w\$ "` |
| 🏭 Function        | `mkcd(){ mkdir -p "$1"; cd "$1"; }`                | `mkcd newdir` – Make+cd      | `extract(){ tar -xvf "$1"; }`         |
| 📜 Source          | `source`                                           | `source ~/.bash_aliases`     | `source /etc/bash_completion`          |
| 🔍 History         | `HISTSIZE/HISTCONTROL`                            | `export HISTSIZE=2000`       | `export HISTCONTROL=ignoredups:erasedups`|
| 🔔 Shell Options  | `shopt`                                            | `shopt -s histappend`        | `shopt -s globstar`                    |

EOF

echo "✅ linux_cheat_sheet.md generated in $(pwd)"

