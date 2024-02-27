```
#include<stdio.h>
int a,b;
int main()
{
    printf("\n\nEnter the two values to find the greatest and smallest number: \n");
    scanf("%d%d", &a, &b);

    if(a == b)
        printf("Both are equal\n");
        
    else if(a < b)
    {
        printf("\n\nThe largest number is %d\n", b);
        printf("\nThe smallest number is %d\n", a);
    }
    else  
    {
        printf("The largest number is %d\n", a);
        printf("The smallest number is %d\n", b);
    }
    return 0;
}
```