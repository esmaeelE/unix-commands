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
$ echo $?
1
```
