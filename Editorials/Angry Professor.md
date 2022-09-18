### Angry Professor

Problem Statement:- **Given an array of integers. And an array of input k.**  
**if the number is greater than 0 the student arrived right on time and if   the number is less than or equal to 0 the student arraived late. We have to find out whether the class will go on or not.**    
**If the count of students arrived late is greater than or equal to k.**    
*Then class will cancel otherwise class will go on.*   

**Pre-Requisite:- Simple Counting.**    
**Difficulty:- Easy**    

[![image](https://www.linkpicture.com/q/Angry-Professor.png)](https://www.linkpicture.com/view.php?img=LPic6325b8d9a7a5c1221998354)

```.java
import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.regex.*;

public class Solution {

    // Complete the angryProfessor function below.
    static String angryProfessor(int k, int[] a) 
    {
        int count=0;
        for(int i=0;i<a.length;i++)
        {
            if(a[i]<=0)
            {
                count++;
            }
        }
        if(count>=k)
        {
            return "NO";
        }
        else
        {
            return "YES";
        }


    }

    private static final Scanner scanner = new Scanner(System.in);

    public static void main(String[] args) throws IOException {
        BufferedWriter bufferedWriter = new BufferedWriter(new FileWriter(System.getenv("OUTPUT_PATH")));

        int t = scanner.nextInt();
        scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");

        for (int tItr = 0; tItr < t; tItr++) {
            String[] nk = scanner.nextLine().split(" ");

            int n = Integer.parseInt(nk[0]);

            int k = Integer.parseInt(nk[1]);

            int[] a = new int[n];

            String[] aItems = scanner.nextLine().split(" ");
            scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");

            for (int i = 0; i < n; i++) {
                int aItem = Integer.parseInt(aItems[i]);
                a[i] = aItem;
            }

            String result = angryProfessor(k, a);

            bufferedWriter.write(result);
            bufferedWriter.newLine();
        }

        bufferedWriter.close();

        scanner.close();
    }
}

```
Time Complexity :-O(N)    
Space Complexity :-O(1)
