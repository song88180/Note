## grep
matching multiple patterns:
```bash
grep -E 'pattern1|pattern2' filename
grep 'pattern1\|pattern2' filename
```
## loop through a list of files in directory.
```bash
for i in ls -1 path/to/dir; do
```

## nice & renice
```bash
nice -n X command
renice -n X -p PID
```

## awk
```bash
## tab delimited
awk -F $'\t' '{print $1,$2,$3}'
```

## sort
```bash
## -t separator, -k column, -r reverse, -n numeric ranking
sort -t, -k2,2 file
```
