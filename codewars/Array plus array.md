# Array plus array


## Description
I'm new to coding and now I want to get the sum of two arrays... Actually the sum of all their elements. I'll appreciate for your help.

P.S. Each array includes only integer numbers. Output is a number too.


## Sample Tests
```python
import codewars_test as test
from solution import array_plus_array

@test.describe("Fixed Tests")
def fixed_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(array_plus_array([1, 2, 3], [4, 5, 6]), 21)
        test.assert_equals(array_plus_array([-1, -2, -3], [-4, -5, -6]), -21)
        test.assert_equals(array_plus_array([0, 0, 0], [4, 5, 6]), 15)
        test.assert_equals(array_plus_array([100, 200, 300], [400, 500, 600]), 2100)
```


## Solution
### Python3
```python
def array_plus_array(arr1,arr2):
    return sum([*arr1, *arr2])
```
