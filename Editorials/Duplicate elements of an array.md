## Duplicate elements of an array
​
**Problem Statement :-So a array of integer will be given to us, we need to check the duplicates element in the array, and we have to print the duplicates.**
​
>Difficulty- Easy<br>
Pre-Requisite:-Basic looping concepts,Array, ArrayList,HashMap(Optional)
​
​
#### Example:
5 4 10 9 9 9 10 10
So ,we can there are three 10 in the array, so it should print 10.
And there are three 9 in the array, so it should print 9
(9 is repeated 2 times , but it should print only One time. You should keep this in mind.).
So output will be 10 and 9. and the order should be maintained?
(Like in which order the element is there , it should print like that.)
​
​
#### 2nd Example
4 5 6 6 1 1 2
So there are two 6 in the the array, so it should print 6.
And there are two 1 in the array, so it should print 1.
So, the output should be 6 and 1.
[6,1]
​
​
##Brute Force Intuition:-
---
We will take an arraylist for putting the duplicate elements.
​
Duplicate element can be found by using two loops. 
Outer loop will go from 0 to array.length-1, and
the inner loop will go from the respective position+1 index to the end of the array
.The outer loop will be used for selecting the element and 
the inner loop is for comparing whether the element is present another time from the respective index+1 to the end of the array. and we put that into the arraylist.
​
Can you tell me guys what will be the output for 
4 5 6 6 1 1 2.
The output will be 6 and 1 , acc. to the brute force intuition that i had written.
​
Let's just think  for another example
will it work for 4 5 6 6 6 1 1 1 2.
So what will be output?
6 6 1 1 (According to my brute force intuition.)
​
But what should be the actual output?
6 1 Right?
So what changes can we do so that our ouput will only print one time 6 and one time 1.
​
Think before you look into the solution atleast for 10 - 20 mins.
​
So, what changes can we make ?
So when a repeating elements comes we check whether the repeating element is already present in the arraylist or not , if its already present we dont need to put into the arraylist, if not then we need to put into the arraylist.
​
​
<br>
```.java
import java.util.*;
public class remove_duplicates {
​
    public static void main(String[] args) {
        // TODO Auto-generated method stub
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        int a[]=new int[n];
        for(int i=0;i<n;i++)
        {
            a[i]=sc.nextInt();
        }
        duplicate(a);
    }
    private static void duplicate(int a[]){
        
        ArrayList<Integer> ar=new ArrayList<>();
        int n=arr.length;
        // we iterate from 0 to n-1.Outer loop
        for(int i=0;i<n-1;i++){
            
            int key=a[i];
            // inner loop that is used for comparing the elements 
            for(int j=i+1;j<n;j++){
                if(key==a[j]){
                    
                    boolean b=true;
                    // we check whether the element is present in the arraylist
                    for(int k=0;k<ar.size();k++){
                        
                    int temp=(Integer) ar.get(k);
                        /* if it is present, we dont need to put again in the arraylist, we break it from there and make                          flag as false*/
                        if(temp==key){
                            b=false;
                            break;
                        }
                    }
            // if flag is true, it means we dont found that the duplicate element is not in the arraylist , so                       put the element in  the arraylist.*/
                    
                if(b==true){
                    ar.add(key);
                    System.out.print(key+" ");
                }
            }
                
        //all duplicate elements are printed.
        System.out.print(al);
        }
            
    }
​
```
​
Time Complexity :-O(N^2)
Space Complexity:-O(1)
​
​
Better Solution:- Using Sorting
Sort the array,iterate from index 1 to the end of the array, check whether a[i]==a[i-1], if it gets true, then ,put the element into the arraylist, and handle the case which i had mentioned above , multiple duplicates should be avoide.
​
Time Complexity :-O(Nlogn)
Space Complexity:-O(1)
​
Optimized Solution:-
​
#### Optimized solution Intuition:-
We will take a hashmap of key value pair. The key will be the number and the value will be its frequency.
if the number is not present in the hashmap we will put the key value pair as(number ,1)
as number is appearing for the first time , so the frequency will be 1.
If the number is already present the frequency of the new number will be old frequency +1. we need to put (number,frequency).
​
We will use LinkedHashMap ,because it maintains insertion order , why not hashmap ? because it dont maintains insertion order.
​
```.java
import java.util.*;
public class remove_duplicates {
​
    public static void main(String[] args) {
        // TODO Auto-generated method stub
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        int a[]=new int[n];
        for(int i=0;i<n;i++)
        {
            a[i]=sc.nextInt();
        }
        duplicate(a);
    }
    private static void duplicate(int a[]){
            LinkedHashMap<Integer,Integer> lmap=new LinkedHashMap<>();
            for(int i=0;i<a.length;i++){
                if(lmap.containsKey(a[i])){
                    int of=lmap.get(a[i]);
                    int nf=of+1;
                    hm.put(a[i],nf);
                }
                else{
                    hm.put(a[i],1);
                }
            }
        for(Integer i:lmap.keySet()){
            
            if(lmap.get(i)>=2)
                System.out.println(i);
        
        }
        
        }
            
    }
```
​
Time Complexity:-O(N)
Space Complexity:-O(N)