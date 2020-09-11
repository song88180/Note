Reformat in vim for a nice column layout:
```vim
:%!column -t
:%!column -s $'\t' -t
```
Add 1 to all the number in the text:
```vim
:%s/\d\+/\=submatch(0)+1/g
```
Insert line numbers before each line:
```vim
:%s/^/\=printf('%-4d', line('.'))
```
Set indent:
```vim
" show existing tab with 4 spaces width
set tabstop=4
" when indenting with '>', use 4 spaces width
set shiftwidth=4
" On pressing tab, insert 4 spaces
set expandtab
```

If forget to sudo:
```vim
w !sudo tee %
```

Find all un-printable charactor:  
https://stackoverflow.com/questions/3844311/how-do-i-replace-or-find-non-printable-characters-in-vim-regex
```vim
/[^[:print:]]  " find <85>, <99>, etc.
/[[:cntrl:]]  " find ^F, ^S, etc.
```
