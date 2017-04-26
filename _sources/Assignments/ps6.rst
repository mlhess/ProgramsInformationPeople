:orphan:

Problem Set 6 (due midnight Feb 26)
===================================

Note: This will be the last problem you submit through the textbook! From now on, you will submit your problem sets as files through Canvas.

..  Copyright (C) Paul Resnick.  Permission is granted to copy, distribute
    and/or modify this document under the terms of the GNU Free Documentation
    License, Version 1.3 or any later version published by the Free Software
    Foundation; with Invariant Sections being Forward, Prefaces, and
    Contributor List, no Front-Cover Texts, and no Back-Cover Texts.  A copy of
    the license is included in the section entitled "GNU Free Documentation
    License".


.. assignment::
    :name: PS6
    :assignment_type: problem_set
    :questions: ps_6_1 5, ps_6_2 5, ps_6_3 5, ps_6_4 5, ps_6_5 5, ps_6_6 5, ps_6_7 5, ps_6_8 5, ps_6_9 5, ps_6_10 5
    :deadline: 2017-02-27 05:00
    :points: 50
    :autograde: unittest

.. activecode:: ps_6_1
    :language: python
    :autograde: unittest
    :hidecode:

    **1.** Write code to sort the list ``fall_list`` in reverse alphabetical order. Assign the result of the sorted list to the variable ``sorted_fall_list``.

    ~~~~
    fall_list = ["leaves","apples","autumn","bicycles","pumpkin","squash","excellent"]



    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):
        def testOne(self):
            self.assertEqual(sorted_fall_list, ['squash', 'pumpkin', 'leaves', 'excellent', 'bicycles', 'autumn', 'apples'], "sorted_fall_list is not accurately sorted")
    myTests().main()

.. activecode:: ps_6_2
    :language: python
    :autograde: unittest
    :hidecode:

    **2.** First, write code to sort the list ``food_amounts`` by the key ``sugar_grams``, from lowest to highest. Assign that sorted list to the variable ``sorted_sugar``. Next, write code to sort the list ``food_amounts`` by the value of the key ``'carbohydrate'`` minus the value of the key ``'fiber'`` in each one, from lowest difference to highest. Assign this sorted list to a variable ``raw_carb_sort``.

    ~~~~
    food_amounts = [{"sugar_grams":245,"carbohydrate":83,"fiber":67},{"carbohydrate":74,"sugar_grams":52,"fiber":26},{"fiber":47,"carbohydrate":93,"sugar_grams":6}]



    =====

<<<<<<< HEAD
    from unittest.gui import TestCaseGui
=======
      def testCode(self):
         print("\n----The following tests are to ensure that you are not hard-coding the values.\n")
         self.assertNotIn("Hello, SI106!!!", self.getEditorText(), "Testing to see if you've put Hello, SI106!!! in your code to hard-code.")
         self.assertNotIn("Hello, world!!!", self.getEditorText(), "Testing to see if you've put Hello, world!!! in your code to hard-code.")
         self.assertNotIn("Hey, everybody!", self.getEditorText(), "Testing code. (Don't worry about actual and expected values)")
         self.assertIn("print", self.getEditorText(), "Testing to see if you've put Hey, everybody! in your code to hard-code.")
      def testOutput(self):
         self.assertIn("Hello, SI106!!!", self.getOutput(), "Testing output. (Don't worry about actual and expected values)")
         self.assertIn("Hello, world!!!", self.getOutput(), "Testing output. (Don't worry about actual and expected values)")
         self.assertIn("Hey, everybody!", self.getOutput(), "Testing output. (Don't worry about actual and expected values)")

   myTests().main()
>>>>>>> origin/python3

    class myTests(TestCaseGui):
        def testOne(self):
            self.assertEqual(sorted_sugar,[{'carbohydrate': 93, 'fiber': 47, 'sugar_grams': 6}, {'carbohydrate': 74, 'fiber': 26, 'sugar_grams': 52}, {'carbohydrate': 83, 'fiber': 67, 'sugar_grams': 245}])
            self.assertEqual(raw_carb_sort,[{'carbohydrate': 83, 'fiber': 67, 'sugar_grams': 245}, {'carbohydrate': 93, 'fiber': 47, 'sugar_grams': 6}, {'carbohydrate': 74, 'fiber': 26, 'sugar_grams': 52}])
    myTests().main()

.. activecode:: ps_6_3
    :language: python
    :autograde: unittest
    :hidecode:

    **3.** Define a function ``trimWords`` that accepts one required argument, ``s`` and two optional integer arguments: ``fromStart`` (default: ``1``) and ``fromEnd`` (default: ``1``). ``trimWords`` should return a new string where *every word* of ``s`` removes ``fromStart`` characters from the start of the word and ``fromEnd`` characters from the end of the word. Note that words whose length is *less than or equal to* ``fromStart+fromEnd`` should be filtered out.

    For example: ``trimWords('this is a sentence', fromStart=1, fromEnd=1)`` should yield ``'hi entenc'``

    Hint: Using ``' '.join()`` and a list comprehension, the body of ``trimWords`` could be just one line


    ~~~~


    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):
        def testOne(self):
            self.assertEqual(trimWords('hello my world'), 'ell orl')
            self.assertEqual(trimWords('this is a sentence', fromStart=0, fromEnd=1), 'thi i sentenc')
            self.assertEqual(trimWords('', fromStart=10, fromEnd=10), '')
            self.assertEqual(trimWords('this is a sentence', fromStart=3, fromEnd=2), 'ten')
    myTests().main()

.. activecode:: ps_6_4
    :language: python
    :autograde: unittest
    :hidecode:

    **4.** Write a function ``best_three_words`` that accepts a string and returns a list of the 3 highest-scoring words in a given sentence. You may assume there are no bonuses that double or triple letter values or entire words. The dictionary saved in ``letter_values`` in the body of ``computeScrabbleScore`` contains the Scrabble score information: its keys are letters, and its values are the scores associated with those letters.

    If you have never played Scrabble before, `here is an explanation <https://en.wikipedia.org/wiki/Scrabble>`_ of what it is. (You do not need that information to solve this problem. All you need to know is that each letter is associated with a number of points, and you want to find the ten words that are associated with the largest point totals.)

<<<<<<< HEAD
    HINT: In the textbook section on Accumulating Results from a Dictionary, there is code that computes the scrabble score for the entire text of “A Study in Scarlet”. You may want to adapt that.
=======
   Here are some questions to consider. We won't grade your answers to these questions, but we suggest that you write them in the code as comments. They may help you think through this big nested data structure. You can test your answers using print statements. e.g. ``print(type(fb_data["data"]))``
      
   * What type is the structure saved in the variable ``fb_data``?
   * What type does the expression ``fb_data["data"]`` evaluate to?
   * What about ``fb_data["data"][1]``?
   * What about ``fb_data["data"][0]["from"]``?
   * What about ``fb_data["data"][0]["id"]``?
>>>>>>> origin/python3


    ~~~~
    def computeScrabbleScore(word):
        # fill this in
        letter_values = {'a': 1, 'b': 3, 'c': 3, 'd': 2, 'e': 1, 'f':4, 'g': 2, 'h':4, 'i':1, 'j':8, 'k':5, 'l':1, 'm':3, 'n':1, 'o':1, 'p':3, 'q':10, 'r':1, 's':1, 't':1, 'u':1, 'v':8, 'w':4, 'x':8, 'y':4, 'z':10}

    def best_three_words(s):
        # return the three best words in s (by scrabble score)
        pass


    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):
        def testOne(self):
            self.assertEqual(best_three_words('working with scrabble scores is fun'), ['working', 'scrabble', 'with'])
            self.assertEqual(best_three_words('not enough'), ['enough', 'not'])
            self.assertEqual(best_three_words('zebras are so cool'), ['zebras', 'cool', 'are'])
    myTests().main()

.. activecode:: ps_6_5
    :language: python
    :autograde: unittest
    :hidecode:

    **5.** We have provided a nested list in the variable ``nl``. Use a list comprehension to accumulate a list containing the second (as humans count) element of each sub-list and save it in a variable ``second_elems``.

    ~~~~
    nl = [["nested","data","is"],["really","fun"],[11,["hooray","hooray"],"yay"]]


    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):
        def testOne(self):
            self.assertEqual(second_elems, ['data', 'fun', ['hooray', 'hooray']], "second_elems does not have the correct value")
    myTests().main()

.. activecode:: ps_6_6
    :language: python
    :autograde: unittest
    :hidecode:

    **6.** Define a function ``convert_nums``. The function should accept an integer as input, representing a number of hours. It should return a tuple of that number converted to minutes (* 60), and then that number converted to seconds (* 3600). For example, if ``1`` were input into the function, the return value of that invocation should be the tuple ``60, 3600``.

    ~~~~
    # your definition of convert_nums


    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):
        def testOne(self):
            self.assertEqual(convert_nums(1),(60,3600),"incorrect output of function with input 1")
            self.assertEqual(convert_nums(50),(60*50,3600*50), "incorrect output of function with input 50")
            self.assertEqual(convert_nums(0), (0,0), "incorrect output of function with input 0")
    myTests().main()

.. activecode:: ps_6_7
    :language: python
    :autograde: unittest
    :hidecode:

    **7.** Define a function ``sort_nested_lists`` that accepts as input a list of lists of integers, e.g. ``[[2,3],[45,100,2],[536],[103,2,8]]``. It should return a sorted version of that list, sorted by the sum of the integers in each sub-list. For example, if that list were the function's input, the return value should be ``[[2,3],[103,2,8],[45,100,2],[536]]``.

<<<<<<< HEAD
    **Suggestion:** It's a good idea to come up with some sample "test cases" to help yourself work through this, in addition to the tests we have provided in your code file. Come up with sample lists where it's easy to figure out what the correct sorting is, and make invocations to your function using that input, and print out the results. If you get different output than you expect, trace through the process to figure out where it might have gone wrong. Writing out an English plan for this and translating it into code bit by bit may also be a good idea.
=======
   ~~~~       
   # Sample calls to this function
   # (Remember, these won't work until you define the function blanked)
   print(blanked("hello", "elj"))
   #should output _ell_
   print(blanked("almost","amsvr"))
   # should output a_m_s_ 
>>>>>>> origin/python3

    ~~~~
    # your definition of sort_nested_lists


    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):
        def testOne(self):
            self.assertEqual(sort_nested_lists([[2,3],[45,100,2],[536],[103,2,8]]),[[2,3],[103,2,8],[45,100,2],[536]],"testing a case of a sorted nested list -- check out your function output")
            self.assertEqual(sort_nested_lists([[1],[50],[6]]),[[1],[6],[50]],"testing a case of a sorted nested list -- check out your function output")
            self.assertEqual(sort_nested_lists([[],[1]]),[[],[1]],"testing a case of a sorted nested list -- check out your function output")
            self.assertEqual(sort_nested_lists([[0],[-4,-5,-7],[-56,4]]),[[-56,4],[-4,-5,-7],[0]],"testing a case of a sorted nested list -- check out your function output")
    myTests().main()

.. activecode:: ps_6_8
    :language: python
    :autograde: unittest
    :hidecode:

    **8.** Define a function ``nthMostCommon`` that accepts a string ``s`` and an integer ``n`` and returns the "nth" most common word. For example, to find the most common word, ``n==1``. To find the second most common word, ``n==2``. If ``n`` is greater than the number of unique words, your function should return ``False``.

    **Hint:** You *don't* want to use max value accumulation here. You *do* want to use sorting.
    **Note:** Remember that sequences in Python are 0-indexed, but this problem is "1-indexed"


    ~~~~
    def nthMostCommon(s, n):
        # your definition of nthMostCommon
        pass


    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):
        def testOne(self):
            self.assertEqual(nthMostCommon('peter piper piper', 2), 'peter')
            self.assertEqual(nthMostCommon('peter piper piper', 1), 'piper')
            self.assertEqual(nthMostCommon('peter piper piper', 3), False)
            self.assertEqual(nthMostCommon('A A A B B C', 3), 'C')
    myTests().main()

.. activecode:: ps_6_9
    :language: python
    :autograde: unittest
    :hidecode:

    **9.** Define a function ``onlyEvenWords`` that accepts a string and **uses list comprehension** and ``join`` to return a new string that only contains words where the length of the word is even. The body of ``onlyEvenWords`` should only be 2 lines or fewer.

<<<<<<< HEAD

    ~~~~
    def onlyEvenWords(s):
        # your definition of onlyEvenWords
        pass
=======
   print(health_prompt(3, 7))
   #this statement should produce the output
   # +++----

   print(health_prompt(0, 4))
   #this statement should produce the output
   # ----
>>>>>>> origin/python3


    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):
        def testOne(self):
            self.assertEqual(onlyEvenWords('this is an example of a sentence'), 'this is an of sentence')
            self.assertEqual(onlyEvenWords('s by sw'), 'by sw')
            self.assertEqual(onlyEvenWords('x'), '')
            self.assertEqual(onlyEvenWords(''), '')
    myTests().main()

.. activecode:: ps_6_10
    :hidecode:

    **10.** Follow the installation instructions below to install and run a terminal and Python. Then, **on Canvas under 106->assignments->Problem Set 06, upload a screenshot of your terminal running two commands:**

    * ``python -V``
    * ``python -c "print('{YOUR NAME}')"``
        * (replace ``{YOUR NAME}`` with your first and last name)

    Example:

    .. image:: Figures/terminal.png


    ~~~~
    #upload on Canvas. no need to do anything here

MacOS, Unbuntu, and GNU/Linux Users
-----------------------------------

You already have a command line. Just find and open the Terminal application

Windows Users
_____________

Install `Git Bash <https://git-for-windows.github.io>`_
(download Git-2XX.exe: try 64 bit if your machine supports it)


Check if you have Python 2
-----------------------------
We use Python 2 in this class.

In your terminal, type:
::
    python -V

and press `<enter>` to see your python version. If you see:
::
    Python 2.7.XX

then you are fine.

If you have Python 3.X, there’s a chance that you also have Python 2 on your machine. Try:
::
    python2 -V

If you don’t have Python 2
--------------------------
Install it from the `official Python distribution site <https://www.python.org>`_

**Yes, uploading this screenshot is a required part of this problem set. The version must be Python 2.x**
You should not need to download any special screen capturing software to take a screenshot.
