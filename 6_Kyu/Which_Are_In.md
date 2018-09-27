# Which Are In?

[6 Kyu Kata](https://www.codewars.com/kata/550554fd08b86f84fe000a58)

## Code

```python
def in_array(a1, a2):
    
    r = []
    
    for s in a1:
        for i in range(len(a2)):
            if a2[i].find(s) != -1:
                if s not in r:
                    r.append(s)
                break
    
    print(a1, a2)
    return sorted(r)
```
