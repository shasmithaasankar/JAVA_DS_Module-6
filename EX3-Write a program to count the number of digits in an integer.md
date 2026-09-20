# EX3 Write a program to count the number of digits in an integer.
## DATE: 20-09-2026
## AIM:
To write a C program to implement Tower of Hanoi

## Algorithm
1. Read the number of disks n.
2. Define a recursive method towerOfHanoi() with the number of disks and three rods: source, auxiliary, and destination.
3. If there is only one disk, move it directly from the source rod to the destination rod.
4. Recursively move n-1 disks from the source rod to the auxiliary rod.
5. Move the remaining largest disk from the source rod to the destination rod.
6. Recursively move the n-1 disks from the auxiliary rod to the destination rod.
7. Repeat these steps until all disks are moved.
8. Display each disk movement.  

## Program:
```
/*
Program to to count the number of digits in an integer
Developed by: SHASMITHAA SANKAR
RegisterNumber:  212224040311
*/
```

```java

import java.util.*;

public class TowerOfHanoi {

    static void towerOfHanoi(int n, char source, char auxiliary, char destination) {

        // Base case
        if (n == 1) {
            System.out.println("Move disk 1 from " + source + " to " + destination);
            return;
        }

        // Move n-1 disks from source to auxiliary
        towerOfHanoi(n - 1, source, destination, auxiliary);

        // Move the largest disk to destination
        System.out.println("Move disk " + n + " from " + source + " to " + destination);

        // Move n-1 disks from auxiliary to destination
        towerOfHanoi(n - 1, auxiliary, source, destination);
    }

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();

        towerOfHanoi(n, 'A', 'B', 'C');
    }
}

```



## Output:


<img width="877" height="388" alt="image" src="https://github.com/user-attachments/assets/5148c3da-dc18-46cf-aedf-1b13c30c45dc" />






## Result:
Thus, the Java program to to count the number of digits in an integer is implemented successfully.
