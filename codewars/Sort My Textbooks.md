# Sort My Textbooks


## Description
HELP! Jason can't find his textbook! It is two days before the test date, and Jason's textbooks are all out of order! Help him sort a list (ArrayList in java) full of textbooks by subject, so he can study before the test.

The sorting should NOT be case sensitive


## Sample Tests
```python
import codewars_test as test
from solution import sorter

@test.describe("Fixed Tests")
def fixed_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(sorter(['Algebra', 'History', 'Geometry', 'English']), ['Algebra', 'English', 'Geometry', 'History'], 'Does not sort strings')
        test.assert_equals(sorter(['Algebra', 'history', 'Geometry', 'english']), ['Algebra', 'english', 'Geometry', 'history'], 'Does not handle capitalization')
        test.assert_equals(sorter(['Alg#bra', '$istory', 'Geom^try', '**english']), ['$istory', '**english', 'Alg#bra', 'Geom^try'], 'Does not handle symbols')
```


## Solution
```python
def sorter(textbooks):
    return sorted(textbooks, key=lambda x: x.lower())
```
