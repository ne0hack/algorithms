# You Can't Code Under Pressure #1


## Description
Code as fast as you can! You need to double the integer and return it.


## Sample Tests
```python
import codewars_test as test

@test.describe('Tests')
def tests():
    @test.it('Sample Test Case')
    def sample_test_case():
        test.assert_equals(double_integer(2), 4);
        test.assert_equals(double_integer(4), 8);
        test.assert_equals(double_integer(-10), -20);
        test.assert_equals(double_integer(0), 0);
        test.assert_equals(double_integer(100), 200);
```


## Solution
```python
def double_integer(i):
    return i * 2
```
