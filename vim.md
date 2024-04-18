# Vim

## Moving to previous spot
* control-o - backwards
* control-i - forwards
* :jumps - see all places

## Panes

* swap panes - control+w control+x
* make panes 50/50 - control+w =
* move pane split left  - control+w  <
* move pane split right - control+w  >

### Moving existing split pane into it's own tab
* control+w, shift-t

see:
```
:help Ctrl-W_T
:help Ctrl-W
```

* https://www.techrepublic.com/blog/linux-and-open-source/using-vi-key-bindings-in-bash-and-zsh/
* https://stackoverflow.com/questions/36843099/in-vim-how-can-i-delete-everything-between-quotes-including-the-quotes/36843100

## Text-objects

* da"  - delete all including quotes
* di"  - delete all including quotes
* va"  - replace all inside quotes
* vi"  - replace all inside quotes

## Capitalization
all of you should know the gu{motion} and gU{motion} commands used to convert a region to lower/upper case. Unfortunately, there is no possibility to capitalize a region. Until now this tip.

capitalize)

* gUw - capitalize word
* guw - lower case word

## Multicursors
https://medium.com/@schtoeffel/you-don-t-need-more-than-one-cursor-in-vim-2c44117d51db

* gn - text object select word
* cgn - change searched for word forwards, dot . - to repeat
* n - skip to next word match

## Refresh Vim screen
* control + l
* :redraw!

## Show Ruler

* :set ruler

## Open last closed tab
```
:ls " get the buffer number
:tabnew +Nbuf " where N is the buffer number
:tabnew +18buf
```

## Open list of last run commands (happens by mistake alot)
```
q:
```
to get out of this just go ahead and
```
:q
```

## Change Directory
### present working directory
```
:pwd
```

### change to the directory of the currently opened file
```
:cd %:p:h
```

### change to the directory of the current window
```
:lcd %:p:h
```

### auto change directory  in vimrc
```
set autochdir
```
