# Sum without highest and lowest number


## Description
Sum all the numbers of a given array ( cq. list ), except the highest and the lowest element ( by value, not by index! ).

The highest or lowest element respectively is a single element at each edge, even if there are more than one with the same value.

Mind the input validation.

### Example

```
{ 6, 2, 1, 8, 10 } => 16
{ 1, 1, 11, 2, 3 } => 6

```

### Input validation

If an empty value ( `null`, `None`, `Nothing` etc. ) is given instead of an array, or the given array is an empty list or a list with only `1` element, return `0`.


## Sample Tests
```python
import codewars_test as test
from solution import sum_array

@test.describe("Fixed Tests")
def fixed_tests():
    @test.it('None or Empty')
    def basic_test_cases():
        test.assert_equals(sum_array(None), 0)
        test.assert_equals(sum_array([]), 0)

    @test.it("Only one Element")
    def one_test_cases():
        test.assert_equals(sum_array([3]), 0)
        test.assert_equals(sum_array([-3]), 0)
        
    @test.it("Only two Element")
    def two_test_cases():
        test.assert_equals(sum_array([ 3, 5]), 0)
        test.assert_equals(sum_array([-3, -5]), 0)

    @test.it("Real Tests")
    def real_test_cases():
        test.assert_equals(sum_array([6, 2, 1, 8, 10]), 16)
        test.assert_equals(sum_array([6, 0, 1, 10, 10]), 17)
        test.assert_equals(sum_array([-6, -20, -1, -10, -12]), -28)
        test.assert_equals(sum_array([-6, 20, -1, 10, -12]), 3)
```


## Soltion
### Python3
```python
def sum_array(arr):
    if not arr: return 0
    arr.remove(max(arr))
    if not arr: return 0
    arr.remove(min(arr))
    if not arr: return 0
    return sum(arr)
```
