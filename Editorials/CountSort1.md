### **Count Sort-1 - Editorial**
### **Difficulty**: Low
### **Prerequisite: Arrays,Sorting**
### **Problem Statement**:
Given a list of integers, count and return the number of times each value appears as an array of integers.

#### Constraints
1<n<10^6    
1<=ar[i]<=100  

 
### **Hint:**
Try to store the data in the form of key, and value pairs.
### **Short Explanation**
There are 2 ways to store the data in key-value pairs. 
1. HashMap
2. Integer Array.

The Key will be the element and the value will be the number of times a particular element is repeated(frequency).
   

### **Detailed Explanation**:

Even though the size of the array is 10^6(n), if I count the distinct elements in the array. It turns out be there are only 100 distinct elements and that too between[1,100].

#### **Intution**
 I will map each number with the index and the value stored in that array would be the frequency.  

Consider this array as an input.
[1,5,6,8,9,20................and so on].

To process each element I will iterate over an array.

Let's trace it.
1. i=0,ar[i]=1, So I found the occurrence of 1. 
If the index is paired with a number, I should go to the first index of count[] and increment the count. count[1]++.
2. i=1, ar[i]=5, So I found the occurrence of 5. 
If the index is paired with a number, I should go to the fifth index of count[] and increment the count. count[5]++.    

Continue this step for all the elements of an array.
At the end print the count array from the index [1 to 100].

As it was mentioned in the problem statement you have to print the frequency of all the elements from [1 to 100].


### **Pseudo Code**
~~~
void cs1(int ar[] , int N){
    //Because size=lastIndex+1;
    //I need the last index to be 100.
    int CNT[101] = {0};
    for(int i=0 ; i<n;  i++){
        CNT[ar[i]]++;
    }
    int freq = 0 ;
    //Loop start with 1 because I don't want to print the occurrence of zero. As element 0 was not part of the constraint.
    for (int i=1 ; i<=100; i++){
        print(cnt[i]);
      }
}

~~~

### **Time Complexity**:
O(N).
### **Space Complexity**:
No extra space is required. Therefore, the space complexity will be O(1).

### **Alternate Solution**:
Instead of counting array, you can use the HashMap
#### **Time Complexity**:
O(n)
#### **Space Complexity**:
No extra space is required. Therefore, the space complexity will be O(1).


