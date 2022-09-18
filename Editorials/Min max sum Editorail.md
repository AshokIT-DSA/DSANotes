## Min max sum Editorial

*Problem Statement:- Given five positive integers, find the minimum and maximum values that can be calculated by summing exactly four of the five integers*   

**Pre-Requisite:- Array, for loops**  
**Difficulty:-easy**  
[![image](https://www.linkpicture.com/q/min-max-sum_1.png)](https://www.linkpicture.com/view.php?img=LPic6325d900d4cea2014105095)

[![image](https://www.linkpicture.com/q/min-max-sum1.png)](https://www.linkpicture.com/view.php?img=LPic6325d6fc6c65b583708203)

```.java
import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.regex.*;

public class Solution {

    // Complete the miniMaxSum function below.
    static void miniMaxSum(int[] arr) 
    {
       Arrays.sort(arr);
       long small=0,big=0;
       for(int i=0;i<arr.length-1;i++){
           small=small+arr[i];
       }
       for(int i=1;i<arr.length;i++){
           big=big+arr[i];
       }
      
       System.out.println(small+" "+big);
       
       
      
        


    }

    private static final Scanner scanner = new Scanner(System.in);

    public static void main(String[] args) {
        int[] arr = new int[5];

        String[] arrItems = scanner.nextLine().split(" ");
        scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");

        for (int i = 0; i < 5; i++) {
            int arrItem = Integer.parseInt(arrItems[i]);
            arr[i] = arrItem;
        }

        miniMaxSum(arr);

        scanner.close();
    }
}

```

Time Complexity:- O(Nlogn)  
Space COmplexity:-O(1)