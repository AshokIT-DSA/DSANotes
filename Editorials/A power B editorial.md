# A power B editorial

## Given two Numbers a and b find the a power b

**Difficulty:-Easy**   <br>
**Pre-Requisite:-Basic Maths, Multiplication ,Looping Conept**<br>


>EXAMPLE:<br>
Let us think two  numbers are given.
a and b
<br>
For example, 2 and 3.<br>
So 2 to power 3=8.<br>
So the answer is 8.

>EXAMPLE:<br>
Let us think two  numbers are given.
a and b
<br>
For example, 4 and 2.<br>
So 4 to power 2=16.<br>
So the answer is 16.



## INTUITION
So as per previous example, 2 to power 3 =8.
So let us breakdown this example.<br>
What is 2 power 1 ? 2.<br>
What is 2 power 2 ? 4.<br>
What is 2 power 3 ? 8.<br>

Let us take another example , 3 power 4=81.
what is 3 power 1 ? 3.<br>
What is 3 power 2 ? 9.<br>
What is 3 power 3 ? 27.<br>
What is 3 power 4 ? 81.<br>

Are you observing any pattern in the previous examples.<br>
Think !!<br>
So the number **a** gets multiplied  **b** times to get *a power b*. <br>

**Please Try On your Own before looking at the code**

```.java
import java.io.*;
import java.util.*;

public class Solution {

    public static void main(String[] args) {
        /* Enter your code here. Read input from STDIN. Print output to STDOUT. Your class should be named Solution. */
        Scanner sc=new Scanner(System.in);
        int a=sc.nextInt();
        int b=sc.nextInt();
        
        boolean ans=power(a,b);
        System.out.println(ans);
    }
    private static boolean power(int a, int b){
        
        int res=1;// what will happen if we initalise res with 0, 0 multiplied with any number is equal to 0.
        for(int i=1;i<=b;i++){
            res=res*a;
        }
        return res;
    }
}
```

Time Complexity:-O(B) Because the loop is running B times. So O(B).
Space Complexity :-O(1)

### ALTERNATIVE SOLUTION:-
>NOT RECOMMENDED.  
    ONLY IN ONLINE TESTS
```.java
import java.io.*;
import java.util.*;

public class Solution {

    public static void main(String[] args) {
        /* Enter your code here. Read input from STDIN. Print output to STDOUT. Your class should be named Solution. */
        Scanner sc=new Scanner(System.in);
        int a=sc.nextInt();
        int b=sc.nextInt();
        
        int ans=(int)Math.pow(a,b);
        System.out.println(ans);
    }
    
}
```

Time Complexity:-O(1)  
Space Complexity:-O(1)
