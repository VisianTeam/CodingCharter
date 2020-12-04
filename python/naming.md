Python Coding Charter - Naming
---


# Main rules

Here are the [basic rules](https://visualgit.readthedocs.io/en/latest/pages/naming_convention.html):

* A class is named such as `MyClass` (StudlyCaps)

* A function/method/ is named such as `do_something` (joined_lower)

* A variable/attribute is named such as `my_variable` (joined_lower)

* A global constant is named such as `MY_GLOBAL_CONSTANT` (joined_upper)

Also, one can refer to those advices to [choose the actual name](https://www.tutorialdocs.com/article/some-tips-for-python-variables-and-code-quality.html).



# Long names

When dealing with long names, one can use [shortforms](../shortforms.md).




# Function naming

**Builders** (Creating new objects):

- Use `build_<object_name>` over ~~create_<object_name>~~ or ~~generate_<object_name>~~ (shorter)

- Distinguish `build_<object_name>` (some computation) from `new_<object_name>` (just definition)

- `build_<object_name>` over `<object_name>`

    > If I have a function that create a phonebook, I will call it `build_phonebook` instead of `phonebook`
    > , because `phonebook` sounds like the name of a variable.

**Modifiers** (transforming objects):

- Use a verb when the function modifies the object inplace (e.g. `fill_list`)

- Use a participle when the functions modifies a copy of the object (e.g. `filled_list`)




# Variable naming

Lets they you have a dictionary such as `{"Octave": "+33699999999", ...}`, representing a phonebook.

Valid names: `name_to_number` / `phone_book` / `number_dict` / `numbers_dict` / `people_numbers`

Invalid names: ~~phone_numbers~~ (sounds like a list)
