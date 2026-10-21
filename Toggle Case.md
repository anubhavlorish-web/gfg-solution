## 01. Toggle Case

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/toggle-case/1)

### Problem Description

**Task:** Given a string s, convert the characters of the string into the opposite case, i.e., if a character is lowercase, then convert it into uppercase and vice versa. Examples:Input: s = "geeksForgEeks"

#### Examples

##### Example 1

- **Output:**
```text
HELLOeVERYoNE
```
- **Explanation:** The cases of the characters in "helloEveryOne" are flipped.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-21 11:54:46
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    public String toggleCase(String s) {
        // code here
        char[] c = s.toCharArray();
        for(int i=0; i<c.length;i++){
            if(Character.isLetter(c[i])){
                c[i] ^=32;
            }
        }
        return new String(c);
    }
}
```

*Generated on: 10/21/2026, 11:55:16 AM*