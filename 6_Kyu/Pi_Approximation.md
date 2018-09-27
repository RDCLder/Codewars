# Pi Approximation

[6 Kyu Kata](https://www.codewars.com/kata/550527b108b86f700000073f)

The aim of the kata is to try to show how difficult it can be to calculate decimals of an irrational number with a certain precision. We have chosen to get a few decimals of the number "pi" using the following infinite series (Leibniz 1646–1716):

PI / 4 = 1 - 1/3 + 1/5 - 1/7 + ... which gives an approximation of PI / 4.

There are several ways to determine the precision of the calculus but to keep things easy we will calculate to within epsilon of your language Math::PI constant. In other words we will stop the iterative process when the absolute value of the difference between our calculation and the Math::PI constant of the given language is less than epsilon.  Your function returns an array or an arryList or a string or a tuple depending on the language (See sample tests) where your approximation of PI has 10 decimals.

## Code

```python
def iter_pi(epsilon):

    from math import pi
    precision = 0
    odd = 1
    sign = 1
    i = 0
    
    while abs(precision * 4 - pi) > epsilon:
        precision +=  1.0 / (odd * sign)
        odd += 2
        sign *= -1
        i += 1
    
    return [i, round(precision * 4, 10)]
```
