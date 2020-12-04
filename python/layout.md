Python Coding Charter - Layout
---


# Imports

Here are the rules on imports:

- Import are at the top of the file, right under the module docstring

- First are the imports of external libraries

    - on top: `import ...`
    
    - right under: `from ... import ...`
    
- Second are the imports of the modules

    - on top: `import ...`
    
    - right under: `from ... import ...`

- Imports are sorted alphabetically

For instance:

```python
""""This is my module docstring"""
import numpy as np
import pandas as pd
from collections import OrderedDict
from os.path import exists, join

import module.params as parameters
import module.tools as tools
from module.containers import (
    DeviceList,
    SensorList,
    System,
)
```

There are some particular cases where you can import within functions/loops:
 
- The libraries are heavy (e.g. keras, tensorflow), so you want the import to be done only if necessary

- The libraries are optional




# Spacing

- 2 line separate functions

- 1 line separate methods

- at most 1 line separate two line of code



# Long declarations


Do not use '\', there are more elegant ways to handle long declarations.

Most of them are based on the use of parenthesis (as `(1) == 1`)


## String

```python

long_text_rule = (
    "When writing a long string, one can use parenthesis and break down the"
    " text on several lines like so. Each segments will automatically be"
    " concatenated. One tricky thing though is to make sure you don't forget"
    " the spaces between the segments."
)

adjective = "convenient"
lg_fstring = (
    "One can use f-strings in such cases, and can switch between class string"
    f" and f-string between lines. It is kind of {adjective}."
    " So go for it !"
)
```


## Containers

```python
dummy_d = {
    'key1': 1,
    'key2': {
        'key21': 21,
        'key22': 22,
    },
}
```

About:

- A coma on the line of the last item of a dictionary (not json-like):  reduce git-diff when adding an extra argument


## Function calls



```python
print(
    "I am printing something not interesting",
    "It is just a showcase",
    sep=". ",
    end="\n\n",
)
```

About:

- One argument per row: ease reading & reduce git-diff when adding/changing/removing an argument

- A coma on the line of the last argument: reduce git-diff when adding an extra argument


## Condition

```python
if (
        <some long statement>
        or <some other long statement>
    ):
    print()"This is true"

```

### Formula

```python
result = (
    (1 + 5)
    / 8
    * 9
)
```

About:

- Operators must start each line (so they are nicely aline)
