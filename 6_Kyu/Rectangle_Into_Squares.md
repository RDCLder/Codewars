# Rectangle Into Squares

[6 Kyu Kata](https://www.codewars.com/kata/55466989aeecab5aac00003e)

## Code

```python
def sqInRect(lng, wdth):

    dimensions = sorted([lng, wdth])
    area = lng * wdth
    sizes = []

    if lng != wdth:
        while area > 0 and dimensions[0] > 1 and dimensions[1] > 1:
            sizes.append(dimensions[0])
            area -= dimensions[0] ** 2
            dimensions[0], dimensions[1] = sorted([(dimensions[1] - dimensions[0]), dimensions[0]])

        if dimensions[0] == 1 or dimensions[1] == 1:
            while area > 0:
                sizes.append(1)
                area -= 1

        return sizes

    elif lng == wdth:
        return None
```
