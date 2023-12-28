# Evil or Odious


## Description
The number n is Evil if it has an even number of 1's in its binary representation.\
The first few Evil numbers: 3, 5, 6, 9, 10, 12, 15, 17, 18, 20

The number n is Odious if it has an odd number of 1's in its binary representation.\
The first few Odious numbers: 1, 2, 4, 7, 8, 11, 13, 14, 16, 19

You have to write a function that determine if a number is Evil of Odious, function should return "It's Evil!" in case of evil number and "It's Odious!" in case of odious number.


## Sample Tests
```python
import codewars_test as test
from solution import evil

@test.describe("Fixed Tests")
def fixed_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(evil(1),"It's Odious!")
        test.assert_equals(evil(2),"It's Odious!")
        test.assert_equals(evil(3),"It's Evil!")
```


## Solution
```python
def evil(n):
    if bin(n).count('1') % 2 == 0:
        return "It's Evil!"
    else:
        return "It's Odious!"
```
