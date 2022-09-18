## Narcissistic numbers editorial
​
**Problem Statement :-What is narcissitic number?<br> Let us understand by example:-
For example 32 is given, how many digits are there in the given number.<br> There are 2 digits in 32. So the sum of every digit to the power of all the digits should be equal to the number itself.**
​
>Difficulty- Easy<br>
Pre-Requisite:-Basic looping concepts, Mathematics
​
​
#### Example:
If the user input is 32<br>
There are 2 digits in 32.<br>
So Sum of power of digit to the number of digits<br>
(3)power 2 +(2)power 2 => 9+4= 13.<br>
13!=32 . So it should return false.<br>
​
#### 2nd Example
If the user input is 8208 . <br>
There are 4 digits in 8208.<br>
So Sum of power of digit to the number of digits<br>
8 power 4+ 2 power 4 + 0 power 4 + 8 power 4= 4096+16+0+4096=8208.<br>
8208==8208, So it should return true.<br>
​
##Intuition:-
---
So , first we have to first find how many digits are there present in the number.<br>
We have to **loop through the number till it becomes 0** and we have to **add the respective digit** to the **power** of **the number of digits** ,to the *answer*.<br>
**If the answer is equal to the user input, then we need to return true as answer or else return false.**
<br>
```.java
import java.io.*;
import java.util.*;
​
public class Solution {
​
    public static void main(String[] args) {
        /* Enter your code here. Read input from STDIN. Print output to STDOUT. Your class should be named Solution. */
            
            Scanner sc=new Scanner(System.in);
            int n=sc.nextInt();
            boolean res=checknarcisstic(n);
            System.out.println(res);
        
           
        }
    
    private static boolean checknarcisstic(int num){
        
        int count=0;
        int temp_num=num;
        
        while(num!=0){
            count++;
            num=num/10;
        }
        //the above loop is for counting the number of digits.
        num=temp_num;
        int res=0;
        
        while(num!=0){
            int rem=num%10;
            res=res+Math.pow(rem,count);
            num=num/10;
        }
        // this loop is for adding the respective digit to the power of the number of digits to the respective answer.
        
        
        if(res==temp_num)// checks whether the result is equal to the number, if yes, then return true.
            return true;
        else
            return false;
        
    }
}
```
​
Time Compleity:- O(N)
Space complexity:-O(1)