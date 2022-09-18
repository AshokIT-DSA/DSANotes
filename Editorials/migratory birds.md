## Migratory Birds Editorail.

**Problem Statement :- Given an array of integers of length n and the values of the array will be from 1 to 5.**  
**We have to find which number appears most of the time.**

**Pre-Requisite:- Array, HashMap(Optional).**
**Difficulty:- Easy**

Basic Intuition:-
We can create an array of result of length 5 .
Why we are doing an array of length 5 ? Why not 6 , why not 7.
Because in the question it's given the values will be from 1 to 5. So we create an array of length 5.


If the value of the array will be 1 ,then we will increment the value at res[0].
If the value of the array will be 2, then we will increment the value at res[1].
If the value of the array will be 3 , then we will increment the value at res[2].

So what relation we are getting here?
If the input is num , then we increment the value at res[num-1].

Dry Run:-
[![image](https://www.linkpicture.com/q/Migratory-Birds.png)](https://www.linkpicture.com/view.php?img=LPic63257dd7cea4f857060803)

```.java
import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.function.*;
import java.util.regex.*;
import java.util.stream.*;
import static java.util.stream.Collectors.joining;
import static java.util.stream.Collectors.toList;

class Result {

    /*
     * Complete the 'migratoryBirds' function below.
     *
     * The function is expected to return an INTEGER.
     * The function accepts INTEGER_ARRAY arr as parameter.
     */

    public static int migratoryBirds(List<Integer> arr) {
    // Write your code here]
    
    int res[]=new int[5];// created an array of length 5.

    // iterated through the input list  
    for(int i=0;i<arr.size();i++){
        res[arr.get(i)-1]++;//  increment the value at i-1 position.
    }
    int max=0;
    int index=0;
    for(int i=0;i<res.length;i++){
        if(max<res[i]){
            max=res[i];// for checking which is the maximum.
            index=i+1;// store the answer as i+1 , in the index ,because we had incremented the result array as num-1. That's why
        }
    }
    return index;

    }

}

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bufferedWriter = new BufferedWriter(new FileWriter(System.getenv("OUTPUT_PATH")));

        int arrCount = Integer.parseInt(bufferedReader.readLine().trim());

        List<Integer> arr = Stream.of(bufferedReader.readLine().replaceAll("\\s+$", "").split(" "))
            .map(Integer::parseInt)
            .collect(toList());

        int result = Result.migratoryBirds(arr);

        bufferedWriter.write(String.valueOf(result));
        bufferedWriter.newLine();

        bufferedReader.close();
        bufferedWriter.close();
    }
}

```

Time Complexity :- O(N)  
Space Complexity :- O(N)