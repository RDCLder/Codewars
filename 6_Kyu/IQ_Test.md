# IQ Test

[6 Kyu Test](https://www.codewars.com/kata/552c028c030765286c00007d)

Bob is preparing to pass IQ test. The most frequent task in this test is to find out which one of the given numbers differs from the others. Bob observed that one number usually differs from the others in evenness. Help Bob — to check his answers, he needs a program that among the given numbers finds one that is different in evenness, and return a position of this number.

Keep in mind that your task is to help Bob solve a real IQ test, which means indexes of the elements start from 1 (not 0)

## Code

```python
def iq_test(numbers):
    
    numbers = numbers.split()
    integers = []
    even = 0
    odd = 0
    output = 0
    
    for i in range(0, len(numbers)):
        integers.append(int(numbers[i]))

    for i in integers:
        if i % 2 == 0:
            even += 1
        else:
            odd += 1
    
    if even > odd:
        for i in range(len(integers)):
           if integers[i] % 2 != 0:
                output = i + 1       
    elif odd > even:
        for i in range(len(integers)):
            if integers[i] % 2 == 0:
                output = i + 1
    
    return output
```
