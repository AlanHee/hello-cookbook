## Linux Script
make your idea as script then forgot it!

### import
```
source .        start shell in current p
```

### var
#### var define

```
l=ls
var=123
var=“hello word”
var='Hello'
set | unset "set version= $ (ls -al)"
let var=10+20
let c=$(ls -l /etc)
#双圆括号是let 命令的简化
(( a = 123  ))
(( a++  ))
$((10+10))
```

#### var use

```
$(var)
$var
```

#### var range

```
export
unset
```


#### var in env
```
/etc/profile
/etc/profile.d
~/.bashc
~/.bash_profile
~/etc/bashc
```

#### var defined
```
$?          last cmd result  `0` for true &  `1` for fase
$PATH       cmd paths
$HOME       home path
$SHELL      witch scsript shell
#exist 0 
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

#### array
```
arr=( 10 5 22 15)
echo $(arr[@])          show all array item
echo $(arr[0])          show array item
echo $(#arr[@])         show array length素
```

### if else fi

### for while

### expression 
```
'var'                       complete express
"var"                       un-complete express
`var`                       execute cmd
expr
expr 4 + 5 
expr 4 +5 // 语法错误
expr 4 + 5.5 //非整数参数
var=`expr 4 + 5`
```

### function
- why function? use muli-time
- how use?  define before call
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
