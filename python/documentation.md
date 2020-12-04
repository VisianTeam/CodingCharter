Python Coding Charter - Documentation
---


# References

For more details, refer to:

- [PEP257](https://www.python.org/dev/peps/pep-0257/)

- [Google style conventions](https://sphinxcontrib-napoleon.readthedocs.io/en/latest/example_google.html)




# Docstring


##

Docstring is required for every function/method your implement, unless it is a magic method or a very simple function (such as `add(a, b)`).

The first line of the docstring must give a clear idea of what the function does


## Function signature


### Example (Google conventions)

```python
def evaluate_data_quality(path, *, to_file=None, w_bounds=True):
    """Create statistics on each column of csv file
    
    Args:
        path (str)      : path to csv file to evaluate quality of
        to_file (str)   : path to a file where to save results
            None for no save
        w_bounds (bool) : create columns with min and max values indicators

    Return:
        (dict): statistics of each column
            {
                column_name (str): {
                    'empty_row_c'   : number of empty rows (int),
                    'filling_r'     : ratio of none empty rows (float),
                    'max_value' (if w_bounds): max value in column,
                    'min_value' (if w_bounds): min value in column,
                },
                ...
            }          
    """
    ...
```

About:

- There is no need to align the ':', but it does make it more readable (just use TAB key)

- When dealing with specific structures (such as multi-ladder dictionaries, list of dictionaries, ...), you should precise the related structure

- Types given in args are understood by Pycharm, which is convenient


### Use of type-hints

I don't like it, but if you do feel free to use it


## Comments


### Content of a container

When initiating variables with specific structures, one should specify the kind of content to give a hint of what it will contain:

Examples:

```python
phone_book = {
    # (first name, last name): number
}
phone_numbers = [
    # list of str such as '+33699999999'
]
```
