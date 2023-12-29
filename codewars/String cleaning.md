# String cleaning


## Description
Your boss decided to save money by purchasing some cut-rate optical character recognition software for scanning in the text of old novels to your database. At first it seems to capture words okay, but you quickly notice that it throws in a lot of numbers at random places in the text.

### Examples (input -> output)

```
'! !'                 -> '! !'
'123456789'           -> ''
'This looks5 grea8t!' -> 'This looks great!'

```

Your harried co-workers are looking to you for a solution to take this garbled text and remove all of the numbers. Your program will take in a string and clean out all numeric characters, and return a string with spacing and special characters `~#$%^&!@*():;"'.,?` all intact.


## Sample Tests
```python
import codewars_test as test
from solution import string_clean

@test.describe("Fixed Tests")
def fixed_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(string_clean(""), "")
        test.assert_equals(string_clean("! !"), "! !")
        test.assert_equals(string_clean("123456789"), "")
        test.assert_equals(string_clean("(E3at m2e2!!)"), "(Eat me!!)")
        test.assert_equals(string_clean("Dsa32 cdsc34232 csa!!! 1I 4Am cool!"), "Dsa cdsc csa!!! I Am cool!")
        test.assert_equals(string_clean("A1 A1! AAA   3J4K5L@!!!"), "A A! AAA   JKL@!!!")
        test.assert_equals(string_clean("Adgre2321 A1sad! A2A3A4 fv3fdv3J544K5L@"), "Adgre Asad! AAA fvfdvJKL@")
        test.assert_equals(string_clean("Ad2dsad3ds21 A  1$$s122ad! A2A3Ae24 f44K5L@222222 "), "Addsadds A  $$sad! AAAe fKL@ ")
        test.assert_equals(string_clean("33333Ad2dsad3ds21 A3333  1$$s122a!d! A2!A!3Ae$24 f2##222 "), "Addsadds A  $$sa!d! A!A!Ae$ f## ")
        test.assert_equals(string_clean("My \"me3ssy\" d8ata issues2! Will1 th4ey ever, e3ver be3 so0lved?"), "My \"messy\" data issues! Will they ever, ever be solved?")
        test.assert_equals(string_clean("Wh7y can't we3 bu1y the goo0d software3? #cheapskates3"), "Why can't we buy the good software? #cheapskates")
```


## Solution
```python
def string_clean(s):
    """
    Function will return the cleaned string
    """
    return ''.join([i for i in s if not i.isdigit()])
```
