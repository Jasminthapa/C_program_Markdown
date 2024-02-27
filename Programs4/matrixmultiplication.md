```
#include<stdio.h>

int main() {
    int m1, n1, m2, n2, i, j, k;

    printf("Enter the size of matrix A:\nNo. of rows: ");
    scanf("%d", &m1);
    printf("No. of columns: ");
    scanf("%d", &n1);

    printf("\nEnter the size of matrix B:\nNo. of rows: ");
    scanf("%d", &m2);
    printf("No. of columns: ");
    scanf("%d", &n2);

    if (n1 != m2) {
        printf("Invalid matrix dimensions for multiplication.\n");
        return 1; // Return an error code
    }

    double a[m1][n1], b[m2][n2], result[m1][n2];

    printf("\nEnter the elements of matrix A:\n");
    for(i = 0; i < m1; i++) {
        for(j = 0; j < n1; j++) {
            scanf("%lf", &a[i][j]);
        }
    }

    printf("\nEnter the elements of matrix B:\n");
    for(i = 0; i < m2; i++) {
        for(j = 0; j < n2; j++) {
            scanf("%lf", &b[i][j]);
        }
    }

    for(i = 0; i < m1; i++) {
        for(j = 0; j < n2; j++) {
            result[i][j] = 0;
        }
    }
    for(i = 0; i < m1; i++) {
        for(j = 0; j < n2; j++) {
            for(k = 0; k < n1; k++) {
                result[i][j] += a[i][k] * b[k][j];
            }
        }
    }

    printf("\nThe product of matrices A and B is:\n");
    for(i = 0; i < m1; i++) {
        for(j = 0; j < n2; j++) {
            printf("%lf \t", result[i][j]);
        }
        printf("\n");
    }

    return 0;
}
```