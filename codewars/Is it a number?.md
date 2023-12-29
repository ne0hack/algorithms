# Is it a number?


## Description
Given a string s, write a method (function) that will return true if its a valid single integer or floating number or false if its not.

Valid examples, should return true:

```
isDigit("3")
isDigit("  3  ")
isDigit("-3.23")
```

should return false:

```
isDigit("3-4")
isDigit("  3   5")
isDigit("3 5")
isDigit("zero")
```


## Sample Tests
```python
import codewars_test as test
try:
    from solution import isDigit as is_digit
except:
    from solution import is_digit

@test.describe("Fixed Tests")
def fixed_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(is_digit("s2324"), False)
        test.assert_equals(is_digit("-234.4"), True)
        test.assert_equals(is_digit("3 4"), False)
        test.assert_equals(is_digit("3-4"), False)
        test.assert_equals(is_digit("3 4   "), False)
        test.assert_equals(is_digit("34.65"), True)
        test.assert_equals(is_digit("-0"), True)
        test.assert_equals(is_digit("0.0"), True)
        test.assert_equals(is_digit(""), False)
        test.assert_equals(is_digit(" "), False)
```


## Solution
### Python3
```python
def is_digit(s):
    try:
        float(s)
        return True
    except:
        return False
```
