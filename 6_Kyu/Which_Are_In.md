# Which Are In?

[6 Kyu Kata](https://www.codewars.com/kata/550554fd08b86f84fe000a58)

Given two arrays of strings a1 and a2 return a sorted array r in lexicographical order of the strings of a1 which are substrings of strings of a2.

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
