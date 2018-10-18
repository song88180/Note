Reformat in vim for a nice column layout:
```vim
:%!column -t
:%!column -s $'\t' -t
```
Add 1 to all the number in the text:
```vim
:%s/\d\+/\=submatch(0)+1/g
```
insert line numbers before each line:
```vim
:%s/^/\=printf('%-4d', line('.'))
```
