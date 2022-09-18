##  Square sum editorial
Problem Statement:- We have to find the sum of square of all natural numbers from 1 to n .
>Difficulty-Easy <br>
>Pre-Requisite-Basic Mathematics like addition and Multiplication<br>
​
**BASIC INTUITION :**
1.  Given an input n.
2.  Declare a variable sum which is would be initialised to 0.
3.  Run a loop from 1 to n , and add the square of the respective number to the sum.
4.  Return the sum as answer.
```
Example 1
If the user input is 4.
So the output is 1 power 2+ 2 power 2 + 3 power 2 + 4 power 2= 1+4+9+16=40
```
```
Example 2
If the user input is 3.
So the output is 1 power 2+ 2 power 2 + 3 power 2 + 4 power 2= 1+4+9=14.
```
​
​
### JAVA CODE
```.java
import java.util.*;
public class Main
{
	public static void main(String[] args) {
​
        Scanner sc=new Scanner(System.in);
        int num=sc.nextInt();
        int res=sumofdigit(num);
        System.out.println(res);
        
	}
	private static int sumofsquare(int num){
	    
	    int sum=0;
	   for(int i=1;i<=num;i++){// loopong from 1 to n
	       sum=sum+i*i;// adding the power of the respective number to the sum.
	   }
	    return sum;// return sum as answer
	}
}
​
```
**Time Complexity:-O(N)**
**Space Complexity:-O(1)**
​
**ALTERNATIVE SOLUTION**
We can find the sum of square of n natural number by using this formula  [n(n+1)(2n+1)] / 6. 
​
### JAVA CODE
```.java
import java.util.*;
public class Main
{
	public static void main(String[] args) {
​
        Scanner sc=new Scanner(System.in);
        int num=sc.nextInt();
        int res=sumofdigit(num);
        System.out.println(res);
        
	}
	private static int sumofsquare(int num){
	    
	    int sum=0;
	    sum= sum=(num*(num+1)*(2*num+1)) / 6;
	    return sum;// return sum as answer
	}
}
​
```
​
**Time Complexity:-O(1)**
**Space Complexity:-O(1)**