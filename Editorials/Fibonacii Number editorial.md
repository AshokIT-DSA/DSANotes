##  Fibonacii Number editorial
Problem Statement:- We have to find the nth fiboonaci Numver
>Difficulty-Easy <br>
>Pre-Requisite-What is a fibonnaci sequence, Basic Mathematics like addition <br>
​
**EXPLANATION**
What is a fiboonaci sequence??
0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144, … and so on.
​
>The Fibonacci numbers, commonly denoted F(n) form a sequence, called the Fibonacci sequence, such that each number is the sum of the two preceding ones,**(Preceding means before)** starting from 0 and 1. That is,
​
F(0) = 0, F(1) = 1
F(n) = F(n - 1) + F(n - 2), for n > 1.
​
In simple words,
The 0th term is **0** and the 1st term is **1**.
if n=3
then 3rd term will be  2nd term + 1 st term . 
Respectively if n=4.
then 3rd term will be  3rd term + 2nd term . 
​
So from this we get a relation
If n>=3.
F(n)=F(n-1)+ F(n-2)
​
​
### JAVA CODE
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
        int res=factorial(n);
       
        System.out.println(res);
        
    }
    private static int factorial(int num){
        if(num==0 || num==1)
            return num;
        
        int a=0;// 0th term
        int  b=1;//1st term
        int  c=0;//2nd term
        for(int i=0;i<=num-2;i++)// why num-2 because we already have the 0 th term and and 1st                             //term
        {
            c=a+b;
            a=b;
            b=c;
           
        }
        return c;
    }
}
​
```
**Time Complexity:-O(N)**
**Space Complexity:-O(1)**
​
**ALTERNATIVE SOLUTION**
By using Bottom up dp approach; 
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
        int dp[]=new int[num+1];
        System.out.println(res);
        
	}
	private static int factorial(int num){
	    long dp[]=new long[n+1];
        dp[0]=0;
        dp[1]=1;
        for(int i=2;i<dp.length;i++){
            dp[i]=dp[i-1]+dp[i-2];
        }
        return dp[num];
	}
}
​
```
​
**Time Complexity:-O(1)**
**Space Complexity:-O(1)**