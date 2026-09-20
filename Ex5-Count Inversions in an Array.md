# Ex5 Count Inversions in an Array
## DATE:20-09-2026
## AIM:
To write a Java program  to Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < j

## Algorithm
1. Read the size n and elements of the array.
2. Initialize count = 0 to store the number of inversions.
3. Use two loops to compare every pair of elements.
4. For each pair (i, j), ensure i < j.
5. Check whether arr[i] > arr[j].
6. If the condition is true, increment count.
7. After checking all pairs, display the total number of inversions. 

## Program:
```
/*
Program toto Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < j
Developed by:  SHASMITHAA SANKAR
RegisterNumber:  212224040311
*/
```

```java

import java.util.Scanner;

public class CountInversions {
    public static int mergeSortAndCount(int[] arr, int left, int right) {
        int count = 0;
        if (left < right) {
            int mid = (left + right) / 2;
            count += mergeSortAndCount(arr, left, mid);
            count += mergeSortAndCount(arr, mid + 1, right);
            count += mergeAndCount(arr, left, mid, right);
        }
        return count;
    }

    private static int mergeAndCount(int[] arr, int left, int mid, int right) {
        int[] leftArr = new int[mid - left + 1];
        int[] rightArr = new int[right - mid];

        for (int i = 0; i < leftArr.length; i++) leftArr[i] = arr[left + i];
        for (int i = 0; i < rightArr.length; i++) rightArr[i] = arr[mid + 1 + i];

        int i = 0, j = 0, k = left, swaps = 0;

        while (i < leftArr.length && j < rightArr.length) {
            if (leftArr[i] <= rightArr[j]) {
                arr[k++] = leftArr[i++];
            } else {
                arr[k++] = rightArr[j++];
                swaps += (leftArr.length - i); // Count inversions
                
            }
       
        }

        while (i < leftArr.length) arr[k++] = leftArr[i++];
        while (j < rightArr.length) arr[k++] = rightArr[j++];

        return swaps;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for (int i = 0; i < n; i++) arr[i] = sc.nextInt();
        System.out.println(mergeSortAndCount(arr, 0, n - 1));
    }
}


```

## Output:

<img width="537" height="360" alt="image" src="https://github.com/user-attachments/assets/82354cb1-0afd-4c85-8673-931e8a1af3e8" />



## Result:
Thus the Java program to to Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < jis implemented successfully.
