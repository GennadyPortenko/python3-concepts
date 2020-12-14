#### triple-quoted strings
```
multi-line strings can be used as multi-line comments, 
as the are ignored when they are not a docstring:
'''
some code 
here
'''
```

#### f-strings
```python
name = 'a'
val = 20.56234
f'name: {name}, val: {val:.3f}'  # name: a, val: 20.562
```

#### Formatting strings
```python
val = 20.56234
'val = {:.2f}'.format(val)  # 'val = 20.56'

# old style :
'val = %.2f' % val  # 'val = 20.56'
```

```python
', '.join(['hello', 'my friend'])  # 'hello, my friend'
```

#### Operations with strings
```python
'abcdef'[1:4:2]  # 'bd' - slicing with step 2
'abcd'[::-1]  # 'dcba' - reverse string with slicing
'abcd'[-1]  # 'd'
if 'bc' in 'abcd': ...
'hello'.upper()  #  'HELLO'
'HELLO'.lower()  #  'hello'
'hello'.find('ell')  # 1
'hello'.replace('hello',  'hi')  # 'hi'
```
