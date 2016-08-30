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

1. Sort the list, ``lst``, from largest to smallest. Save this new list to the variable ``lst_sorted``.

.. activecode:: ee_sort_01
   :tags:Sort/intro-SortingwithSortandSorted.rst

   lst = [3, 5, 1, 6, 7, 2, 9, -2, 5]
   
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(sorted(lst_sorted), sorted([3, 5, 1, 6, 7, 2, 9, -2, 5]), "Testing that lst_sorted value is assigned to correct values.")

   myTests().main()

2. The dictionary, ``medals``, shows the medal count for six countries during the Rio Olympics. Sort the country names so they appear alphabetically. Save this list to the variable ``alphabetical``.

.. activecode:: ee_sort_02
   :tags:Sort/SortingaDictionary.rst
  
   medals = {'Japan':41, 'Russia':56, 'South Korea':21, 'United States':121, 'Germany':42, 'China':70}
   
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testTwo(self):
         self.assertEqual(alphabetical, sorted(medals.keys()), "Testing that alphabetical value is assigned to correct values.")

   myTests().main()

3. Given the same dictionary, ``medals``, now sort by the medal count. Save the three countries with the highest medal count to the list, ``top_three``. 

.. activecode:: ee_sort_03
   :tags:Sort/Anonymousfunctionswithlambdaexpressions.rst
   
   medals = {'Japan':41, 'Russia':56, 'South Korea':21, 'United States':121, 'Germany':42, 'China':70}
   
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testThree(self):
         self.assertEqual(top_three, sorted(medals, key = lambda x: medals[x], reverse = True)[:3], "Testing that top_three value is assigned to correct values.")

   myTests().main()

4. Create a function called ``last_four`` that takes in an ID number and returns the last four digits. For example, the number 17573005 should return 3005. Then, use this function to sort the list of ids stored in the variable, ``ids``, from lowest to highest. Save this sorted list in the variable, ``sorted_ids``. Hint: Remember that only strings can be indexed, so conversions may be needed.

.. activecode:: ee_sort_04
   :tags:Sort/intro-SortingwithSortandSorted.rst
   
   def last_four(x):




   ids = [17573005, 17572342, 17579000, 17570002, 17572345, 17579329]

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testFour(self):
         self.assertEqual(sorted_ids, sorted(ids, key = last_four), "Testing that sorted_ids is assigned to correct values.")

   myTests().main()

5. Similar to the previous problem, sort the list ``ids`` by the last four digits of each id. Do this using lambda and not using a defined function. Save this sorted list in the variable ``sorted_id``.

.. activecode:: ee_sort_05
   :tags:Sort/Anonymousfunctionswithlambdaexpressions.rst
      
   ids = [17573005, 17572342, 17579000, 17570002, 17572345, 17579329]

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testFive(self):
         self.assertEqual(sorted_id, [17570002, 17572342, 17572345, 17573005, 17579000, 17579329], "Testing that sorted_id is assigned to correct value.")

   myTests().main()

6. **Challenge** Given is the nested dictionary, ``pokemon``, which shows the pokemon each trainer has caught in the early stages of Pokemon Go. Pool this data together in a dictionary assigned to the variable name, ``pooled``. The pooled dictionary should have the total number of rattatas, eevees, etc. Then, sort the compiled dictionary based on the number of pokemon from greatest number to least number to the variable ``sorted_pooled``. Assign the most common pokemon to the variable ``common``. 

.. activecode:: ee_sort_06
   :tags:Sort/SortingaDictionary.rst
      
   pokemon = {'Trainer1':
                    {'rattatas':15, 'eevees': 2, 'ditto':1, 'magikarps':3, 'zubats':8, 'pidgey': 12}, 
               'Trainer2':
                    {'rattatas':25, 'eevees': 1, 'magikarps':7, 'zubats':3, 'pidgey': 15}, 
               'Trainer3':
                    {'rattatas':10, 'eevees': 3, 'ditto':2, 'magikarps':2, 'zubats':3, 'pidgey': 20}, 
               'Trainer4':
                    {'rattatas':17, 'eevees': 1, 'magikarps':9, 'zubats':12, 'pidgey': 14}}

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testSixA(self):
         self.assertEqual(sorted(pooled.items()), [('ditto', 3), ('eevees', 7), ('magikarps', 21), ('pidgey', 61), ('rattatas', 67), ('zubats', 26)], "Testing that pooled contains correct values.")
      def testSixB(self):
         self.assertEqual(common, "rattatas", "Testing that common contains the correct value.")

   myTests().main()

