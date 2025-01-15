## Linux

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

### file test
```
- test with  $? 
- cmd for context(上下文)
```

### file help
```
man
help
info
```

### file path 
```
/           root dir
/root       root user home
/sbin       root super cmd
/etc        global config dir
/usr        UNIX software resource
/usr/bin     usr/sbin preinstall cmd
```

#### file type
```
type [cmd]  determine inner or outter file

```

#### file create
```
echo 
touch
mkdir fold/{fold1,fold2}/path
```

#### file read
```
ls -h # show file sizeon m 
ls -R # tree look 
ls -r # revive on time
ls -l # as list view
ls -t # sort list by time
cd -  # go to pre pwd 
tree -a
pwd
ln |ln -s  soft link
more/less/cat       -f
head/tail
tail  -f  ... # view on time 
tail -1 -f # view last line on time
history  !!
whatis
file 
awk 'NR >= 3 && NR <=6' path/to/file
date: +/%Y/%m/%d
bc
cal
type cmd
wc -l # count lines 
stat file
du   
```

#### file modify
```
mv
rm -r 
touch /echo
#cp
cp -p # keep time
cp -a # keep own group...
```

#### file tar
```
tar -xzvf archive.tar.gz 
tar czvf archive.tar.gz /path/to/files
```

#### file expression
```
zip -r archive.zip path/to/files
zip -er archive.zip path/to/files   # crypt
unzip archive.zip
gzip
bzip2

```

#### file run
```
. 
source 
bash
```

### file type
```
- normal
d fold
b black
c char
l link
f pipe
s suit
```

### file primession 
```
r4 w2 x1
chown  user_name file
chown :group_name file // or chgrp...
chown user:group file
/special 
chmod 4755  /etc/passwd
chmod 1777 /tmp

特殊权限
SUID 用于二进制执行文件 运行命令时取得文件属组权限
SGID 用于目录 里面创建的目录 自动更改为该目录属性组
SBIT  用于目录 里面新建的自己和root 可删除 eg /tmp

### 目录权限的表示方法
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

### file filter in a file
```
grep 
-i  ignore case
-R  
-v  
-a 
e.g:
grep # string fiter in a file
grep password /root/anaconda-ks.cfg
grep pass... /root/anaconda-ks.cfg
grep pass* /root/anaconda-ks.cfg
grep pass....$ /root/anaconda-ks.cfg

```

#### file init
```
df                  see disk size cmd
du                  see fold size cmd
fdisk   [-i]         sperete disk cmd
mkfs                disk format cmd
```

#### file regex
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
```

#### file start
```
BIOS  → MBR → bootLoader （grub）→kernel 
→ systemd→  init  system shell scripts
```

#### file's user & group

```
#user operate
id
useradd -g manager -m user_name 
userdel [-r] user_name 
usermod -d /home/path user_name 
passwd 
su - user_name 切换用户（使用login shell） 
su - root

```

```
#group operate
groupadd
groupmod
groupdel

```


```
#update user and group
#users config file /etc/passwd 
#password file /etc/shadow 

chage 
change user's group usermode -g

```

```
#change file owner and its group
chown
chgrp
chmod
sudo 使用其他用户身份执行命令
#login as root user 

```
