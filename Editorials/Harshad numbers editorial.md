## Harshad  numbers editorial
​
**Problem Statement :-To check whwter a number is harshad number or not.

​
>Difficulty- Easy<br>
Pre-Requisite:-Basic looping concepts, Mathematics
​
​
#### Example:
If the user input is 18<br>
There are 2 digits in 1 and 8.<br>
So Sum of its digit is 9<br>
As 18 is divisible by 9, so the answer should return true.<br>
​
​
#### 2nd Example
If the user input is 19 . <br>
There are 2 digits in 1 and 9.<br>
So Sum of its digit is 10<br>
As 19 is not  divisible by 10, so the answer should return false.<br>
​
​
##Intuition:-
---
For example 18 is given, so, there are two digits in 18, and if we add every digits to the sum , what do we get  9 . Is 18 divisible by 9 ? Yes, so it should return true answer.  
So , first we need to iterate through the number till it becomes 0 and add it's respective digit to thes sum,. Then we check if the the number that was provided as input modulo to the sum of its digit is 0 or not , if 0 then return true ,else return false.  
<br>
```.java
​
import java.io.*;
import java.util.*;
​
public class Solution {
​
    public static void main(String[] args) {
        /* Enter your code here. Read input from STDIN. Print output to STDOUT. Your class should be named Solution. */
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        boolean ans=checkharshad(n);
        System.out.println(ans);
    }
    private static boolean checkharshad(int num){
            int temp=num;
            int sum=0;
            while(temp!=0)
            {
                int rem=temp%10;
                sum=sum+rem;
                temp=temp/10;
            }
            if(temp%sum==0)
            {
                return true;
            }
            else
            {
                return false;
            }
    }
}
```
​
​
Time Compleity:- O(N)
Space complexity:-O(1)
​