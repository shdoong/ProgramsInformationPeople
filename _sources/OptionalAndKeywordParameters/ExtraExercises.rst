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

1. Write a function called ``str_mult`` that takes in a required string parameter and an optional integer parameter. The default value for the integer parameter should be 3. The function will return the string multiplied by the integer parameter. 

.. activecode:: ee_Opt_Params_01
   :tags:OptionalAndKeywordParameters/OptionalParameters.rst

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(str_mult("ha"), "hahaha", "Testing that str_mult('ha') returns 'hahaha'")
         self.assertEqual(str_mult("ha", 10), "hahahahahahahahahaha", "Testing that str_mult('ha') returns 'hahahahahahahahahaha'")
         self.assertEqual(str_mult("ha", 0), "", "Testing that str_mult('ha', 0) returns ''")

   myTests().main()

2. The following function, ``greeting``, does not work. Please fix the code so that it runs without error. This only requires one change in the definition of the function.

.. activecode:: ee_Opt_Params_02
   :tags:OptionalAndKeywordParameters/KeywordParameters.rst

   def greeting(greeting = "Hello ", name, excl = "!"):
       return greeting + name + excl
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testTwo(self):
         self.assertEqual(greeting("Bob"), "Hello Bob!", "Testing that greeting('Bob') returns 'Hello Bob!'.")
         self.assertEqual(greeting(""), "Hello !", "Testing that greeting('') return 'Hello !'.")

   myTests().main()


3. Write a function, ``test``, that takes in three parameters: a required integer, an optional boolean whose default value is True, and an optional dictionary whose default value is {2:3, 4:5, 6:8}. If the boolean parameter is True, the function should test to see if the integer is a key in the dictionary. The value of that key should then be returned. If the boolean parameter is False, return the boolean value "False". If the boolean parameter is False, the function should return "None".

.. activecode:: ee_Opt_Params_03
   :tags:OptionalAndKeywordParameters/OptionalParameters.rst
      
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testThree(self):
         self.assertEqual(test(2), 3, "Testing that test(2) returns 3")
         self.assertEqual(test(4, False), False, "Testing that test(4, False) returns False")
         self.assertEqual(test(5, dict1 = {5:4, 2:1}), 4, "Testing that test(5, dict1 = {5:4, 2:1}) returns 4")

   myTests().main()


4. Write a function called ``math``, that takes in three parameters: two numbers and an optional string with the default value "add". If the string value is add, the function should add the two integers. If the string value is "subtract", subtract the second integer from the first integer. If the value is "multiply", multiply the integers and if the value is "divide", divide the first integer by the second integer.

.. activecode:: ee_Opt_Params_04
   :tags:OptionalAndKeywordParameters/OptionalParameters.rst

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testFour(self):
         self.assertEqual(math(1,2), 3, "Testing that math(1,2) returns 3")
         self.assertEqual(math(12,2, "divide"), 6, "Testing that math(12,2, 'divide') returns 6")
         self.assertEqual(math(0, 2, "multiply"), 0, "Testing that math(0, 2, 'multiply') returns 0")
         self.assertEqual(math(0, 7, "subtract"), -7, "Testing that math(0, 7, 'subtract') returns -7")

   myTests().main()

5. Given is below is the function ``test`` from earlier with some modifications. Correctly call the function indicated by the comments below. 

.. activecode:: ee_Opt_Params_05
   :tags:OptionalAndKeywordParameters/KeywordParameters.rst

   def test(int1, dict1, boolean = True):
       if boolean == True:
           for x in dict1:
               if int1 in dict1:
                   return True
               else:
                   return False
       else:
           return "Bool is false"

   #Call the function with the correct parameters so that the function returns "Bool is false". Save the output to the variable ``output``.



   #Call the function with the correct parameters so that the function returns False. Save the output to the variable ``output2``. 


   #Now, call the function with parameters such that output will be True. Save the output to the variable ``output3``. 


   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testFive(self):
         self.assertEqual(output, "Bool is false", "Testing that output is assigned to correct value.")
         self.assertEqual(output2, False, "Testing that output is assigned to correct value.")
         self.assertEqual(output3, True, "Testing that output is assigned to correct value.")

   myTests().main()


