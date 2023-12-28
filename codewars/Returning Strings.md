# Returning Strings


## Description
Make a function that will return a greeting statement that uses an input; your program should return, `"Hello, <name> how are you doing today?"`.


## Sample Tests
```python
import codewars_test as test
from solution import greet

@test.describe("Fixed Tests")
def basic_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(greet('Ryan'), "Hello, Ryan how are you doing today?")
        test.assert_equals(greet('Shingles'), "Hello, Shingles how are you doing today?")
```


## Solution
```python
def greet(name):
    return f"Hello, {name} how are you doing today?"
```
