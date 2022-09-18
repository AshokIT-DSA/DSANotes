
# Insertion Sort
    Index:-    0    1    2  3   4    5    6   7 
    Ar:-       2    7    5  12  4   -3    8  -1

In general, you sort the array in 
1. Ascending / increasing/ non-decreasing
2. Descending/decreasing/non-increasing 

Let's understand insertion sort  


## Step 1
[![image](https://www.linkpicture.com/q/Screenshot-332_1.png)](https://www.linkpicture.com/view.php?img=LPic631acfd6def3b464552067)

## Step 2
We will start picking up the elements from index 1.

If I look into the array from the index[0,1]  
Element 7 is in its correct position right so need not do anything.

## Step-3

The next index is 2.
The element present in index 2 is 5.

You will somehow shift 7, but you will not shift 2 because it is lesser than 5. 

After shift array will look something like this.

[![image](https://www.linkpicture.com/q/Screenshot-333_1.png)](https://www.linkpicture.com/view.php?img=LPic631ad127555ae1618377541).

## Step-4

The next index is 3.
The element present in index 3 is 12.

Now pick up the next element “12” and place it in its correct position.

Element 12 is in its correct position right so need not do anything.

## Step-5

The next index is 4.  
Let's represent the index with the variable **i**  

The sorted array is from [0,i-1].  

So basically we are trying to place the element in its correct position in the sorted array.    

[![image](https://www.linkpicture.com/q/Screenshot-334_1.png)](https://www.linkpicture.com/view.php?img=LPic631adea9665e4822907150)

So first we compare 4 with 12. We shift 12 towards the right. We do not swap the elements as we did in bubble sort.  

[![image](https://www.linkpicture.com/q/Screenshot-335_1.png)](https://www.linkpicture.com/view.php?img=LPic631adf34c70591016256306)


If we shift 12,
You will lose 4.  

So before you start shifting, you should store 4 in a temporary variable. Let's say x.  
Now you compare 12 with x, so make a shift. Since
12 is more than x. 

 [![image](https://www.linkpicture.com/q/Screenshot-335_1.png)](https://www.linkpicture.com/view.php?img=LPic631adf34c70591016256306)
Now you compare 7 with x, so make a shift. Since
7 is more than x. 

[![image](https://www.linkpicture.com/q/Screenshot-336_1.png)](https://www.linkpicture.com/view.php?img=LPic631ae1d7e5a6f1195937416).

Now you compare 5 with x, so make a shift. Since
5 is more than x.

[![image](https://www.linkpicture.com/q/Screenshot-337_1.png)](https://www.linkpicture.com/view.php?img=LPic631ae3029a5542101345752).

Now you compare 2 with x . 2 is not more than x. 

**So store the result in the current index+1**  
**ar[j+1] = x**

## Algorithm

1. Array having 1 element is always sorted.
2. You start from index 1, and pick up the elements stored in the temporary variable.
3. From the left-sorted array, you will shift the elements.[i-1 to 0]  
And insert it in the correct position.

**Follow step 3 for all the elements in an array. From 1 to n-1.**

## Code
~~~
package org.ar.sorting;

import java.util.Arrays;

public class InsertionSort {
    public static void main(String[] args) {
        int ar[]= {2,7,5,12,4,-3,8,-1};

        int n=ar.length;
        for(int i=0;i<n;i++) {
            int x=ar[i];        
            int j=0;
            for(j=i-1;j>=0;j--) {
                if(ar[j]>x) {
                    ar[j+1]=ar[j];
                }
                else {
                    break;
                }
            }
            ar[j+1]=x;
            }
        System.out.println("Sorted Array"+Arrays.toString(ar));
    }
}


~~~
### Complexity:- O(n^2)

#### Worst case scenario array is in descending order.
#### Best case example array is in ascending order.
