# Parabolic Arc Length

[6 Kyu Test](https://www.codewars.com/kata/562e274ceca15ca6e70000d3)

## Code

```python
def len_curve(n):
    
    x = [0]
    y = [0]
    length = 0
    
    for i in range(1, n + 1):
        x.append((1 / n) * i)
        y.append(x[i] ** 2)
        length += ((y[i] - y[i - 1]) ** 2 + (x[i] - x[i - 1]) ** 2) ** (1/2)
    
    return round(length, 9)
```
