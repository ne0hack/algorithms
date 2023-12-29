# Grasshopper - Array Mean


## Description
Find the mean (average) of a list of numbers in an array.

### Information

To find the mean (average) of a set of numbers add all of the numbers together and divide by the number of values in the list.

For an example list of `1, 3, 5, 7`

1. Add all of the numbers

```
1+3+5+7 = 16
```

2. Divide by the number of values in the list. In this example there are 4 numbers in the list.

```
16/4 = 4
```

3. The mean (or average) of this list is 4


## Sample Tests
```python
import codewars_test as test
from solution import find_average

@test.describe("Fixed Tests")
def fixed_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(find_average([1]), 1)
        test.assert_equals(find_average([1, 3, 5, 7]), 4)
        test.assert_equals(find_average([-1, 3, 5, -7]), 0)
        test.assert_equals(find_average([5, 7, 3, 7]), 5.5)
        test.assert_equals(find_average([0]), 0)
```


## Solution
### Python3
```python
def find_average(nums):
    return sum(nums) / len(nums)
```
