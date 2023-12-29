# Simple multiplication


## Description
This kata is about multiplying a given number by eight if it is an even number and by nine otherwise.


## Sample Tests
```python
import codewars_test as test
from solution import simple_multiplication

@test.describe("Fixed Tests")
def fixed_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(simple_multiplication(2), 16)
        test.assert_equals(simple_multiplication(1), 9)
        test.assert_equals(simple_multiplication(8), 64)
        test.assert_equals(simple_multiplication(4), 32)
        test.assert_equals(simple_multiplication(5), 45)
```


## Solution
### Python3
```python
def simple_multiplication(number):
    return number * 8 if number % 2 == 0 else number * 9
```

