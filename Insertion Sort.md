## 01. Insertion Sort

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/insertion-sort/1)

### Problem Description

**Task:** Given an array arr[] of positive integers.The task is to complete the insertsort() function which is used to implement Insertion Sort. Examples:Input: arr[] = [4, 1, 3, 9, 7]

#### Examples

##### Example 1

- **Output:**
```text
[1, 4, 9]Explanation: The sorted array will be [1, 4, 9].
```

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n^2)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (2)

#### Solution 1 (Java)

- **Submitted:** 2026-10-16 10:39:37
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
    // Please change the array in-place
    public void insertionSort(int arr[]) {
        // code here
        int n =arr.length;
        for(int i=1;i<n;i++){
            int j=i;
            while(j>0 && arr[j]<arr[j-1]){
                int temp=arr[j];
                arr[j]=arr[j-1];
                arr[j-1]=temp;
                j--;
            }
        }
    }
}
```

#### Solution 2 (Java)

- **Submitted:** 2026-10-13 15:42:08
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    // Please change the array in-place
    public void insertionSort(int arr[]) {
        // code here
        int n=arr.length;
        int temp;
        for(int i=0;i<n;i++){
            for(int j=0;j<n-1-i;j++){
                if(arr[j]>arr[j+1]){
                    temp=arr[j];
                    arr[j]=arr[j+1];
                    arr[j+1]=temp;
                }
            }
            
        }

    //  System.out.print(Arrays.toString(arr));
}
}
```

*Generated on: 10/16/2026, 10:45:09 AM*