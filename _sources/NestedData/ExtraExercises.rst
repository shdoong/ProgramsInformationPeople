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

1. The variable ``nested`` contains a nested list. Assign the 3rd element of the second list to the variable ``output`` using indexing. 

.. activecode:: ee_nested_data_01
   :tags:NestedData/ListswithComplexItems.rst

   nested = [['dog', 'cat', 'horse'], ['frog', 'turtle', 'snake', 'gecko'], ['hamster', 'gerbil', 'rat', 'ferret']]
      
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(output, "snake", "Testing that output is assigned to correct value")

   myTests().main()

2. Below, a list of lists is provided. Use in and not in tests to create variables with Boolean values. See comments for further instructions.

.. activecode:: ee_nested_data_02
   :tags:NestedData/ListswithComplexItems.rst

   lst = [['apple', 'orange', 'banana'], [5, 6, 7, 8, 9.9, 10], ['green', 'yellow', 'purple', 'red']]

   #Test to see if 'yellow' is in the third list of lst. Save to variable ``yellow``


   #Test to see if 4 is in the second list of lst. Save to variable ``four``


   #Test to see if 'orange' is in the first element of lst. Save to variable ``orange``
      
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testTwo(self):
         self.assertEqual(yellow, True, "Testing that yellow is assigned to correct value")
      def testTwoB(self):
         self.assertEqual(four, False, "Testing that four is assigned to correct value")
      def testTwoC(self):
         self.assertEqual(orange, True, "Testing that orange is assigned to correct value")

   myTests().main()

3. The variable ``nested_d`` contains a nested dictionary with the gold medal counts for the top four countries in the past three Olympics. Assign the value of Great Britain's gold medal count from the London Olympics to the variable ``london_gold``. 

.. activecode:: ee_nested_data_03
   :tags:NestedData/NestedDictionaries.rst

   nested_d = {'Beijing':{'China':51, 'USA':36, 'Russia':22, 'Great Britain':19}, 'London':{'USA':46, 'China':38, 'Great Britain':29, 'Russia':22}, 'Rio':{'USA':35, 'Great Britain':22, 'China':20, 'Germany':13}}
      
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(london_gold, 29, "Testing that london_gold is assigned to correct value")

   myTests().main()

4. Given the same list, ``nested_d``, save the medal count for the USA from all three Olympics in the dictionary to the list ``US_count``.  

.. activecode:: ee_nested_data_04
   :tags:NestedData/NestedIteration.rst
      
   nested_d = {'Beijing':{'China':51, 'USA':36, 'Russia':22, 'Great Britain':19}, 'London':{'USA':46, 'China':38, 'Great Britain':29, 'Russia':22}, 'Rio':{'USA':35, 'Great Britain':22, 'China':20, 'Germany':13}}

   US_count = []
      

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testFour(self):
         self.assertEqual(sorted(US_count), [35, 36, 46], "Testing that US_count is assigned to correct values.")

   myTests().main()

5. Given below is a list of lists of athletes. Create a list, ``t``, that saves the only the athlete's name if it contains the letter "t". If it does not contain the letter "t", save the athlete name into lst ``other``. 

.. activecode:: ee_nested_data_05
   :tags:NestedData/ListswithComplexItems.rst

   athletes = [['Phelps', 'Lochte', 'Schooling', 'Ledecky', 'Franklin'], ['Felix', 'Bolt', 'Gardner', 'Eaton'], ['Biles', 'Douglas', 'Hamm', 'Raisman', 'Mikulak', 'Dalton']]

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testFive(self):
         self.assertEqual(t, ['Lochte', 'Bolt', 'Eaton', 'Dalton'], "Testing that t is assigned to correct values.")
      def testFiveA(self):
         self.assertEqual(other, ['Phelps', 'Schooling', 'Ledecky', 'Franklin', 'Felix', 'Gardner', 'Biles', 'Douglas', 'Hamm', 'Raisman', 'Mikulak'], "Testing that other is assigned to correct values.")

   myTests().main()

6. **Challenge** The nested dictionary, ``pokemon``, shows the number of various Pokemon that each person has caught while playing Pokemon Go. Find the total number of rattatas, dittos, and pidgeys caught and assign to the variables ``r``, ``d``, and ``p`` respectively. Do not hardcode. Note: Be aware that not every trainer has caught a ditto. 

.. activecode:: ee_nested_data_06
   :tags:NestedData/NestedDictionaries.rst
      
   pokemon = {'Trainer1':{'normal': {'rattatas':15, 'eevees': 2, 'ditto':1}, 'water': {'magikarps':3}, 'flying': {'zubats':8, 'pidgey': 12}}, 'Trainer2':{'normal': {'rattatas':25, 'eevees': 1}, 'water': {'magikarps':7}, 'flying': {'zubats':3, 'pidgey': 15}}, 'Trainer3':{'normal': {'rattatas':10, 'eevees': 3, 'ditto':2}, 'water': {'magikarps':2}, 'flying': {'zubats':3, 'pidgey': 20}}, 'Trainer4':{'normal': {'rattatas':17, 'eevees': 1}, 'water': {'magikarps':9}, 'flying': {'zubats':12, 'pidgey': 14}}}

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testSix(self):
         self.assertEqual(r, 67, "Testing that r is assigned to correct value.")
      def testSixB(self):
         self.assertEqual(d, 3, "Testing that d is assigned to correct value.")
      def testSixC(self):
         self.assertEqual(p, 61, "Testing that p is assigned to correct value.")
     
   myTests().main()














​


