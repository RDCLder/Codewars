# Duplicate Encoder

[6 Kyu Kata](https://www.codewars.com/kata/54b42f9314d9229fd6000d9c)

## Code

```python
def duplicate_encode(word):
    
    word = word.lower()
    output = ''
    
    for char in word:
        if word.count(char) == 1:
            output += '('
        else:
            output += ')'
    
    return output
```
