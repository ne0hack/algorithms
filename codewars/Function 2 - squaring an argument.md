# Function 2 - squaring an argument


## Description
Now you have to write a function that takes an argument and returns the square of it.


## Sample Tests
```python
import codewars_test as test
from solution import square

@test.describe("Fixed Tests")
def fixed_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(square(2), 4)
        test.assert_equals(square(50), 2500)
        test.assert_equals(square(1), 1)
```


## Solution
### Python
```python
def square(n):
    return n ** 2
```
