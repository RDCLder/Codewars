# Prime Word

[6 Kyu Kata](https://www.codewars.com/kata/5b1e2c04553292dacd00009e)

X and Y are playing a game. A list will be provided which contains n pairs of strings and integers. They have to add the integeri to the ASCII values of the stringi characters. Then they have to check if any of the new added numbers is prime or not. If for any character of the word the added number is prime then the word will be considered as prime word.  Can you help X and Y to find the prime words?

## Code

```python
def prime_word(array):

    output = 0
    prime = []
    
    for i in range(len(array)):
        for j in range(len(array[i][0])):
            if ord(array[i][0][j]) + array[i][1] > 1:
                for k in range(2, ord(array[i][0][j]) + array[i][1]):
                    if (ord(array[i][0][j]) + array[i][1]) % k == 0:
                        output = 0
                        break
                else:
                    output = 1
                    break
        prime.append(output)
                
    return prime
```
