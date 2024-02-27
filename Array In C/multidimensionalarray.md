
+++ title = "Multidimensional Array in C" weight = 3 description = "Learn about multidimensional arrays in C, including two-dimensional and three-dimensional arrays. Explore initialization, transpose, and diagonal sum examples." keywords = "multidimensional array in C, 2D array, 3D array, array initialization, transpose matrix, diagonal sum in C." +++

### Multidimensional Array
Multidimensional arrays are those which have more than one dimension.
The general form is:
```c
Datatype arrayName[size1][size2][size3]
```
### Types Of Multidimensioanl
- Two dimensional array
- Three dimensional array
### Two-Dimensional Array**
In 2-D array,two subsripts are used.So it is called matrix.
The general form of 2-D array is:
```c
Datatype arrayName[row size][colum size];
```

### Initialization of 2D Array in C
In 2D array we have to declare at least second dimension of the array.It can be declared by both **compile time** and **run time**.
### Compile time initialization
Compile time refers to assinging values to the array while writing the **source code**.
General form is:
```c
DataType ArrayName[rowsize][rowsize]={{values in first row},{values in second row}{values in last row}};
```
```c
int num[3][3]={{1,2,3},{4,5,6}{6,7,8}};
```
It also can be written as:
```c
int num[][3]={{1,2,3},{4,5,6}{6,7,8}};
```
{{% notice %}}If we don't give row size the compiler automatically sets the row size.{{% /notice %}}
**Example To Show Compile Time Initialization** 
```c
#include <stdio.h>

int main() {
    int i,j;
    // 2D array initialization
    int matrix[3][4] = {
        {1, 2, 3, 4},
        {5, 6, 7, 8},
        {9, 10, 11, 12}
    };

    // Displaying the initialized array
    for ( i = 0; i < 3; i++) {
        for (j = 0; j < 4; j++) {
            printf("%d\t", matrix[i][j]);
        }
        printf("\n");
    }

    return 0;
}
```
### Run time initialization
Run time initialization refers to assinging the values after the program execution.In this loops are used to control row-wise and column-wise data entry.
### Example
 
```c
 #include <stdio.h>

int main() {
    int rows, cols,i,j;

    
    printf("Enter the number of rows: ");
    scanf("%d", &rows);

    printf("Enter the number of columns: ");
    scanf("%d", &cols);

    // Declare a 2D array with user-specified dimensions
    int matrix[rows][cols];

    // Get input for each element from the user
    printf("Enter the elements of the matrix:\n");
    for ( i = 0; i < rows; i++) {
        for ( j = 0; j < cols; j++) {
            printf("Element[%d][%d]: ", i, j);
            scanf("%d", &matrix[i][j]);
        }
    }

    // Display the initialized array
    printf("\nThe matrix you entered is:\n");
    for ( i = 0; i < rows; i++) {
        for ( j = 0; j < cols; j++) {
            printf("%d\t", matrix[i][j]);
        }
        printf("\n");
    }

    return 0;
}
```
### Example To Demonstrate Transpose of Matrix.
```c
#include <stdio.h>

#define MAX_ROWS 10
#define MAX_COLS 10

void transposeMatrix(int mat[MAX_ROWS][MAX_COLS], int result[MAX_COLS][MAX_ROWS], int rows, int cols) {
    int i, j;  // Declare i and j here
    for (i = 0; i < rows; ++i) {
        for (j = 0; j < cols; ++j) {
            result[j][i] = mat[i][j];
        }
    }
}
void displayMatrix(int mat[MAX_ROWS][MAX_COLS], int rows, int cols) {
    int i, j;  // Declare i and j here
    for (i = 0; i < rows; ++i) {
        for (j = 0; j < cols; ++j) {
            printf("%d\t", mat[i][j]);
        }
        printf("\n");
    }
}

int main() {
    int matrix[MAX_ROWS][MAX_COLS];
    int transposed[MAX_COLS][MAX_ROWS];
    int rows, cols, i, j;

    printf("Enter the number of rows and columns for the matrix (max 10 each):\n");
    scanf("%d%d", &rows, &cols);

    if (rows > MAX_ROWS || cols > MAX_COLS) {
        printf("Error: Matrix size exceeds the maximum limit.\n");
        return 1;
    }

    printf("Enter the elements of the matrix:\n");
    for (i = 0; i < rows; ++i) {
        for (j = 0; j < cols; ++j) {
            scanf("%d", &matrix[i][j]);
        }
    }

    printf("\nOriginal Matrix:\n");
    displayMatrix(matrix, rows, cols);

    transposeMatrix(matrix, transposed, rows, cols);

    printf("\nTransposed Matrix:\n");
    displayMatrix(transposed, cols, rows);

    return 0;
}
```
### Example: To Find The Sum Of Diagnol Elements
```c 
#include <stdio.h>

#define ROWS 3
#define COLS 3

// Function to find the sum of the diagonal elements in a 2D array
int findDiagonalSum(int arr[ROWS][COLS]) {
    int sum = 0,i,j;

    for (i = 0; i < ROWS; i++) {
        for (j = 0; j < COLS; j++) {
            // Check if the element is on the diagonal
            if (i == j) {
                sum += arr[i][j];
            }
        }
    }

    return sum;
}

int main() {
    int arr[ROWS][COLS],i,j;

    // Input array elements
    printf("Enter the elements of the 2D array (%d x %d):\n", ROWS, COLS);
    for (i = 0; i < ROWS; i++) {
        for (j = 0; j < COLS; j++) {
            scanf("%d", &arr[i][j]);
        }
    }

    // Display the entered array
    printf("Entered 2D array:\n");
    for (i = 0; i < ROWS; i++) {
        for (j = 0; j < COLS; j++) {
            printf("%d\t", arr[i][j]);
        }
        printf("\n");
    }

    // Find and display the sum of diagonal elements
    int diagonalSum = findDiagonalSum(arr);
    printf("Sum of diagonal elements: %d\n", diagonalSum);

    return 0;
}

```
### Three dimensional array

 A three-dimensional array is an array of arrays of arrays.It's syntax is

 ```c
 datatype arrayName[x_size][y_size][z_size];
```
  