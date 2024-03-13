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

### Count line number
```
wc -l file_name.txt
# faster with gawk
awk 'END{print NR}' file_name.txt
```

### list all files in fullpath form

```
/bin/ls -1dU $PWD/* > $output_path
```

### Make a list out of all files in full path form, by adding prefix to each line
```
awk '{print "/icb/product/ict/ICTPRD/ICTPRD/rating/data/mvne/"$0}' all_files.list > fullpath.list
```


