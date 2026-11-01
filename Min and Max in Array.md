## 01. Min and Max in Array

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/find-minimum-and-maximum-element-in-an-array4428/1)

### Problem Description

**Task:** Given an array arr[]. Your task is to find the minimum and maximum elements in the array.Examples:Input: arr[] = [1, 4, 3, 5, 8, 6]

#### Examples

##### Example 1

- **Output:**
```text
[3, 15]Explanation: minimum and maximum element of array are 3 and 15.
```

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-11-01 23:30:03
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public ArrayList<Integer> getMinMax(int[] arr) {
        int n= arr.length;
        // code Here
        int min=arr[0];
        for(int i=0; i<n;i++){
            if(arr[i]<min){
                min=arr[i];
            }
        }
        int max=arr[0];
        for(int i=0; i<n;i++){
            if(arr[i]>max){
                max=arr[i];
            }
        }
        ArrayList<Integer> result = new ArrayList<>();
    result.add(min);
    result.add(max);
    return result;

    }
}
```

*Generated on: 11/1/2026, 11:30:32 PM*