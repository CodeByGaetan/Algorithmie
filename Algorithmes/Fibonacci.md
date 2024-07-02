# Fibonacci Number

The Fibonacci numbers, commonly denoted F(n) form a sequence, called the Fibonacci sequence, such that each number is the sum of the two preceding ones, starting from 0 and 1. That is,

- F(0) = 0, F(1) = 1
- F(n) = F(n - 1) + F(n - 2), for n > 1.

Given n, calculate F(n).

## TypeScript

```typescript
function fib(n) {
  let list: number[] = [0, 1];

  for (let i = 2; i <= n; i++) {
    list[i] = list[i - 1] + list[i - 2];
  }

  return list[n];
}
```

## Python

```python
class Solution(object):
    def fib(self, n):
        fib_list = [0, 1]

        for i in range(2, n + 1):
            fib_list.append(fib_list[-1] + fib_list[-2])

        return fib_list[n]
```

## Java

```java
class Solution {
    public int fib(int n) {
        ArrayList<Integer> list = new ArrayList(Arrays.asList(0, 1));

        for (Integer i = 2; i <= n; i++) {
            list.add(list.get(i-1) + list.get(i-2));
        }

        return list.get(n);
    }
}
```
