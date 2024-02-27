```
#include<stdio.h>
#include<math.h>
int main()
{

    int row_size,col_size;
    printf("Enter the row Size Of the Matrix:");
    scanf("%d",&row_size);
    printf("Enter the columns Size Of the Matrix:");
    scanf("%d",&col_size);

    int matrix[row_size][col_size];

    int i,j;
    printf("Enter the Matrix Element:\n");
    for(i=0;i<row_size;i++)
    {
        for(j=0;j<col_size;j++)
        {
            scanf("%d",&matrix[i][j]);
        }
    }

     for(i=0;i<row_size;i++)
    {
        for(j=0;j<col_size;j++)
        {
            matrix[i][j]=pow(matrix[i][j],2);
        }
    }
    printf("Square of the Matrix elements are:\n");
     for(i=0;i<row_size;i++)
    {
        for(j=0;j<col_size;j++)
        {
           printf("%d ",matrix[i][j]);
        }
        printf("\n");
    }
}
```