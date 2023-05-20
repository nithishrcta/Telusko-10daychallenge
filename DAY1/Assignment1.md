# Assignment 1

### Pascal's Triangle - using Memoization
Languages : (Java, Python, Javascript)

#### Pascal's Traingle :
Pascal's triangle, in algebra, a triangular arrangement of numbers that gives the coefficients in the expansion of any binomial expression, such as (x + y)n

![image](https://github.com/nithishrcta/Telusko-10daychallenge/blob/274e7f4f7804c159b2b2aed1e564c1370f37896e/DAY1/download%20(1).png)

#### Explaination :
* We declare a static HashMap called cache to store computed values. The keys in the map will be in the format "row-col", and the corresponding values will be the computed Pascal's Triangle values.
* The getPascalValue method takes two parameters: row and col. It computes the value at the specified row and column in Pascal's Triangle using memoization.
* The method starts with two base cases:
    * If the column is 0 or equal to the row, it means we are at the beginning or end of the row, so the value is always 1.
    * If the computed value is already present in the memo, we directly return it.
* If the value is not in the memo, we compute it recursively:
    * We call getPascalValue for the previous row and the two adjacent columns (one column to the left and one column to the right).
    * We add the values from the two recursive calls to get the current value.
* After computing the value, we store it in the memo using the put method, with the key as "row-col" and the value as the computed value.
* Finally, in the main method, we specify the number of rows (numRows) we want to print in Pascal's Triangle.
* We use nested loops to iterate over the rows and columns and print the values using the getPascalValue method.
* Each row is printed on a new line using System.out.println().

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
