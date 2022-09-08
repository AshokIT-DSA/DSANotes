 
## Complexity Analysis of Algorithm
### Q. Let’s say for a given problem there are multiple solution, out these how you will figure it out which one is the best solution for you?
 

[![image](https://www.linkpicture.com/q/Screenshot-331_1.png)](https://www.linkpicture.com/view.php?img=LPic631a44fc05c9a1306707651)
 
### Ans:-Based on their time & space complexity.
 
### Q.For given a value of n you have to simply count the number of divisors.  
 
| N     | No of divisor |
| ----------- | ----------- |
| 10     |  1,2,5,10 (3)        |
| 25   |  1,2,5,25 (4)     |
 
### Ans:-
```
int divisors (int m) {
    count=0
    for(int i=1; i<=n; i++){
        if (n%i == 0) {
        count++;
    }
    return count;
}
 
```
 
 
For n=10^9, let's calculate the number of iteration and instruction in the code.    
Iteration=10^9  
Number of instruction in each iteration=5  
 
**So, there are around 4-5 instructions per iterations.
For simplicity of computation, we assume  
1 instruction = 1 iteration.**  
 
### How much time will it take to execute the code?
 
Time = 1 sec(If we follow the assumption)  
Time =5 sec(As total number of iteration)  
### Q.Now if increase the value of n to be 10^18.  
 
### Ans. 10^9sec (31.7years)
 
 
**We notice that brute force solution may needs years to execute, hence we need optimization**.  
So, there are 2 ways to increase the speed of our execution.  
->Increase your hardware configuration.    
->Optimize your code.  
 
Hardware upgradation has the limitations, it's better to optimize your code.
 
# Find the complexity of the following code snippet  
~~~
Int m11(int ar[], int n){
        int a = N+2;
        int b= N/2;
        int c = a+b;
        int d = N*d;
    return a+b+(c-d);
}  
~~~
How many instructions are there in this code?  
 
Let say 10 instruction(approximately) are there
Q. If value of N is 10000    
How many instructions are there?
 
Ans. 15  
 
Q. If value of N is 500,  how many instructions are there?  
 
Ans. 15
 
**__So the point is whatever the value of n no. of instruction are same.  
In other words number of instruction are independent from the value of given input.__**
 
It will take constant time doesn't matter what's the value of n. O(1)  
## Asymptotic notations
    Big – O Notation => Worst Case
    Ω Notation => Best Case
    ϴ Notation => Average Case
We generally do a analysis what will happen to our piece of code when it is executed in worst case.
 
 
void fun 2 ( int ar[], int n) {
~~~
for(int i = 0; i<n ; i++){
         int a= n+1;
         int b = ar.length -1;
         int c = n*n;
         int d = n+2/(n-100);
     }
}
--O(n)
~~~
~~~
void fun3(int n){
  for ( int i =1; i<=n; i++){
        for(int j=1; j<=n; j++){
              print(“X”); =>O(1)
           }
}
 
}
--O(N x N) = O(N^2)
~~~
~~~
Void fun 4( int n, int ar[]){
 for ( int i =1; i<=n; i++){
        for(int j=1; j<=n; j++){
              print(“X”); =>O(1)
           }
}
for(int i = 0; i<n ; i++){
         int a= n+1;
         int b = ar.length -1;
         int c = n*n;
         int d = n+2/(n-100);
     }
}
}
--We ignore the lower order terms so complexity of this solution is O(N^2)
~~~
 
## Lets say you are solving the problem , and constraints are
                                 1≤T≤10^5
                                 1≤N≤10^4
### Q. Will N^2 SOLUTION WORK HERE?
Ans:- T*N^2  
10^5 * 10^8  
=10^13  
10^13 Is greater than 10^8  , hence you will get a TLE.  
### Q. Will Big-0(N) work?    
Ans:- T * n    
10^5 * 10^4  
=10^9  
Which is still greater than 10^8 , so it will TLE .  
 
### Q. Will big-0 (√N) work ?
Ans:- T*√N  
 10^5 * 10^2  
10^7 <10^8
This will work.
## Lets say you are solving the problem , and constraints are
 
                                 1≤T≤10^4
                                1≤N≤10^3
### Q. Will N^2 solution will work over here?
Ans:- T*N^2  
10^4 * 10^6  
10^10  
10^10  is greater than 10^8 . so you will get TLE.
 
### Q.Will Big0(N) will work?
 Ans:- T * N  
10^4 *10^3  
10^7 < 10^8    
It will work over here .  
 
**So like this you have to calculate the number of iterations before written the actual code , as it will help you to determine feasable and non feasable solution**
 

