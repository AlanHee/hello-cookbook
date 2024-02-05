# VIM

- one move one action
- Goft
- 合理利用 leader 键而不用频繁地使用 ctrl 、 alt 等

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
### How many vim version?
vim 
vim-gtk
vim-python

### Any tips or rututorial?
vimtutor zh 
