..  Copyright (C)  Brad Miller, David Ranum, Jeffrey Elkner, Peter Wentworth, Allen B. Downey, Chris
    Meyers, and Dario Mitchell.  Permission is granted to copy, distribute
    and/or modify this document under the terms of the GNU Free Documentation
    License, Version 1.3 or any later version published by the Free Software
    Foundation; with Invariant Sections being Forward, Prefaces, and
    Contributor List, no Front-Cover Texts, and no Back-Cover Texts.  A copy of
    the license is included in the section entitled "GNU Free Documentation
    License".

Extra Exercises
=====

1. The module "keyword" determines if a string is a keyword. keyword.iskeyword(s) where s is the string will return either True or False depending on whether or not the string is a Python keyword. Import this module and test to see if the words in list ``test`` are keywords. Save the answers in the list, ``keyword_test``.

.. activecode:: ee_inheritance_01
   :tags:Inheritance/inheritVarsAndMethods.rst

   test = ["else", "integer", "except", "elif"]
   keyword_test = []

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOneA(self):
         self.assertEqual(keyword_test, [True, False, True, True], "Testing that keyword_test is correct and p1 assigned to correct values")
      
   myTests().main()

2. The module "operator" exports functions that correspond to operators of Python. operator.lt(a,b) is one example that is equivalent to a < b. Another example is operator.neg(a) which returns -a. Import this module and use its functions to find the negative values of ``x`` and ``y`` and compare the values to see if the negative value of y is greater than the negative value of x. Save the response to the variable ``output``.

.. activecode:: ee_inheritance_02
   :tags:Inheritance/inheritVarsAndMethods.rst,Inheritance/OverrideMethods.rst

   x = 5
   y = 2

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOneA(self):
         self.assertEqual(output, True, "Testing that output is assigned to correct value.")
  
   myTests().main()

3. The module "math" provides access to mathematical functions. Import this module and use math.exp(x), which is equivalent to e**x, to populate the list ``exp`` with the value of e to the power of each number in the list ``numbs``. 

.. activecode:: ee_inheritance_03
   :tags:Inheritance/inheritVarsAndMethods.rst,Inheritance/OverrideMethods.rst,Inheritance/InvokingSuperMethods.rst

   numb = [1, 2, 3, 4, 5]
   exp = []
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOneA(self):
         self.assertEqual(str(exp), str([2.71828182846, 7.38905609893, 20.0855369232, 54.5981500331, 148.413159103]), "Testing that exp is assigned to correct values.")
   myTests().main()

4. The module "string" provides several constants, such as ascii_letters which returns all lowercase and uppercase letters, and digits, which returns the numbers 0-9. Using these constants and the string module, go through the string, ``str1``, and determine whether each element is a number or a letter. If it is a number, the string "number" should return. If it is a letter, the string "letter" should return. Save your responses in the list, ``resp``.

.. activecode:: ee_inheritance_04
   :tags:Inheritance/inheritVarsAndMethods.rst,Inheritance/InvokingSuperMethods.rst,Inheritance/OverrideMethods.rst

   str1 = "ab532dcrkjoe579ldije1344kl"
   resp = []

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOneA(self):
         self.assertEqual(resp, ['letter', 'letter', 'number', 'number', 'number', 'letter', 'letter', 'letter', 'letter', 'letter', 'letter', 'letter', 'number', 'number', 'number', 'letter', 'letter', 'letter', 'letter', 'letter', 'number', 'number', 'number', 'number', 'letter', 'letter'], "Testing that resp is assigned to correct values.")
     
   myTests().main()

