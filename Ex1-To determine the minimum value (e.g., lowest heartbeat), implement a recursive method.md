# EX 1 You’re creating a health monitoring device which stores several sensor readings in an array. To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.
## DATE: 20-09-2026
## AIM:
To write a JAVA program To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.

## Algorithm
1. Read the number of heartbeat values n.
2. Store the heartbeat values in an integer array.
3. Create a recursive method findMin() to find the minimum value.
4. If only one value is present, return that value as the minimum.
5. Recursively find the minimum among the first n-1 values.
6. Compare the last value with the recursive minimum.
7. Return the smaller value.
8. Display the minimum heartbeat value.  

## Program:
```
/*
Program To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.
Developed by: SHASMITHAA SANKAR
RegisterNumber:  212224040311
*/
```

```java

import java.util.*;

public class Main {
    static int getMin(int[] arr, int i, int n) 
    {
        
        if (i == n - 1)
            return arr[i];
        
        int minRest = getMin(arr, i + 1, n);
        return Math.min(arr[i], minRest);
        
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for(int i=0; i<n; i++) {
            arr[i] = sc.nextInt();
        }
        System.out.println(getMin(arr, 0, n));
    }
}

```

## Output:


<img width="715" height="376" alt="image" src="https://github.com/user-attachments/assets/105ba0b8-39ec-4a5d-a60e-4f1591cc41cd" />




## Result:
Thus the JAVA prograM ti find the minimum value (e.g., lowest heartbeat), implement a recursive method has implemented successfully
