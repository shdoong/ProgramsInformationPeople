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

1. Create a list with numbers 0 through 52 and assign to the variable ``numbers``. Do not hardcode.

.. activecode:: ee_ch10_01
      
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(numbers, [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33, 34, 35, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50, 51, 52], "Testing that numbers is assigned to correct values.")

   myTests().main()

2. Append each character in string ``str1`` to a list. Assign this list to ``chars``. 

.. activecode:: ee_ch10_02

   str1 = "I love python"
      
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testTwo(self):
         self.assertEqual(chars, ['I', ' ', 'l', 'o', 'v', 'e', ' ', 'p', 'y', 't', 'h', 'o', 'n'], "Testing that characters is assigned to correct values.")

   myTests().main()

3. Create an empty string and assign to ``output``. Using range, for each item in range, add the letter "a" so once you are done, ``output`` should have 35 a's.

.. activecode:: ee_ch10_03
      
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testThree(self):
         self.assertEqual(output, "aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa", "Testing that output is assigned to correct values.")

   myTests().main()

4. Given the list of numbers, ``numbs``, create a new list of those same numbers increased by 5. Assign this new list to ``newlist``. 

.. activecode:: ee_ch10_04
      
   numbs = [5, 10, 15, 20, 25]

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testFour(self):
         self.assertEqual(newlist, [10, 15, 20, 25, 30], "Testing that newlist is assigned to correct values.")

   myTests().main()

5. **Challenge** Now do ths same as above, but do not create a new list. Write over the list ``numbs``. 

.. activecode:: ee_ch10_05
      
   numbs = [5, 10, 15, 20, 25]

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testFive(self):
         self.assertEqual(numbs, [10, 15, 20, 25, 30], "Testing that newlist is assigned to correct values.")

   myTests().main()

6. For each verb in the list ``verbs``, add -ing ending. Save this new list in ``ing``.

.. activecode:: ee_ch10_06
      
   verbs = ["kayak", "cry", "walk", "eat", "drink", "fly"]

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testSix(self):
         self.assertEqual(ing, ['kayaking', 'crying', 'walking', 'eating', 'drinking', 'flying'], "Testing that newlist is assigned to correct values.")

   myTests().main()

7. **Challenge** Do the same as above but do not create a new list. Write over ``verbs``. 

.. activecode:: ee_ch10_07
      
   verbs = ["kayak", "cry", "walk", "eat", "drink", "fly"]

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testSeven(self):
         self.assertEqual(verbs, ['kayaking', 'crying', 'walking', 'eating', 'drinking', 'flying'], "Testing that verbs is assigned to correct values.")

   myTests().main()

8. Count the number of characters in string ``str1``. Do not use len. Save the number in ``numbs``.

.. activecode:: ee_ch10_08
      
   str1 = "I like nonsense, it wakes up the brain cells. Fantasy is a necessary ingredient in living."

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testEight(self):
         self.assertEqual(numbs, 90, "Testing that numbs is assigned to correct values.")

   myTests().main()

9. Create a list of numbers 0 through 40. Save this list in ``numbers``. Then, add these numbers together and save the sum in variable ``sum1``. 

.. activecode:: ee_ch10_09
      
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testNineA(self):
         self.assertEqual(numbers, [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33, 34, 35, 36, 37, 38, 39, 40], "Testing that numbs is assigned to correct values.")

      def testNineB(self):
         self.assertEqual(sum1, 820, "Testing that numbs is assigned to correct values.")

   myTests().main()














​


