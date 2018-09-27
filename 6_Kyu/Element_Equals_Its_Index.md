# Element Equals Its Index

[6 Kyu Test](https://www.codewars.com/kata/5b7176768adeae9bc9000056)

## Code

```python
def index_equals_value(arr):
    i = 0
    output = -1
    
    while arr[i] <= i:
        if arr[i] == i:
            output = i
            break
        i += 1
    return output
```
