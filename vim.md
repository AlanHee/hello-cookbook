  effect move action batch, make your own workflow

## keyword
- more moudle in action to better with `.` eg: `diw` more then `dw`
- use leader key better press  ctrl  alt...
- 3 mode: command Ex insert 

## Normal mode

### into edit mode
```
iIoOAa
```

### into visual mode
```
v               col or line v mode
ctrl+v          module v mode
```

### Move
```
hjkl											   
gg/G            start / end
^/0 | $         move to start of line | last of line
%               join to reg
f | F + [char]  to char locate (`;` forwrd  type `,` back way)
Ctrl + d/u      farword/back half page
Ctrl + f/b      forward/back a page
Ctrl + i/o      farword /back cursor locateº
Ctrl + p/n      naming...
h/m             meddle

```
### Move by word
```
w:              word
e:              word's end locate
b:              back word
```

### Move by mark 
```
m{mark}:        mark current locate as `mark`
`{mark}:        go to mark locate
``:             last jump locate
```

### repeat 
```
.                           repeat last change
u                           disable last change
ctrl + r                    redo last change
```


### comment (vim-commentary plug)
```
gcc             toggle comment current line
gcap            comment current part
gcu             cancel comment current part
```

## Command mode
```
:grep -r /                  find in other file
:!grep -r                   find in other file 
:sp	ctrl + w + up|down      switch opens window
:D
!cmd                        run cmd in man screen
:e                          reload current file
```

#### search in line
```
f{char}/t{char}:            jump next char in current line
F{char}/T{char}:            not forward but after 
;/,                         quck next/pre search 
```

#### search in file
```
/{pattern}                  search forward
?{pattern}                  search before
n/N                         jump next
Ctrl + L                    clear search high light
```

### reg
```
:reg {register}             print register
.                           last insert content
:                           last excute cmd
"                           default register while yy 
%                           current doc name

```
### replace
```
:[range]s/{pattern}/{string}/[flags]
# replace pattern as string

flags:
g           for repace all in line
i           inore case
c           make sure for repace
n           just  count
eg: count how many times `Vim` appear
:%s/Vim//gn
```
### Ex
Diff Ex with CMD line?
CMD for unit in a line
CMD no need point address
```
:[range] delete
:[range] yank
:[range] print

:[range] copy {address}
:[range] move {address}
:[range] put [x]
```

## Edit mode
```
Ctrl + e        disable autocomplete
Ctrl + y        submit autocomplete

s                       delete a line
J                       join with next line
x
r/R
u
Ctrl + s | x    +- current num 
```
### {operator}
```
yy | Y          yank
d               delete
c               change
cc | C | S      clear current line and edit
dd | D          delete current line
```

### {operator}{motion}=action
```
ye              copy to end of word 
d$              delete to end of line
dgg             delete to 1st line
dt;             delete util map the `;`
```

### {textobjects}
```
w/W/s/p                 word/word word/string/p
i/a                     inner/around
```

### {operator}{textobjects}=action 
```
- with `.` repeat last operator
- `[count]` repeat opertor
diw                 delete a word
da{                 delete around context with{}
ci(                 change iinner () text
yi{                 copy inner {} text 
```

### {operator}{motion} vs {operator}{textobjects}
- motion can be with `w` `b` `e` etc..
- motion 更加灵活，但并不明确
- textobjects due is 明确的
- textobjects  只能跟在operator后面

