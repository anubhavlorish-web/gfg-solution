## 01. Spirally Traversing Matrix

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/spirally-traversing-a-matrix-1587115621/1)

### Problem Description

**Task:** Given a rectangular matrix mat[][] of size n x m, and return a 1D array containing all its elements in spiral order.Examples:Input: mat[][] = [[1, 2, 3, 4], [5, 6, 7, 8], [9, 10, 11, 12], [13, 14, 15, 16]]

#### Examples

##### Example 1

- **Output:**
```text
[32, 44, 27, 23, 62, 50, 28, 54]
```
- **Explanation:** Applying same technique as shown above, output will be [32, 44, 27, 23, 62, 50, 28, 54].Constraints:1 ≤ n, m ≤10000 ≤ mat[i][j] ≤100

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n * m)
- **Expected Auxiliary Space Complexity:** O(n * m)

### Accepted Solutions (2)

#### Solution 1 (Java)

- **Submitted:** 2026-10-19 10:20:01
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
    public ArrayList<Integer> spirallyTraverse(int[][] matrix) {
        // code here
        int n = matrix.length, m = matrix[0].length;
        int up =0, down = n-1, left = 0, right = m-1;
        ArrayList<Integer> ans = new ArrayList<>();
        while (left <= right && up <= down){
            for(int i= left; i <= right; i++){
                ans.add(matrix[up][i]);
            }
            up++;
            for(int i= up; i <=down; i++){
                ans.add(matrix[i][right]);
            }
            right--;
            if (up <= down){
            for(int i=right; i>= left; i--){
                ans.add(matrix[down][i]);
            }
            }
            down--;
            if (left <= right){
            for(int i= down; i>= up; i--){
                ans.add(matrix[i][left]);
            }
            left++;
            }
        } 
        return ans;
    }
}
```

#### Solution 2 (Java)

- **Submitted:** 2026-10-19 10:19:34
- **Status:** Correct
- **Marks:** 4

```java
class Solution {
    public ArrayList<Integer> spirallyTraverse(int[][] matrix) {
        // code here
        int n = matrix.length, m = matrix[0].length;
        int up =0, down = n-1, left = 0, right = m-1;
        ArrayList<Integer> ans = new ArrayList<>();
        while (left <= right && up <= down){
            for(int i= left; i <= right; i++){
                ans.add(matrix[up][i]);
            }
            up++;
            for(int i= up; i <=down; i++){
                ans.add(matrix[i][right]);
            }
            right--;
            if (up <= down){
            for(int i=right; i>= left; i--){
                ans.add(matrix[down][i]);
            }
            }
            down--;
            if (left <= right){
            for(int i= down; i>= up; i--){
                ans.add(matrix[i][left]);
            }
            left++;
            }
        } 
        return ans;
    }
}
```

*Generated on: 10/21/2026, 11:17:31 AM*