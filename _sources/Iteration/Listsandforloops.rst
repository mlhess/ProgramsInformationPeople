..  Copyright (C)  Brad Miller, David Ranum, Jeffrey Elkner, Peter Wentworth, Allen B. Downey, Chris
    Meyers, and Dario Mitchell.  Permission is granted to copy, distribute
    and/or modify this document under the terms of the GNU Free Documentation
    License, Version 1.3 or any later version published by the Free Software
    Foundation; with Invariant Sections being Forward, Prefaces, and
    Contributor List, no Front-Cover Texts, and no Back-Cover Texts.  A copy of
    the license is included in the section entitled "GNU Free Documentation
    License".

.. _iter_list:

Lists and ``for`` loops
-----------------------

It is also possible to perform **list traversal** using iteration by item as well as iteration by index.


.. activecode:: chp09_03a

    fruits = ["apple","orange","banana","cherry"]

    for afruit in fruits:     # by item
        print(afruit)

It almost reads like natural language: For (every) fruit in (the list of) fruits,
print (the name of the) fruit.

We can also use the indices to access the items in an iterative fashion.

.. activecode:: chp09_03b

    fruits = ["apple","orange","banana","cherry"]

    for position in range(len(fruits)):     # by index
        print(fruits[position])


In this example, each time through the loop, the variable ``position`` is used as an index into the
list, printing the ``position``-eth element. Note that we used ``len`` as the upper bound on the range
so that we can iterate correctly no matter how many items are in the list.

Since lists are mutable, it is often desirable to traverse a list, modifying
each of its elements as you go. The following code squares all the numbers from ``1`` to
``5`` using iteration by position.

.. activecode:: chp09_for4

    numbers = [10, 20, 30, 40, 50]
    print(numbers)

    for i in range(len(numbers)):
        numbers[i] = numbers[i]**2

    print(numbers)

Take a moment to think about ``range(len(numbers))`` until you understand how
it works. In this case, since ``len(numbers)`` is 5, it's the same as saying ``range(5)``.
We are interested here in both the *value* (10, 20, 30, etc.) and its *index* within the
list (0, 1, 2, etc.), so that we can assign a new value to the position in the list.

:ref:`Later in this chapter <list_accum>` you will see how to transform an existing list into a new list without mutating (modfiying) the existing list.

