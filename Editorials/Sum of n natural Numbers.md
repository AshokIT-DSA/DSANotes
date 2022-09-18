## Sum of n natural Numbers

Problem Statement :
So, in this question, we have to print the sum of the first **n** natural numbers.

**Difficulty:- EASY**
**Pre- Requisite:- Basics Of Mathematics like addition**
**HINT: -Add from 1 to n to get the result**

For, example if the user input is **2**
So, the output will be 1+2=3.

Let us consider another example. If the user input is **4**
So, the output will be 1+2+3+4= **10**
*So, the answer will be 10*.

Let us consider another example. If the user input is **5**
So, the output will be 1+2+3+4+5= **15**   
*So, the answer will be 15*

**Intution:- Addition**

### JAVA CODE
```
import java.util.*;

class HelloWorld {
    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        int num=sc.nextInt();
        int res=sumofn(num);
        System.out.println(res);
    }
    private static int sumofn(int num){
        int sum=0;
        /* we will be iterating from 1 to num and will be adding each number 
        like 1,2,3,4,..... n to the sum and return the sum as a result */
        for(int i=1;i<=num;i++){
            sum=sum+i;
        }
        return sum;
    }
}
```

Time Complexity:- O(N)
Space Complexity:-O(1)


**OPTIMIZATION**
We can further optimize the code, and we can reduce its time complexity to O(1).
Let's do some observation.

**INTUITION**
For example, if the user input is 4.
For, input 4 the answer will be 1+2+3+4=10;
Do you remember the trick we use in childhood to get the sum of n natural numbers in just 1 sec?
Think for a sec.

```
int  res= n*(n+1)/2;
Can we write this, let us check
4*(4+1)/2
```
It can be further simplified to:-
- 4*5/2
- 20/2
- 10

---
### Example 2

Let us consider another example:-
For example, if the user input is 5.
For, input 4 the answer will be 1+2+3+4+5=15;
Do you remember the trick we use in childhood to get the sum of n natural numbers in just 1 sec?
Think for a sec.

```.java
int  res= n*(n+1)/2;
Can we write this, let us check
5*(5+1)/2
```
It can be further simplified to:-
- 5*6/2
- 30/2
- 15


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
        return sum;
    }
}
```

Time Complexity:- O(1)
Space Complexity:- O(1)

Thank You!!