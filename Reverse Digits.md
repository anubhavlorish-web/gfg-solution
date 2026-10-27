## 01. Reverse Digits

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/reverse-digit0316/1)

### Problem Description

**Task:** You are given an integer n. Your task is to reverse the digits, ensuring that the reversed number has no leading zeroes.

#### Examples

##### Example 1

- **Input:**
```text
n = 122
```
- **Output:**
```text
221
```
- **Explanation:** By reversing the digits of number, number will change into 221.

##### Example 2

- **Input:**
```text
n = 200
```
- **Output:**
```text
2
```
- **Explanation:** By reversing the digits of number, number will change into 2.

##### Example 3

- **Input:**
```text
n = 12345
```
- **Output:**
```text
54321
```
- **Explanation:** By reversing the digits of number, number will change into 54321.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(log n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-27 22:49:16
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public int reverseDigits(int n) {
        // Code here
        int rev=0;
        while(n>0){
            int last= n%10;
            n=n/10;
            rev= (rev*10)+last;
        }
        return(rev);
    }
}
```

*Generated on: 10/27/2026, 10:49:44 PM*