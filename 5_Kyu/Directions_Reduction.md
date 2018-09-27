# Directions Reduction (Unfinished)

[5 Kyu Kata](https://www.codewars.com/kata/550f22f4d758534c1100025a)

The goal is to take a list of cardinal directions (NORTH, SOUTH, EAST, WEST) and return a list with all directly opposite directions removed.  For example, NORTH and SOUTH cancel out when next to each other.  NORTH, WEST, SOUTH do not.

## Code

```python
def dirReduc(arr):
    
    print(arr)
    n = arr.count('NORTH')
    s = arr.count('SOUTH')
    e = arr.count('EAST')
    w = arr.count('WEST')
    output = []
    
    if 0 < n < s:
        s -= n
        n = 0
    elif 0 < s < n:
        n -= s
        s = 0
    elif n == s and n > 1 and s > 1:
        n = 0
        s = 0
    
    if 0 < e < w:
        w -= e
        e = 0
    elif 0 < w < e:
        e -= w
        w = 0
    elif e == w and e > 1 and w > 1:
        e = 0
        w = 0
    
    if n > 0:
        output.append('NORTH' * n)
    if w > 0:
        output.append('WEST' * w)
    if s > 0:
        output.append('SOUTH' * s)
    if e > 0:
        output.append('EAST' * e)
    
    return output
    
#     while arr.count('NORTH') > 1 and arr.count('SOUTH') > 1:
#         arr.remove('NORTH')
#         arr.remove('SOUTH')
#     while arr.count('EAST') > 1 and arr.count('WEST') > 1:
#     return ['NORTH' * n, 'WEST' * w, 'SOUTH' * s, 'EAST' * e]
```
