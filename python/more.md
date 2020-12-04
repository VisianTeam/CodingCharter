Python Coding Charter - More
---


# Single Quotes vs Double Quotes

There are no official consensus within the python community but we can say:

- Use single quotes for simple strings, for instance `'word', 'some_characteristic'`

- Use double quotes for sentences, for instance `"I can't pronounce the word 'characteristic'"`




# Keyword only (since python 3.8)

You can force some arguments to be named when used.
This is useful when the order of the arguments is arbitrary or may vary when the project evolve (for instance new arguments added).

To make an argument keyword-only, one can use `*` in definition:

```python
def my_func(array, *, width=1, color='blue'):
    pass
```




# Positional only (since python 3.8)

You can force some arguments to be positional only, meaning they can't be used as keyword argument.
This is useful when the order of the arguments has a real meaning.

To make an argument positional-only, one can use `/` in definition:

```python
def my_func(start, end, /):
    pass
```

> more [here](https://www.python.org/dev/peps/pep-0570/#how-to-teach-this)




# f-string (since 3.6)

When building a string from variables, you should prefer f-string to `format` or `%`.
It is a light and easy-to-read syntax, so don't be afraid to abuse it.

To create a f-string, just place `f` in front of the definition:

```python
my_var = 5
string = f"The current value of my variable is {my_var}"
assert isinstance(string, str)
print(string)
```
