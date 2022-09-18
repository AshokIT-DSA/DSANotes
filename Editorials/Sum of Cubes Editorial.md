### Sum of Cubes Editorial
---
**Problem Statement - In this question, we have to find the sum of the cube of first n natural numbers.**
>For example if the user input is 4.
>So the sum of the cube of the first 4 natural numbers is 100.
	
**Difficulty:- EASY**
**Pre- Requisite:- Basics Of Mathematics like multiplication**
**HINT: -Addition of cube of all the digits.** 

#### Example
- Step 1:- 1 * 1 * 1+ 2 * 2 * 2+3 * 3 * 3+4 *4 *4
- Step 2:- 1+8+27+64
- Step 3:- 100
So the answer will be 100, for the input 4

---

#### 2nd example 

If the user input is 5.
- Step 1:- 1 * 1 * 1+ 2 * 2 * 2+3 * 3 * 3+4 *4 *4+5 * 5 * 5
- Step 2:- 1+8+27+64+125
- Step 3:- 225
So the answer will be 225, for the input 5

---
Intuition :- We need to iterate from 1 to n, and add the cube of the respective number to the sum and return the sum.

#### JAVA CODE

```.java
import java.util.*;

class HelloWorld{
    
 public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        int num=sc.nextInt();
        int res=sumofn(num);
        System.out.println(res);
    }
    
   private static int sumofcube(int num){
    
    int res=0;
    
    /* we iterate from 1 to number, and add the cube of each number 
    1, 2,,3 .... n and we add it to the result.*/
    
    for(int i=1;i<=num;i++){
        int cube=i*i*i;
        res=res+cube;
    }
    return res;
   }
}
```
```
Time Complexity:- O(N)
Space Complexity:-O(1)
```
---

 **Optimization** 
We can further optimize it to 0(1). 
By using the same concept of finding the sum of first n natural numbers (optimized approach).


> Intuition 
In the previous Question, to find the sum of natural numbers from 1 to n, we used an optimized approach of  ```(n *  (n+1)/2) ```, the same concept we will apply here, after finding the sum of natural numbers from 1 to n, then we will find the cube of the result, and then we return the result as an answer.


JAVA CODE:-

```
import java.util.*;

class HelloWorld{
    
 public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        int num=sc.nextInt();
        int res=sumofn(num);
        System.out.println(res);
    }
    
    private static int sumofn(int num){
        int sum=0;
        sum=(num*(num+1))/2;
        return sum*sum;
    }
}
```
```
Time Complexity:- O(1)
Space Complexity:- O(1)
```
Thank you