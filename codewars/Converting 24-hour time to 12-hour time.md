# Converting 24-hour time to 12-hour time


## Description
Converting a 24-hour time like "0830" or "2030" to a 12-hour time (like "8:30 am" or "8:30 pm") sounds easy enough, right? Well, let's see if you can do it!

You will have to define a function named "to12hourtime", and you will be given a four digit time string (in "hhmm" format) as input.

Your task is to return a 12-hour time string in the form of "h:mm am" or "h:mm pm". (Of course, the "h" part will be two digits if the hour is greater than 9.)


## Sample Tests
```python
import codewars_test as test
try:
    from solution import to12hourtime as to_12_hour_time
except:
    from solution import to_12_hour_time

@test.describe("Fixed Tests")
def fixed_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(to_12_hour_time('0100'), '1:00 am')
        test.assert_equals(to_12_hour_time('1300'), '1:00 pm')
        test.assert_equals(to_12_hour_time('0630'), '6:30 am')
        test.assert_equals(to_12_hour_time('2145'), '9:45 pm')
```


## Solution
```python
def to_12_hour_time(time_string):
    if int(time_string[:2]) == 0:
        return f'12:{time_string[2:]} am'
    elif int(time_string[:2]) == 12:
        return f'12:{time_string[2:]} pm'
    elif int(time_string[:2]) > 12:
        return f'{int(time_string[:2])-12}:{time_string[2:]} pm'
    return f'{int(time_string[:2])}:{time_string[2:]} am'
```
