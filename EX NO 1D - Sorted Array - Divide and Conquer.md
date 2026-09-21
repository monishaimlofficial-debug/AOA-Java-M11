# EX 1D Sorted Array using Divide and Conquer Approach.

## AIM:
To write a Java program to for given constraints.
Given two sorted arrays nums1 and nums2 of size m and n respectively, return the median of the two sorted arrays.

The overall run time complexity should be O(log (m+n)).

## Algorithm
1.Start the program.
Read the sizes of two sorted arrays m and n, then input the elements of both arrays nums1 and nums2.

2.Initialize two pointers p1 = 0 and p2 = 0 to traverse both arrays.

3.Use a helper function getMin() to return the smaller of the current elements from both arrays and move the corresponding pointer forward.

4.Find the median:

If the total number of elements (m + n) is even, skip (m + n)/2 - 1 elements, then take the average of the next two smallest elements as the median.

If (m + n) is odd, skip (m + n)/2 elements, then take the next smallest element as the median.

5.Display the computed median and stop the program.  

## Program:
```

/*
Program to implement Reverse a String
Developed by: MONISH N
Register Number: 212223240097
*/

import java.util.Scanner;
public class Solution {
    private int p1 = 0, p2 = 0;
    // Get the smaller value between nums1[p1] and nums2[p2], and move the pointer forward
    private int getMin(int[] nums1, int[] nums2) {
        if (p1 < nums1.length && p2 < nums2.length) {
            return nums1[p1] < nums2[p2] ? nums1[p1++] : nums2[p2++];
        } else if (p1 < nums1.length) {
            return nums1[p1++];
        } else if (p2 < nums2.length) {
            return nums2[p2++];
        }
        return -1; // Should not reach here if input is valid
    }
    // Main logic to find median of two sorted arrays
    public double findMedianSortedArrays(int[] nums1, int[] nums2) {
       int m=nums1.length,n=nums2.length;
       if((m+n)%2==0){
           for(int i=0;i<(m+n)/2-1;++i){
               int tmp=getMin(nums1,nums2);
           }
           return (double) (getMin(nums1,nums2)+getMin(nums1,nums2))/2;
       }
       else{
           for(int i=0;i<(m+n)/2;++i){
               int tmp=getMin(nums1,nums2);
           }
           return getMin(nums1,nums2);
       }
    }
    // Main method with user input
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Solution sol = new Solution();

        // Input for nums1
        //System.out.print("Enter size of first sorted array: ");
        int m = sc.nextInt();
        int[] nums1 = new int[m];
        //System.out.println("Enter " + m + " sorted integers for first array:");
        for (int i = 0; i < m; i++) {
            nums1[i] = sc.nextInt();
        }
        // Input for nums2
        //System.out.print("Enter size of second sorted array: ");
        int n = sc.nextInt();
        int[] nums2 = new int[n];
        //System.out.println("Enter " + n + " sorted integers for second array:");
        for (int i = 0; i < n; i++) {
            nums2[i] = sc.nextInt();
        }

        // Find and display the median
        double median = sol.findMedianSortedArrays(nums1, nums2);
        System.out.println("Median of the two sorted arrays = " + median);
        
        sc.close();
    }
}

```

## Output:
<img width="883" height="330" alt="image" src="https://github.com/user-attachments/assets/d430c9c0-0455-4220-811f-1a6ab58b32f7" />

## Result:
The program successfully implemented and the expected output is verified.
