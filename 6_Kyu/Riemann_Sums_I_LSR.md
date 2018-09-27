# Riemann Sums I (Left Side Rule)

[6 Kyu Kata](https://www.codewars.com/kata/5562ab5d6dca8009f7000050)

## Code

```python
def left_riemann(f, n, a, b):
    
    sum = 0
    h = (b - a) / n
    
    for i in range(n):
        x = h * i + a
        sum += f(x)

    return sum * h
```
