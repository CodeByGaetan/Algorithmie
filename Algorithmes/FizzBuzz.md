# FizzBuzz

Given an integer n, return a string array answer (1-indexed) where:

- answer[i] == "FizzBuzz" if i is divisible by 3 and 5.
- answer[i] == "Fizz" if i is divisible by 3.
- answer[i] == "Buzz" if i is divisible by 5.
- answer[i] == i (as a string) if none of the above conditions are true.

## TypeScript

```typescript
function fizzBuzz(n: number): string[] {
  const answer: string[] = [];

  for (let i = 1; i <= n; i++) {
    if (i % 3 === 0 && i % 5 === 0) {
      answer.push("FizzBuzz");
    } else if (i % 3 === 0) {
      answer.push("Fizz");
    } else if (i % 5 === 0) {
      answer.push("Buzz");
    } else {
      answer.push(String(i));
    }
  }

  return answer;
}
```

## Python

```python
class Solution(object):
    def fizzBuzz(self, n):
        answer = []

        for i in range(1, n + 1):
            if i % 3 == 0 and i % 5 == 0:
                answer.append("FizzBuzz")
            elif i % 3 == 0:
                answer.append("Fizz")
            elif i % 5 == 0:
                answer.append("Buzz")
            else:
                answer.append(str(i))

        return answer
```

## Java

```java
class Solution {
    public List<String> fizzBuzz(int n) {
        List<String> answer = new ArrayList<>();

        for (int i = 1; i <= n; i++) {
            if (i % 3 == 0 && i % 5 == 0) {
                answer.add("FizzBuzz");
            } else if (i % 3 == 0) {
                answer.add("Fizz");
            } else if (i % 5 == 0) {
                answer.add("Buzz");
            } else {
                answer.add(String.valueOf(i));
            }
        }

        return answer;
    }
}
```
