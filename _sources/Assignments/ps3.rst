:orphan:

Problem Set 3 (due midnight Jan 29)
===================================

..  Copyright (C) Paul Resnick.  Permission is granted to copy, distribute
    and/or modify this document under the terms of the GNU Free Documentation
    License, Version 1.3 or any later version published by the Free Software
    Foundation; with Invariant Sections being Forward, Prefaces, and
    Contributor List, no Front-Cover Texts, and no Back-Cover Texts.  A copy of
    the license is included in the section entitled "GNU Free Documentation
    License".


.. assignment::
  :name: PS3
  :assignment_type: problem_set
  :questions: ps_3_1 5, ps_3_2 8, ps_3_3 5, ps_3_4 8, ps_3_5 8, ps_3_6 8, ps_3_7 8
  :deadline: 2017-01-30 05:00
  :points: 50
  :autograde: unittest

.. activecode:: ps_3_1
     :language: python
     :autograde: unittest
     :hidecode:

     **1.** Write code that uses iteration and conditionals to print out every even number in the list ``several_numbers``.
     ~~~~
     several_numbers = [2, 4, 3, 6, 7, 234352354, 99]

     =====

<<<<<<< HEAD
     from unittest.gui import TestCaseGui
=======

   from unittest.gui import TestCaseGui
>>>>>>> origin/python3

     class myTests(TestCaseGui):

       def test_output(self):
           self.assertIn('for', self.getEditorText(), "Testing your code (Don't worry about actual and expected values).")
           self.assertIn("2\n4\n6\n234352354", self.getOutput(), "Testing output (Don't worry about actual and expected values).")

     myTests().main()

.. activecode:: ps_3_2
     :language: python
     :autograde: unittest
     :hidecode:

<<<<<<< HEAD
     **2.** The code provided does not iterate over the words in the English sentence that's stored in the variable ``sent``. Why not? Write a comment in the box below explaining why not. (Hint: Knowing what you know about how computers and programming languages deal with sequences, what do you need to do to make sure you can iterate over the words in the sentence?)
=======
   **2.** The code provided does not iterate over the words in the English sentence that's stored in the variable ``sent``. Why not? Write a comment in the box below explaining why not. (Hint: Knowing what you know about how computers and programming languages deal with sequences, what do you need to do to make sure you can iterate over the words in the sentence?)
>>>>>>> origin/python3

     Then, write code that assigns a variable word_list to hold a LIST of all the WORDS in the string sent. (It's fine if words include punctuation.)
     ~~~~
     sent = "The magical mystery tour is waiting to take you away."

     for x in sent:
        print x

     =====

<<<<<<< HEAD
     from unittest.gui import TestCaseGui

     class myTests(TestCaseGui):
=======
   class myTests(TestCaseGui):
>>>>>>> origin/python3

        def testOne(self):
           print "No tests for the comment -- we have to read those!\n"
           self.assertEqual(word_list, sent.split(), "Testing that word_list has been set to a list of all the words in sent")

     myTests().main()

.. activecode:: ps_3_3
     :language: python
     :autograde: unittest
     :hidecode:

     **3.** Assign the variable ``mystery`` to a string that will result in every single ``print`` statement executing. DO NOT modify the conditional statement. Only change the initial value of ``mystery``.
     ~~~~
     mystery = 'X?????' # < - change this

     # DO NOT MODIFY THE CODE BELOW
     if mystery[0] == 'X':
      print 'check 1'
     if len(mystery) <= 3:
      print 'check 2'
     if mystery[-1] == 'Y':
      print 'check 3'
      if mystery[1] == 'Z':
        print 'check 4'

     =====

     from unittest.gui import TestCaseGui

     class myTests(TestCaseGui):

       def testOne(self):
        self.assertIn("check 1\ncheck 2\ncheck 3\ncheck 4", self.getOutput(), "Testing output (Don't worry about actual and expected values).")

     myTests().main()

.. activecode:: ps_3_4
<<<<<<< HEAD
     :language: python
     :autograde: unittest
     :hidecode:
=======
   :language: python
   :available_files: about_programming.txt
   :autograde: unittest
   :hidecode:

   **4.** Write code to open the file we've included in this problem set, ``about_programming.txt``, and print out each of the first two lines only. (Don't worry about blank lines appearing.)
>>>>>>> origin/python3

     **4** Write code to count the number of strings in list ``items`` that have the character ``w`` in it. Assign that number to the variable ``acc_num``.

     HINT 1: Use the accumulation pattern!

     HINT 2: the ``in`` operator checks whether a substring is present in a string.
     ~~~~
     items = ["whirring", "calendar", "wry", "glass", "", "llama","tumultuous","owing"]
     =====

     from unittest.gui import TestCaseGui

     class myTests(TestCaseGui):

       def testOne(self):
           self.assertIn('in', self.getEditorText(), "Testing your code (Don't worry about actual and expected values).")
           self.assertEqual(acc_num, 3, "Testing that acc_num has been set to the number of strings that have 'w' in them.")

     myTests().main()

.. activecode:: ps_3_5
     :language: python
     :autograde: unittest
     :hidecode:

     **5** Write code to count the number of words in string ``sentence`` that start with the character ``q``. Assign that number to the variable ``num_start_q``.

     ~~~~
     sentence = "I have a question and inquiry about the quakes that quiver the quail in the quads in the city of Albuquerque."
     =====

     from unittest.gui import TestCaseGui

<<<<<<< HEAD
     class myTests(TestCaseGui):
=======
     def testOne(self):
       self.assertIn('open', self.getEditorText(), "Testing your code (Don't worry about actual and expected values).")
       self.assertEqual(file_lines_num,len(open("about_programming.txt","r").readlines()), "Testing to see that file_lines_num has been set to the number of lines in the file.")
>>>>>>> origin/python3

       def testOne(self):
           self.assertEqual(num_start_q, 5, "Testing that acc_num has been set to the number of words that start with 'q'.")

     myTests().main()

.. activecode:: ps_3_6
     :language: python
     :autograde: unittest
     :hidecode:

     **6** Write code to count the number of occurrences of the lowercase letter ``'i'`` in ``sentence``. Assign that value to the variable ``i_count``.

     ~~~~
     sentence = "This is the University of Michigan."
     =====

     from unittest.gui import TestCaseGui

     class myTests(TestCaseGui):

       def testOne(self):
           self.assertEqual(i_count, 6, "Testing that i_count has been set to the number of i's.")

     myTests().main()

.. activecode:: ps_3_7
<<<<<<< HEAD
     :language: python
     :autograde: unittest
     :hidecode:
=======
   :language: python
   :autograde: unittest
   :hidecode:

   **7.** How many characters are in each element of list ``lp``? Write code to print the length (number of characters) of each element of the list, on a separate line. (Do not write 8+ lines of code to do this. Use a for loop.)

   The output you get should be:

   :: 

     5
     13
     11
     12
     3
     12
     11
     6 

   Then, write code to print out each element of list ``lp`` *only if* the length of the element is an even number. Use iteration (a for loop!).
   ~~~~
   lp = ["hello","arachnophobia","lamplighter","inspirations","ice","amalgamation","programming","Python"]
   ====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

     def test_output(self):
         self.assertIn('for', self.getEditorText(), "Testing your code (Don't worry about actual and expected values).")
     def test_outputB(self):
         self.assertIn("5\n13\n11\n12\n3\n12\n11\n6", self.getOutput(), "Testing output (Don't worry about actual and expected values).")
     def test_outputB(self):
         self.assertIn("inspirations\namalgamation\nPython", self.getOutput(), "Testing output (Don't worry about actual and expected values).")

   myTests().main()

.. activecode:: ps_3_8
   :language: python
   :autograde: unittest
   :hidecode:

   **8.** Write code to count the number of strings in list ``items`` that have the character ``w`` in it. Assign that number to the variable ``acc_num``. 

   HINT 1: Use the accumulation pattern!

   HINT 2: the ``in`` operator checks whether a substring is present in a string.
   ~~~~
   items = ["whirring", "calendar", "wry", "glass", "", "llama","tumultuous","owing"]
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

     def testOne(self):
         self.assertIn('in', self.getEditorText(), "Testing your code (Don't worry about actual and expected values).")
         self.assertEqual(acc_num, 3, "Testing that acc_num has been set to the number of strings that have 'w' in them.")

   myTests().main()

.. activecode:: ps_3_9
   :language: python
   :autograde: unittest
   :hidecode:

   **9.** Below is a dictionary ``diction`` with two key-value pairs inside it. The string ``"python"`` is one of its keys. Using dictionary mechanics, print out the value of the key ``"python"``.
   ~~~~
   diction = {"python":"you are awesome","autumn":100}

   # Write your code here.

   ====
>>>>>>> origin/python3

     **7** Write code to count the number of words that contain the lowercase character ``'i'`` but NOT the lowercase character ``'s'``. Assign that value to the variable ``i_not_s``.

  	HINT 1: Use the ``and`` and ``not`` operators.

     ~~~~
     sentence = "This is the University of Michigan."
     =====

     from unittest.gui import TestCaseGui

     class myTests(TestCaseGui):

       def testOne(self):
           self.assertEqual(i_not_s, 1, "Testing that i_not_s has been set to the number of words that contain an i but not an s.")

<<<<<<< HEAD
     myTests().main()
=======
  Submit your `Demonstrate Your Understanding <https://umich.instructure.com/courses/105657/assignments/131286>`_ for this week on Canvas.
>>>>>>> origin/python3
