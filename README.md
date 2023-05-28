# get_next_line 

## Because reading line by line is easier

This project is part of the first circle of projects of the 42 cursus. The goal is to create a function which return the next line of a file based on a file descriptor. It also make me learn about static variables(variables that are declared only one time and keep their value between two calls of the same function). You will find the subject of the project into the repository. My grade : 112/100 

## How to use it

1. Clone it `git clone git@github.com:AnthonyVerdon-42Projects/get_next_line.git`
1. Add `get_next_line.h` to your file. You can also add `get_next_line_bonus.h` to be able to read on multiple files at the same time.
2. Compile it on your project.

## Examples of usage

```
#include <fcntl.h>
#include "get_next_line.h"

int fd;
char *line;

fd = open({filename}, O_RDONLY);
line = get_next_line(fd); //return the first line of the file
free(line);
line = get_next_line(fd); // return the second one
free(line);
...
```

This function allocate memory on the heap. Don't forget to use the `free` function after a call to this function.

## Find a bug ?

If you find an undefined behaviour (crash, leaks, ...), please submit an issue or contact me
