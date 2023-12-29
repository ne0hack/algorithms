# Square(n) Sum


## Description
Complete the square sum function so that it squares each number passed into it and then sums the results together.

For example, for `[1, 2, 2]` it should return `9` because 1\*\*2 + 2\*\*2 + 2\*\*2 = 9.


## Sample Tests
```python
import codewars_test as test
from solution import square_sum

@test.describe("Fixed Tests")
def basic_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(square_sum([1,2]), 5)
        test.assert_equals(square_sum([0, 3, 4, 5]), 50)
        test.assert_equals(square_sum([]), 0)
        test.assert_equals(square_sum([-1,-2]), 5)
        test.assert_equals(square_sum([-1,0,1]), 2)
```


## Solution
### Python3
```python
def square_sum(numbers):
    result = 0
    for num in numbers:
        result += num ** 2
    return result
```
