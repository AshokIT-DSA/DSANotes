**Problem Statemnt:- Given an array of integers, calculate the ratios of its elements that are positive, negative, and zero. Print the decimal value of each fraction on a new line with  places after the decimal.**

**Pre- Requisite:- Arrays, for loop concept.**  
**Difficulty:- Easy.**  

[![image](https://www.linkpicture.com/q/Plus-Minus.png)](https://www.linkpicture.com/view.php?img=LPic6325cab73cc871915219114)


```.java
import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.regex.*;

public class Solution {

    // Complete the plusMinus function below.
    static void plusMinus(int[] arr)
     {
         int count=0,count2=0,count3=0;
         double div1,div2,div3; 
         for(int i=0;i<arr.length;i++)
         {
             if(arr[i]>0)
             {
                 count++;
             }
             else if(arr[i]<0)
             {
                 count2++;
             }
             else
             {
                 count3++;
             }
         }
         div1=count/(double)arr.length;
         div2=count2/(double)arr.length;
         div3=count3/(double)arr.length;
         System.out.println(div1);
         System.out.println(div2);
         System.out.println(div3);

    }

    private static final Scanner scanner = new Scanner(System.in);

    public static void main(String[] args) {
        int n = scanner.nextInt();
        scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");

        int[] arr = new int[n];

        String[] arrItems = scanner.nextLine().split(" ");
        scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");

        for (int i = 0; i < n; i++) {
            int arrItem = Integer.parseInt(arrItems[i]);
            arr[i] = arrItem;
        }

        plusMinus(arr);

        scanner.close();
    }
}

```
Time Complexity :- O(N)  
Space Complexity:- O(1)