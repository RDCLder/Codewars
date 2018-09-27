# Are They The Same?

[6 Kyu Kata](https://www.codewars.com/kata/550498447451fbbd7600041c)

Given two arrays a and b write a function comp(a, b) (compSame(a, b) in Clojure) that checks whether the two arrays have the "same" elements, with the same multiplicities. "Same" means, here, that the elements in b are the elements in a squared, regardless of the order.

## Code

```python
def comp(array1, array2):
    
    if (array1 == None and array2 != None) or (array1 != None and array2 == None):
        return False
    elif array1 == None and array2 == None:
        return True
    elif array1 == [] and array2 == []:
        return True
    elif len(array1) == len(array2):
        
        check = 0
        array1 = sorted(array1)
        array2 = sorted(array2)
        
        for i in range(len(array1)):
            if array1[i] == array2[i] or array1[i] ** 2 == array2[i]:
                check += 1
        if check == len(array1):
            return True
        else:
            return False
    else:
        return False
```
