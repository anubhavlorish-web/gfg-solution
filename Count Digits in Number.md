## 01. Count Digits in Number

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/count-total-digits-in-a-number/1)

### Problem Description

**Task:** Given a number n, return the count of digits in this number.Examples :Input: n = 1567

#### Examples

##### Example 1

- **Output:**
```text
5
```
- **Explanation:** The number of digits in 99999 is 5.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(log n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (3)

#### Solution 1 (Java)

- **Submitted:** 2026-10-27 22:34:08
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
    public int countDigits(int n) {
        // Code here
        int digits = 1;
                while (n >= 10) {
                    n /= 10;
                    digits++;
                }

                return (digits);
            }
        }
```

#### Solution 2 (Java)

- **Submitted:** 2026-10-15 22:28:36
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
    public static int countDigits(int n) {
        // Base case: 0 has 1 digit
        if (n == 0) {
            return 1;
        }

        int count = 0;
        while (n > 0) {
            count++;
            n /= 10; // Remove the last digit
        }

        return count;
    }
}
```

#### Solution 3 (Java)

- **Submitted:** 2026-09-18 11:40:20
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    public static int countDigits(int n) {
        if (n==0){
            return 1;
        }
    int count =0;
    while (n != 0) {
          count++;
          n /= 10;
    }
    return count;
    }
    
}
```

*Generated on: 10/27/2026, 10:36:27 PM*