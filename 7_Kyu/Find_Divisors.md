# Find Divisors of a Number

[7 Kyu Kata](https://www.codewars.com/kata/542c0f198e077084c0000c2e)

Find the number of divisors of a positive integer n.

## Code

```python
def divisors(n):
    
    output = 0
    i = 2
    
    if n == 1:
        return 1
    elif n > 1:
        while i <= n:
            if n % i == 0:
                output += 1
            i += 1
    
    return output + 1
```
