**Keyboard shortcuts**
<pre>
ctr alt t  - open terminal
ctr shift +   - size
ctr L - clear
ctr c - stop process
ctr z - pause
</pre>

**File commands**
<pre>
ls ,ls -l,ls -la,ls -lh
touch, mkdir , rm , rm -R 
echo "abc" > ab.txt
mv ab.txt bv.txt
mv bv.txt folder1
cat /etc/password > note.txt     (file)
cp ab.txt folder1                         (dir)
du -sh *
du folder1
du
</pre>


**File Permissions: (octal or symbolic)**
<pre>
4-read  ,2-write  ,1-execute
eg: drwxrw-r--   here first is dir or file , then 3 sets of rwx for owner, groups, other-user
chmod 777  file/foldername    - gives all permission to all
chmod 611   folder     (drw---x---x)     or     you can use:  chmod u+rw g-x g+rw
-
chown root test.py
chgrp root test.sh
</pre>

**Grep and Piping:**
<pre>
grep   "dynamic"   /etc
grep   -i  "dynamic"   /etc    (case insensitive)
(or)
cat /etc | grep "dynamic"
</pre>

**File Finding:**
<pre>
locate --all  "passwd"
locate /etc --all  "passwd"
(or)
locate "* . passwd"  | grep "/etc/passwd"
find / -name "file1" -size 2056c
find /etc -type d -iname "File1"
</pre>

**Info:**
<pre>
whoami
hostname
sudo nano /etc/host      (changing)
lsb_release -a    or cat /etc/release
lscpu
uname -a
</pre>

