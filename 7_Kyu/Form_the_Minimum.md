# Form the Minimum

[7 Kyu Kata](https://www.codewars.com/kata/5ac6932b2f317b96980000ca)

Given a list of digits, return the smallest number that could be formed from these digits, using the digits only once ( ignore duplicates).

## Code

```python
def min_value(digits):
    string = []
    order = sorted(list(digits))
    
    for i in order:
        while order.count(i) > 1:
            order.remove(i)
    
    for i in range(len(order)):
        string.append(str(order[i]))
    joinString = ''.join(string)
    return int(joinString)
```
