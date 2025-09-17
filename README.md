  
<p class="has-line-data" data-line-start="0" data-line-end="1">#!/usr/bin/env bash</p>
<h1 class="code-line" data-line-start=1 data-line-end=2 ><a id="_1"></a>-----------------------------------------------------------------------------</h1>
<h1 class="code-line" data-line-start=2 data-line-end=3 ><a id="generatelinuxcheatsheetsh_2"></a><a href="http://generate-linux-cheatsheet.sh">generate-linux-cheatsheet.sh</a></h1>
<h1 class="code-line" data-line-start=3 data-line-end=4 ><a id="Generates_linux_cheat_sheetmd_in_your_current_directory_3"></a>Generates linux_cheat_sheet.md in your current directory.</h1>
<h1 class="code-line" data-line-start=4 data-line-end=5 ><a id="_4"></a>-----------------------------------------------------------------------------</h1>
<p class="has-line-data" data-line-start="6" data-line-end="7">cat &lt;&lt; ‘EOF’ &gt; linux_cheat_sheet.md</p>
<h1 class="code-line" data-line-start=7 data-line-end=8 ><a id="_Linux_Command_Cheat_Sheet_7"></a>🐧 Linux Command Cheat Sheet</h1>
<p class="has-line-data" data-line-start="9" data-line-end="10">A concise Markdown reference for common Linux commands, organized by category.</p>
<hr>
<h2 class="code-line" data-line-start=13 data-line-end=14 ><a id="_File__Directory_Commands_13"></a>🗂️ File &amp; Directory Commands</h2>
<table class="table table-striped table-bordered">
<thead>
<tr>
<th>Type</th>
<th>Command</th>
<th>Example 1</th>
<th>Example 2</th>
</tr>
</thead>
<tbody>
<tr>
<td>📂 Navigation</td>
<td><code>cd</code></td>
<td><code>cd /var/log</code> – Go to system logs</td>
<td><code>cd ~/projects</code> – Jump to projects</td>
</tr>
<tr>
<td>📋 Listing</td>
<td><code>ls</code></td>
<td><code>ls -l</code> – Long format</td>
<td><code>ls -lha /etc</code> – All files human-readable</td>
</tr>
<tr>
<td>➕ Creation</td>
<td><code>mkdir</code></td>
<td><code>mkdir newdir</code> – Create “newdir”</td>
<td><code>mkdir -p a/b/c</code> – Nested dirs</td>
</tr>
<tr>
<td>📝 Viewing</td>
<td><code>cat</code></td>
<td><code>cat README.md</code> – Dump file</td>
<td><code>cat file1 file2</code> – Concat &amp; view</td>
</tr>
<tr>
<td>🔍 Searching</td>
<td><code>find</code></td>
<td><code>find . -name &quot;*.log&quot;</code> – Find logs</td>
<td><code>find /home -size +1M</code> – Files &gt;1 MB</td>
</tr>
<tr>
<td>📄 Copy</td>
<td><code>cp</code></td>
<td><code>cp a.txt b.txt</code> – Copy file</td>
<td><code>cp -r src/ dest/</code> – Copy dir</td>
</tr>
<tr>
<td>🚚 Move</td>
<td><code>mv</code></td>
<td><code>mv old.txt new.txt</code> – Rename</td>
<td><code>mv *.log archive/</code> – Move logs</td>
</tr>
<tr>
<td>🗑️ Deletion</td>
<td><code>rm</code></td>
<td><code>rm file.txt</code> – Delete file</td>
<td><code>rm -rf temp/</code> – Force delete dir</td>
</tr>
<tr>
<td>📊 Disk Usage</td>
<td><code>du</code></td>
<td><code>du -h .</code> – Folder sizes</td>
<td><code>du -sh ~/</code> – Summarize home</td>
</tr>
<tr>
<td>💾 Disk Free</td>
<td><code>df</code></td>
<td><code>df -h</code> – FS usage</td>
<td><code>df -Th</code> – Type + human</td>
</tr>
<tr>
<td>🔗 Linking</td>
<td><code>ln</code></td>
<td><code>ln -s /usr/bin/python3 python</code> – Symlink</td>
<td><code>ln file.txt hardlink.txt</code> – Hard link</td>
</tr>
</tbody>
</table>
<hr>
<h2 class="code-line" data-line-start=31 data-line-end=32 ><a id="_Network_Commands_31"></a>🌐 Network Commands</h2>
<table class="table table-striped table-bordered">
<thead>
<tr>
<th>Type</th>
<th>Command</th>
<th>Example 1</th>
<th>Example 2</th>
</tr>
</thead>
<tbody>
<tr>
<td>📶 Connectivity</td>
<td><code>ping</code></td>
<td><code>ping google.com</code> – Reachability</td>
<td><code>ping -c3 1.1.1.1</code> – 3 packets</td>
</tr>
<tr>
<td>🛰️ Trace Route</td>
<td><code>traceroute</code></td>
<td><code>traceroute example.com</code></td>
<td><code>traceroute -n 8.8.8.8</code></td>
</tr>
<tr>
<td>🌐 HTTP Client</td>
<td><code>curl</code></td>
<td><code>curl https://api.github.com</code></td>
<td><code>curl -I https://example.com</code></td>
</tr>
<tr>
<td>⬇️ Download</td>
<td><code>wget</code></td>
<td><code>wget file.tar.gz</code></td>
<td><code>wget -qO- https://site.com</code></td>
</tr>
<tr>
<td>🕵️ DNS Lookup</td>
<td><code>dig</code></td>
<td><code>dig +short example.com</code></td>
<td><code>dig @8.8.8.8 example.com</code></td>
</tr>
<tr>
<td>🔌 Socket Info</td>
<td><code>netstat</code></td>
<td><code>netstat -tuln</code></td>
<td><code>netstat -p</code></td>
</tr>
<tr>
<td>🔌 Socket Info</td>
<td><code>ss</code></td>
<td><code>ss -tuln</code></td>
<td><code>ss -p</code></td>
</tr>
<tr>
<td>⚙️ IP Config</td>
<td><code>ip</code></td>
<td><code>ip addr show</code></td>
<td><code>ip route show</code></td>
</tr>
<tr>
<td>🔍 Port Scan</td>
<td><code>nmap</code></td>
<td><code>nmap localhost</code></td>
<td><code>nmap -sS 192.168.1.0/24</code></td>
</tr>
</tbody>
</table>
<hr>
<h2 class="code-line" data-line-start=47 data-line-end=48 ><a id="_Permissions_Management_47"></a>🔐 Permissions Management</h2>
<table class="table table-striped table-bordered">
<thead>
<tr>
<th>Type</th>
<th>Command</th>
<th>Example 1</th>
<th>Example 2</th>
</tr>
</thead>
<tbody>
<tr>
<td>🔑 Modify Mode</td>
<td><code>chmod</code></td>
<td><code>chmod 755 script.sh</code></td>
<td><code>chmod -R u+rwX,g-w,o-rwx dir/</code></td>
</tr>
<tr>
<td>👤 Change Owner</td>
<td><code>chown</code></td>
<td><code>chown parvez file.txt</code></td>
<td><code>chown -R user:group dir/</code></td>
</tr>
<tr>
<td>🔒 Default Mask</td>
<td><code>umask</code></td>
<td><code>umask 022</code></td>
<td><code>umask 077</code></td>
</tr>
<tr>
<td>📜 Get ACL</td>
<td><code>getfacl</code></td>
<td><code>getfacl file.txt</code></td>
<td><code>getfacl -R dir/</code></td>
</tr>
<tr>
<td>🛠️ Set ACL</td>
<td><code>setfacl</code></td>
<td><code>setfacl -m u:alice:rw file.txt</code></td>
<td><code>setfacl -x g:staff file.txt</code></td>
</tr>
</tbody>
</table>
<hr>
<h2 class="code-line" data-line-start=59 data-line-end=60 ><a id="_systemd_systemctl_59"></a>🔧 systemd (systemctl)</h2>
<table class="table table-striped table-bordered">
<thead>
<tr>
<th>Type</th>
<th>Command</th>
<th>Example 1</th>
<th>Example 2</th>
</tr>
</thead>
<tbody>
<tr>
<td>ℹ️ Status</td>
<td><code>systemctl status</code></td>
<td><code>systemctl status sshd</code></td>
<td><code>systemctl status nginx.service</code></td>
</tr>
<tr>
<td>▶️ Start</td>
<td><code>systemctl start</code></td>
<td><code>systemctl start sshd</code></td>
<td><code>systemctl start apache2</code></td>
</tr>
<tr>
<td>⏹️ Stop</td>
<td><code>systemctl stop</code></td>
<td><code>systemctl stop sshd</code></td>
<td><code>systemctl stop apache2</code></td>
</tr>
<tr>
<td>🔄 Restart</td>
<td><code>systemctl restart</code></td>
<td><code>systemctl restart sshd</code></td>
<td><code>systemctl restart apache2</code></td>
</tr>
<tr>
<td>🛡️ Enable</td>
<td><code>systemctl enable</code></td>
<td><code>systemctl enable sshd</code></td>
<td><code>systemctl enable nginx</code></td>
</tr>
<tr>
<td>❌ Disable</td>
<td><code>systemctl disable</code></td>
<td><code>systemctl disable sshd</code></td>
<td><code>systemctl disable nginx</code></td>
</tr>
<tr>
<td>🔃 Reload</td>
<td><code>systemctl daemon-reload</code></td>
<td><code>systemctl daemon-reload</code></td>
<td><code>systemctl reload-or-restart sshd</code></td>
</tr>
<tr>
<td>📜 List Units</td>
<td><code>systemctl list-unit-files</code></td>
<td><code>systemctl list-unit-files</code></td>
<td><code>systemctl list-units --type=service</code></td>
</tr>
</tbody>
</table>
<hr>
<h2 class="code-line" data-line-start=74 data-line-end=75 ><a id="_Service_Management_service_74"></a>⚙️ Service Management (<code>service</code>)</h2>
<table class="table table-striped table-bordered">
<thead>
<tr>
<th>Type</th>
<th>Command</th>
<th>Example 1</th>
<th>Example 2</th>
</tr>
</thead>
<tbody>
<tr>
<td>ℹ️ Status</td>
<td><code>service &lt;name&gt; status</code></td>
<td><code>service sshd status</code></td>
<td><code>service apache2 status</code></td>
</tr>
<tr>
<td>▶️ Start</td>
<td><code>service &lt;name&gt; start</code></td>
<td><code>service sshd start</code></td>
<td><code>service apache2 start</code></td>
</tr>
<tr>
<td>⏹️ Stop</td>
<td><code>service &lt;name&gt; stop</code></td>
<td><code>service sshd stop</code></td>
<td><code>service apache2 stop</code></td>
</tr>
<tr>
<td>🔄 Restart</td>
<td><code>service &lt;name&gt; restart</code></td>
<td><code>service sshd restart</code></td>
<td><code>service apache2 restart</code></td>
</tr>
<tr>
<td>🔃 Reload</td>
<td><code>service &lt;name&gt; reload</code></td>
<td><code>service sshd reload</code></td>
<td><code>service apache2 reload</code></td>
</tr>
</tbody>
</table>
<hr>
<h2 class="code-line" data-line-start=86 data-line-end=87 ><a id="_bashrc_Snippets_86"></a>📝 .bashrc Snippets</h2>
<table class="table table-striped table-bordered">
<thead>
<tr>
<th>Type</th>
<th>Snippet</th>
<th>Example 1</th>
<th>Example 2</th>
</tr>
</thead>
<tbody>
<tr>
<td>🔗 Alias</td>
<td><code>alias</code></td>
<td><code>alias ll='ls -la'</code></td>
<td><code>alias gs='git status'</code></td>
</tr>
<tr>
<td>🌿 Export</td>
<td><code>export</code></td>
<td><code>export PATH=$PATH:/opt/bin</code></td>
<td><code>export EDITOR=vim</code></td>
</tr>
<tr>
<td>🎨 PS1 Prompt</td>
<td><code>PS1</code></td>
<td><code>PS1=&quot;\u@\h:\w\$ &quot;</code></td>
<td>`PS1=&quot;</td>
</tr>
</tbody>
</table>
<p class="has-line-data" data-line-start="94" data-line-end="95">[\e[32m]</p>
<p class="has-line-data" data-line-start="96" data-line-end="97">\u@\h</p>
<p class="has-line-data" data-line-start="98" data-line-end="99">[\e[m]</p>
<p class="has-line-data" data-line-start="100" data-line-end="105">:\w$ &quot;<code>| | 🏭 Function |</code>mkcd(){ mkdir -p “$1”; cd “$1”; }<code>|</code>mkcd newdir<code>– Make+cd |</code>extract(){ tar -xvf “$1”; }<code>| | 📜 Source |</code>source<code>|</code>source ~/.bash_aliases<code>|</code>source /etc/bash_completion<code>| | 🔍 History |</code>HISTSIZE/HISTCONTROL<code>|</code>export HISTSIZE=2000<code>|</code>export HISTCONTROL=ignoredups:erasedups<code>| | 🔔 Shell Options |</code>shopt<code>|</code>shopt -s histappend<code>|</code>shopt -s globstar`                    |</p>
<p class="has-line-data" data-line-start="106" data-line-end="107">EOF</p>
<p class="has-line-data" data-line-start="108" data-line-end="109">echo “✅ linux_cheat_sheet.md generated in $(pwd)”</p>
