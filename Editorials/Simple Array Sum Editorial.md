## Simple Array sum editorial

*Problem Statement:- Given an array of integers, we have to find out the sum of all the elements of the array.*

**Pre-Requisite:- For loops, Arrays.**     
**Difficulty:-Easy.**  

Basic Intuition:-
We will iterate through the whole array till it reaches the end and add all the elements to the sum variable and return sum as answer.


```.java
import java.io.*;
import java.math.*;
import java.text.*;
import java.util.*;
import java.util.regex.*;

public class Solution {

    /*
     * Complete the simpleArraySum function below.
     */
    static int simpleArraySum(int[] ar) {
        /*
         * Write your code here.
         */
         int sum=0;
         for(int i=0;i<ar.length;i++)
         {
             sum=sum+ar[i];
         }
         return sum;

    }

    private static final Scanner scanner = new Scanner(System.in);

    public static void main(String[] args) throws IOException {
        BufferedWriter bufferedWriter = new BufferedWriter(new FileWriter(System.getenv("OUTPUT_PATH")));

        int arCount = Integer.parseInt(scanner.nextLine().trim());

        int[] ar = new int[arCount];

        String[] arItems = scanner.nextLine().split(" ");

        for (int arItr = 0; arItr < arCount; arItr++) {
            int arItem = Integer.parseInt(arItems[arItr].trim());
            ar[arItr] = arItem;
        }

        int result = simpleArraySum(ar);

        bufferedWriter.write(String.valueOf(result));
        bufferedWriter.newLine();

        bufferedWriter.close();
    }
}
```

Time Complexity:- O(N)  
Space Complexity :- O(1)