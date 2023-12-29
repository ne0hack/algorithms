# Reversed Words


## Description
Complete the solution so that it reverses all of the words within the string passed in.

Words are separated by exactly one space and there are no leading or trailing spaces.

**Example(Input --> Output):**

```
"The greatest victory is that which requires no battle" --> "battle no requires which that is victory greatest The"
```


## Sample Tests
```python
import codewars_test as test

try:
    from solution import reverseWords as reverse_words
except ImportError:
    from solution import reverse_words

@test.describe("Fixed Tests")
def fixed_tests():
    @test.it("Basic Tests")
    def basic_tests():
        test.assert_equals(reverse_words("hello world!"), "world! hello")
```


## Solution
### Python3
```python
def reverse_words(s):
    return ' '.join(s.split()[::-1])
```
