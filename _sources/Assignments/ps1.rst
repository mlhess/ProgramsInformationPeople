:orphan:

Problem Set 1 (due midnight Jan 15)
===================================

..  Copyright (C) Paul Resnick.  Permission is granted to copy, distribute
    and/or modify this document under the terms of the GNU Free Documentation
    License, Version 1.3 or any later version published by the Free Software
    Foundation; with Invariant Sections being Forward, Prefaces, and
    Contributor List, no Front-Cover Texts, and no Back-Cover Texts.  A copy of
    the license is included in the section entitled "GNU Free Documentation
    License".


.. assignment for problem set
.. assignment::
  :name: PS1
  :assignment_type: problem_set
  :questions: ps_1_1 5, ps_1_2 5, ps_1_3 5, ps_1_4 5, ps_1_5 5, ps_1_6 10, ps_1_7 10, ps_1_8 5
  :deadline: 2017-01-16 04:00
  :points: 50
  :autograde: unittest


.. highlight:: python
    :linenothreshold: 500


.. _problem_set_1:


**Instructions:** Click "Show Code" to show code entry boxes. Write the code you want to save in the provided boxes, and click **Run** for each one. That will  *run* your code, so you can see the output, if any, and the result of the tests, if there are any. It will also *save* your code. You should run your code each time you want to save it. You can then load the history of the code you have run and saved. The *last* code you have saved for each problem by the deadline is what will be graded.



.. activecode:: ps_1_1
    :language: python
    :autograde: unittest
    :hidecode:

    **1.** The variable ``tpa`` currently has the value ``0``. Assign the variable ``tpa`` the value ``6`` .
    ~~~~
    tpa = 0


    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):

        def testOne(self):
           self.assertEqual(tpa, 6, "Testing that tpa's value is 6.")

    myTests().main()


.. activecode:: ps_1_2
    :language: python
    :autograde: unittest
    :hidecode:

    **2.** Write code to assign the variable ``yb`` to have the same value that variable ``cw`` has. Do not change the first line of code (``cw = "Hello"``). Also, do not "hard code" the result by setting ``yb = "Hello"``. Instead, write code that would work no matter what the current value of ``cw`` is.
    ~~~~
    cw = "Hello"
    yb = 0

    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):

        def testOne(self):
           self.assertEqual(cw, yb, "Testing that yb has the same value as cw")
           self.assertEqual(cw, "Hello", "Testing that cw's value is 'Hello'.")

    myTests().main()


.. activecode:: ps_1_3
    :language: python
    :autograde: unittest
    :hidecode:

    **3.** Write code to print out the type of the variable ``apples_and_oranges``, the type of the variable ``abc``, and the type of the variable ``new_var``. (Use the print command!)
    ~~~~
    apples_and_oranges = """hello, everybody
                               how're you?"""

    abc = 6.75483

    new_var = 824


    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):
        def testOne(self):
            self.assertIn('print', self.getEditorText(), "Testing that 'print' is in the code. (Don't worry about Actual and Expected Values.)")
            self.assertIn('type', self.getOutput(), "Testing output. (Don't worry about Actual and Expected Values.)")

    myTests().main()

.. .. activecode:: ps_1_4
..     :include: addl_functions
..     :language: python
..     :autograde: unittest
..     :hidecode:
..
..     **4.** There is a function we are giving you called ``square``. It takes one integer and returns the square of that integer value. Write code to assign a variable callex ``xyz`` the value ``5*5`` (five squared). Use the square function, rather than just multiplying with ``*``.
..     ~~~~
..     xyz = ""
..
..     =====
..
..     from unittest.gui import TestCaseGui
..
..     class myTests(TestCaseGui):
..
..         def testOne(self):
..             self.assertEqual(type(xyz), type(3), "Checking type of xyz")
..             self.assertEqual(xyz, 25, "Checking if xyz is 25")
..             self.assertIn('square', self.getEditorText(), "Testing that 'square' is in your code. (Don't worry about Actual and Expected Values.)")
..
..     myTests().main()
..
..
.. .. activecode:: ps_1_5
..     :include: addl_functions
..     :language: python
..     :autograde: unittest
..     :hidecode:
..
..     **5.** Write code to assign the return value of the function call ``square(3)`` to the variable ``new_number``.
..     ~~~~
..     # Write your code here:
..
..     =====
..
..     from unittest.gui import TestCaseGui
..
..     class myTests(TestCaseGui):
..
..         def testOne(self):
..             self.assertEqual(new_number, 9, "Testing that new_number's value is 9")
..
..     myTests().main()


.. .. activecode:: ps_1_6
..     :include: addl_functions
..     :language: python
..     :hidecode:
..
..     **6.** Write in a comment what each line of this code does. (You should be very specific! This exercise will train your brain for when you write more complicated code.)
..     ~~~~
..     # Here's an example.
..     xyz = 12 # The variable xyz is being assigned the value 12, which is an integer
..
..     # Now do the same for these!
..     a = 6
..
..     b = a
..
..     # make sure to be very clear and detailed about the following line of code
..     orange = square(b)
..
..     print a
..
..     print b
..
..     print orange
..
..     pear = square
..
..     print pear
..
..     =====
..
..     print "\n\nThere are no tests for this problem. We have to read your comments.\n"


.. .. activecode:: ps_1_7
..     :include: addl_functions
..     :language: python
..     :autograde: unittest
..     :hidecode:
..
..     **7.** There are a couple more functions we're giving you in this problem set. One is a function called ``greeting``, which takes any string and adds ``"Hello, "`` in front of it. (You can see examples in the code.) Another one is a function called ``random_digit``, which returns a value of any random integer between 0 and 9 (inclusive). (You can also see examples in the code.)
..
..     Write code that assigns to the variable ``func_var`` the **function** ``greeting`` (without executing the function).
..
..     Then, write code that assigns to the variable ``new_digit`` the **return value** from executing the function ``random_digit``.
..
..     Then, write code that assigns to the variable ``digit_func`` the **function** ``random_digit`` (without executing the function).
..     ~~~~
..     # For example
..     print greeting("Jackie")
..     print greeting("everybody")
..     print greeting("sdgadgsal")
..
..     # Try running all this code more than once, so you can see how calling the function
..     # random_digit works.
..     print random_digit()
..     print random_digit()
..
..     # Write code that assigns the variables as mentioned in the instructions.
..
..
..     =====
..
..     from unittest.gui import TestCaseGui
..
..     class myTests(TestCaseGui):
..
..         def testOne(self):
..             self.assertEqual(type(func_var), type(greeting), "Testing that func_var is same type as greeting")
..         def testTwo(self):
..             self.assertEqual(type(new_digit), type(1), "Testing that new_digit's value is an integer")
..         def testThree(self):
..             self.assertEqual(type(digit_func), type(random_digit), "Testing that digit_func is same type as random_digit")
..
..     myTests().main()
..
..
.. .. activecode:: ps_1_8
..     :include: addl_functions
..     :language: python
..     :autograde: unittest
..     :hidecode:
..
..     **8.** Now write code that assigns the variable ``newval`` to hold the **return value** of ``greeting("everyone in class")``.
..     ~~~~
..
..
..
..
..     =====
..
..     from unittest.gui import TestCaseGui
..
..     class myTests(TestCaseGui):
..
..         def testOne(self):
..             self.assertEqual(newval, greeting("everyone in class"), "Testing that newval was created correctly.")
..
..     myTests().main()


.. activecode:: ps_1_4
    :language: python
    :hidecode:

    **4.** This code causes an error. Why? Write a comment in the code window to explain.
    ~~~~
    another_variable = "?!"
    b = another_variable()

.. activecode:: ps_1_5
    :language: python
    :autograde: unittest
    :hidecode:

    **5.** Assign the variable ``fl`` the value of the first element of the string value in ``original_str``. Use string indexing to assign the variable ``last_l`` the value of the last element of the string value in ``original_str``. Write code so that will work no matter how long ``original_str``'s value is.
    ~~~~
    original_str = "The quick brown rhino jumped over the extremely lazy fox."

    # assign variables as specified below this line!

    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):

        def testOne(self):
           self.assertEqual(fl, original_str[0], "Testing that fl has been set to first char in original_str")
           self.assertEqual(last_l, original_str[-1], "Testing that last_l has been set to last char in original_str")
           self.assertIn('-1', self.getEditorText(), "Testing that you indexed correctly. (Don't worry about Actual and Expected Values.)")

    myTests().main()


.. activecode:: ps_1_6
    :language: python
    :autograde: unittest
    :hidecode:

    **6.** How long (how many characters) is the string in the variable ``sent``? Write code to assign the length of that string to a variable called ``len_of_sent``.

    How long is the string in the variable ``short_sent``? Write code to assign the value of that string's length to a variable ``short_len``.

    Write code to print out the value of ``short_len`` (and the value of len_of_sent, if you want!) so you can see it.

    Consider (ungraded but important): Why is the length of ``short_sent`` longer than 15 characters?

<<<<<<< HEAD
    Finally, write code to assign the index of the first ``'v'`` in the value of the variable ``sent`` TO a variable called ``index_of_v``. (Hint: we saw a method of the string class that can help with this)
    ~~~~
    sent = """
    He took his vorpal sword in hand:
    Long time the manxome foe he sought
    So rested he by the Tumtum tree,
    And stood awhile in thought.
    - Jabberwocky, Lewis Carroll (1832-1898)"""

    short_sent = """
    So much depends
    on
    """

    # Write your code here.
=======
    print(a)

    print(b)

    print(orange)
>>>>>>> origin/python3


<<<<<<< HEAD
     =====
=======
    print(pear)
>>>>>>> origin/python3

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):

        def testOne(self):
           self.assertEqual(len_of_sent, len(sent), "Testing that len_of_sent has been set to the length of the variable sent.")
        def testTwo(self):
           self.assertEqual(short_len,len(short_sent), "Testing that short_len has been set to the length of the variable short_sent")
        def testThree(self):
           self.assertEqual(index_of_v, sent.find('v'), "Testing that index_of_v has been set to the index of v in the variable sent.")
        def testFour(self):
           self.assertIn('20', self.getOutput(), "Testing that you printed the length of short_sent. (Don't worry about Actual and Expected Values.)")

    myTests().main()
..
..
.. .. activecode:: ps_2_3
..     :language: python
..     :autograde: unittest
..     :hidecode:
..
..     **3.** Assign the value of the third element of ``num_lst`` to a variable called ``third_elem``.
..
..     Assign the value of the sixth element of ``num_lst`` to a variable called ``elem_sixth``.
..
..     Assign the length of ``num_lst`` to a variable called ``num_lst_len``.
..
..     *Consider:* what is the difference between ``mixed_bag[-1]`` and ``mixed_bag[-2]`` (you may want to print out those values or print out information about those values, so you can make sure you know what they are!)?
..
..     Write code to print out the type of the third element of ``mixed_bag``.
..
..     Write code to assign the **type of the fifth element of** ``mixed_bag`` to a variable called ``fifth_type``.
..
..     Write code to assign the **type of the first element of** ``mixed_bag`` to a variable called ``another_type``.
..
..     **Keep in mind:** All ordinal numbers in *instructions*, like "third" or "fifth" refer to the way HUMANS count. How do you write code to find the right things?
..     ~~~~
..     num_lst = [4,16,25,9,100,12,13]
..     mixed_bag = ["hi", 4,6,8, 92.4, "see ya", "23", 23]
..
..     # Write your code here:
..
..
..     =====
..
..     from unittest.gui import TestCaseGui
..
..     class myTests(TestCaseGui):
..
..         def testOne(self):
..            self.assertEqual(third_elem, num_lst[2], "Testing that third_elem has been set to the third element of num_lst")
..         def testTwo(self):
..            self.assertEqual(elem_sixth, num_lst[5], "Testing that elem_sixth has been set to the sixth element of num_lst")
..         def testThree(self):
..            self.assertEqual(num_lst_len,len(num_lst), "Testing that num_len has been set to the length of num_lst")
..         def testFour(self):
..            self.assertEqual(fifth_type, type(mixed_bag[4]), "Testing that fifth_type has been set to the type of the fifth element in mixed_bag")
..         def testFive(self):
..            self.assertEqual(another_type, type(mixed_bag[0]), "Testing that another_type has been set to the type of the first element of mixed_bag")
..         def testSix(self):
..            self.assertIn('print', self.getEditorText(), "Testing that 'print' is in your code. (Don't worry about Actual and Expected Values.)")
..         def testSeven(self):
..            self.assertIn('int', self.getOutput(), "Testing that you printed the correct element of mixed_bag. (Don't worry about Actual and Expected Values.)")
..
..
..     myTests().main()
..
.. .. activecode:: ps_2_4
..     :include: addl_functions_2
..     :language: python
..     :hidecode:
..
..     **4.** There is a function we are giving you for this problem set that takes two strings as inputs, and returns the length of both of those strings added together, called ``add_lengths``. We are also including the functions from Problem Set 1 called ``random_digit`` and ``square`` in this problem set.
..
..     Now, take a look at the following code and related questions, in this code window.
..     ~~~~
..     new_str = "'Twas brillig"
..
..     y = add_lengths("receipt","receive")
..
..     x = random_digit()
..
..     z = new_str.find('b')
..
..     l = new_str.find("'")
..
..     # notice that this line of code is made up of a lot of different expressions
..     fin_value = square(len(new_str)) + (z - l) + (x * random_digit())
..
..     # DO NOT CHANGE ANY CODE ABOVE THIS LINE
..     # But below here, putting print statements and running the code may help you!
..
..     # The following questions are based on that code. All refer to the types of the
..     #variables and/or expressions after the above code is run.
..
..     #####################
..
..     # Write a comment explaining each of the following, after each question.
..     # Don't forget to press **run** to save!
..
..     # What is square?
..
..     # What type of object does the expression square(len(new_str)) evaluate to?
..
..     # What type is z?
..
..     # What type is l?
..
..     # What type is the expression z-l?
..
..     # What type is x?
..
..     # What is random_digit? How many inputs does it take?
..
..     # What type does the expression x * random_digit() evaluate to?
..
..     # Given all this information, what type will fin_value hold once all this code is run?
..
..     ====
..
..     print "\n\nThere are no tests for this problem"
..
..
..
.. .. activecode:: ps_1_10
..     :language: python
..     :autograde: unittest
..     :hidecode:
..
..     **5.** Write code to assign the number of characters in the string ``rv`` to a variable ``num_chars``. Then write code to assign the number of words in the string ``rv`` to the variable ``num_words``. (Hint: remember how to split strings?)
..     ~~~~
..     rv = """Once upon a midnight dreary, while I pondered, weak and weary,
..         Over many a quaint and curious volume of forgotten lore,
..         While I nodded, nearly napping, suddenly there came a tapping,
..         As of some one gently rapping, rapping at my chamber door.
..         'Tis some visitor, I muttered, tapping at my chamber door;
..         Only this and nothing more."""
..
..     # Write your code here!
..
..     =====
..
..     from unittest.gui import TestCaseGui
..
..     class myTests(TestCaseGui):
..
..         def testOne(self):
..            self.assertEqual(num_chars, len(rv), "Testing that num_chars has been set to the length of rv")
..            self.assertEqual(num_words, len(rv.split()), "Testing that num_words has been set to the number of words in rv")
..
..     myTests().main()
..
..
..
.. **10.** Here's another complicated expression, using the Turtle framework we talked about. Arrange these sentences in the order they are executed in the following code, like you did in an exercise in Chapter 2 of the textbook. (It may help to think about what specifically is happening in the first four lines of code as well.)
..
.. .. sourcecode:: python
..
..      import turtle
..
..      ella = turtle.Turtle()
..      x = "hello class".find("o") - 1
..      ella.speed = 3
..
..
..      ella.move(square(x*ella.speed))
..
.. .. parsonsprob:: ps_1_10
..
..    Order the code fragments in the order in which the Python interpreter would evaluate them, when evaluating that last line of code.
..
..    -----
..    Look up the variable ella and find that it is an instance of a Turtle object
..    =====
..    Look up the attribute move of the Turtle ella and find that it's a method object
..    =====
..    Look up the function square
..    =====
..    Look up the value of the variable x and find that it is an integer
..    =====
..    Look up the value of the attribute speed of the instance ella and find that it is an integer
..    =====
..    Evaluate the expression x * ella.speed to one integer
..    =====
..    Call the function square on an integer value
..    =====
..    Call the method .move of the Turtle ella on its input integer
..
..
.. .. activecode:: ps_1_11
..     :language: python
..
..     **11.** Write a program that uses the turtle module to draw something interesting. It doesn't have to be complicated, but draw something different than we did in the textbook or in class. (Optional but encouraged: post a screenshot of the artistic outcome to the Facebook group, or a short video of the drawing as it is created.) (Hint: if you are drawing something complicated, it could get tedious to watch it draw over and over. Try setting ``.speed(10)`` for the turtle to draw fast, or ``.speed(0)`` for it to draw super fast with no animation.)
..     ~~~~
..     import turtle
..
..
.. .. external:: ps1_dyu
..
..     **12.** Complete the `Demonstrate Your Understanding <https://umich.instructure.com/courses/105657/assignments/131293>`_ for this week.
..
..
.. That's the end of the problem set. In the hidden code below, you will find the definitions of functions square, random_digit, and greeting that were used elsewhere in the problem set. They're hidden because you don't yet need to understand how function definitions work. But if you want a preview, feel free to click on Show/hide code.
..
.. .. activecode:: addl_functions
..     :nopre:
..     :hidecode:
..
..     def square(num):
..         return num**2
..
..     def greeting(st):
..         st = str(st) # just in case
..         return "Hello, " + st
..
..     def random_digit():
..         import random
..         return random.choice([0,1,2,3,4,5,6,7,8,9])
..

.. activecode:: ps_1_7
    :language: python
    :autograde: unittest
    :hidecode:

    **7.** Assign the value of the third element of ``num_lst`` to a variable called ``third_elem``.

    Assign the value of the sixth element of ``num_lst`` to a variable called ``elem_sixth``.

    Assign the length of ``num_lst`` to a variable called ``num_lst_len``.

    *Consider:* what is the difference between ``mixed_bag[-1]`` and ``mixed_bag[-2]`` (you may want to print out those values or print out information about those values, so you can make sure you know what they are!)?

    Write code to print out the **type** of the third element of ``mixed_bag``.

    Write code to assign the **type** of the fifth element of ``mixed_bag`` to a variable called ``fifth_type``.

    Write code to assign the **type** of the first element of ``mixed_bag`` to a variable called ``another_type``.

    **Keep in mind:** All ordinal numbers in *instructions*, like "third" or "fifth" refer to the way HUMANS count. How do you write code to find the right things?
    ~~~~
<<<<<<< HEAD
    num_lst = [4,16,25,9,100,12,13]
    mixed_bag = ["hi", 4,6,8, 92.4, "see ya", "23", 23]
=======
    # For example
    print greeting("Jackie")
    print greeting("everybody")
    print greeting("sdgadgsal")

    # Try running all this code more than once, so you can see how calling the function
    # random_digit works.
    print random_digit()
    print random_digit()
>>>>>>> origin/python3

    # Write your code here:


    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):

        def testOne(self):
<<<<<<< HEAD
           self.assertEqual(third_elem, num_lst[2], "Testing that third_elem has been set to the third element of num_lst")
=======
            self.assertEqual(type(func_var), type(greeting), "Testing that func_var is same type as greeting")
>>>>>>> origin/python3
        def testTwo(self):
           self.assertEqual(elem_sixth, num_lst[5], "Testing that elem_sixth has been set to the sixth element of num_lst")
        def testThree(self):
           self.assertEqual(num_lst_len,len(num_lst), "Testing that num_len has been set to the length of num_lst")
        def testFour(self):
           self.assertEqual(fifth_type, type(mixed_bag[4]), "Testing that fifth_type has been set to the type of the fifth element in mixed_bag")
        def testFive(self):
           self.assertEqual(another_type, type(mixed_bag[0]), "Testing that another_type has been set to the type of the first element of mixed_bag")
        def testSix(self):
           self.assertIn('print', self.getEditorText(), "Testing that 'print' is in your code. (Don't worry about Actual and Expected Values.)")
        def testSeven(self):
           self.assertIn('int', self.getOutput(), "Testing that you printed the correct element of mixed_bag. (Don't worry about Actual and Expected Values.)")


    myTests().main()

.. .. activecode:: ps_1_8
..     :include: addl_functions_2
..     :language: python
..     :hidecode:
..
..     **8.** There is a function we are giving you for this problem set that takes two strings as inputs, and returns the length of both of those strings added together, called ``add_lengths``. We are also including the functions from Problem Set 1 called ``random_digit`` and ``square`` in this problem set.
..
..     Now, take a look at the following code and related questions, in this code window.
..     ~~~~
..     new_str = "'Twas brillig"
..
..     y = add_lengths("receipt","receive")
..
..     x = random_digit()
..
..     z = new_str.find('b')
..
..     l = new_str.find("'")
..
..     # notice that this line of code is made up of a lot of different expressions
..     fin_value = square(len(new_str)) + (z - l) + (x * random_digit())
..
..     # DO NOT CHANGE ANY CODE ABOVE THIS LINE
..     # But below here, putting print statements and running the code may help you!
..
..     # The following questions are based on that code. All refer to the types of the
..     #variables and/or expressions after the above code is run.
..
..     #####################
..
..     # Write a comment explaining each of the following, after each question.
..     # Don't forget to press **run** to save!
..
..     # What is square?
..
..     # What type of object does the expression square(len(new_str)) evaluate to?
..
..     # What type is z?
..
..     # What type is l?
..
..     # What type is the expression z-l?
..
..     # What type is x?
..
..     # What is random_digit? How many inputs does it take?
..
..     # What type does the expression x * random_digit() evaluate to?
..
..     # Given all this information, what type will fin_value hold once all this code is run?
..
..     ====
..
..     print "\n\nThere are no tests for this problem"
..

.. activecode:: ps_1_8
    :language: python
    :autograde: unittest
    :hidecode:

    **8.** Write code to assign the number of characters in the string ``rv`` to a variable ``num_chars``. Then write code to assign the number of words in the string ``rv`` to the variable ``num_words``. (Hint: remember how to split strings?)
    ~~~~
    rv = """Once upon a midnight dreary, while I pondered, weak and weary,
        Over many a quaint and curious volume of forgotten lore,
        While I nodded, nearly napping, suddenly there came a tapping,
        As of some one gently rapping, rapping at my chamber door.
        'Tis some visitor, I muttered, tapping at my chamber door;
        Only this and nothing more."""

<<<<<<< HEAD
    # Write your code here!

    =====

=======
>>>>>>> origin/python3
    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):

        def testOne(self):
           self.assertEqual(num_chars, len(rv), "Testing that num_chars has been set to the length of rv")
           self.assertEqual(num_words, len(rv.split()), "Testing that num_words has been set to the number of words in rv")

    myTests().main()
