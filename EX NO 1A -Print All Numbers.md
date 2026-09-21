
# EX 1A Print All Numbers 

## AIM:
To Write a Java program that takes an integer input N from the user and prints all the numbers from 1 to N, separated by spaces, on a single line..

## Algorithm
1.Start the program.

2.Input an integer N from the user.

3.Check condition:
If N <= 0, display "Invalid input. N must be greater than 0." and stop.

4.Initialize a variable i = 1.

5.Use a loop to print numbers from 1 to N:

While i <= N, print i followed by a space.

Increment i by 1.

End loop and stop the program. 
 

## Program:
```

/*
Program to implement Reverse a String
Developed by: MONISH N
Register Number: 212223240097
*/


import java.util.*; 
public class demo   
{
    public static void main(String args[]) 
    {
        int N,i;
        Scanner sc=new Scanner(System.in);
        N=sc.nextInt();  
        if(N<=0)
        {
            System.out.println("Invalid input. N must be greater than 0.");
            
        }
        else{
            for(i=1;i<=N;i++){
                System.out.print(i+" ");    
            }
        }
    }
}
```

## Output:
<img width="425" height="152" alt="image" src="https://github.com/user-attachments/assets/54163f54-8ab1-4383-ad7b-35428ac584b3" />


## Result:
The program successfully print all the numbers from 1 to N. 
