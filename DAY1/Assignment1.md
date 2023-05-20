# Assignment 1

### Pascal's Triangle - using Memoization
#### Languages : (Java, Python, Javascript)

#### Explaination :

Pascal's Traingle :
Pascal's triangle, in algebra, a triangular arrangement of numbers that gives the coefficients in the expansion of any binomial expression, such as (x + y)n

![image](https://github.com/nithishrcta/Telusko-10daychallenge/blob/274e7f4f7804c159b2b2aed1e564c1370f37896e/DAY1/download%20(1).png)


#### Java Code 

```
import java.util.HashMap;
import java.util.Map;

public class PascalTriangleMemoization {

    private static Map<String, Integer> cache = new HashMap<>();

    public static int getPascalValue(int row, int col) {
        if (col == 0 || col == row) {
            return 1;
        }
        
        String key = row + "-" + col;
        if (cache.containsKey(key)) {   // Memoization
            return cache.get(key);
        }
        
        int value = getPascalValue(row - 1, col - 1) + getPascalValue(row - 1, col);
        cache.put(key, value);

        return value;
    }

    public static void main(String[] args) {
        int numRows;
        Scanner sn = new Scanner(System.in);
        numRows = sn.nextInt():
        for (int i = 0; i < numRows; i++) {
            for (int j = 0; j <= i; j++) {
                System.out.print(getPascalValue(i, j) + " ");
            }
            System.out.println();
        }
    }
}


```
