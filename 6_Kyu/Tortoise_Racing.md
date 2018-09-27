# Tortoise Racing

[6 Kyu Test](https://www.codewars.com/kata/55e2adece53b4cdcb900006c)

## Code

```python
def race(v1, v2, g):

    t = g / ((v2 - v1) / 3600)
    h = int(t / 3600)
    m = int((t - h * 3600) / 60)
    s = int(t - h * 3600 - m * 60)
  
    if h >= 0 and m >= 0 and s >= 0:
        return [h, m, s]
```
