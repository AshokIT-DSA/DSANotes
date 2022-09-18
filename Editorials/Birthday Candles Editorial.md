Problem Statemnt : - Given an Array of Integers, we have to find out that how many times the maximum is appearing.

**Pre- Requisite:- for loops.**  
**Difficulty:- Easy**  

>Intuition:-
We are given a list of integers.  
First we need to find out the maximum among the list.  
After that in the 2nd iteration we will check how many times max is appearing in the list and then return the count as the answer.  

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
     * Complete the 'birthdayCakeCandles' function below.
     *
     * The function is expected to return an INTEGER.
     * The function accepts INTEGER_ARRAY candles as parameter.
     */

    public static int birthdayCakeCandles(List<Integer> candles) 
    {
    // Write your code here
    int count=0;
    int max=candles.get(0);
    // this is for finding out the maximum
    for(int i=1;i<candles.size();i++)
    {
        if(max<candles.get(i))
        {
            max=candles.get(i);
        }
        
    }
    // this is for finding out how many times the max appears

    for(int i=0;i<candles.size();i++)
    {
        if(max==candles.get(i))
        {
            count++;
        }
    }
    return count;

    }

}

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bufferedWriter = new BufferedWriter(new FileWriter(System.getenv("OUTPUT_PATH")));

        int candlesCount = Integer.parseInt(bufferedReader.readLine().trim());

        List<Integer> candles = Stream.of(bufferedReader.readLine().replaceAll("\\s+$", "").split(" "))
            .map(Integer::parseInt)
            .collect(toList());

        int result = Result.birthdayCakeCandles(candles);

        bufferedWriter.write(String.valueOf(result));
        bufferedWriter.newLine();

        bufferedReader.close();
        bufferedWriter.close();
    }
}

```
Time Complexity:-O(N)  
Space Complexity:- O(1)  