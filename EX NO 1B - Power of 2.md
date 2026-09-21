# EX 1B Power of 2

## AIM:
To write a Java program to for given constraints.Given an integer n, return true if it is a power of two. Otherwise, return false.
An integer n is a power of two, if there exists an integer x such that n == 2x.

## Algorithm
1.Start the program.

2.Input an integer n from the user.

3.Check if n is less than or equal to 0:

If yes, display false and stop (since negative numbers and 0 are not powers of two).

4.Use bitwise operation:

Compute (n & (n - 1)).

If the result is 0, then n is a power of two; otherwise, it is not.

5.Display the result (true or false) and stop the program.
  

## Program:
```

/*
Program to implement Reverse a String
Developed by: POZHILAN V D
Register Number: 212223240118
*/

import java.util.Scanner;

public class Solution {

    public boolean isPowerOfTwo(int n) {
     if(n<=0)
     return false;
     else
     return (n&(n-1))==0;     
    }
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Solution sol = new Solution();
        int n = scanner.nextInt();
        boolean result = sol.isPowerOfTwo(n);
        System.out.println(result);

        scanner.close();
    }
}

```

## Output:
<img width="403" height="198" alt="image" src="https://github.com/user-attachments/assets/5ad4dd66-64a4-4aff-b00d-a9d51f790f20" />


## Result:
The program successfully implemented and the expected output is verified.
