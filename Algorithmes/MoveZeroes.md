# Move Zeroes

Given an integer array nums, move all 0's to the end of it while maintaining the relative order of the non-zero elements.
Note that you must do this in-place without making a copy of the array.

## TypeScript

```typescript
function moveZeroes(nums: number[]): void {
  let insertPos: number = 0;

  for (let i = 0; i < nums.length; i++) {
    if (nums[i] !== 0) {
      nums[insertPos] = nums[i];
      insertPos++;
    }
  }

  while (insertPos < nums.length) {
    nums[insertPos] = 0;
    insertPos++;
  }
}
```

## Python

```python
class Solution(object):
    def moveZeroes(self, nums):
        insPos = 0

        for i, num in enumerate(nums):
            if num != 0:
                nums[insPos] = num
                insPos += 1

        while insPos < len(nums):
            nums[insPos] = 0
            insPos += 1
```

## Java

```java
class Solution {
    public void moveZeroes(int[] nums) {
        int insPos = 0;
        for (int i = 0; i < nums.length; i++) {
            if (nums[i] != 0) {
                nums[insPos] = nums[i];
                insPos++;
            }
        }

        while (insPos < nums.length) {
            nums[insPos] = 0;
            insPos++;
        }
    }
}
```
