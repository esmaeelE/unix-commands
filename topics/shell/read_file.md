# loop in bash

# read a file line by line with while
```
while IFS="" read -r p || [ -n "$p" ]
do
    ((i=i+1))
    stem=$(basename "${p}")
    echo $p
    env/bin/python3 code.py "$p" out/$i_$stem

done < "list.txt"
```

