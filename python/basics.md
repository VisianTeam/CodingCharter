Python Coding Charter - Basics
---




# Introduction

For more details, please refer to **[PEP8 documentation](https://www.python.org/dev/peps/pep-0008/)**, as it is the official style guide for python.
This document sums up the main guidelines, choose when multiple styles are allowed, and add tweaks here & there.


## Rule breakers

Please, keep in mind there is no obligation to follow the rules, these are guidelines to ensure consistency of coding.
But as mentioned in PEP8, there are cases where you can ignore them:
1. When it keeps the code more readable, even for someone used to PEP8
2. When the code needs to remain compatible with older versions of Python that don't support the feature recommended by the style guide
3. When the code predates the introduction of the guideline and there is no other reason to be modifying that code
4. When you want to keep consistency with the surrounding code that breaks the guideline (maybe for historic reasons)

> About 3 and 4, such projects may need some styling rework. It usually takes less than a day to change the coding style of an entire project, so it may be worth doing it.
> Make sure to have tests implemented first.


## Key rules

* Use 4 spaces per indentation level

* One line must have at must 79 characters (indents/spaces included)

    > One may go over the limit when writing docstring or comments (PEP 8 limits those to 72, seems)


## Helpers

* Use an IDLE with a **linter** to check basic styling rules, for instance:
    
    - PyCharm
    
    - SublimeText, with SublimeLinter and SublimeLinter-flake8

* Add a ruler at 80 characters

* Make sure your IDLE writes 4 spaces when pressing TAB

* Use version of python 3
