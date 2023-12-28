# Do you speak "English"?


## Description
Given a string of arbitrary length with any ascii characters. Write a function to determine whether the string contains the whole word "English".

The order of characters is important -- a string "abcEnglishdef" is correct but "abcnEglishsef" is not correct.

Upper or lower case letter does not matter -- "eNglisH" is also correct.

Return value as boolean values, true for the string to contains "English", false for it does not.


## Sample Tests
```python
@test.describe('Example Tests')
def example_tests():
    @test.it('Example Test Case')
    def example_test_case():
        test.assert_equals(sp_eng("english"), True)
        test.assert_equals(sp_eng("egnlish"), False)
        test.assert_equals(sp_eng("engliish"), False)
        test.assert_equals(sp_eng("1234egn lis;h"), False)
        test.assert_equals(sp_eng("1234english ;k"), True)
        test.assert_equals(sp_eng("English"), True)
        test.assert_equals(sp_eng("eNgliSh"), True)
        test.assert_equals(sp_eng("1234#$%%eNglish ;k9"), True)
        test.assert_equals(sp_eng("EGNlihs"), False)
        test.assert_equals(sp_eng("1234englihs**"), False)
        
    @test.it('Edge Test Case')
    def edge_test_case():
        test.assert_equals(sp_eng(""), False)
```


## Solution
```python
def sp_eng(sentence):
    return 'english' in sentence.lower()
```
