:orphan:

Problem Set 5 (due midnight Feb 12)
===================================

..  Copyright (C) Paul Resnick.  Permission is granted to copy, distribute
    and/or modify this document under the terms of the GNU Free Documentation
    License, Version 1.3 or any later version published by the Free Software
    Foundation; with Invariant Sections being Forward, Prefaces, and
    Contributor List, no Front-Cover Texts, and no Back-Cover Texts.  A copy of
    the license is included in the section entitled "GNU Free Documentation
    License".


.. assignment::
    :name: PS5
    :assignment_type: problem_set
    :questions: ps_5_1 5, ps_5_2 5, ps_5_3 5, ps_5_4 5, ps_5_5 5, ps_5_6 5, ps_5_7 5, ps_5_8 5, ps_5_9 5, ps_5_10 5
    :deadline: 2017-02-13 05:00
    :points: 50
    :autograde: unittest

.. activecode:: ps_5_1
    :language: python
    :autograde: unittest
    :hidecode:

    **1.** Take a look at the code below. The function ``subtract_five`` is supposed to take one integer as input and return that integer minus 5. You'll get an error if you run it as is. Change the function so it works and passes the test!

    ~~~~
    def subtract_five(inp):
        print inp-5

    y = subtract_five(9) - 6

    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):
        def testOne(self):
            self.assertEqual(y, -2, "Testing if y is -2")
    myTests().main()

.. activecode:: ps_5_2
    :language: python
    :autograde: unittest
    :hidecode:

    **2.** Here's another bit of code that generates an error. Think about what's going on with the code below that causes a problem. Why does it cause an error? Write a comment explaining why an error occurs. Then change line 5 to print out the result of an expression that invokes the function ``change_amounts`` and evaluates to ``7``. (So line 5 should be a print statement whose result is printing the integer ``7``.)

    ~~~~
    def change_amounts(yp):
        n = yp - 4
        return n * 7

    print yp

    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):

        def testOne(self):
            self.assertIn("7", self.getOutput(), "Testing output (Don't worry about actual and expected values).")

    myTests().main()

.. activecode:: ps_5_3
    :language: python
    :autograde: unittest
    :hidecode:

    **3.** Define a function called ``change_amounts`` that takes one integer as input. If the input is larger than 10, it should return the input + 5. If the input is smaller than or equal to 10, it should return the input + 2.

    ~~~~
    # We've started you off with the first line...
    def change_amounts(num_here):
        pass # delete this line and put in your own code for the body of the function

    =====

<<<<<<< HEAD
    from unittest.gui import TestCaseGui
=======
   # Some function calls and lines that print out the results
   l = [3,46,6]
   b = [4,"hi",10,"12",12,123,"whoa!"]
   print(list_end_with_string([1,2]))
   print(list_end_with_string(l))
   print(list_end_with_string(b))
>>>>>>> origin/python3

    class myTests(TestCaseGui):

        def testOne(self):
            self.assertEqual(change_amounts(9), 11, "Testing if change_amounts(9) equals 11")
            self.assertEqual(change_amounts(12), 17, "Testing if change_amounts(12) equals 17")

    myTests().main()

.. activecode:: ps_5_4
<<<<<<< HEAD
    :language: python
    :autograde: unittest
    :hidecode:
=======
   :language: python
   :autograde: unittest

   **4.** Define a function ``is_prefix`` that takes two strings as inputs and returns the boolean value ``True`` if the first string is a prefix of the second string, but returns ``False`` otherwise.

   ~~~~   
   # Define your function here.


   # Here's a couple example function calls, printing the return value
   # to show you what it is.
   print(is_prefix("He","Hello")) # should print True
   print(is_prefix("Hello","He")) # should print False
   print(is_prefix("Hi","Hello")) # should print False
   print(is_prefix("lo","Hello")) # should print False
   print(is_prefix("Hel","Hello")) # should print True
   # Remember, these won't work at all until you have defined a function called is_prefix
>>>>>>> origin/python3

    **4.** Write a function named ``words_starting_with`` that accepts a string ``sentence`` as an argument and returns a dictionary whose keys are letters that words in ``sentence`` start with and each value is a list of words starting with that letter. For example:

    ``words_starting_with("this is the correct terminal")`` returns:
    ``{ "t": ["this", "the", "terminal"], "i": ["is"], "c": ["correct"]}``

    ~~~~
    # We've started you off with the first line...
    def words_starting_with(sentence):
        return {} # delete this line and put in your own code for the body of the function

    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):

        def testOne(self):
            R1 = words_starting_with("the quick brown fox jumps over the lazy dog")
            self.assertEqual(R1['q'], ['quick'], "Testing sentence")
            R2 = words_starting_with("")
            self.assertEqual(R2, {}, "Testing empty sentence")
            R3 = words_starting_with("peter piper picked a peck of pickled peppers")
            self.assertEqual(sorted(R3['p']), sorted(['peter', 'piper', 'picked', 'peck', 'pickled', 'peppers']), "Testing example sentence")

    myTests().main()

.. activecode:: ps_5_5
    :language: python
    :autograde: unittest
    :hidecode:

    **5.** Define a function called ``shortest_string`` that takes a list of strings as input and returns the string with the fewest characters in it. (You can assume that one string in any input list will be shorter than the rest.) If the list of strings is empty, your code should return ``False``

    ~~~~

    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):

        def testOne(self):
            self.assertEqual(shortest_string(["ABCDE", "ABC", "ABCDEFGH"]), "ABC", "Testing for example input")
            self.assertEqual(shortest_string([]), False, "Testing for empty input")
            self.assertEqual(shortest_string(["X", "X"*(10**4), "ABCDEFGH"]), "X", "Testing for example input")
            self.assertEqual(shortest_string(["", "X"*(10**4)]), "", "Testing for example input")

    myTests().main()

<<<<<<< HEAD
.. activecode:: ps_5_6
    :language: python
    :autograde: unittest
    :hidecode:
=======
**This is part of your Problem Set 5. It is graded. The other part is writing Python code, in Activecode windows, above.**

For each step of this assignment, please take a screenshot that shows us the command(s) you typed and the results. Save the screenshots as ``step1.jpg`` (or ``.png``), ``step2.jpg``, etc. Upload them all to `the PS 5 Unix Exercises <https://umich.instructure.com/courses/105657/assignments/139051>`_ assignment on Canvas.

----------

.. external:: problem_set_5_unix_1

    1. Open the text editor you installed: Sublime Text. You will be creating and saving 4 different files to your ``Desktop``. 

    **In the first file,** put the following:

    .. sourcecode:: python

        print("hello world")

    Save the file as ``prog1.py``. You've now saved a Python program on your computer!


    **In the second file,** put the following:
>>>>>>> origin/python3

    **6.** Write three assignment statements with function calls to the function ``give_greeting``:

        * one that will return the string ``Hello, SI106!!!``
        * one that will return the string ``Hello, world!!!``
        * and one that will return the string ``Hey, everybody!``

<<<<<<< HEAD
    You must write only the ``print`` command and function invocations of ``give_greeting`` to earn full credit on this problem.
=======
        print(greeting("there"))
>>>>>>> origin/python3

    You can see the function definition in the code below, but that's only so you can understand exactly what the code is doing, so you can choose how to invoke this function. Feel free to make comments to help yourself understand, but otherwise DO NOT change the function definition code! **HINT:** calling the function with different inputs and printing the results, to see what happens, may be helpful! Make sure your final answer prints out all three of the strings listed above.
    ~~~~
    def give_greeting(greet_word="Hello",name="SI106",num_exclam=3):
        final_string = greet_word + ", " + name + "!"*num_exclam
        return final_string

    #### DO NOT change the function definition above this line (OK to add comments)

    # Write your three print statements with function calls below

    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):

        def testCode(self):
            print "\n----The following tests are to ensure that you are not hard-coding the values.\n"
            self.assertNotIn("Hello, SI106!!!", self.getEditorText(), "Testing to see if you've put Hello, SI106!!! in your code to hard-code.")
            self.assertNotIn("Hello, world!!!", self.getEditorText(), "Testing to see if you've put Hello, world!!! in your code to hard-code.")
            self.assertNotIn("Hey, everybody!", self.getEditorText(), "Testing code. (Don't worry about actual and expected values)")
            self.assertIn("print", self.getEditorText(), "Testing to see if you've put Hey, everybody! in your code to hard-code.")
        def testOutput(self):
            self.assertIn("Hello, SI106!!!", self.getOutput(), "Testing output. (Don't worry about actual and expected values)")
            self.assertIn("Hello, world!!!", self.getOutput(), "Testing output. (Don't worry about actual and expected values)")
            self.assertIn("Hey, everybody!", self.getOutput(), "Testing output. (Don't worry about actual and expected values)")

    myTests().main()


.. activecode:: ps_5_7
    :language: python
    :autograde: unittest
    :hidecode:

    **7.** Define a function called ``mult_both`` whose input is two integers, whose default parameter values are the integers 3 and 4. The function's return value should be the two input integers multiplied together.

    ~~~~
    # Write your code here

    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):

        def testCode(self):
            self.assertIn("3", self.getEditorText(), "Testing code. (Don't worry about actual and expected output)")
            self.assertIn("4", self.getEditorText(), "Testing code. (Don't worry about actual and expected output)")

        def testOne(self):
            self.assertEqual(mult_both(), 12, "Testing whether your function works as expected (calling the function mult_both)")
            self.assertEqual(mult_both(5,10), 50, "Testing whether your function works as expected (calling the function mult_both)")

    myTests().main()

.. activecode:: ps_5_8
    :language: python
    :autograde: unittest
    :hidecode:

    **8.** Define a function called ``circle_metrics`` whose input is a float representing a circle's radius, ``r``. Your function should return a tuple where the first item represents the circle's circumference (computed by ``2*pi*r``) and whose second item represents the circle's area (computed by ``pi*r*r``).

    ~~~~
    pi = 3.141592653589793

    def circle_metrics(r):
        # Write your code here
        print r

    circumference, area = circle_metrics(10)

    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):

        def testCode(self):
            c,a = circle_metrics(100)
            self.assertTrue(abs(c-2*pi*100) < 0.0001, "Testing for example input")
            self.assertTrue(abs(a-pi*(100*100)) < 0.0001, "Testing for example input")

    myTests().main()

.. activecode:: ps_5_9
    :language: python
    :autograde: unittest
    :hidecode:

    **9.** Define a function called ``max_and_min`` that returns a tuple containing the maximum and minimum numbers in a list. If the list is empty, your function should return ``(False, False)``
    ~~~~
    def max_and_min(L):
        # Write your code here
        pass
    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):

        def testCode(self):
            self.assertEqual(max_and_min([1,2,3]), (3,1), "Testing for [1,2,3]")
            self.assertEqual(max_and_min([5]), (5,5), "Testing for [5]")
            self.assertEqual(max_and_min([]), (False,False), "Testing for []")

    myTests().main()

.. activecode:: ps_5_10
    :language: python
    :autograde: unittest
    :hidecode:

    **10.** Define a function called ``my_map`` that accepts two arguments: a list ``L`` and a function ``fn``. Your function should "map" ``fn`` onto ``L``, meaning that it should call ``fn`` on each individual element of ``L`` and return a list whose values are ``fn`` called on each element.

    In other words, given a list ``L == [{a},{b},{c}, ... {z}]``, ``my_map(fn,L)`` should return ``[fn({a}), fn({b}), fn({c}), ... fn({z})]``.

    ~~~~
    def my_map(fn, l):
        pass

    print my_map(lambda x: x*2, [1,2,3]) # should be [2,4,6]
    =====

<<<<<<< HEAD
    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):

        def testCode(self):
            self.assertEqual(my_map(lambda x: x, [1,2,3]), [1,2,3], "Example input")
            self.assertEqual(my_map(lambda x: x, []), [], "Example input")
            self.assertEqual(my_map(lambda x: x*5, [10, 20]), [50, 100], "Example input")
            self.assertEqual(my_map(lambda c: c+'x', ["A", "B"]), ["Ax", "Bx"], "Example input")

    myTests().main()
=======
>>>>>>> origin/python3
