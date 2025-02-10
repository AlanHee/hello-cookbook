# VIM

## how
- more moudle in action to better with `.` eg: `diw` more then `dw`
- use leader key better press  ctrl  alt...

## visual mode
```
v                           col or line v mode
ctrl+v                      module v mode
```

## cmd mode
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

### repeat `.`

```
.                           repeat last change
u                           disable last change
ctrl + r                    redo last change
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
#### Ex
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

## view mode
```
w/e | b         forward | back a word
*|#             find  next | pre cursor words
^/0 | $         move to start of line | last of line
%               join to reg
f + [char]      to char locate (`;` forwrd  type `,` back way)
F + [char]      to char locate in back way
hjkl											   
gg/G            start / end
h/m             meddle
Ctrl + d/u      farword/back half page
Ctrl ++ f/b      forward/back a page
Ctrl + i/o      farword /back cursor locateº
Ctrl + p/n      naming...
Ctrl + e        disable autocomplete
Ctrl + y        submit autocomplete
cc | C | s      clear current line and edit
zf              zip code create
zo              zip code open
zc              zip code close
```
#### mark 
```
m{mark}:        mark current locate as `mark`
`{mark}:        go to mark locate

mark can be [a-z]

``:             last jump locate
'.:             last change locate
'^:             last insert locate
```


## edit mode
```
iIoOAa
dd/n1,n2 dd             delete line
s                       delete a line
J                       join with next line
yy/Y
p
x
r/R
u
v h|j|k|l               costom select
Ctrl + s | x    +- current num 
```

### {operator}
```
y               copy
d               delete
c               change
v               into visual mode
yy/dd/cc        operator current line 
```

### {operator}{motion}
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

### {operator}{textobjects} 
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

## FAQ
### How many vim version?
```
vim / vim-gtk / vim-python
```

## Plug 

### vim-lsc 
```
#Complete default mappings are:
let g:lsc_auto_map = {
    \ 'GoToDefinition': '<C-]>',
    \ 'GoToDefinitionSplit': ['<C-W>]', '<C-W><C-]>'],
    \ 'FindReferences': 'gr',
    \ 'NextReference': '<C-n>',
    \ 'PreviousReference': '<C-p>',
    \ 'FindImplementations': 'gI',
    \ 'FindCodeActions': 'ga',
    \ 'Rename': 'gR',
    \ 'ShowHover': v:true,
    \ 'DocumentSymbol': 'go',
    \ 'WorkspaceSymbol': 'gS',
    \ 'SignatureHelp': 'gm',
    \ 'Completion': 'completefunc',
    \}
```
### NERDTree
```
shilt B                     toggle bookmark
:Bookmark                   add current to bookmark
Shift d                     remove bookmark by selected
```

### vim-commentary
```
gcc             toggle comment current line
gcap            comment current part
gcu             cancel comment current part
```
