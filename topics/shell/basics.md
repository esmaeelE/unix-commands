# Unix shell commands

## BASH

Environment variables

```
$ : pid of current shell

? : last command return value, exit status of the last executed command.

0 : shell name

```

Example
```
echo $$
echo $? 
```

## Example code

**C**

`hello.c`
```
#include <stdio.h>                                                            
                                                                              
int main(void){                   
    printf("Hello world!\n");                                                 
    return 1;                                                                 
}
```

Output

```
$ gcc -Wall hello.c -o hello
$ ./hello
Hello world!
$ echo $?
1
```

**python**

```
$ cat test.py 
#!/bin/python3 
import sys
print("Hello python")
sys.exit(5)
```

Output

```
$ python3 hello.py 
Hello python
$ echo $?
5
```
