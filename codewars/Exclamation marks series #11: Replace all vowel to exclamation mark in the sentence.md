# Exclamation marks series #11: Replace all vowel to exclamation mark in the sentence


## Description
Replace all vowel to exclamation mark in the sentence. `aeiouAEIOU` is vowel.

### Examples

```
replace("Hi!") === "H!!"
replace("!Hi! Hi!") === "!H!! H!!"
replace("aeiou") === "!!!!!"
replace("ABCDE") === "!BCD!"
```


## Sample Tests
```python
import codewars_test as test
from solution import replace_exclamation

@test.describe("Fixed Tests")
def fixed_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(replace_exclamation("Hi!") , "H!!")
        test.assert_equals(replace_exclamation("!Hi! Hi!") , "!H!! H!!")
        test.assert_equals(replace_exclamation("aeiou") , "!!!!!")
        test.assert_equals(replace_exclamation("ABCDE") , "!BCD!")
```


## Solution
### Python3
```python
def replace_exclamation(st):
    vowel = list("aeiouAEIOU")
    st = list(st)
    for i, v in enumerate(st):
        if v in vowel:
            st[i] = '!'
    return ''.join(st)
```
