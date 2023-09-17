# Capitals first!


## Description
Create a function that takes an input String and returns a String, where all the uppercase words of the input String are in front and all the lowercase words at the end. The order of the uppercase and lowercase words should be the order in which they occur.

If a word starts with a number or special character, skip the word and leave it out of the result.

Input String will not be empty.

For an input String: "hey You, Sort me Already!" the function should return: "You, Sort Already! hey me"


## Sample Tests
```python
import codewars_test as test
from solution import capitals_first

@test.describe("Fixed Tests")
def fixed_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(capitals_first("sense Does to That Make you?"), "Does That Make sense to you?")
        test.assert_equals(capitals_first("hey You, Sort me Already"), "You, Sort Already hey me")
        test.assert_equals(capitals_first("sense Does to That Make you?"), "Does That Make sense to you?")
        test.assert_equals(capitals_first("i First need Thing In coffee The Morning"), "First Thing In The Morning i need coffee")
        test.assert_equals(capitals_first("123 baby You and Me"), "You Me baby and")
        test.assert_equals(capitals_first("Life gets Sometimes pretty !Hard"), "Life Sometimes gets pretty")
```


## Solution
### Python3
```python
def capitals_first(text):
    up, low = [], []
    for word in text.split():
        if not word[0].isalpha():
            continue
        elif word[0] == word[0].upper():
            up.append(word)
        else:
            low.append(word)
    return " ".join(up + low)
```
