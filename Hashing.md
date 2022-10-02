# Hashing
Say you are dealing with the list of phone numbers.
Our standard phone numbers.  
Each phone number consists of 10 digits.  
On this list, you have to perform three operations.  
~~~
1. Insert(x)
2. Search(x)
3. Delete(x)    
~~~
The simplest solution will be, to maintain an **unsorted array.**  

Q. Inserting a single element, will take how much time?  
 A. O(1)  
Q. Searching for a phone number, will take how much time?  
A. O(N) [we will simply perform linear search]  
Q. Deleting a phone number will take how much time?   
O(N) [ because you have to first search for it]  

## Direct Access Table
Next, we can use something like a **boolean count table[DAT]**   
 bool count[] = {F}
everything initializes to false.  
~~~
Insertion :-count[x] = true;

For searching:- check value count[X], if it's storing true, then the number is present, else we can say that number is not present in the list.  

For deletion :- count[X] = false;
~~~  
**Q. So, if we do this, what is the time complexity for each operation?
A. 0(1)**  


### Problem
**The space complexity**

Since we are storing 10-digit phone numbers, can you tell me the size of the count array you will take?

So boolean array of size **10^10** will occupy **10^10** bytes, which is equal to **10GB.**  


**So it is the best possible solution but impossible to implement practically .**  

### Solution

So to tackle this, we use the concept of hashing!  

We were treating the phone numbers as the index of the count array, which was giving an issue.  
If we can somehow apply a function, to the phone numbers.    
**hash(x) = x%s;**  
And reduce it to a smaller value, will solve our problem.
We should not treat “x” as the index, reduce it to a smaller value and then use it.
                  
**Q. Why do we take mod with s?  
A. Because to limit the index to the hash table size. 
As (x%s) will return the value between ( 0 to s-1) .**  

### Example:-
So here we are taking the hash table of size **10**, 

Assume that you are trying to insert these array elements into the hash table.
Now if you apply hash function on elements of array ,  
ar[]= 3 , 17 , 48 , 6 , 97 , 14 , 17 , 23   
 what will hash (3) will give you?  
So 3 will go to index 3.   
Similarly,   
Hash(17) = 7  
Hash(48) = 8  
Hash(6) = 6  

~~~
0   1   2   3   4   5   6   7   8   9  
            3           6   17  48  
 ~~~


So what happens at 97?
Hash(97) = 7  
But the index is already occupied. All though we have solved the issue with large space.  
We have run into another issue called a collision.  
**Q. What do you mean by collision?  
Two different hash keys give the same hash value.**
 
### Collision Resolution

1. separate chaining (SC)

2. open address(OA)


