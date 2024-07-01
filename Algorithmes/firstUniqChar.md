# Find First Unique Character

Given a string s, find the first non-repeating character in it and return its index. If it does not exist, return -1.

## TypeScript

```typescript
function firstUniqChar(s: string): number {
  const charCount = new Map<string, number>();

  for (let char of s) {
    charCount.set(char, (charCount.get(char) || 0) + 1);
  }

  for (let i = 0; i < s.length; i++) {
    if (charCount.get(s[i]) === 1) {
      return i;
    }
  }

  return -1;
}
```

## Python

```python
def firstUniqChar(s: str) -> int:
    charCount = {}

    for char in s:
        charCount[char] = charCount.get(char, 0) + 1

    for i, char in enumerate(s):
        if charCount[char] == 1:
            return i

    return -1
```

## Java

```java
class Solution {
    public int firstUniqChar(String s) {
        Map<Character, Integer> charCount = new HashMap<>();

        for (char c : s.toCharArray()) {
            charCount.put(c, charCount.getOrDefault(c, 0) + 1);
        }

        for (int i = 0; i < s.length(); i++) {
            if (charCount.get(s.charAt(i)) == 1) {
                return i;
            }
        }

        return -1;
    }
}
```
