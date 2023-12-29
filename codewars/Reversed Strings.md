# Reversed Strings


## Description
Complete the solution so that it reverses the string passed into it. 

```
'world'  =>  'dlrow'
'word'   =>  'drow'
```


## Sample Tests
```python
import codewars_test as test
from solution import solution

@test.describe("Fixed Tests")
def basic_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(solution('world'), 'dlrow')
        test.assert_equals(solution('hello'), 'olleh')
        test.assert_equals(solution(''), '')
        test.assert_equals(solution('h'), 'h')
```


## Solution
### Python3
```python
def solution(string):
    return string[::-1]
```
