## A big sum editorial

Problem Statement:- Given an array of integers, we have to find out the sum of all the elements of the array.

**Pre-Requisite:- For loops, Arrays.**    
**Difficulty:-Easy.**    

Basic Intuition:-
We will iterate through the whole array till it reaches the end and add all the elements to the sum variable and return sum as answer.
Hint : - We just need to initial sum as long and the rest of the code remains same.

```.java
import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.regex.*;

public class Solution {

    // Complete the aVeryBigSum function below.
    static long aVeryBigSum(long[] ar) 
    {
        long sum=0;
        for(int i=0;i<ar.length;i++)
        {
            sum=sum+ar[i];
        }

return sum;
    }

    private static final Scanner scanner = new Scanner(System.in);

    public static void main(String[] args) throws IOException {
        BufferedWriter bufferedWriter = new BufferedWriter(new FileWriter(System.getenv("OUTPUT_PATH")));

        int arCount = scanner.nextInt();
        scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");

        long[] ar = new long[arCount];

        String[] arItems = scanner.nextLine().split(" ");
        scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");

        for (int i = 0; i < arCount; i++) {
            long arItem = Long.parseLong(arItems[i]);
            ar[i] = arItem;
        }

        long result = aVeryBigSum(ar);

        bufferedWriter.write(String.valueOf(result));
        bufferedWriter.newLine();

        bufferedWriter.close();

        scanner.close();
    }
}

```

Time Complexity:- O(N)  
Space Complexity :- O(1)