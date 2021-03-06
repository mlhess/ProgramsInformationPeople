:orphan:

..  Copyright (C) Jackie Cohen, Paul Resnick.  Permission is granted to copy, distribute
    and/or modify this document under the terms of the GNU Free Documentation
    License, Version 1.3 or any later version published by the Free Software
    Foundation; with Invariant Sections being Forward, Prefaces, and
    Contributor List, no Front-Cover Texts, and no Back-Cover Texts.  A copy of
    the license is included in the section entitled "GNU Free Documentation
    License".



.. highlight:: python
    :linenothreshold: 500


Activities: Week 1
==================

* **As soon as you can / after class 9/5:**

  * Read `the course syllabus <TBALINK.com>`_ 
  * Fill out `this google form assignment <TBALINK.com>`_
  * Check out our Piazza forums on the Canvas site.
  * Read `this piece, called Coding Magic <http://marieflanagan.com/coding-magic/>`_ by Marie LeBlanc Flanagan
  * Watch `this introductory video <https://www.youtube.com/watch?v=rPAg44k6LxA>`_. You'll notice it says "SI 106", which is an undergraduate course similar to this one. That's okay -- pretend it says "506" instead of "106". (We'll provide more from this video series as the semester goes on, for which the same goes -- pretend 106 is 506, unless of course it's a number we're doing math on!)


* **Before class 9/7:**

  * Read :ref:`General Intro <the_way_of_the_program>`, :ref:`Simple Python Data<simple_python_data>`, and :ref:`Objects and Turtle Graphics<turtles_chap>`.
  * Read :ref:`Debugging tips<debugging_chap>` and :ref:`Sequences<sequences_chap>`.
  * There are also some video resources for a bunch of these topics. If you find these helpful, I strongly suggest watching them. Each is a few minutes long: 

    * `Expressions <https://www.youtube.com/watch?v=e-FSJQ02bQk>`_, 
    * `Variables <https://www.youtube.com/watch?v=KcWQG6geZ_0>`_, 
    * `Data Types <https://www.youtube.com/watch?v=54hFgo1OAQA>`_,
    * `Print and Input <https://www.youtube.com/watch?v=j_xlOtEDl_c>`_,
    * `Comments in programming <https://www.youtube.com/watch?v=PdkAvKKptb8>`_,
    * `Sequences <https://www.youtube.com/watch?v=Exm2PL7jks8>`_,
    * `Errors <https://www.youtube.com/watch?v=F8pL4qoaTYU>`_
  * When reading, run the activecodes and answer the multiple choice questions. There may also be exercises at the end of each chapter. These are optional (though trying them is recommended, trying all of those is not required, and getting them correct is also *not required*).
  * We are starting out with a *lot* of material. That is because we are going to speed through a lot of the beginning foundational material, and slow down in a couple weeks -- this stuff is the basis of everything else we'll do, so it is important to absorb and review as we go -- you can always come back to this! When you have questions about this stuff, you should ask them, come to office hours, post on Piazza!


* Go to your discussion section this week, Wednesday or Thursday afternoon

* **By Sunday 9/10 at 11:59 PM:** 

  * Save answers to the exercises in :ref:`Problem Set 1 <problem_set_1>`, including doing the first `Demonstrate Your Understanding <https://umich.instructure.com/courses/172984/assignments/329347>`_ that goes with the readings.

.. _problem_set_1:

Problem Set
-----------

**Instructions:** Write the code you want to save in the provided boxes, and click **Save & Run** for each one. That will  *run* your code, so you can see the output, if any, and the result of the tests, if there are any. It will also *save* your code. You should run your code each time you want to save it. You can then load the history of the code you have run and saved. The *last* code you have saved for each problem by the deadline is what will be graded.



.. activecode:: ps_1_01
    :language: python
    :autograde: unittest

    **1.** Write code to assign the number of characters in the string ``rv`` to a variable ``num_chars``. Then write code to assign the number of words in the string ``rv`` to the variable ``num_words``. (Hint: remember how to split strings?)
    ~~~~
    rv = """Once upon a midnight dreary, while I pondered, weak and weary,
        Over many a quaint and curious volume of forgotten lore,
        While I nodded, nearly napping, suddenly there came a tapping,
        As of some one gently rapping, rapping at my chamber door.
        'Tis some visitor, I muttered, tapping at my chamber door;
        Only this and nothing more."""

    # Write your code here!

    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):

        def testOne(self):
           self.assertEqual(num_chars, len(rv), "Testing that num_chars has been set to the length of rv")
           self.assertEqual(num_words, len(rv.split()), "Testing that num_words has been set to the number of words in rv")

    myTests().main()
   
    
.. activecode:: ps_1_02
    :include: addl_functions
    :language: python
    :autograde: unittest

    **2.** There is a function we are providing in for you in this problem set called ``square``. It takes one integer and returns the square of that integer value. Write code to assign a variable called ``xyz`` the value ``5*5`` (five squared). Use the square function, rather than just multiplying with ``*``.
    ~~~~
    xyz = ""
      
    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):

        def testOne(self):
            self.assertEqual(type(xyz), type(3), "Checking type of xyz")
            self.assertEqual(xyz, 25, "Checking if xyz is 25")
            self.assertIn('square', self.getEditorText(), "Testing that 'square' is in your code. (Don't worry about Actual and Expected Values.)")

    myTests().main()


.. activecode:: ps_1_03
    :include: addl_functions
    :language: python
    :autograde: unittest

    **3.** Write in a comment next to each line of code, what each line of this code does. (You should be very specific! This exercise will train your brain for when you write more complicated code.)
    ~~~~
    # Here's an example.
    xyz = 12 # The variable xyz is being assigned the value 12, which is an integer

    # Now do the same for each of these lines!
    a = 6

    b = a

    # make sure to be very clear and detailed about the following line of code
    orange = square(b)

    print(a)

    print(b)

    print(orange)

    pear = square

    print(pear)


.. activecode:: ps_1_05
    :include: addl_functions
    :language: python
    :autograde: unittest

    **5.** There are a couple functions we're giving you in this problem set. One is a function called ``greeting``, which takes any string and adds ``"Hello, "`` in front of it. (You can see examples in the code.) Another one is a function called ``random_digit``, which returns a value of any random integer between 0 and 9 (inclusive). (You can also see examples in the code.)

    Write code that assigns to the variable ``func_var`` the **function** ``greeting`` (without executing the function). 

    Then, write code that assigns to the variable ``new_digit`` the **return value** from executing the function ``random_digit``.

    Then, write code that assigns to the variable ``digit_func`` the **function** ``random_digit`` (without executing the function).
    ~~~~
    # For example
    print(greeting("Jackie"))
    print(greeting("everybody"))
    print(greeting("sdgadgsal"))
     
    # Try running all this code more than once, so you can see how calling the function
    # random_digit works.
    print(random_digit())
    print(random_digit())

    # Write code that assigns the variables as mentioned in the instructions.


    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):

        def testOne(self): 
           self.assertEqual(type(func_var), type(greeting), "Testing that func_var is same type as greeting")
        def testTwo(self):
           self.assertEqual(type(new_digit), type(1), "Testing that new_digit's value is an integer")
        def testThree(self):
           self.assertEqual(type(digit_func), type(random_digit), "Testing that digit_func is same type as random_digit")

    myTests().main()

.. activecode:: ps_1_06
       :language: python
       :autograde: unittest

       **6.** Write code that uses iteration to print out each element of the list stored in ``excited_words``, BUT print out each element **without** its ending punctuation. You should see:

       ::

           hello
           goodbye
           wonderful
           I love Python

       (Hint: remember string slicing?)
       ~~~~
       excited_words = ["hello!", "goodbye!", "wonderful!", "I love Python?"]

       # Write your code here.
       =====
       from unittest.gui import TestCaseGui

       class myTests(TestCaseGui):

           def test_output(self):
               self.assertIn('for', self.getEditorText(), "Testing your code (Don't worry about actual and expected values).")
               self.assertIn("hello\ngoodbye\nwonderful\nI love Python", self.getOutput(), "Testing output (Don't worry about actual and expected values).")

       myTests().main()

.. activecode:: ps_1_07
    :include: addl_functions
    :language: python

    **7.** There is a function we are giving you for this problem set that takes two strings as inputs, and returns the length of both of those strings added together, called ``add_lengths``. We are also including the functions from Problem Set 1 called ``random_digit`` and ``square`` in this problem set. 

    Now, take a look at the following code and related questions, in this code window.
    ~~~~
    new_str = "'Twas brillig"
     
    y = add_lengths("receipt","receive")
     
    x = random_digit()
     
    z = new_str.find('b')
     
    l = new_str.find("'")
     
    # notice that this line of code is made up of a lot of different expressions
    fin_value = square(len(new_str)) + (z - l) + (x * random_digit())
     
    # DO NOT CHANGE ANY CODE ABOVE THIS LINE
    # But below here, putting print statements and running the code may help you!
     
    # The following questions are based on that code. All refer to the types of the 
    #variables and/or expressions after the above code is run.
     
    #####################   
     
    # Write a comment explaining each of the following, after each question.
    # Don't forget to press **run** to save once you've done this!
     
    # What is square? 
     
    # What type of object does the expression square(len(new_str)) evaluate to?
     
    # What type is z?
     
    # What type is l?
     
    # What type is the expression z-l?
     
    # What type is x?
     
    # What is random_digit? How many inputs does it take?
     
    # What type does the expression x * random_digit() evaluate to?
     
    # Given all this information, what type will fin_value hold once all this code is run?

    ====

    print "==========="
    print "\n\nThere are no tests for this problem"

.. activecode:: ps_1_08
    :language: python
    :autograde: unittest

    **8.** Assign the value of the third element of ``num_lst`` to a variable called ``third_elem``.

    Assign the value of the sixth element of ``num_lst`` to a variable called ``elem_sixth``.

    Assign the length of ``num_lst`` to a variable called ``num_lst_len``.

    *Consider:* what is the difference between ``mixed_bag[-1]`` and ``mixed_bag[-2]`` (you may want to print out those values or print out information about those values, so you can make sure you know what they are!)?

    Write code to print out the type of the third element of ``mixed_bag``.

    Write code to assign the **type of the fifth element of** ``mixed_bag`` to a variable called ``fifth_type``.

    Write code to assign the **type of the first element of** ``mixed_bag`` to a variable called ``another_type``.

    **Keep in mind:** All ordinal numbers in *instructions*, like "third" or "fifth" refer to the way HUMANS count. How do you write code to find the right things?
    ~~~~
    num_lst = [4,16,25,9,100,12,13]
    mixed_bag = ["hi", 4,6,8, 92.4, "see ya", "23", 23]

    # Write your code here:


    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):

        def testOne(self):
           self.assertEqual(third_elem, num_lst[2], "Testing that third_elem has been set to the third element of num_lst")
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


**9.** Here's another complicated expression, using the Turtle framework we talked about. Arrange these sentences in the order they are executed in the following code, like you did in an exercise in Chapter 2 of the textbook. (It may help to think about what specifically is happening in the first four lines of code as well.)

.. sourcecode:: python

     import turtle

     ella = turtle.Turtle()
     x = "hello class".find("o") - 1
     ella.speed = 3


     ella.move(square(x*ella.speed))
  
.. parsonsprob:: ps_1_09

   Order the code fragments in the order in which the Python interpreter would evaluate them, when evaluating that last line of code.

   Not graded for pset points. But important practice!

   -----
   Look up the variable ella and find that it is an instance of a Turtle object
   =====
   Look up the attribute move of the Turtle ella and find that it's a method object
   =====
   Look up the function square
   =====
   Look up the value of the variable x and find that it is an integer
   =====
   Look up the value of the attribute speed of the instance ella and find that it is an integer
   =====
   Evaluate the expression x * ella.speed to one integer
   =====
   Call the function square on an integer value
   =====
   Call the method .move of the Turtle ella on its input integer


.. activecode:: ps_1_10
    :language: python

    **10.** Write a program that uses the turtle module to draw something. It doesn't have to be complicated, but draw something different than we did in the textbook or in class. (Optional but encouraged: post a screenshot of the artistic outcome to Piazza, or a short video of the drawing as it is created.) (Hint: if you are drawing something complicated, it could get tedious to watch it draw over and over. Try setting ``.speed(10)`` for the turtle to draw fast, or ``.speed(0)`` for it to draw super fast with no animation.)
    ~~~~
    import turtle



That's the end of the problem set. In the hidden code below, you will find the definitions of functions that were used elsewhere in the problem set. They're hidden because you don't yet need to understand how function definitions work. But if you want a preview, feel free to click on Show/Hide Code.

.. activecode:: addl_functions
    :nopre:
    :hidecode:

    def square(num):
        return num**2

    def greeting(st):
        st = str(st) # just in case
        return "Hello, " + st

    def random_digit():
        import random
        return random.choice([0,1,2,3,4,5,6,7,8,9])

    def add_lengths(str1, str2):
        return len(str1) + len(str2)