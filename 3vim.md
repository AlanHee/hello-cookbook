# VIM

### tips
- one move one action
- use leader key better  press  ctrl  alt...

### visual mode
```
ctrl+v
shift+i    
```

### cmd mode
```
/searh_string n | shilf n   find 
:s/old/new                  repace one line
:%s/old/new                 repace hole file
:%s/old/new/g               repace hole file global time
:3,5s:/old/new              relace in due line 
:sp	ctrl + w + up|down		switch opens window
```

### view mode
```
w/e | b     forward | back a word
*|#	        find  next | pre cursor words
^/0         move to start of line
f + [char]	to char locate (`;` forwrd  type `,` back way)
F + [char]	to char locate in back way
hjkl											   
gg/G		start / end
h/m			meddle
Ctrl + d/u	farword/back half page
Ctrl + f/b	forward/back a page
Ctrl + i/o	farword /back cursor locateº
gcc         toggle comment current line
```

### edit mode
```
iIoOAa
dd/n1,n2 dd         delete line
s					delete a line
J					join with next line
yy/Y
p
x
diw	 / dw			delete a word
di{	 / di(	        delete inner {}  / ()
da{  / da(	        delete with {} and its context 
r/R
u
```

### How many vim version?
```
vim 
vim-gtk
vim-python
```

### Any tips or rututorial?
```
vimtutor zh 
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
