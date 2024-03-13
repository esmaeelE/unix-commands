# File processing in Unix environment

## Remove first line from text file
```
sed '1d' file_name.txt
```

### Add file name to first coloumn
```
awk '{print FILENAME (NF?" , ":"") $0}' file_name.txt
```

### Print first coloumn/ not work
```
$ awk -F: '{print $1}' file_name.txt
```
