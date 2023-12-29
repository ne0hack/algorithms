# Convert boolean values to strings 'Yes' or 'No'.


## Description
Complete the method that takes a boolean value and return a `"Yes"` string for `true`, or a `"No"` string for `false`.


## Sample Tests
```python
import codewars_test as test
from solution import bool_to_word

@test.describe("Fixed Tests")
def basic_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(bool_to_word(True), 'Yes')
        test.assert_equals(bool_to_word(False), 'No')
```


## Solution
### Python3
```python
def bool_to_word(boolean):
    if boolean: return 'Yes'
    return 'No'
```
