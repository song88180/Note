Run matlab in bash script:
```bash
matlab -nodisplay -nodesktop -r "run /path/to/script.m"
```

Replace substring:
```matlab
newStr = strrep(str,old,new)
newStr = replace(str,[old1,old2],[new1,new2])
```

Get positions of a number in an array:
```matlab
find(Array==1)
```

Delete multiple column in an matrix:
```matlab
a(:,[1,3,5]) = [];
```
