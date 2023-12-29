# Exclamation marks series #2: Remove all exclamation marks from the end of sentence


## Description
Remove all exclamation marks from the end of sentence.

### Examples

```
"Hi!"     ---> "Hi"
"Hi!!!"   ---> "Hi"
"!Hi"     ---> "!Hi"
"!Hi!"    ---> "!Hi"
"Hi! Hi!" ---> "Hi! Hi"
"Hi"      ---> "Hi"
```


## Sample Tests
```python
test.describe("Basic Tests")

tests = [
    #[input, expected],
    ["Hi!" , "Hi"],
    ["Hi!!!" ,"Hi"],
    ["!Hi" , "!Hi"],
    ["!Hi!" , "!Hi"],
    ["Hi! Hi!" , "Hi! Hi"],
    ["Hi" , "Hi"],
]

for inp, exp in tests:
    test.assert_equals(remove(inp), exp)
```


## Solution
### Python3
```python
def remove(s):
    while s and s[-1] == '!':
        s = s[:-1]
    return s
```
