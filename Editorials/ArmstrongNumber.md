Armstrong Number.
### Armstrong Editorial
---
**Problem Statement - In this question, we have to find the whether the given number is armstrong or not.**
>For example if the user input is 153.
>So the sum of the cube of all the digits is equal to the number itself so ,it is a armstrong number.
	
**Difficulty:- EASY**
**Pre- Requisite:- Basics Of Mathematics like multiplication**
**HINT: -Addition of cube of all the digits and check whether it is equal to the user input.** 

#### Example
- Step 1:- 1 * 1 * 1+ 5 * 5 * 5+3 * 3 * 3
- Step 2:- 1+125+7
- Step 3:- 153
- Step 4:- As 153=153
So the answer will be true.

---

#### 2nd example 

If the user input is 400.
- Step 1:- 4 * 4 * 4+ 0 * 0 * 0+0 * 0 * 0
- Step 2:- 64+0+0
- Step 3:- 64
So the answer will be false as 64 not equal to 400.

---


#### JAVA CODE

```.java
import java.util.*;

class HelloWorld{
    
 public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        int num=sc.nextInt();
        boolean  res=armstrong(num);
        System.out.println(res);
    }
    
   private static boolean armstrong(int num){
    
    int result=0;
    int temp=num;
    /*  it will only come out of the loop when num =0.
So we lost the original value. It's better to store in a temp variable.*/
    
     while (num != 0)
        {
            int remainder = num % 10;// last digit is taken out
            result += Math.pow(remainder, 3);// we added the the digits 
            num= num/10;
        }
        if(temp==num)
            return true;
        else
            return false;
   }
}
```
```
Time Complexity:- O(N)
Space Complexity:-O(1)
```
---