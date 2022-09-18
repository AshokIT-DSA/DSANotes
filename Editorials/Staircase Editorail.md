Problem Statement :- Print the Stair Case Pattern as shown in the figure.

**Pre- Requiste:- for loops**   
**Difficulty:- Easy**  

[![image](https://www.linkpicture.com/q/Staircase.png)](https://www.linkpicture.com/view.php?img=LPic6325cc5d660401875252619)

```.java
import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.regex.*;

public class Solution {

    // Complete the staircase function below.
    static void staircase(int n)
     {
          for(int i=0;i<n;i++) 
        {
            
            for(int j=n-1;j>i;j--)
            {
                System.out.print(" ");
            }
            for(int k=0;k<=i;k++ )
            {
                System.out.print("#");
            }
            
            System.out.println();
        }    

    }

    private static final Scanner scanner = new Scanner(System.in);

    public static void main(String[] args) {
        int n = scanner.nextInt();
        scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");

        staircase(n);

        scanner.close();
    }
}

```