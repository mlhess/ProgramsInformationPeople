..  Copyright (C)  Paul Resnick.  Permission is granted to copy, distribute
    and/or modify this document under the terms of the GNU Free Documentation
    License, Version 1.3 or any later version published by the Free Software
    Foundation; with Invariant Sections being Forward, Prefaces, and
    Contributor List, no Front-Cover Texts, and no Back-Cover Texts.  A copy of
    the license is included in the section entitled "GNU Free Documentation
    License".

Exercises
---------


Write equivalent code using map instead of the manual accumulation below

.. activecode:: map_exercise_1

   things = [3, 5, -4, 7]
   
   accum = []
   for thing in things:
       accum.append(thing+1)
   print(accum)
   
Use manual accumulation to define the lengths function below.
 
.. activecode:: map_exercise_2

   def lengths(strings):
       """lengths takes a list of strings as input and returns a list of numbers that are the lengths
       of strings in the input list. Use manual accumulation!"""
       # fill in this function's definition to make the test pass.
   
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(lengths(["Hello", "hi", "bye"]), [5, 2, 3], "Testing whether lengths has been correctly defined.")

   myTests().main()
  
Now define lengths using map instead.
 
.. activecode:: map_exercise_3

   def lengths(strings):
       """lengths takes a list of strings as input and returns a list of numbers that are the lengths
       of strings in the input list. Use map!"""
       # fill in this function's definition to make the test pass.

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(lengths(["Hello", "hi", "bye"]), [5, 2, 3], "Testing whether lengths has been correctly defined.")

   myTests().main()

Now define lengths using a list comprehension instead.
 
.. activecode:: listcomp_exercise_1

   def lengths(strings):
       """lengths takes a list of strings as input and returns a list of numbers that are the lengths
       of strings in the input list. Use a list comprehension!"""
       # fill in this function's definition to make the test pass.
   
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(lengths(["Hello", "hi", "bye"]), [5, 2, 3], "Testing whether lengths has been correctly defined.")

   myTests().main()
   
   
.. activecode:: filter_exercise_1

   things = [3, 5, -4, 7]
   # write code to produce a list of only the positive things, [3, 5, 7], via manual accumulation

.. activecode:: filter_exercise_2

   things = [3, 5, -4, 7]
   # write code to produce a list of only the positive things, [3, 5, 7], using the filter function


.. activecode:: filter_exercise_2a

   things = [3, 5, -4, 7]
   # write code to produce a list of only the positive things, [3, 5, 7], using a list comprehension

# define longwords using manual accumulation

.. activecode:: filter_exercise_3

   def longwords(strings):
       """Return a shorter list of strings containing only the strings with more than four characters. Use manual accumulation."""
       # write your code here

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(longwords(["Hello", "hi", "bye", "wonderful"]), ["Hello", "wonderful"], "Testing whether longwords has been correctly defined.")

   myTests().main()

# define longwords using filter
   
.. activecode:: filter_exercise_4

   def longwords(strings):
       """Return a shorter list of strings containing only the strings with more than four characters. Use the filter function."""
       # write your code here

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(longwords(["Hello", "hi", "bye", "wonderful"]), ["Hello", "wonderful"], "Testing whether longwords has been correctly defined.")

   myTests().main()

# define longwords using a list comprehension

.. activecode:: listcomp_exercise_2

   def longwords(strings):
       """Return a shorter list of strings containing only the strings with more than four characters. Use a list comprehension."""
       # write your code here
              
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(longwords(["Hello", "hi", "bye", "wonderful"]), ["Hello", "wonderful"], "Testing whether longwords has been correctly defined.")

   myTests().main()

 
Now combine lengths with longwords to make a function that returns the lengths of those strings that have at least 4 characters. Try it first with a list comprehension.
 
.. activecode:: listcomp_exercise_3

   def longlengths(strings):
       return None

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(longlengths(["Hello", "hi", "bye", "wonderful"]), [5, 9], "Testing whether longlengths has been correctly defined.")

   myTests().main()

Now try doing it using map and filter.

.. activecode:: listcomp_exercise_4

   def longlengths(strings):
       return None
       
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(longlengths(["Hello", "hi", "bye", "wonderful"]), [5, 9], "Testing whether longlengths has been correctly defined.")

   myTests().main()

Write a function that takes a list of numbers and returns the sum of the squares of all the numbers. First try it using an accumulator pattern.

.. activecode:: reduce_exercise_2
   
   def sumSquares(L):
       return None
   
   nums = [3, 2, 2, -1, 1]
   
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(sumSquares(nums), 19, "Testing whether sumSquares has been correctly defined.")

   myTests().main()

Now, try it using map and sum 

.. activecode:: reduce_exercise_3
   
   def sumSquares(L):
       return None
   
   nums = [3, 2, 2, -1, 1]
   
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(sumSquares(nums), 19, "Testing whether sumSquares has been correctly defined.")

   myTests().main()
  
   
Finally, try doing it using reduce 

.. activecode:: reduce_exercise_4
   
   def sumSquares(L):
       return None
   
   nums = [3, 2, 2, -1, 1]
   
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(sumSquares(nums), 19, "Testing whether sumSquares has been correctly defined.")

   myTests().main()

Use the zip function to take the lists below and turn them into a list of tuples, with all the first items in the first tuple, etc.

.. activecode:: zip_exercise_1

   L1 = [1, 2, 3, 4]
   L2 = [4, 3, 2, 3]
   L3 = [0, 5, 0, 5]
   
   tups = []
   
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(tups, [(1, 4, 0), (2, 3, 5), (3, 2, 0), (4, 3, 5)], "Testing whether tups has been correctly defined.")

   myTests().main()

Use zip and map or a list comprehension to make a list consisting the maximum value for each position.

.. activecode:: zip_exercise_2

   L1 = [1, 2, 3, 4]
   L2 = [4, 3, 2, 3]
   L3 = [0, 5, 0, 5]
   
   maxs = []
   
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(maxs, [4, 5, 3, 5], "Testing whether maxs has been correctly defined.")

   myTests().main()

