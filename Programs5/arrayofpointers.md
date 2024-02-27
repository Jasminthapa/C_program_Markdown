```
#include <stdio.h>

int main()
{
  // array declaration and initialization
  int arr[5] = {2, 4, 6, 8, 10}, i;
	
  for(i = 0; i < 5; i++)
  {
	// printing the elements address and value at
	// arr[i] using *(arr + i) syntax
	printf("[index %d] Address : %u, Value : %d\n", i, (arr + i), *(arr + i));
  }
	
  return 0;
}
```
