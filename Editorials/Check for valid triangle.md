# Check for a valid Triangle

## Given threes sides, check whether it is a valid rectangle or not.

**Difficulty:-Easy**   <br>
**Pre-Requisite:-Basic Maths**<br>

> HINT:
THE SUM OF ANY TWO SIDES SHOULD BE GREATER THAN THE THIRD SIDE.


#### EXAMPLE
Let us think three sides are given.
they are of 3 cm, 4 cm, 5 cm.
<br>
so according to the hint sum of any two sides should be gretaer than third side.  
so 3+4 =7 7>5 so true.<br>
4+5=9   9>3 , so true.<br>
5+3=8   8>4 , so true.<br>
All the three condition satisfies so it is true.



### INTUITION
Let us consider three sides having a cm, b cm, and c cm. (Here cm:-centimeter)
So According to the hint a+b should be greater than c and b+c should be greater than a and a+c should be greater than b.

```.java
import java.io.*;
import java.util.*;

public class Solution {

    public static void main(String[] args) {
        /* Enter your code here. Read input from STDIN. Print output to STDOUT. Your class should be named Solution. */
        Scanner sc=new Scanner(System.in);
        int a=sc.nextInt();
        int b=sc.nextInt();
        int c=sc.nextInt();
        boolean ans=check(a,b,c);
        System.out.println(ans);
    }
    private static boolean check(int a, int b, int c){
        if(a+b>c && b+c> a && c+a>b){
            return true;
        }
        else{
            return false;
        }
    }
}
```

Time Complexity:-O(1)<br>
Space Complexity :-O(1)

### Alternate Solution:-
You no need to check all the three condition written in the if block.
Let's consider out of a,b and c. b is the maximum.
Therefore sum of a+c>b ( if this is true a+b>c && b+c>a will aslo be true)