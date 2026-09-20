# Ex4 You are given a Java program that performs matrix addition. If Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension, what will be the nature (even/odd/mixed) of the resulting matrix?
## DATE:20-09-2026
## AIM:
To write a java function to evaluate weather the given Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension and find the nature of resultant matrrix.

## Algorithm
1. Read the dimensions of matrices A and B.
2. Check whether both matrices have the same dimensions.
3. Check every element of matrix A; all elements must be odd.
4. Check every element of matrix B; all elements must be even.
5. If both conditions are satisfied, add corresponding elements of A and B to form the resultant matrix.
6. Since odd + even = odd, every element of the resultant matrix will be odd.
7. If either matrix does not satisfy its required condition or dimensions differ, display that the condition is not satisfied.  

## Program:
```
/*
Program to ind the nature of resultant matrrix.

Developed by: SHASMITHAA SANKAR
RegisterNumber:  212224040311
*/
```

```java

import java.util.*;

public class MatrixNature {

    static boolean isOddMatrix(int[][] A) {
        for (int i = 0; i < A.length; i++) {
            for (int j = 0; j < A[0].length; j++) {
                if (A[i][j] % 2 == 0) {
                    return false;
                }
            }
        }
        return true;
    }

    static boolean isEvenMatrix(int[][] B) {
        for (int i = 0; i < B.length; i++) {
            for (int j = 0; j < B[0].length; j++) {
                if (B[i][j] % 2 != 0) {
                    return false;
                }
            }
        }
        return true;
    }

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        int r = sc.nextInt();
        int c = sc.nextInt();

        int[][] A = new int[r][c];
        int[][] B = new int[r][c];
        int[][] result = new int[r][c];

        // Read Matrix A
        for (int i = 0; i < r; i++) {
            for (int j = 0; j < c; j++) {
                A[i][j] = sc.nextInt();
            }
        }

        // Read Matrix B
        for (int i = 0; i < r; i++) {
            for (int j = 0; j < c; j++) {
                B[i][j] = sc.nextInt();
            }
        }

        if (isOddMatrix(A) && isEvenMatrix(B)) {

            for (int i = 0; i < r; i++) {
                for (int j = 0; j < c; j++) {
                    result[i][j] = A[i][j] + B[i][j];
                }
            }

            System.out.println("Resultant Matrix:");

            for (int i = 0; i < r; i++) {
                for (int j = 0; j < c; j++) {
                    System.out.print(result[i][j] + " ");
                }
                System.out.println();
            }

            System.out.println("Nature of resultant matrix: Odd");

        } else {
            System.out.println("Condition not satisfied");
        }
    }
}

```

## Output:


<img width="978" height="552" alt="image" src="https://github.com/user-attachments/assets/c2514404-c9e9-4bde-b505-c807f9847352" />






## Result:
Thus, the java program to evaluate weather the given Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension and find the nature of resultant matrrix is implemented successfully.
