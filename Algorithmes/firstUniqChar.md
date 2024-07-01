# Find First Unique Character

## TypeScript

```typescript
function firstUniqChar(s: string): number {
  let map = new Map<string, number>();

  for (let char of s) {
    const occ = map.get(char);
    if (occ) {
      map.set(char, occ + 1);
    } else {
      map.set(char, 1);
    }
  }

  for (let i = 0; i < s.length; i++) {
    if (map.get(s[i]) === 1) return i;
  }

  return -1;
}
```

## Python

```python
def firstUniqChar(s: str) -> int:
    map = {}

    for char in s:
        if char in map:
            map[char] += 1
        else:
            map[char] = 1

    for i, char in enumerate(s):
        if map[char] == 1:
            return i

    return -1
```

## Java

```java
import java.util.HashMap;
import java.util.Map;

public class Solution {
    public int firstUniqChar(String s) {
        Map<Character, Integer> map = new HashMap<>();

        for (char c : s.toCharArray()) {
            map.put(c, map.getOrDefault(c, 0) + 1);
        }

        for (int i = 0; i < s.length(); i++) {
            if (map.get(s.charAt(i)) == 1) {
                return i;
            }
        }

        return -1;
    }
}
```
