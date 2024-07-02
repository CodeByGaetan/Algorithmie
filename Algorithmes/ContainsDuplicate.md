# Contains Duplicate

Given an integer array nums, return true if any value appears at least twice in the array, and return false if every element is distinct.

## TypeScript

```typescript
function containsDuplicate(nums: number[]): boolean {
  const numSet = new Set<number>();
  for (const num of nums) {
    if (numSet.has(num)) return true;
    numSet.add(num);
  }
  return false;
}
```

## Python

```python
class Solution(object):
    def containsDuplicate(self, nums):
        numSet = set()
        for i in nums:
            if i in numSet :
                return True
            numSet.add(i)
        return False
```

## Java

```java
class Solution {
    public boolean containsDuplicate(int[] nums) {
        Set<Integer> hashSet = new HashSet<>();
        for (int num : nums) {
            if (!hashSet.add(num)) {
                return true;
            }
        }
        return false;
    }
}
```
