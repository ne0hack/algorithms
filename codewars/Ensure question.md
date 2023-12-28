# Ensure question


## Description
Given a string, write a function that returns the string with a question mark ("?") appends to the end, unless the original string ends with a question mark, in which case, returns the original string.

For example (**Input --> Output**)

```
"Yes" --> "Yes?"
"No?" --> "No?"
```


## Sample Tests
```python
import codewars_test as test
from solution import ensure_question

@test.describe("Fixed Tests")
def fixed_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(ensure_question(""),"?","Expected: '?'")
        test.assert_equals(ensure_question("Yes"),"Yes?","Expected: '?'")
        test.assert_equals(ensure_question("No?"),"No?","Expected: '?'")
        test.assert_equals(ensure_question("Well????"),"Well????","Expected: '?'")
```


## Solution
### Python3
```python
def ensure_question(s):
    if not s or s[-1] != '?':
        return s + '?'
    return s
```
