## 01. Prime Number

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/prime-number2314/1)

### Problem Description

**Task:** Given a number n, determine whether it is a prime number or not.Note: A prime number is a number greater than 1 that has no positive divisors other than 1 and itself.Examples :Input: n = 7

#### Examples

##### Example 1

- **Output:**
```text
false
```
- **Explanation:** 1 has only one divisor (1 itself), which is not sufficient for it to be considered prime.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(sqrt(n))
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-28 23:54:29
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    static boolean isPrime(int n) {
        // code here
       int count=0;
             for(int i =1; i<=n; i++){
               if(n%i==0)
               count++;
             }
             if(count==2){
               return true;
             }else{
               return false;
             }
           }
       }
```

*Generated on: 10/29/2026, 12:19:31 AM*