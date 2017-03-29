..  Copyright (C)  Brad Miller, David Ranum, Jeffrey Elkner, Peter Wentworth, Allen B. Downey, Chris
    Meyers, and Dario Mitchell.  Permission is granted to copy, distribute
    and/or modify this document under the terms of the GNU Free Documentation
    License, Version 1.3 or any later version published by the Free Software
    Foundation; with Invariant Sections being Forward, Prefaces, and
    Contributor List, no Front-Cover Texts, and no Back-Cover Texts.  A copy of
    the license is included in the section entitled "GNU Free Documentation
    License".

Extra Exercises
===============

1. The module "keyword" determines if a string is a keyword. keyword.iskeyword(s) where s is the string will return either True or False depending on whether or not the string is a Python keyword. Import this module and test to see if the words in list ``test`` are keywords. Save the answers in the list, ``keyword_test``.

.. activecode:: ee_mod_01
   :tags:Inheritance/inheritVarsAndMethods.rst

   test = ["else", "integer", "except", "elif"]
   keyword_test = []

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOneA(self):
         self.assertEqual(keyword_test, [True, False, True, True], "Testing that keyword_test is correct and p1 assigned to correct values")

   myTests().main()


1.1 Import the module called ``keyword`` and use the method called iskeyword that takes one string as input and returns True or False in order to check if certain words are keywords in python. Follow instructions in the comments for specific assignment statements.

.. activecode:: ee_mod_011
   :tags: PythonModules/intro-ModulesandGettingHelp.rst

   # assign to the variable check_one, the value returned by checking the string "and"

   # assign to the variable check_two, the value returned by checking the string "And"

   # assign to the variable check_three, the value returned by checking the string "python"

   # assign to the variable check_four, the value returned by checking the string "in"

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(check_one, True, "Testing that check_one has the correct value.")
      def testTwo(self):
         self.assertEqual(check_two, False, "Testing that check_two has the correct value.")
      def testThree(self):
         self.assertEqual(check_three, False, "Testing that check_three has the correct value.")
      def testFour(self):
         self.assertEqual(check_four, True, "Testing that check_four has the correct value.")

   myTests().main()

1.2 The module called ``keyword`` has an attribute called kwlist that is a list of all Python keywords. Import the ``keyword`` module and assign this list to the variable ``kws``. Then, produce a list of all three-letter keywords and assign it to the variable ``kw3``.

.. activecode:: ee_mod_012
   :tags: PythonModules/intro-ModulesandGettingHelp.rst

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testA(self):
         self.assertEqual(kws, ['and', 'as', 'assert', 'break', 'class', 'continue', 'def', 'del', 'elif', 'else', 'except', 'exec', 'finally', 'for', 'from', 'global', 'if', 'import', 'in', 'is', 'lambda', 'not', 'or', 'pass', 'print', 'raise', 'return', 'try', 'while', 'with', 'yield'], "Testing that kws was created correctly.")
      def testB(self):
         self.assertEqual(kw3, ['and', 'def', 'del', 'for', 'not', 'try'], "Testing that kw3 was created correctly.")

   myTests().main()

2. The module "operator" exports functions that correspond to operators of Python. operator.lt(a,b) is one example that is equivalent to a < b. Another example is operator.neg(a) which returns -a. Import this module and use its functions to find the negative values of ``x`` and ``y`` and compare the values to see if the negative value of y is greater than the negative value of x. Save the response to the variable ``output``.

.. activecode:: ee_mod_02
   :tags:Inheritance/inheritVarsAndMethods.rst,Inheritance/OverrideMethods.rst

   x = 5
   y = 2

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOneA(self):
         self.assertEqual(output, True, "Testing that output is assigned to correct value.")

   myTests().main()

2.1 Provided are two variables, ``a`` and ``c``. Import the module ``operator`` and assign to the variable ``adding``, the result of using the method .add, which takes two numbers as its input. Assign to the variable ``multi`` the result of using the method .mul, which takes two numbers as its input. In both cases, use a and c as their input.

.. activecode:: ee_mod_021
   :tags: PythonModules/intro-ModulesandGettingHelp.rst

   a = 7
   c = 6

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(adding, 13, "Testing that adding has the correct value.")
      def testTwo(self):
         self.assertEqual(multi, 42, "Testing that multi has the correct value.")


   myTests().main()

2.2 The ``operator`` module contains functions that correspond to mathematical operations (such as .add and .sub). Import the ``operator`` module and use the .pow method, which takes two numbers as input and returns the first number raised to the second number, on the variables ``a`` and ``b``. Assign the output to the variable ``c``. Then, use the .div method, which takes two numbers as input and returns the first number divided by the second number, to find ``c`` divided by ``d``. Save this output to the variable ``e``.

.. activecode:: ee_mod_022
   :tags: PythonModules/intro-ModulesandGettingHelp.rst

   a = 5
   b = 8
   d = 125

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testA(self):
         self.assertEqual(c, 390625, "Testing that c has the correct value.")
      def testB(self):
         self.assertEqual(e, 3125, "Testing that e has the correct value.")

   myTests().main()

3. The module "math" provides access to mathematical functions. Import this module and use math.exp(x), which is equivalent to e**x, to populate the list ``exp`` with the value of e to the power of each number in the list ``numbs``.

.. activecode:: ee_mod_03
   :tags:Inheritance/inheritVarsAndMethods.rst,Inheritance/OverrideMethods.rst,Inheritance/InvokingSuperMethods.rst

   numbs = [1, 2, 3, 4, 5]
   exp = []
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOneA(self):
         self.assertEqual(str(exp), str([2.71828182846, 7.38905609893, 20.0855369232, 54.5981500331, 148.413159103]), "Testing that exp is assigned to correct values.")
   myTests().main()

3.1 Import the module ``Math`` and use the .ceil and .floor methods. .ceil takes a float as input and returns the integer above the float, .floor takes a float as input and returns the integer below the float. Assign to the variable ``top`` the return value when using the .ceil method on the float 2.09. Assign to the variable ``bottom`` the return value when using the .floor method on the float 94.999.

.. activecode:: ee_mod_031
   :tags: PythonModules/intro-ModulesandGettingHelp.rst


   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(top, 3, "Testing that top has the correct value.")
      def testTwo(self):
         self.assertEqual(bottom, 94, "Testing that bottom has the correct value.")


   myTests().main()

3.2 The ``math`` module contains mathematical functions, including trigonemetric ones. Import the ``math`` module and use the .sin, .cos, and .tan methods to prove that sin(0.6)/cos(0.6) = tan(0.6). Save sin(0.6) to the variable ``s``, save cos(0.6) to the variable ``c``, and save tan(0.6) to the variable ``t``. Test whether the two values are equal, and save the result - which will be a Boolean - to the variable ``test``.

.. activecode:: ee_mod_032
   :tags: PythonModules/intro-ModulesandGettingHelp.rst

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(test, True, "Testing that test has the correct value.")

   myTests().main()

4. The module "string" provides several constants, such as ascii_letters which returns all lowercase and uppercase letters, and digits, which returns the numbers 0-9. Using these constants and the string module, go through the string, ``str1``, and determine whether each element is a number or a letter. If it is a number, the string "number" should return. If it is a letter, the string "letter" should return. Save your responses in the list, ``resp``.

.. activecode:: ee_mod_04
   :tags:Inheritance/inheritVarsAndMethods.rst,Inheritance/InvokingSuperMethods.rst,Inheritance/OverrideMethods.rst

   str1 = "ab532dcrkjoe579ldije1344kl"
   resp = []

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOneA(self):
         self.assertEqual(resp, ['letter', 'letter', 'number', 'number', 'number', 'letter', 'letter', 'letter', 'letter', 'letter', 'letter', 'letter', 'number', 'number', 'number', 'letter', 'letter', 'letter', 'letter', 'letter', 'number', 'number', 'number', 'number', 'letter', 'letter'], "Testing that resp is assigned to correct values.")

   myTests().main()

4.1 The module ``string`` provides several constants, such as .punctuation and .printable where punctionation returns a string of ASCII charaters that are considered punctionation, and printable returns all ASCII characters that are able to be printed, such as digits, letters, punctuation, and whitespace. For every element in options, if it is in .punctionation or .printable, then add it to a new list called ``small_options``.

.. activecode:: ee_mod_041
   :tags: PythonModules/intro-ModulesandGettingHelp.rst

   options = ["   ", '', '!', 'A', ".", "B", 'b', "a", 'abd', 'abc', ",", ":"]

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(small_options, ['', '!', 'A', '.', 'B', 'b', 'a', 'abc', ',', ':'], "Testing that small_options has the correct list assigned.")


   myTests().main()


4.2 The ``string`` module provides sequences of various types of Python characters. It has an attribute called digits that produces the string '0123456789'. Import the module and assign this string to the variable ``nums``. Below, we have provided a list of characters called ``chars``. Using ``nums`` and ``chars``, produce a list called ``is_num`` that consists of tuples. The first element of each tuple should be the character from ``chars``, and the second element should be a Boolean that reflects whether or not it is a Python digit.

.. activecode:: ee_mod_042
   :tags: PythonModules/intro-ModulesandGettingHelp.rst

   chars = ['h', '1', 'C', 'i', '9', 'True', '3.1', '8', 'F', '4', 'j']

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(is_num, [('h', False), ('1', True), ('C', False), ('i', False), ('9', True), ('True', False), ('3.1', False), ('8', True), ('F', False), ('4', True), ('j', False)], "Testing that is_num was created correctly.")

   myTests().main()
