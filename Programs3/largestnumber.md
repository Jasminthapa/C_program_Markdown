```
#include<stdio.h>

int main()
{
    int n,i;
    float c,big;

    printf("\n\nEnter the number of elements you wish to find the greatest element of: ");
    scanf("%d", &n);
    printf("\n\nEnter %d numbers :\n", n);

    printf("\n\n\t\t\tElement 1: ");
    scanf("%f", &big);

    for(i = 2; i <= n; i++)
    {
        printf("\n\t\t\tElement %d  : ", i);
        scanf("%f", &c);
        if(big < c)  
            big = c;    value
    }

    printf("\n\n\nThe largest of the %d numbers is  %f ", n, big);5
    
    return 0;
}
```