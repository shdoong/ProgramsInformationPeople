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

1. Create a tuple called ``olympics`` with four elements: "Beijing", "London", "Rio", "Tokyo".

.. activecode:: ee_Ch09_01
   :tags:Tuples/Tuples.rst
      
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(olympics, ('Beijing', 'London', 'Rio', 'Tokyo'), "Testing that olympics is assigned to correct values")

   myTests().main()

2. The list below, `tuples_lst`, is a list of tuples. Create a list of the second elements of each tuple and assign this list to the variable ``country``. 

.. activecode:: ee_ch09_02
   :tags:Tuples/Tuples.rst

   tuples_lst = [('Beijing', 'China', 2008), ('London', 'England', 2012), ('Rio', 'Brazil', 2016, 'Current'), ('Tokyo', 'Japan', 2020, 'Future')]
      
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testTwo(self):
         self.assertEqual(country, ['China', 'England', 'Brazil', 'Japan'], "Testing that third is assigned to correct values")

   myTests().main()

3. With only one line of code, assign the variables ``city``, ``country``, and ``year`` to the values of the tuple ``olymp``.

.. activecode:: ee_ch09_03
   :tags:Tuples/TupleAssignmentwithunpacking.rst

   olymp = ('Rio', 'Brazil', 2016)
      
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testThree(self):
         self.assertEqual(city, "Rio", "Testing that city is assigned to correct value.")
         self.assertEqual(country, "Brazil", "Testing that country is assigned to correct value.")
         self.assertEqual(year, 2016, "Testing that year is assigned to correct value.")

   myTests().main()

4. Define a function called ``info`` with five parameters: name, gender, age, bday_month, and hometown. The function should then return a tuple with all five parameters in that order. 

.. activecode:: ee_ch09_04
   :tags:Tuples/TuplesasReturnValues.rst

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testFour(self):
         self.assertEqual(info("Sue", "Female", 20, "March", "Ann Arbor"), ("Sue", "Female", 20, "March", "Ann Arbor"), "Testing that info('Sue', 'Female', 20, 'March', 'Ann Arbor') returns('Sue', 'Female', 20, 'March', 'Ann Arbor')")

   myTests().main()

5. Given is the dictionary, ``gold``, which shows the country and the number of gold medals they have earned so far in the 2016 Olympics. Create a list, ``num_medals``, that contains only the number of medals for each country. Note: The .items() method provides a list of tuples. Do not use .keys() method.

.. activecode:: ee_ch09_05
   :tags:Tuples/UnpackingDictionaryItems.rst
      
   gold = {'USA':31, 'Great Britain':19, 'China':19, 'Germany':13, 'Russia':12, 'Japan':10, 'France':8, 'Italy':8}

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testFive(self):
         self.assertEqual(sorted(num_medals), sorted([31, 19, 19, 13, 12, 10, 8, 8]), "Testing that num_medals is assigned to correct values.")

   myTests().main()












​


