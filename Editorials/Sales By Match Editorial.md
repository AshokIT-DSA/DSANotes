## Sales By Match Editorial.

**Problem Statement: - Given an array of Integer , which contains numbers , The numbers here are represented as socks, we have to return how many matching pair of socks are there.**  

**Pre-Requisite:- Array, HashMap(Optional).**  
**Difficulty:- Easy**  


[![image](https://www.linkpicture.com/q/Sock-Match_1.png)](https://www.linkpicture.com/view.php?img=LPic6325b787797031760922137)



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
     * Complete the 'sockMerchant' function below.
     *
     * The function is expected to return an INTEGER.
     * The function accepts following parameters:
     *  1. INTEGER n
     *  2. INTEGER_ARRAY ar
     */

    public static int sockMerchant(int n, List<Integer> arr) {
    // Write your code here
    int res[]=new int[101];// why we created an array of 
    for(int i=0;i<arr.size();i++){
        res[arr.get(i)]++;
    }
    int score=0;
    for(int i=0;i<res.length;i++){
        score=score+(res[i]/2);
    }
    return score;

    }

}

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bufferedWriter = new BufferedWriter(new FileWriter(System.getenv("OUTPUT_PATH")));

        int n = Integer.parseInt(bufferedReader.readLine().trim());

        List<Integer> ar = Stream.of(bufferedReader.readLine().replaceAll("\\s+$", "").split(" "))
            .map(Integer::parseInt)
            .collect(toList());

        int result = Result.sockMerchant(n, ar);

        bufferedWriter.write(String.valueOf(result));
        bufferedWriter.newLine();

        bufferedReader.close();
        bufferedWriter.close();
    }
}

```
Time Complexity :-O(N)  
Space COmplexity:- O(101)
