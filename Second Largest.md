## 01. Second Largest

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/second-largest3735/1)

### Problem Description

**Task:** Given an array of positive integers arr[], return the second largest element from the array. If the second largest element doesn't exist then return -1.Note: The second largest element should not be equal to the largest element.Examples:Input: arr[] = [12, 35, 1, 10, 34, 1]

#### Examples

##### Example 1

- **Output:**
```text
-1
```
- **Explanation:** The largest element of the array is 10 and the second largest element does not exist.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-11-01 23:57:34
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    public int getSecondLargest(int[] arr) {
        // code here
        int n=arr.length;
        int largest=arr[0];
        for(int i=0; i<n;i++){
            if(arr[i]>largest){
                largest=arr[i];
            }
        }
        int sl=-1;
        for(int i=0; i<n;i++){
            if(arr[i]>sl && arr[i]!=largest){
                sl=arr[i];
            }
        }
        return sl;
    }
}
```

*Generated on: 11/1/2026, 11:58:33 PM*