**Keyboard shortcuts**
<pre>
terminal open  - ctr alt t , term close = ctr shift w
font size increase  = ctr shift +  ,     decrease   =  ctr -
clear scr =  ctr l
suspend or pause     =   ctr z
single tab = autocomplete
double tab  = shows

</pre>

**Basic commands**
<pre>
ls –alps
rm –r
hostname , whoami
lsb_release –a
lscpu
du –sh *      (size check)
sudo service network-manager restart	
sudo gparted                = for checking disc allocation
>= overwrite
>>= append
</pre>


**File Permissions: (octal or symbolic)**
<pre>
d---rwx-w-         = here d refers to dir,  first 3  dash – owner perm, second 3 dash – group perm , next 3 dash – all other users perm
chmod – for changing permissions
  1.chmod u=rw g-x o=x filename
  2.chmod  717 filename       (binary or octal format)     use –r for recursive dir.
where r=4, w=2, x=1.
chown root filename   (changing file ownership)
chgrp root filename
</pre>

**Clear tracks and logs:**
<pre>
cd /var/log         - logs can be found here
shred     - a tool for permanent deletion , shred –vfwu filename    (permanently deletes any file using overwriting 01 method) 
.bash_hist    - all bash commands used are stored here (should be deleted using shred)
> .bash_hist      -   null directs (for making it empty)
</pre>

**Grep, locate, find:**
<pre>
cat /etc/pass | grep “dynamic”     finds the word in the file
cat /etc/pass | grep “dynamic” –i       case insensitive search
locate “passwd” | grep “/etc/”          finding files with ease
</pre>

**File Compressions**
<pre>
tar -cvf  file.tar  filename      (c- compressing, f – file, v -verbose) 
tar -xvf  file.tar          (x-extracting)
tar -cvzf  file.tar.gz  file/     (same for gzip g-gzip)
tar -xvzf  file.tar.gz  
</pre>

**Useradd grpadd**
<pre>
visudo
usermod –aG user1 user1          (adding user and grp  for sudo cmds)
sudo useradd user2
sudo userdel –r user2
sudo passwd user2
</pre>

**Ufw**  
<pre>
sudo apt-get install ufw
sudo ufw status, sudo ufw status numbered(sudo ufw delete 4)
sudo ufw enable   , sudo ufw disable,  sudo ufw reset
default config of ufw:  sudo ufw default allow outgoing , sudo ufw default deny incoming
sudo ufw allow ssh, sudo ufw allow 80, sudo ufw deny http
sudo ufw allow proto tcp from any to any 80,443     - here any is any ipaddress 
sudo ufw allow proto tcp from any to any port 22     - here any is any ipaddress  any port is port
</pre>

**Services and Process**
<pre>
sudo apt-get install htop
htop
•	press f3    - for searching name in htop 
•	space     -  for next
•	f9 – options to kill
•	9 and enter – to kill
ps
•	ps aux   
•	ps aux | grep ssh
•	sudo kill 7817
</pre>

**SSH         (client server connection model)**
<pre>
sudo apt-get install openssh-client            (source)
sudo apt-get install openssh-server            (target)
cat /etc/ssh/ssh_config   -client
cat /etc/ssh/ssdh_config  -server
sudo systemctl restart ssh
sudo root@ipaddress
sudo root@ipaddress –p 20        (p - port)
</pre>







