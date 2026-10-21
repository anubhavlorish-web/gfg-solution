## 01. Count Words in String

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/count-number-of-words1500/1)

### Problem Description

**Task:** Given a string s consisting of lowercase English alphabets, spaces, tab characters (\t), and newline characters (\n), count the total number of words present in the string. A word is defined as a continuous sequence of lowercase English letters, while spaces, tabs, and newline characters act as separators between words.Examples:Input: s = "abc def"

#### Examples

##### Example 1

- **Output:**
```text
2
```
- **Explanation:** There is a space at 4th position which works as a seperator between "abc" and "def".

##### Example 2

- **Input:**
```text
s = "a\nyo\t"
```
- **Output:**
```text
2
```
- **Explanation:** There are two words in the string: "a" and "yo". The characters \n and \t act as separators, splitting the string into words.Constraints:2 <= Length of String <= 10⁶

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-21 10:48:31
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    public int countWords(String s) {
        // code here
        int count=0;
        int a =s.length();
        boolean b=false;
        
        for(int i =0; i<a ; i++){
            char ch = s.charAt(i);
            if (ch >= 'a' && ch <= 'z') {
                if (!b) {
                     count++;
                     b= true;
        }
    }else{ 
        b = false;
        }
      } 
      return count;
    }
}
```

*Generated on: 10/21/2026, 11:16:34 AM*