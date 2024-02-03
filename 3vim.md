# VIM



### visual mode
ctrl+v
shift+i    

### command mode

```
#find 
/searh_string n| shilf n
#repace one line
:s/old/new
#repace hole file
:%s/old/new
#repace hole file global time
:%s/old/new/g
#relace in due line 
:3,5s:/old/new

```
### view mode

```
w/e | b forward | back a word
*|#	 find  next | pre cursor words
^/0 	move to start of line
f + [char]									to char locate (`;` forwrd  type `,` back way)
F + [char]									to char locate in back way
hjkl											   
gg/G											  start / end
h/m													meddle
Ctrl + d/u									farword/back half page
Ctrl + f/b					„„				forward/back a page
Ctrl + i/o									farword /back cursor locateº
:sp												
Ctrl + w + up/down				Switch opens tabs
```

### edit mode

```
iIoOAa
dd/n1,n2 dd                 delete line
s														delete a line
J														join with next line
yy/Y
p
x
diw	 / dw										delete a word
di{	 / di(									delete inner {}  / ()
da{  / da(									delete with {} and its context 

r/R

u
```

### how 
#### How usage <leader>?
vim 自带有很多快捷键，再加上各类插件的快捷键，大量快捷键出现在单层空间中难免引起冲突，为缓解该问题，引入了前缀键 <leader>，这样，键 r 可以配置成 r、<leader>r、<leader><leader>r 等等多个快捷键

合理利用 leader 键 就可以在主键盘里完成大部分功能而且不用频繁地使用 ctrl 、 alt 等键。

```
<Esc>代表Escape键:
<CR>代表Enter键；
<D>代表Command键。*
*Alt键可以使用<M-key>或<A-key>来表示。
<C>代表Ctrl.*
*对于组合键，可以用<C-Esc>代表Ctrl-Esc；使用<S-F1>表示Shift-F1.*
静默执行命令(silent)
```

#### How many vim version?
vim 
vim-gtk
vim-python

#### Any tips or rututorial?
vimtutor zh 
