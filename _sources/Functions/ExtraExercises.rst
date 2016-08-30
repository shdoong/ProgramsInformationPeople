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

1. Write a function called ``int_return`` that takes an integer and returns the same integer.

.. activecode:: ee_Functions_01
   :tags:Functions/Returningavaluefromafunction.rst, Functions/FunctionDefinitions.rst

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(int_return(10), 10, "Testing that function int_return(10) returns 10")

   myTests().main()

1.1 Write a function named ``same`` that takes a string as input, and simply returns that string. 

.. activecode:: ee_functions_011
   :tags: Functions/Returningavaluefromafunction.rst, Functions/FunctionDefinitions.rst

   
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(same('hello'), 'hello', "Testing the same function on input 'hello'.")

   myTests().main()

2. Write a function called ``add`` that takes any number as its input and returns that sum with 2 added. 

.. activecode:: ee_Function_02
   :tags:Functions/Returningavaluefromafunction.rst
   
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testTwo(self):
         self.assertEqual(add(-2), 0, "Testing that add(-2) returns 0")
         self.assertEqual(add(6), 8, "Testing that add(6) returns 8")
         self.assertEqual(add(4), 6, "Testing that add(4) returns 6")

   myTests().main()


2.1 Write a function called ``subtract_three`` that takes an integer or any number as input, and returns that number minus three. 

.. activecode:: ee_functions_021
   :tags: Functions/Returningavaluefromafunction.rst

   
   ===== 

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(subtract_three(9), 6, "Testing the subtract_three function on input 9.")
         self.assertEqual(subtract_three(-5), -8, "Testing the subtract_three function on input -5.")

   myTests().main()

3. Write a function called ``change`` that takes any string, adds "Nice to meet you!", and returns that new string.

.. activecode:: ee_Function_03
   :tags:Functions/Returningavaluefromafunction.rst

   
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testThree(self):
         self.assertEqual(change("I'm Bob. "), "I'm Bob. Nice to meet you!", "Tests that change('I'm Bob. '') returns 'I'm Bob. Nice to meet you!'")   
         self.assertEqual(change(""), "Nice to meet you!", "Tests that change() returns 'Nice to meet you!'")

   myTests().main()

3.1 Write a function named ``intro`` that takes a string as input. Given the string "Becky" as input, the function should return: "Hello, my name is Becky and I love SI 106."

.. activecode:: ee_functions_031
   :tags: Functions/Returningavaluefromafunction.rst


   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(intro("Mike"), "Hello, my name is Mike and I love SI 106.", "Testing the intro function on input 'Mike'.")

   myTests().main()

4. Write a function, ``accum``, that takes a list of integers as input and returns the sum of those integers.

.. activecode:: ee_Function_04
   :tags:Functions/Afunctionthataccumulates.rst, Functions/Returningavaluefromafunction.rst

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testFourA(self):
         self.assertEqual(accum([5]), 5, "Tests that accum([5]) returns 5")
         self.assertEqual(accum([]), 0, "Tests that accum([]) returns 0")
         self.assertEqual(accum([2,4,6,8]), 20, "Tests that accum([2,4,6,8]) returns 20")

   myTests().main()

4.1 Write a function named ``total`` that takes a list of integers as input, and returns the total value of all those integers added together. 

.. activecode:: ee_functions_041
   :tags: Functions/Returningavaluefromafunction.rst, Functions/Afunctionthataccumulates.rst



   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(total([1, 2, 3, 4, 5]), 15, "Testing the total function on input [1, 2, 3, 4, 5].")
         self.assertEqual(total([0, 0, 0, 0]), 0, "Testing the total function on input [0, 0, 0, 0].")
         self.assertEqual(total([]), 0, "Testing the total function on input [].")
         self.assertEqual(total([2]), 2, "Testing the total function on input [2].")

   myTests().main() 

5. Write a function, ``length``, that takes in a list as the input. If the length of the list is greater than or equal to 5, return "Longer than 5". If the length is less than 5, return "Less than 5".

.. activecode:: ee_Function_05
   :tags:Functions/Returningavaluefromafunction.rst

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testFive(self):
         self.assertEqual(length([]), "Less than 5", "Tests that length([]) returns 'Less than 5'")
         self.assertEqual(length([2, 2]), "Less than 5", "Tests that length([2, 2]) returns 'Less than 5'")
         self.assertEqual(length([4, 4, 4, 3, 5, 6, 7, 8, 9]), "Longer than 5", "Tests that length([4, 4, 4, 3, 5, 6, 7, 8, 9]) returns 'Less than 5'")
         self.assertEqual(length([1, 1, 1, 1, 1]), "Longer than 5", "Tests that length([1, 1, 1, 1, 1]) returns 'Longer than 5'")

   myTests().main()


5.1 Write a function named ``num_test`` that takes a number as input. If the number is greater than 10, the function should return "Greater than 10." If the number is less than 10, the function should return "Less than 10." If the number is equal to 10, the function should return "Equal to 10."

.. activecode:: ee_functions_051 
   :tags: Functions/Returningavaluefromafunction.rst

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(num_test(5), "Less than 10.", "Testing the num_test function on input 5.")
         self.assertEqual(num_test(0), "Less than 10.", "Testing the num_test function on input 0.")
         self.assertEqual(num_test(12.99), "Greater than 10.", "Testing the num_test function on input 12.99.")
         self.assertEqual(num_test(10.00), "Equal to 10.", "Testing the num_test function on input 10.00.")

   myTests().main() 

6. You will need to write two functions for this problem. The first function, ``divide`` that takes in any number and returns that same number divided by 2. The second function called ``sum`` should take any number, divide it by 2, and add 6. It should return this new number. You should call the ``divide`` function within the ``sum`` function. Do not worry about decimals.

.. activecode:: ee_Function_06
   :tags:Functions/Functionscancallotherfunctions.rst, Functions/Returningavaluefromafunction.rst


   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testSixA(self):
         self.assertEqual(divide(4), 2, "Tests that divide(4) returns 2")
      def testSixB(self):
         self.assertEqual(sum(4), 8, "Tests that sum(4) returns 8")
         self.assertEqual(sum(2), 7, "Tests that sum(2) returns 7")
         self.assertEqual(sum(-6), 3, "Tests that sum(-6) returns 3")
         self.assertEqual(sum(0), 6, "Tests that sum(0) returns 6")

   myTests().main()

6.1 This problem will require you to write two functions. The first function, named ``func1``, should take a number as input, and return that number multiplied by 3. The second function, named ``func2``, should take a number as input, multiply it by 3, and then add 10. You should call on ``func1`` within ``func2`` to accomplish this.

.. activecode:: ee_functions_061
   :tags: Functions/Returningavaluefromafunction.rst, Functions/Functionscancallotherfunctions.rst

   def func1():


   def func2():

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(func1(10), 30, "Testing func1 on input 10.")
         self.assertEqual(func1(0), 0, "Testing func1 on input 0.")
         self.assertEqual(func2(-2), 4, "Testing func2 on input -2.")
         self.assertEqual(func2(0), 10, "Testing func2 on input 0.")

   myTests().main() 

7. **Challenge** Write a function called ``dict_test`` that takes in 2 parameters: a dictionary of strings and a character. The function should go through the dictionary and see if the inputted character is in each key of the dictionary. If so, it should add the values and return the total sum. 

.. activecode:: ee_Function_07
   :tags:Functions/Afunctionthataccumulates.rst, Functions/Returningavaluefromafunction.rst

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testSeven(self):

         self.assertEqual(dict_test({'swimming':10, 'running':15, 'walking':5, 'jogging':10}, 'w'), 15, "Testing that dict_test({'swimming':10, 'running':15, 'walking':5, 'jogging':10}, 'w') returns 15")

         self.assertEqual(dict_test({}, "x"), 0, "Testing that dict_test({}, 'x') returns 0")

         self.assertEqual(dict_test({'cat':4, 'dog':4,'chicken':2, 'snake':0, 'horse':4}, 'g'), 4, "Testing that dict_test({'cat':4, 'dog':4,'chicken':2, 'snake':0, 'horse':4}, 'g') returns 4")


   myTests().main()

8. Write a function named ``add_all`` that takes two parameters. The first parameter should be a list of numbers, and the second should be an integer. The function should return a new list whose elements are all the numbers from the old list with the integer added to them (i.e.: Given the inputs [1, 2, 3], 1, the function should return [2, 3, 4]).

.. activecode:: ee_functions_08
   :tags: Functions/Returningavaluefromafunction.rst

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(add_all([1, 2, 3], 0), [1, 2, 3], "Testing add_all on inputs [1, 2, 3], 0.")
         self.assertEqual(add_all([], 10), [], "Testing add_all on inputs [], 10.")
         self.assertEqual(add_all([5], 7), [12], "Testing add_all on inputs [5], 7.")

   myTests().main() 



      



