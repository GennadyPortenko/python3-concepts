### Data types

#### Boolean type
```python
print(type(True))  # <class 'bool'>
```

#### Numeric types
```python
print(type(1))  # <class 'int'>
print(type(1.1))  # <class 'float'>
print(type(1 + 2j))  # <class 'complex'>
```

#### Sequences
`1. String (immutable) `
```python
print(type("abc"))  # <class 'str'>  -  Immutable
```

```2. List (mutable) ```
```python
type([3, 'four', 5])  # <class 'list'>
len(some_list)
l1 = some_list.copy()  # shallow copy
l2 = list(some_list)  # shallow copy
some_list.pop(0)  # remove element and return it
some_list.insert(2, 'five')  # if 2 > len-1 then appends to the end
some_list.append(5)
some_list[-2]  # second element from the end
some_list = [1, 2] * 2  # [1, 2, 1, 2]
[1, 2, 3, 4][:]  # slicing creates a new object
[1, 2, 3, 4][::-1]  # reverse a list
[1, 2, 3, 4, 5][1:4]  # (2, 3, 4) - with step 2
[1, 2, 3, 4, 5][::2]  # (1, 3, 5)
[1, 2, 3, 4, 5][1::2]  # (2, 4)
[i*i for i in some_list]  # list of squared elements
for i in some_list: ...
first, second = some_tuple  # unpack a list
```

```3. Tuple (immutable)  -  Immutable 'list' ```
```python
type((1, 2, 3))  # <class 'tuple'>
('first',)  # tuple of 1 element
tuple(some_list)  # create a tuple from a list
```

#### Set (mutable)
```python
type({1, 'Second'})  # <class 'set'>
{}  # an empty dictionary, not a set
{1, 3, 4, 5}.union({2, 3, 7, 8})  # {1, 2, 3, 4, 5, 7, 8}
{1, 3, 4, 5}.intersection({2, 3, 7, 8})  # {3}
{1, 3, 4, 5}.difference({2, 3, 7, 8})  # {1, 4, 5}
frozenset([1, 2, 3])  # immutable set
```

#### Dictionary (mutable)
```python
type({1:1.0, 'name':'first'})  # <class 'dictionary'>
some_dict['name'] = 'second'  # update a key-value pair
del some_dict[1]  # delete a key-value pair
if 'name' in some_dict: ...
for key in some_dict.values(): ...
for key, value in some_dict.items(): ...
some_dict.update(another_dict)  # merge dictionaries (values'll be overridden)
```

