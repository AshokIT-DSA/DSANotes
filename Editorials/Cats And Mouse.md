## Cats And Mouse.
>Problem Statement:- Given a cat A , Cat b And Mouse C , at given co ordinates. So we have to find out which cat reaches faster.
Then return CAT a or b as the answer depending upon the situation.    
If noth the cat reaches at the same time , then return  Mouse C as answer.    

**Pre- Requiste:- Mathematics**  
**Difficulty:-Easy**    
Basic Intuition:-  

[![image](https://www.linkpicture.com/q/Cat-And-Mouse.png)](https://www.linkpicture.com/view.php?img=LPic6325b95a8db081094543526)

```.java
import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.regex.*;

public class Solution {

    // Complete the catAndMouse function below.
    static String catAndMouse(int x, int y, int z) {
        
        int res1=Math.abs(x-z);
        int res2=Math.abs(y-z);
        if(res1>res2){
            return "Cat B";
        }
        else if(res2>res1){
            return "Cat A";
        }
        else{
            return "Mouse C";
        }

    }

    private static final Scanner scanner = new Scanner(System.in);

    public static void main(String[] args) throws IOException {
        BufferedWriter bufferedWriter = new BufferedWriter(new FileWriter(System.getenv("OUTPUT_PATH")));

        int q = scanner.nextInt();
        scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");

        for (int qItr = 0; qItr < q; qItr++) {
            String[] xyz = scanner.nextLine().split(" ");

            int x = Integer.parseInt(xyz[0]);

            int y = Integer.parseInt(xyz[1]);

            int z = Integer.parseInt(xyz[2]);

            String result = catAndMouse(x, y, z);

            bufferedWriter.write(result);
            bufferedWriter.newLine();
        }

        bufferedWriter.close();

        scanner.close();
    }
}

```
Time Complexity:-O(1)  
Space Complexity:-O(1)