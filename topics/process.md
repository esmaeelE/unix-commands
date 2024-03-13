# Processing many files

Obvious way to find desired files and execute command on each one is very slow and not suitable.

We can divide task

* Generate list of files
* Do work on list of files

I find two methods to do this

1. This is much more faster

```
#make sure output directory exists.
mkdir -p output

# save current directory address
CURRNT_DIR=$PWD

## raw file path
/bin/ls -1U /icb/product/ict/ICTPRD/ICTPRD/rating/data/mvne/  > $CURRNT_DIR/output/all_files.list

cd $CURRNT_DIR/output
# make a list out of all files in full path form, by adding prefix to each line
awk '{print "/icb/product/ict/ICTPRD/ICTPRD/rating/data/mvne/"$0}' all_files.list > fullpath.list
```


2. s

```
# You can change these two lines
input_path=/icb/product/ict/ICTPRD/ICTPRD/AAR/archive/csv
output_path=/tmp/$1

# go to source directory
cd $input_path

# list all files in fullpath form
/bin/ls -1dU $PWD/* > $output_path

# return to previous directory
cd -

```





