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

1. Using map, create a list assigned to the variable ``greeting_doubled`` that doubles each element in the list ``lst``. 

.. activecode:: ee_listcomp_01
   :tags:AdvancedAccumulation/map.rst
  
   lst = [["hi", "bye"], "hello", "goodbye", [9, 2], 4]
      
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOneA(self):
         self.assertEqual(greeting_doubled, [['hi', 'bye', 'hi', 'bye'], 'hellohello', 'goodbyegoodbye', [9, 2, 9, 2], 8], "Testing that greeting_doubled is assigned to correct values")

   myTests().main()

2. Using filter, filter ``lst`` so that it only contains words containing the letter "o". Assign to variable ``lst2``. Do not hardcode this.

.. activecode:: ee_listcomp_02
   :tags:AdvancedAccumulation/filter.rst

   lst = ["witch", "halloween", "pumpkin", "cat", "candy", "wagon", "moon"]
      
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testTwo(self):
         self.assertEqual(lst2, ['halloween', 'wagon', 'moon'], "Testing that lst is assigned to correct values.")

   myTests().main()

3. Using reduce, join the strings in the list, ``str_lst``, with the symbol "&" and assign the variable ``joined``. Then, combine ``joined`` with the string ``beg`` so that the final string reads "I like apples & peaches & oranges & grapes & pineapples". Save this final string in the variable ``final``. Do not hardcode.

.. activecode:: ee_listcomp_03
   :tags:AdvancedAccumulation/reduce.rst

   str_lst = ["apples ", " peaches ", " oranges ", " grapes ", " pineapples"]
   beg = "I like "

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testThree(self):
         self.assertEqual(joined, "apples & peaches & oranges & grapes & pineapples", "Testing that t1 is assigned to correct value")
      def testThreeB(self):
         self.assertEqual(final, "I like apples & peaches & oranges & grapes & pineapples", "Testing that final is assigned to correct value")

   myTests().main()

4. The for loop below produces a list of numbers greater than 10. Below the given code, use list comprehension to accomplish the same thing. Assign it the the variable ``lst2``. Only one line of code is needed.

.. activecode:: ee_listcomp_04
   :tags:AdvancedAccumulation/listcomp.rst
   
   L = [12, 34, 21, 4, 6, 9, 42]
   lst = []
   for x in L:
       if x > 10:
           lst.append(x)
   print lst

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testFourA(self):
         self.assertEqual(lst2, [12, 34, 21, 42], "Testing that lst2 is assigned to correct values")
      

   myTests().main()

5. Use list comprehension to create a list called ``lst2`` that doubles each element in the list, ``lst``.

.. activecode:: ee_listcomp_05
   :tags:AdvancedAccumulation/listcomp.rst

   lst = [["hi", "bye"], "hello", "goodbye", [9, 2], 4]

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testFiveA(self):
         self.assertEqual(lst2, [['hi', 'bye', 'hi', 'bye'], 'hellohello', 'goodbyegoodbye', [9, 2, 9, 2], 8], "Testing that  lst2 is assigned to correct values")
      
   myTests().main()

6. Below we have provided two lists of numbers, ``L1`` and ``L2``. Using zip and list comprehension, create a new list, ``L3``, that sums the two numbers if the number from ``L1`` is greater than 10 and the number from ``L2`` is less than 5. This can be accomplished in one line of code. 

.. activecode:: ee_listcomp_06
   :tags:AdvancedAccumulation/listcomp.rst,AdvancedAccumulation/zip.rst

   L1 = [1, 5, 2, 16, 32, 3, 54, 8, 100]
   L2 = [1, 3, 10, 2, 42, 2, 3, 4, 3]

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testSix(self):
         self.assertEqual(L3, [18, 57, 103], "Testing that L3 is assigned to correct values")
      
   myTests().main()

7. **Challenge** The nested for loop given takes in a list of lists and combines the elements into a single list. Do the same thing using a list comprehension for the list ``L``. Assign it to the variable ``result2``. 

.. activecode:: ee_listcomp_07
   :tags:AdvancedAccumulation/listcomp.rst

   def onelist(lst):
       result = []
       for each_list in lst:
           for item in each_list:
               result.append(item)
       return result

   L = [["hi", "bye"], ["hello", "goodbye"], ["hola", "adios", "bonjour", "au revoir"]]


   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testSeven(self):
         self.assertEqual(result2, ['hi', 'bye', 'hello', 'goodbye', 'hola', 'adios', 'bonjour', 'au revoir'], "Testing that result2 is assigned to correct values")
      
   myTests().main()
















​


