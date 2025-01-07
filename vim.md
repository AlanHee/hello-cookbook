# VIM

### tips
- more moudle in action to better with `.` eg: `diw` more then `dw`
- use leader key better press  ctrl  alt...

### visual mode
```
ctrl+v
```

### cmd mode
```
n | N                       find next | pre match 
/ | ?                       find in up | down in current file
Ctrl + L                    clear search high light
:grep -r /                  find in other file
:!grep -r                   find in other file 
:s/old/new                  repace one line
:%s/old/new                 repace hole file
:%s/old/new/g               repace hole file global time
:%s/old\C/new/g             repace with no ignore case
:3,5s:/old/new              relace in due line 
:sp	ctrl + w + up|down      switch opens window
:D
!cmd                        run cmd in man screen
:e                          reload current file
```

#### reg
```
:reg {register}             print register
.                           last insert content
:                           last excute cmd
"                           default register while yy 
%                           current doc name

```

### view mode
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
Ctrl + s | x    +- current num 
```

### edit mode: basic
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

```

#### edit mode: {textobjects}
```
w/W/s/p                 word/word word/string/p
i/a                     inner/around
```

#### edit mode: {operator}{textobjects} e.g:
```
- with `.` repeat last operator
- `[count]` repeat opertor
diw                 delete a word
da{                 delete around context with{}
ci(                 change iinner () text
yi{                 copy inner {} text 
```

#### edit mode: {operator}{motion} vs {operator}{textobjects}
- motion can be with `w` `b` `e` etc..
- motion 更加灵活，但并不明确
- textobjects due is 明确的
- textobjects  只能跟在operator后面

### How many vim version?
```
vim / vim-gtk / vim-python
```

### what is the default lsc hotkey? 
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
### How to add bookmark with NERDTree?
```
shilt B                     toggle bookmark
:Bookmark                   add current to bookmark
Shift d                     remove bookmark by selected
```

### how comment with shortcut?
```
gcc             toggle comment current line
gcgc            cancel comments
gcap            comment current part
gcu             cancel comment current part
```
