## Diagonal Difference.

Problem Statement :- Given a square matrix, calculate the absolute difference between the sums of its diagonals.

**Pre- Requisite:- 2d arrays, for loops.**     
**Difficulty:- Easy**   

[![image](https://www.linkpicture.com/q/Diagonal-Matrix_1.png)](https://www.linkpicture.com/view.php?img=LPic6325c831b5b8e533958911)
**We just need to find the difference between the sum of left and right diagonal**  

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
     * Complete the 'diagonalDifference' function below.
     *
     * The function is expected to return an INTEGER.
     * The function accepts 2D_INTEGER_ARRAY arr as parameter.
     */

    public static int diagonalDifference(List<List<Integer>> arr) 
    {
        int sum=0;
        int sum1=0;
        int diff;
        for(int i=0;i<arr.size();i++)
        {
            sum=sum+arr.get(i).get(i);
        }
        for(int i=0;i<arr.size();i++)
        {
            for(int j=0;j<arr.size();j++)
            {
                if(i+j==arr.size()-1)
                {
                    sum1=sum1+arr.get(i).get(j);
                }
            }
        }
        int dif=sum-sum1;
        int result=Math.abs(dif);
        return result;
        
    

    }

}

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bufferedWriter = new BufferedWriter(new FileWriter(System.getenv("OUTPUT_PATH")));

        int n = Integer.parseInt(bufferedReader.readLine().trim());

        List<List<Integer>> arr = new ArrayList<>();

        IntStream.range(0, n).forEach(i -> {
            try {
                arr.add(
                    Stream.of(bufferedReader.readLine().replaceAll("\\s+$", "").split(" "))
                        .map(Integer::parseInt)
                        .collect(toList())
                );
            } catch (IOException ex) {
                throw new RuntimeException(ex);
            }
        });

        int result = Result.diagonalDifference(arr);

        bufferedWriter.write(String.valueOf(result));
        bufferedWriter.newLine();

        bufferedReader.close();
        bufferedWriter.close();
    }
}

```

Time Complexity:- O(N*N)
Space Complexity :- O(1)