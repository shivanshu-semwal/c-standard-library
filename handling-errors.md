# Handling Errors

```c
#include <stdio.h>
#include <string.h>
#include <errno.h>

int main () {
    FILE *fp;   
    fp = fopen("file.txt","r");
    if( fp == NULL ) {
        // strerror generates the error message for you
        // Declaration: char *strerror(int errnum)
        printf("Error: %s\n", strerror(errno));
    }

    return(0);
}
```