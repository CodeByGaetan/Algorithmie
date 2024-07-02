# Reverse String

Write a function that reverses a string. The input string is given as an array of characters s.
Note that you must do this in-place without making a copy of the array.

## TypeScript

```typescript
function reverseString(s: string[]): void {
  let left = 0;
  let right = s.length - 1;

  while (left < right) {
    const temp = s[left];
    s[left] = s[right];
    s[right] = temp;
    left++;
    right--;
  }
}
```

## Python

```python
class Solution(object):
    def reverseString(self, s):
        n = len(s)
        for i in range(n // 2):
            s[i], s[n - 1 - i] = s[n - 1 - i], s[i]
```

## Java

```java
class Solution {
    public void reverseString(char[] s) {
        int left = 0;
        int right = s.length - 1;

        while (left < right) {
            char temp = s[left];
            s[left] = s[right];
            s[right] = temp;
            left++;
            right--;
        }
    }
}
```
