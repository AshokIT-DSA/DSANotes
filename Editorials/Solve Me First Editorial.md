## Solve me First Editorial.

Problem Statement :- Given two numbers a and b we have to find out the sum.  

**Pre-Requisite:- Mathematics.**    
**Difficulty:-Basic.**    

Intuition:- 
We just have to add two numbers.  
Let's understand it by the help of the example.    
a=2  
b=3  
a+b=5.  
return 5 as answer.  

```.java
import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

public class Solution {


    static int solveMeFirst(int a, int b) {
      	// Hint: Type return a+b; below 

        return a+b;
   }

 public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        int a;
        a = in.nextInt();
        int b;
        b = in.nextInt();
        int sum;
        sum = solveMeFirst(a, b);
        System.out.println(sum);
   }
}

```

Time Complexity:- O(1).
Space Complexity:- O(1).
