# Isograms

[7 Kyu Kata](https://www.codewars.com/kata/54ba84be607a92aa900000f1)

An isogram is a word that has no repeating letters, consecutive or non-consecutive. Implement a function that determines whether a string that contains only letters is an isogram. Assume the empty string is an isogram. Ignore letter case.

## Code

```python
def is_isogram(string):    
    
    string = str.lower(string)
    numbers = '123456789'
    
    if len(string) > 0:
        for i in range(len(string)):
            if (string[i] in numbers) or (string.count(string[i]) > 1):
                is_isogram = False
                break
            else:
                is_isogram = True
    else:
        is_isogram = True
    return is_isogram
```
