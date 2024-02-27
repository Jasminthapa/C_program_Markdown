```
#include <stdio.h>

int main() {
  int a;
  int *pt;

  printf("Pointer Example Program : Increment and Decrement Integer\n");
  a = 10;
  pt = &a;

  (*pt)++; 
  printf("\n[a]:Increment Value of A = %d", a);

  ++(*pt); 
  printf("\n[a]:Increment Value of A = %d", a);


  (*pt)--; 
  printf("\n[a]:Decrement Value of A = %d", a);

  --(*pt); 
  printf("\n[a]:Decrement Value of A = %d", a);

  return 0;
}
```