## Linux Shell

### Keymap
```
Ctrl - r search history
Ctrl - w delete current word
Ctrl - k clean current to end
Ctrl - u/l clean line or all lines
Ctrl - p/n pre or next cmd
Ctrl - a/e	to line start or end 
Ctrl - b/f	to back or forward
Ctrl - z|fg	swith to backgroud | return
```

### Pipe
管道
管道和信号一样 也是进程通信的方法之一 匿名管道（|）是 shell 编程常用的通信工具 eg cat | ps -f

重定向符号
一个进程默认会打开 三个文件描述符 标准输入 标准输出 错误输出
输入重定向
```
eg: read var < /path/to/a/file 输出重定向
eg: rm -fv file >success.text 2>error.text
fg/bg
```

### tmux 
```
#new screen
tmux new -t screen_name

#demon screen 
ctrl + b + d 

#restore window
tmux attach -t screen_name 

#switch screen 
ctrl + b + s 

#remove screen 
ctrl + d | `exit`

#remove all sessions
pkill -f tmux

#help
ctrl + b + ?

```

### at
```
run just 1 time
```

### cron
```
crontab -l          list all plan
crontab -e          edit plan
```
