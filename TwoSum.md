### **Two Sum - Editorial**
### **Difficulty**: Low
### **Prerequisite: Arrays,Sorting,2-Pointer**
### **Problem Statement**:
Given an array of integer nums and an integer target, return indices of the two numbers such that they add up to the target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.

You can return the answer in any order.

### **Hint:**
A single loop can be used to find the pair, Try to use the property that the array is sorted and use 2-Pointers.
### **Short Explanation**
Declare 2 Pointer left=0,right=ar.length-1  
**If**
1. ar[left]+ar[right]==k return true
2. ar[left]+ar[right]>k right--
3. ar[left]+ar[right]<k left++

### **Detailed Explanation**:

In this question, we are given a sorted array A, of size N, and an integer K, and we have to find out if there exist two values in the array, stored at different indexes, such that their sum is equal to K. 

- A brute force approach is to, fix one value, and then try to find the sum of this particular value with all the other values in the array, and check if any of them become equal to K.
- The worst-case time complexity of this approach is `O(N^2)`, where N is the size of the array.
- But since the array is sorted, a two-pointer approach can be useful here, such that we have two pointers, **left** and **right**, where the left pointer iterates the array from left to right, while the right pointer iterates from right to left.
- Left=0,Right=ar.length-1;
- At every step, we find the sum of the elements stored at the left and the right pointer in the array.
1.  If the value of the sum is greater than the required sum K, we check for a smaller sum, by decreasing the right pointer.[Reason discussed in the session]
2.  If the sum is lesser than K, then we add a higher value by moving the left pointer ahead.[Reason discussed in the session]
- If the value is equal to K, we return the index of the left and the right pointer.

### a) **Pseudo Code**

```
Code
```

### **Example**

```
Array = [3,5,6,7,11] and the value of K = 13. So, we have a pointer iterating from left to right, 
while another pointer iterates, from right to left. 
So, initally, the value of left = 0 and right = arr.length - 1.
    
1. Initially, when left = 0, and right = 4, then sum = array[left] + array[right], which is equal to 14. 
     Since this sum is greater than K = 13, we decrement the right pointer.
     So left=0 and right=3. 
2. sum = array[left] + array[right], which is equal to 10. 
     Since this sum is lesser than K = 13, we increment the left pointer.
     So left=1 and right=3
3. sum = array[left] + array[right], which is equal to 12. 
     Since this sum is lesser than K = 13, we increment the left pointer.
     So left=2 and right=3.
     
4. sum = array[left] + array[right], which is equal to 13. 
     Since this sum ==k, we return true or the index of left and the right pointers in the form of an array.
     
```

### b) **Time Complexity:**

- The time complexity will be `O(N)`, where N is the size of the array.

### c) **Space Complexity:**

- `O(1)`, No extra space is required.