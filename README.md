# low-level_programming_in_c
Code snippets to embed assembly code in C programs.


## Basic

```c
#include <stdio.h>

int main(){
  int x = 5;
  int y = 999;
  
  __asm__(
    "xchg 1, 0"
    : "+m" (x), "+r" (y)
  );
  
  printf("%d\n", x);
  printf("%d\n", y);
  return 0;
}
```

## Compiling

```
$ gcc sample.c -o sample -masm=intel
```
