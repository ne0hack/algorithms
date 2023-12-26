# Exclamation marks series #5: Remove all exclamation marks from the end of words


## Description
Remove all exclamation marks from the end of words. Words are separated by a single space. There are no exclamation marks within a word.

### Examples

```
remove("Hi!") === "Hi"
remove("Hi!!!") === "Hi"
remove("!Hi") === "!Hi"
remove("!Hi!") === "!Hi"
remove("Hi! Hi!") === "Hi Hi"
remove("!!!Hi !!hi!!! !hi") === "!!!Hi !!hi !hi"
```


## Sample Tests
```python
import codewars_test as test
from solution import remove

@test.describe("Fixed Tests")
def fixed_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(remove('Hi!'), 'Hi')
        test.assert_equals(remove('Hi!!!'),'Hi')
        test.assert_equals(remove('!Hi'), '!Hi')
        test.assert_equals(remove('!Hi!'), '!Hi')
        test.assert_equals(remove('Hi! Hi!'), 'Hi Hi')
        test.assert_equals(remove('!!!Hi !!hi!!! !hi') , '!!!Hi !!hi !hi')
```


## Solution
### Python3
```python
def remove(st):
    result = ""
    for word in st.split():
        new_word = ""
        can_add = False
        for a in word[::-1]:
            if a != '!':
                can_add = True
            elif not can_add:
                continue
            new_word += a
        result += new_word[::-1] + " "
    return result.strip()
```
