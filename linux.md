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

### Tips and workflow
```
- test with  $? 
- cmd for context(上下文)
```

### path 
```
/           root dir
/root       root user home
/usr        UNIX software resource
/sbin       root super cmd
usr/bin     usr/sbin preinstall cmd
/etc        global config dir
```

#### help
```
man
help
info
```

#### How to determine inner or outter file
`type` [cmd] 

```

```

#### add file
```
echo 
touch
mkdir
tar czvf archive.tar.gz /path/to/files
zip -r archive.zip path/to/files
# crypt
zip -er archive.zip path/to/files
```

#### read file
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
more/less/cat
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

#### write file
```
mkdir fold/{fold1,fold2}path
mv
rm -r 
touch /echo
#cp
cp -p # keep time
cp -a # keep own group...
tar -xzvf archive.tar.gz 
unzip archive.zip
```

#### run file
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

### find file in path
```
find [path] -name | -perm | -user | -type  file_name_to_find
e.g:
find /home -name cat.jpg
find /home -type d -name myfold
find / -type f -size +500M -size -1G
```

### grep string in a file
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

### init file
```
df                  see disk size cmd
du                  see fold size cmd
fdisk   [-i]         sperete disk cmd
mkfs                disk format cmd
```

### shell var
```
var=123
var=“hello word”
var='Hello'
let var=10+20
l=ls
letc=$(ls -l /etc)

#### 变量的引用
$(var) // 有时也可以省略 $var

#### 变量的默认范围
导出 export
删除 unset


#### 环境变量配置文件
/etc/profile
/etc/profile.d
~/.bashc
~/.bash_profile
~/etc/bashc

#### 特殊变量
echo $？// 上次命令的运行结果   0/2
exist 0 

#### 数字常量
let "变量名 = 变量值"
变量值 0开头为八进制 0x 为16进制

```

#### shell var

```
set | unset "set version= $ (ls -al)"
env | $PATH |$HOME |$SHELL
export var make var as enviroment
```

### regex file
```
#one char
. one
* more
[] due in []
^ start
$ end
\ transfer
#extend char
| or
[^] not in due
() group
\b
\B
[?:]
```

### 括号总结
```
圆括号
单独使用一个会产生子shell 
数组初始化

方括号 
[] test
[[]] 测试表达式

尖括号 重定向

花括号
输出范围  echo {0..9}
文件复制/生成
```

其他通配符
```
* 通配符
？ 条件测试或通配符
$ 取值符号
| 管道
& 后台运行
_ 空格
# 注释
; 命令分隔   case ;; 
: 空指令
. 和 source 相同
~ home目录
, 分隔目录
```

#### 特殊变量
```
echo $？// 上次命令的运行结果   0/2
exist 0 
```

#### 数字常量
```
let "变量名 = 变量值"
变量值 0开头为八进制 0x 为16进制

双圆括号是let 命令的简化
(( a = 123  ))
(( a++  ))
echo $((10+10))

#### 数组变量
定义
arr=( 10 5 22 15)

显示数组所有元素
echo $(arr[@])

显示数组个数
echo $(#arr[@])

显示数组第1个元素
echo $(arr[0])

### 引用 
''  完全引用 var=123
"" 不完全引用
`` 执行命令
eg :
var=123
echo '$var'  // output $var 
echo "$var" // output 123
expr 4 + 5 
expr 4 +5 // 语法错误
expr 4 + 5.5 //非整数参数
var=`expr 4 + 5`
```

### function
```
$1,$2,$3..$n  #get function args
/etc/init.d/functions # system self funs
unset function_name #release fun
```

### test
```
[] 扩展写法[[]]  支持&& || < > 
可作为:
文件测试
整数比较测试
字符串测试
man test 
```


### boot flow
```
BIOS  → MBR → bootLoader （grub）→kernel 
→ systemd→  init  system shell scripts
```

#### user & group

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
