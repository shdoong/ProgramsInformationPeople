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

1. Using a while loop, create a list ``numbers`` that contains the numbers 0 through 35. Your while loop should initialize a counter variable to 0. On each iteration, the loop should append the current value of the counter to the list and the counter should increase by 1. The while loop should stop when the counter is greater than 35. 

.. activecode:: ee_07_01
   :tags:IndefiniteIteration/ThewhileStatement.rst

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(numbers, [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33, 34, 35], "Testing that numbers is assigned to correct values")

   myTests().main()


2. Create a while loop that initializes a counter at 0 and will run until the counter reaches 50. If the value of the counter is divisible by 10, append the value to the list, ``tens``.  

.. activecode:: ee_ch07_02
   :tags:IndefiniteIteration/ThewhileStatement.rst

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testTwo(self):
         self.assertEqual(tens, [0, 10, 20, 30, 40, 50], "Testing that tens is assigned to correct value.")

   myTests().main()

2.1 Use a while loop to iterate through the numbers 0 through 35. If a number is divisible by 3, it should be appended to a list called ``three_nums``. 

.. activecode:: ee_ch7_021
   :tags:IndefiniteIteration/ThewhileStatement.rst


   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(three_nums, [0, 3, 6, 9, 12, 15, 18, 21, 24, 27, 30, 33], "Testing that three_nums was created correctly.")

   myTests().main()

3. Write a function, ``sublist``, that takes in a list of numbers as the parameter. In the function, use a while loop to return a sublist of the input list. The sublist should contain the same values of the original list up until it reaches the number 5 (it should not contain the number 5).

.. activecode:: ee_ch07_03
   :tags:IndefiniteIteration/listenerLoop.rst
      
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testThree(self):
         self.assertEqual(sublist([1, 2, 3, 4, 5, 6, 7, 8]), [1, 2, 3, 4], "Testing that sublist([1, 2, 3, 4, 5, 6, 7, 8]) returns [1, 2, 3, 4]")
         self.assertEqual(sublist([5]), [], "Testing that sublist([5]) returns []")
         self.assertEqual(sublist([8, 6, 5]), [8, 6], "Testing that sublist([8, 6, 5]) returns [8, 6]")

   myTests().main()


4. Write a function, ``sublist``, that takes in a list of strings as the parameter. In the function, use a while loop to return a sublist of the input list. The sublist should contain the same values of the original list up until it reaches the string "STOP" (it should not contain the string "STOP").

.. activecode:: ee_ch07_04
   :tags:IndefiniteIteration/listenerLoop.rst

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testFour(self):
         self.assertEqual(sublist(["bob", "joe", "lucy", "STOP", "carol", "james"]), ["bob", "joe", "lucy"], "Testing that sublist(['bob', 'joe', 'lucy', 'STOP', 'carol', 'james']) returns ['bob', 'joe', 'lucy']")
         self.assertEqual(sublist(["STOP"]), [], "Testing that sublist(['STOP']) returns []")
         self.assertEqual(sublist(["jackie", "paul", "STOP"]), ["jackie", "paul"], "Testing that sublist(['jackie', 'paul', 'STOP']) returns ['jackie', 'paul']")

   myTests().main()

5. Below is a for loop that works. Underneath the for loop, rewrite the problem so that it does the same thing, but using a while loop instead of a for loop. Assign the accumulated total in the while loop code to the variable ``sum2``. Once complete, sum2 should equal sum1.

.. activecode:: ee_ch07_05
   :tags:IndefiniteIteration/ThewhileStatement.rst

   sum1 = 0

   lst = [65, 78, 21, 33]

   for x in lst:
       sum1 = sum1 + x

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testFive(self):
         self.assertEqual(sum2, 197, "Testing that sum2 is assigned to correct value.")

   myTests().main()

6. **Challenge** Create a function called ``first_five`` that takes in a list of numbers. In this function, create a sublist of the inputted list by using a while loop that stops when it reaches the number 0. The function should only return a list of the first five numbers of the sublist, regardless of where the while loop stops. i.e. the sublist [1, 1, 2, 3, 4, 3, 2] will only return [1, 1, 2, 3, 4]. For a challenge, do this without using slicing.

.. activecode:: ee_ch07_06
   :tags:IndefiniteIteration/listenerLoop.rst
   
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testSix(self):
         self.assertEqual(first_five([1, 2, 0]), [1,2], "Testing that first_five([1, 2, 0]) returns [1,2]")
         self.assertEqual(first_five([1, 2, 3, 4, 3, 2, 5, 0, 3, 4]), [1, 2, 3, 4, 3], "Testing that first_five([1, 2, 3, 4, 3, 2, 5, 0, 3, 4]) returns [1, 2, 3, 4, 3]")
         self.assertEqual(first_five([0]), [], "Testing that first_five([0]) returns []")

   myTests().main()

