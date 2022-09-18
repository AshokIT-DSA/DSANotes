### **Min and Max element in the array - Editorial**
### **Difficulty**: Low
### **Prerequisite: Arrays,Sorting**
### **Problem Statement**:
Given an array, A, of N integers, print the smallest and largest element present in the array



### **Hint:**
A single loop can be used to calculate the maximum and minimum value.
### **Short Explaination**
The question demands to print the minimum value and the maximum value in the array. A single loop can be used to compare the current value with the current minimum value, and updated if the current value is smaller than the current minimum value. Similarly, maximum value can also be found.
### **Detailed Explanation**:
The question states that we need to find the maximum and the minimum value in the array. This can be done by comparing each value in the array to the current maximum value and current minimum value. Initially, minimum value must be set to MAXIMUM POSSIBLE VALUE(Integer.MAX_VALUE/Long.MAX_VALUE), and maximum value must be set to (Integer.MIN_VALUE/Long.MIN_VALUE). The idea is to run a loop, and for each element check if it is greater than the maximum value found so far. If the condition holds true, maximum value can be modified. Similarly, if the current value is less than the minimum value found, then the minimum value will be modified. An array with only one element will have maximum value equal to the minimum value.


### **Pseudo Code**
 * maximum = Integer.MAX_VALUE/Long.MAX_VALUE
 * minimum = (Integer.MIN_VALUE/Long.MIN_VALUE)
 * for i in array: 
 		* if (i is less than minimum) minimum = i
 		* if (i is greater than maximum) maximum = i;
 * print (minimum)
 * print (maximum)

### **Time Complexity**:
Looping through the array to find the maximum and minimum requires O(N) time. Therefore, Time Complexity is O(N).
### **Space Complexity**:
No extra space is required. Therefore, the space complexity will be O(1).

### **Alternate Solution**:
Sorting can be used to find the minimum and the maximum in the array. In a conventional sorted array, the first value is the smallest and the last value is the largest. Therefore minimum value is equal to the first element in the array, and the maximum value is the last value in the array. 
### **Time Complexity**:
The time complexity depends on the sorting algorithm used for sorting the array. Some algorithms give time complexity of O(N^2),on an average, whereas some give O(NlogN).
### **Space Complexity**:
No extra space is required. Therefore, the space complexity will be O(1).
