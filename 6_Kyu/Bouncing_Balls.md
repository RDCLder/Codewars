# Bouncing Balls

[6 Kyu Kata](https://www.codewars.com/kata/5544c7a5cb454edb3c000047)

A child is playing with a ball on the nth floor of a tall building at height h.  He drops the ball out of the window, and the ball bounces to two-thirds of its height.  His mother looks out of a window 1.5 meters from the ground.  How many times will the mother see the ball pass in front of her window (including when it's falling and bouncing?

## Code

```python
def bouncingBall(h, bounce, window):
    
    if 0 < window < h and 0 < bounce < 1:
        count = 0
        while 0 < window < h:
            if count == 0:
                count += 1
            else:
                count += 2
            h *= bounce
        return count
    
    else:
        return -1
```
