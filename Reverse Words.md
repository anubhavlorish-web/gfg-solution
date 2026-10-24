## 01. Reverse Words

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/reverse-words-in-a-given-string5459/1)

### Problem Description

**Task:** Given a string s, reverse the string without reversing its individual words. Words are separated by dots(.).The string may contain leading or trailing dots(.) or multiple dots(.) between two words. The returned string should only have a single dot(.) separating the words and no extra dots should be included.Examples :Input: s = "i.like.this.program.very.much"Output: "much.very.program.this.like.i"

#### Examples

##### Example 1

- **Output:**
```text
"home"
```
- **Explanation:** The input string contains only one word with extra dots around it. After removing the extra dots, the output is "home".

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-24 14:38:54
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    public String reverseWords(String s) {
        // Code here
        String[] arr = s.split("\\.");
        StringBuilder ans = new StringBuilder();
        
        for(int i = arr.length-1; i>=0;i--){
            if(!arr[i].isEmpty()){
                if(ans.length()>0){
                    ans.append(".");
                }
                ans.append(arr[i]);
            }
        }
        return ans.toString();
    }
}
```

*Generated on: 10/24/2026, 2:39:20 PM*