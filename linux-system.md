## Linux

### 4 basic
- core + GUN + shell + desktop env
- stores files in a single directory called a virtual directory
### what 
```
- all is file
- just services
- safe security free never shutdown
```

### How 
```
- centos live for servic
- ubuntu live for desktop
- yum（centos redhat)
- apt （ubuntu debian）
- $ normal user
- # root user
```

### test
```
- test with  $? 
- cmd for context(上下文)
```

### help
```
man
help
info
```

### path 
filesystem hierarchy standard，FHS,Many Linux distributions follow FHS.
```
/           root dir
/root       root user home
/sbin       root super cmd
/etc        global config dir
/usr        UNIX software resource
/usr/bin     usr/sbin preinstall cmd
```

### determine inner or outter
```
type [cmd]  

```

### create
```
echo 
echo $0         print current shell file name
touch
mkdir fold/{fold1,fold2}/path
cp              after with`\` means copy to fold
ln              If you need to maintain two or more copies of the same file in the system, you can use a single physical copy and multiple virtual copies (links) instead of creating multiple physical copies
```

### read
```
file            determine file type
ls -h           show file sizeon m 
ls -R           tree look 
ls -r           revive on time
ls -l           as list view
ls -t           sort list by time
ls -i           To view the inode number of a file or directory,
cd -            go to pre pwd 
tree            -a
pstree
pwd
ln target link -ls
more/less/cat   -f
head/tail
tail  -f        view on time 
tail -1 -f      view last line on time
history  !!
whatis
date: +/%Y/%m/%d
bc
cal
type cmd
wc -l           count lines 
stat file
less            'less is more' is actually an upgraded version of the 'more' command. Provides multiple very practical features that enable flipping back and forth in text files, as well as some advanced search functions
```

#### read by ls
```
-c          char
-b          block
-s          steam
-l          link
-d          dir
-           file
*           execute 
-s          socket
-p          pip

```

### modify
```
mv
rm -r 
touch /echo
#cp
cp -p # keep time
cp -a # keep own group...
```

### archive
```
tar -xzvf archive.tar.gz 
tar czvf archive.tar.gz /path/to/files
```

### compression
```
zip -r archive.zip path/to/files
zip -er archive.zip path/to/files   # crypt
unzip archive.zip
gzip file
gzip -d file.gz
bzip2

```

### run
```
. 
source 
bash
```

### type
```
- normal
d fold
b black
c char
l link
f pipe
s suit
```

### primession 
```
r4 w2 x1
chmod
chmod 4755  /etc/passwd
chmod 1777 /tmp

特殊权限
SUID 用于二进制执行文件 运行命令时取得文件属组权限
SGID 用于目录 里面创建的目录 自动更改为该目录属性组
SBIT  用于目录 里面新建的自己和root 可删除 eg /tmp
```

### 目录权限的表示方法
```
x 进入目录
rx 显示目录文件名
wx 修改目录文件名
```

### file find
```
find [path] -name | -perm | -user | -type  file_name_to_find
e.g:
find /home -name cat.jpg
find /home -type d -name myfold
find / -type f -size +500M -size -1G
```

### find text in a file
```
grep 
-i  ignore case
-R  
-v  
-a 

# search recursively for pattern in file
grep password /root/anaconda-ks.cfg
grep pass... /root/anaconda-ks.cfg
grep pass* /root/anaconda-ks.cfg
grep pass....$ /root/anaconda-ks.cfg

# search recursively for pattern in dir
grep -r pattern dir 
```

### init
```
df                  see disk size cmd
du                  see fold size cmd
fdisk   [-i]         sperete disk cmd
mkfs                disk format cmd
```

### regex
```
.           one
*           more
[]          due in
[^]         not due in
^           start
$           end
\           transfer
|           or
()          group
{...}       times
```

### start
```
BIOS  → MBR → bootLoader （grub）→kernel 
→ systemd→  init  system shell scripts
```

### user & group
```
id
su - user-name      switch user
su - root

useradd -g manager -m user_name 
userdel [-r] user_name 
usermod -d /home/path user_name 
passwd 

groupadd
groupmod
groupdel

chown
chgrp

/etc/passwd 
/etc/shadow 
```

### file road
```
|
sort
join
>
>>
<

```

### net
```
ip
ping host           result
whois domain        Who
dig domain          DNS info
netstat -pnltu      localhost info
ifconfig            ip interface
ssh usr@host        remote login
scp                 remote copy
wget url            get file 
curl url            send a request  
traceroute domain   print the route 
mtr domain          combines traceroute and ping
ss                  modern netstat
nmap                net exploration and security scanner
```

### mount
```
mount -t            file system
mount -o rw | rw    file read only | read & write
mount -o remoute
```

### LVM(3level) 
```
pvcreate & pvs      phical  create & see
vgcreate & vgs      logic group create & see
lvcreate % lvs      logic craete & see
lvextend            logic extend
```


### common  standrad
```
i                   alert 
h                   help
s                   silent
v                   vobose
```

### advance operate

#### awk
```
awk 'NR >= 3 && NR <=6' path/to/file
#TODO
```

#### sed
```
#TODO
```
