# Multiply


## Description
This code does not execute properly. Try to figure out why.


## Sample Tests
```python
import codewars_test as test
from solution import multiply

@test.describe("Fixed Tests")
def fixed_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(multiply(2,1), 2)
```


## Solution
```python
def multiply(a, b):
    return a * b
```
