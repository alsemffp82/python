High-Level Overview
===================

Key Characteristics
-------------------

-   General-Purpose
-   Dynamic Typing
-   Concise and Expressive
-   "Batteries Included"
-   Multi-Paradigm (OOP, FP, etc.)
-   Philosophy

        import this

Where It's Used
---------------

-   **Web**: Django, Flask, Chalice (on AWS), etc.
-   **Data Science**: Jupyter Notebook (Formerly IPython Notebook),
    TensorFlow, Spark (PySpark), etc.
-   Scripting, automation, etc.

Basics
======

Types
-----

-   Boolean: `True`, `False`
-   String: `"hello"`, `'world'`
-   Integers: `5`, `-100`
-   Floats: `3.14`
-   `None`

Arithmetics
-----------

-   `+`
-   `-`
-   `*`
-   `/`
-   `//`
-   `%`
-   `**`

Control Flow
------------

-   `if` / `elif` / `else`

        if a and b:
            print("Both true!")
        elif a and not b:
            print("Only a true!")
        elif not a and b:
            print("Only b true!")
        else:
            print("Neither true!")

        "Both true!" if a and b else "Only one or neither is true!"

-   `for`

        for x in [1, 2, 3]:
            print(x)

-   `while`

        a = 1
        while a < 10:
            print(a)
            a = a + 1

Collections
===========

List
----

    [1, 2, 3]

-   Ordered
-   Mutable
-   (0-)indexed

### Slices

    words = ["nz", "kr", "dev", "study", "group", "is", "fun"]
    words[0]
    words[0:3]
    words[:3]
    words[3:7]
    words[3:]

Tuple
-----

    (1, 2, 3)

-   Ordered
-   Immutable
-   (0-)indexed
-   Multiple return values, variable-length argument list, etc.

Dictionary
----------

    {"a": 1, "b": 2}

-   Unordered (ordered in 3.6+) key-value pairs, mutable
-   Also known as map or hash map in other languages

Set
---

    {1, 2, 2}

-   Unordered
-   No duplicates
-   `union`, `difference`, `intersection`, etc.

Idioms: Comprehensions
======================

List Comprehension
------------------

    [x for x in "helloworld"]  # ['h', 'e', 'l', 'l', 'o', 'w', 'o', 'r', 'l', 'd']

Dictionary Comprehension
------------------------

    import string
    {x: string.ascii_lowercase.index(x) for x in "helloworld"}  # {'h': 7, 'e': 4, 'l': 11, 'o': 14, 'w': 22, 'r': 17, 'd': 3}

Set Comprehension
-----------------

    {x for x in "helloworld"}  # {'r', 'l', 'e', 'd', 'h', 'w', 'o'}

Functions
=========

Basic Syntax
------------

    def add(a, b):
        return a + b

    def add_nums(*nums):
        return sum(nums)

    add_nums(1, 2, 3, 4)  # 10

    def add_to(n, to=10):
        return n + to

    add_to(20)  # Add 20 to 10 => 30
    add_to(50, to=100)  # Add 50 to 100 => 150

    def build_msg(template, **vals):
        return template.format(**vals)

    build_msg("{a} {b}!", a="hello", b="world")  # "hello world!"

Anonymous Functions
-------------------

    lambda a, b: a + b

Higher-Order Functions
----------------------

    filter(lambda x: x % 2 == 0, range(1, 5))  # [2, 4] when realised
    map(lambda x: x ** 2, [2, 4])  # [4, 16] when realised

    import functools
    functools.reduce(lambda a, b: a + b, range(1, 5))  # 10 == 1 + 2 + 3 + 4

Generators
==========

    def doubles(n):
        while n < 10:
            doubled = n * 2
            yield doubled
            n = n + 1

    def doubles_infinite(n):
        while True:
            doubled = n * 2
            yield doubled
            n = n + 1

    doubles_gen = (x * 2 for x in range(1, 10))

    import itertools
    doubles_gen_infinite = (x * 2 for x in itertools.count(1))

Tips
====

-   Choose Python 3 (Python 2 is a dead language)
-   REPL-driven development (Install `ipython`!)
-   Inspection
    -   `type`
    -   `dir`
    -   `help`
    -   `?` (view docstring)
    -   `??` (view source)

            import this
            this??
