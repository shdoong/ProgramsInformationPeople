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

1. Write code to assign the string "You can apply to SI!" to ``output`` if "SI 106" is in the list ``courses``. If it is not in ``courses``, assign ``output`` to "Take SI 106!"

.. activecode:: ee_ch11_01
   :tags:Selection/ConditionalExecutionBinarySelection.rst

   courses = ["ENGR 101", "SI 110", "ENG 125", "SI 106", "CHEM 130"]

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(output, "You can apply to SI!", "Testing that output is assigned to correct values")

   myTests().main()

2. Create another variable, ``b``, and assign it the value of 15. Then, test to see if ``b`` is greater than ``a``. If so, then multiply ``a`` by 2. If ``b`` is less than ``a``, nothing should happen. Finally, create variable ``c`` and assign it the value of the sum of ``a`` and ``b``.

.. activecode:: ee_ch11_02
   :tags:Selection/OmittingtheelseClauseUnarySelection.rst

   a = 20
      
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testTwoA(self):
         self.assertEqual(a, 20, "Testing that a is assigned to correct value.")

      def testTwoB(self):
         self.assertEqual(c, 35, "Testing that c is assigned to correct value.")

   myTests().main()

3. Create one conditional to test if "false" is in string ``str1``. If so, assign variable ``output`` to "False. You aren't you?". Otherwise, test if "true" is in string ``str1``. If so, assign variable ``output`` to "True! You are you!". If neither are in ``str1``, assign ``output`` to "Neither true nor false!"

.. activecode:: ee_ch11_03
   :tags:Selection/Chainedconditionals.rst

   str1 = "Today you are you! That is truer than true! There is no one alive who is you-er than you!"
      
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testThree(self):
         self.assertEqual(output, "True! You are you!", "Testing that action is assigned to correct values.")

   myTests().main()

4. **Challenge** For each grade in list ``grades``, if the grade is greater than 90, add "Good job!" to list ``notes``. If less than 90 but greater than 80, add "Keep it up!". If less than 80 but greater than 70, add "Study some more!". If less than 70, add "Try going to office hours!"

.. activecode:: ee_ch11_04
   :tags:Selection/Chainedconditionals.rst
      
   grades = [95, 50, 85, 74, 67]

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testFour(self):
         self.assertEqual(notes, ['Good job!', 'Try going to office hours!', 'Keep it up!', 'Study some more!', 'Try going to office hours!'], "Testing that notes is assigned to correct values.")

   myTests().main()


5. For each word in list ``words``, find the number of characters in the string. If the number of characters in each string is greater than 3, add 1 to the variable "num_words" so that num_words should have the total number of words with less than 3 characters.

.. activecode:: ee_ch11_05
   :tags:Selection/ConditionalExecutionBinarySelection.rst
      
   words = ["water", "chair", "pen", "basket", "hi", "car"]

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testFive(self):
         self.assertEqual(num_words, 3, "Testing that num_words is assigned to correct values.")

   myTests().main()

6. We have created conditionals for you to use. Find an integer value of x that will output "True" and "None".

.. activecode:: ee_ch11_06
  :tags:Selection/Chainedconditionals.rst

   x = 
   output = []

   if x > 63:
      output.append("True")
   elif x > 55:
      output.append("False")
   else: 
      output.append("Neither")

   if x > 67:
      output.append("True")
   else:
      output.append("None")

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testSixA(self):
         self.assertEqual(output, ["True", "None"], "Testing that output is correct.")

      def testSixB(self):
         self.assertEqual(x in [64, 65, 66, 67], True, "Testing that value of x is correct.")

   myTests().main()

.. works for 64-67

7. Create a set of conditionals to determine shipping prices. Usually, it will cost you $7 to ship a large package within your state. In this case, ``location`` would be "domestic", the variable ``cost`` would be set to 7, and ``destination`` would be ``0``. If you continue to ship domestically, the cost of shipping for 1 state away is $11. For 2 states away, the cost is $15. For 3 states away, the cost is $19. If the destination is 4 or more states away, the shipping cost is fixed at $25. If you ship international the variable ``i_dest`` is 0 (within your continent), the cost is $30. Anywhere other than your continent ``i_dest`` would be set to 1 and the cost is $45. 
The variable ``location`` will have either the value "domestic" or "international". If domestic, the variable ``destination`` could have the values 0 (within the state), 1 (1 state away), 2 (2 states away), 3 (3 states away), or 4 and above (4 or more states away). If international, ``i_dest`` will either be 0 (within your continent) or 1 (out of your continent)
Use nested conditionals to help someone determine the shipping cost. Uncomment each set of variables one at a time to test.

.. activecode:: ee_ch11_07

   #Uncomment next two lines to test domestic and 2 states away.
   #location = "domestic"
   #destination = 2

   #Uncomment next two lines to test international and not on your continent.
   #location = "international"
   #i_dest = 1

   #Uncomment next two lines to test domestic and 6 states away.
   #location = "domestic"
   #destination = 6
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testSeven(self):
         if location == "domestic" and destination == 2:
          self.assertEqual(cost, 15, "Testing that cost is assigned to correct value.")

         elif location == "international" and i_dest == 1:
          self.assertEqual(cost, 45, "Testing that cost is assigned to correct value.")

         elif location == "domestic" and destination == 6:
          self.assertEqual(cost, 25, "Testing that cost is assigned to correct value.")

         else:
          print "Test not able to run. Check for specific values."

   myTests().main()

8. **Challenge** In XYZ University, upper level math classes are numbered 300 and up. Upper level English classes are numbered 200 and up. Upper level Psychology classes are 400 and up. Create two lists, ``upper`` and ``lower``. Assign each course in ``classes`` to the correct list, upper or lower. As a hint, remember you can convert strings to different types.

.. activecode:: ee_ch11_08
      
   classes = ["MATH 150", "PSYCH 111", "PSYCH 313", "PSYCH 412", "MATH 300", "MATH 404", "MATH 206", "ENG 100", "ENG 103", "ENG 201", "PSYCH 508", "ENG 220", "ENG 125", "ENG 124"]

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testEightA(self):
         self.assertEqual(upper, ['PSYCH 412', 'MATH 300', 'MATH 404', 'ENG 201', 'PSYCH 508', 'ENG 220'], "Testing that u_math is assigned to correct values.")
      def testEightB(self):
         self.assertEqual(lower, ['MATH 150', 'PSYCH 111', 'PSYCH 313', 'MATH 206', 'ENG 100', 'ENG 103', 'ENG 125', 'ENG 124'], "Testing that l_math is assigned to correct values.")
      

   myTests().main()

9. For each word in ``words``, add '-d' to the end of the word if the word ends in "e" to make it past tense. Otherwise, add '-ed' to make it past tense. Save these past tense words to a list called ``past_tense``.

.. activecode:: ee_ch11_09

   words = ["adopt", "bake", "beam", "confide", "grill", "plant", "time", "wave", "wish"]
      
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testNine(self):
         self.assertEqual(past_tense, ['adopted', 'baked', 'beamed', 'confided', 'grilled', 'planted', 'timed', 'waved', 'wished'], "Testing that past_tense is assigned to correct values.")

   myTests().main()














​


