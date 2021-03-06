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
## make alias for cd
```bash
## Make alias for the path to a frequently used directory.
alias cdHtml="cd /usr/share/nginx/html/"
```

## sort files in a directory by size recursively
```bash
du -ah $DIR | grep -v "/$" | sort -rh

# Don't show directory
find . -type f -printf "%s\t%p\n" | sort -n

# Don't show directory, more readable
find . -name "*.ipynb" -print0 | du -sh --files0-from=- 

# Find the total size of certain files within a directory branch
find . -type f -name '*.jpg' -exec du -ch {} + | grep total$
```
