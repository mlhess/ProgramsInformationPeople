..  Copyright (C)  Brad Miller, David Ranum, Jeffrey Elkner, Peter Wentworth, Allen B. Downey, Chris
    Meyers, and Dario Mitchell.  Permission is granted to copy, distribute
    and/or modify this document under the terms of the GNU Free Documentation
    License, Version 1.3 or any later version published by the Free Software
    Foundation; with Invariant Sections being Forward, Prefaces, and
    Contributor List, no Front-Cover Texts, and no Back-Cover Texts.  A copy of
    the license is included in the section entitled "GNU Free Documentation
    License".

.. _modules_chap: 

Modules
=======

.. video:: inputvid
    :controls:
    :thumb: ../_static/modules.png

    http://media.interactivepython.org/thinkcsVideos/modules.mov
    http://media.interactivepython.org/thinkcsVideos/modules.webm

A **module** is a file containing Python definitions and statements intended for
use in other Python programs. There are many Python modules that come with
Python as part of the **standard library**. 

The  `Python Documentation <https://docs.python.org/3.4/>`_ site for Python version
3.4 is an extremely useful reference for all aspects of Python. The site
contains a listing of all the standard modules that are available with Python
(see `Global Module Index <https://docs.python.org/3.4/py-modindex.html>`_). You
will also see that there is a
`Standard Library Reference <https://docs.python.org/3.4/library/index.html>`_
(Next week, there will be a chapter explaining how to read the language
reference documentation) and a
`Tutorial <https://docs.python.org/3.4/tutorial/index.html>`_, as well as
installation instructions, how-tos, and frequently asked questions.  We
encourage you to become familiar with this site and to use it often.

If you have not done so already, take a look at the Global Module Index.  Here
you will see an alphabetical listing of all the modules that are available as
part of the standard library.  Find the turtle module.

Importing Modules
-----------------

In order to use Python modules, you have to **import** them into a Python program. That happens with an import statement: the word ``import``, and then the *name* of the module. The name is case-sensitive. Roughly translated to English, an import statement says "there's some code in another file; please make its functions and variables available in this file." More technically, an import statement causes all the code in another file to be executed. Any variables that are bound during that execution (including functions that are defined) may then be referred in some way (to be discussed) in the current file.

By convention, all ``import`` commands are put at the very top of your file. They can be put elsewhere, but that can lead to some confusions, so it's best to follow the convention.

Where do these other files that you can import come from? It could be a code file that you wrote yourself, or it could be code that someone else wrote and you copied on to your computer.

For example, if you have a file ``myprog.py`` in directory ``~\Desktop\mycode\``, and myprog.py contains a line of code ``import morecode``, then the python interpreter will look for a file called ``morecode.py``, excecute its code, and make its object bindings available for reference in the rest of the code in myprog.py. 

Note that it is ``import morecode``, not ``import morecode.py``, but the other file has to be called ``morecode.py``.

The python interpreter will look for ``morecode.py`` in the following places, in this order:

1. The directory where the current file lives (``~\Desktop\mycode\`` in the example). If it finds ``morecode.py`` there, it uses it. If not, it goes on to step 2.

2. Other directories that are on the PYTHONPATH. PYTHONPATH is a list of directories on your computer that is automatically configured for you when you install python on your computer. It can be changed if you know what you're doing, but you probably shouldn't mess with it. Indeed, for the duration of this class, you should never need to know what your PYTHONPATH is set to. You will use an installer called ``pip`` to download new modules from the Internet; it will automatically figure out what your PYTHONPATH is and copy the files in those modules to directories that are on the PYTHONPATH. If the interpreter fails to find ``morecode.py`` on the PYTHONPATH, it goes on to step 3.

3. The directory for modules that are built into the python **standard library**. The code files for those libraries are automatically copied into a folder on your computer when you install python. You don't need to worry about where they are installed. In this course, you will use some modules that are part of the python standard library (e.g., the ``random`` module for generating random numbers). The interpreter will fail to find ``morecode.py`` in the standard library and will then yield an error message of the form ``ImportError: No module named morecode``.

.. note::

    Bottom line: make sure you put ``morecode.py`` in the same directory as ``myprog.py``

The tests you see in your problem sets are also using a Python module that's in the standard library, called ``UnitTest``. Right now, you can't see the code that causes those tests to run, because we have hidden it from you, but later in the course, you will learn how to write your own Unit Tests for code, and to do so, you will need to write an import statement at the beginning of your programs. Even before you learn how to write your own tests, you will see code for Unit Tests in your problem set files.

.. admonition:: Don't overwrite standard library modules!

    Given the order of search for external Python modules that is described in the list above, it is possible to overwrite a standard library. For example, if you create a file ``random.py`` in the same directory where ``myprog.py`` lives, and then myprog.py invokes ``import random``, it will import *your* file rather than the standard library module. That's not usually what you want, so be careful about how you name your python files! 


Syntax for Importing Modules and Functionality
----------------------------------------------

When you see imported modules in a Python program, there are a few variations that have slightly different consequences.

1. The most common is ``import morecode``. That imports everything in morecode.py. To invoke a function f1 that is defined in morecode.py, you would write ``morecode.f1()``. Note that you have to explicitly mention morecode again, to specify that you want the f1 function from morecode namespace. If you just write ``f1()``, python will look for an f1 that was defined in the current file, rather than in morecode.py.

2. You can also give the imported module an alias (a different name, just for when you use it in your program). For example, after executing ``import morecode as mc``, you would invoke ``f1`` as ``mc.f1()``. You have now given the ``morecode`` module the alias ``mc``. Programmers often do this to make code easier to type.

3. A third possibility for importing occurs when you only want to import SOME of the functionality from a module, and you want to make those objects be part of the current module's namespace. For example, you could write ``from morecode import f1``. Then you could invoke f1 without referencing morecode again: ``f1()``.


.. admonition:: Note: Python modules and limitations with activecode

   Throughout the chapters of this book, activecode windows allow you to practice the Python that you are learning.
   We mentioned in the first chapter that programming is normally done using some type of development
   environment and that the
   activecode used here was strictly to help us learn.  It is not the way we write production programs.

   To that end, it is necessary to mention that many of the  modules available in standard Python
   will **not** work in the activecode environment.  In fact, only ``turtle``, ``math``, ``random``, and a couple others have been
   ported at this point.  If you wish to explore any
   additional modules, you will need to run from the native python interpreter on your computer.

**Check your understanding**

.. mchoice:: question4_1_1
   :answer_a: A file containing Python definitions and statements intended for use in other Python programs.
   :answer_b: A separate block of code within a program.
   :answer_c: One line of code in a program.
   :answer_d: A file that contains documentation about functions in Python.
   :feedback_a: A module can be reused in different programs.
   :feedback_b: While a module is separate block of code, it is separate from a program.
   :feedback_c: The call to a feature within a module may be one line of code, but modules are usually multiple lines of code separate from the program.
   :feedback_d: Each module has its own documentation, but the module itself is more than just documentation.
   :correct: a

   In Python a module is:

.. mchoice:: question4_1_2
   :answer_a: Go to the Python Documentation site.
   :answer_b: Look at the import statements of the program you are working with or writing.
   :answer_c: Ask the professor.
   :answer_d: Look in this textbook.
   :feedback_a: The site contains a listing of all the standard modules that are available with Python.
   :feedback_b: The import statements only tell you what modules are currently being used in the program, not how to use them or what they contain.
   :feedback_c: While the professor knows a subset of the modules available in Python, chances are the professor will have to look up the available modules just like you would.
   :feedback_d: This book only explains a portion of the modules available.  For a full listing you should look elsewhere.
   :correct: a

   To find out information on the standard modules available with Python you should:

.. mchoice:: question4_1_3
   :answer_a: True
   :answer_b: False
   :feedback_a: Only turtle, math, and random have been ported to work in activecode at this time.
   :feedback_b: Only turtle, math, and random have been ported to work in activecode at this time.
   :correct: b

   True / False:  All standard Python modules will work in activecode.

