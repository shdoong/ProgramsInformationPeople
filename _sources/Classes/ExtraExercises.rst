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

1. Create a class called ``inst_var`` that defines two instance variables: ``num1`` and ``num2``. Then, create an instance where num1 is 6 and num2 is 10 and save this instance to the variable ``t``. 

.. activecode:: ee_ch13_01
   :tags:Classes/ImprovingourConstructor.rst

      
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOneA(self):
         self.assertEqual(t.num1, 6, "Testing that t.num1 calls 6")
      def testOneB(self):
         self.assertEqual(t.num2, 10, "Testing that t.num2 calls 10")

   myTests().main()

2. Create a class called ``math_op`` with one instance variable and a method. The instance variable should be ``numb``. The method should be called ``squared`` and return the instance variable squared. Create an instance of this class with an initial number of 8. Assign to the variable ``output`` the value of numb without hardcoding. Call the method two times.

.. activecode:: ee_ch13_02
   :tags:Classes/AddingOtherMethodstoourClass.rst,

      
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(output, 512, "Testing that output returns 64")

   myTests().main()

3. Create a class called ``bank`` that contains two instance variables, ``name`` and ``amt``. Add the instance method that allows you to customize the message returned when you print the instance so that it says "Your account, [name goes here], has [start_amt goes here] dollars." Create an instance of this class with "Bob" as the name and 100 as the amount. Save this to the variable ``t1``.

.. activecode:: ee_ch13_03
   :tags:Classes/AddingOtherMethodstoourClass.rst

   

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(t1.__str__(), "Your account, Bob, has 100 dollars.", "Testing that t1 is assigned to correct value")

   myTests().main()

4. This problem will modify your previously defined class, ``bank``. Add two more instance variables, ``deposits`` and ``withdrawals``.Add two more methods, ``add_deposit`` and ``less_withdrawals``. The add_deposit method should add the deposit amount to amt and the less_withdrawals method should subtract the withdrawal amount from amt. Create two instances of the class, the first assigned to ``bob`` and the second to ``sally``. The first uses "Bob" as the name, 100 as the start_amt, and 50 as the deposit amount. The second uses "Sally" as the name, 200 as the start amount, 0 as the deposit, and 125 as the withdrawal amount. For ``bob``, call add_deposit enough times so that the start_amt is 200 dollars and save to the variable ``bob_amt``. For ``sally``, call less_withdrawal enough times so that the start_amt is 75 dollars and save to the variable ``sally_amt``.

.. activecode:: ee_ch13_04
   :tags:Classes/AddingOtherMethodstoourClass.rst
   

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testFourA(self):
         self.assertEqual(bob.__str__(), "Your account, Bob, has 200 dollars.", "Testing that bob is assigned to correct value")
      def testFourB(self):
         self.assertEqual(sally.__str__(), 'Your account, Sally, has 75 dollars.', "Testing that sally is assigned to correct value")
      def testFourC(self):
         self.assertEqual(bob_amt, 200, "Testing that bob_amt is assigned to correct value")
      def testFourD(self):
         self.assertEqual(sally_amt, 75, "Testing that sally is assigned to correct value")

   myTests().main()

5. **Challenge** The class, ``Olympics``, is given and has two instance variables, country and medal, referencing a country and its corresponding medal count in the Rio Olympics. The list, ``L``, gives some countries and their medal counts. Create a list of instances from the given list and assign it to the variable ``instances``. Then, sort the instances based on medal count and then alphabetically by country name. The sorted medal count list should be assigned to the variable ``sort_medal`` and be a list of tuples displaying both the country name and medal count from highest medal count to lowest. The list sorted alphabetically should only display the country name and be assigned to the variable ``sort_alpha``. 

.. activecode:: ee_ch13_05
   :tags:Classes/sorting_instances.rst

   class Olympics():
       def __init__(self, country, medal):
           self.country = country
           self.medal = medal
        
       def sort_medal(self):
           return self.medal
   
       def sort_country(self):
           return self.country

   L = [("Italy", 28), ("China", 70), ("Australia", 29), ("United States", 121), ("Russia", 56), ("South Korea", 21), ("Venezuela", 3)]

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testFiveA(self):
         self.assertEqual(len(instances), 7, "Testing that instances is assigned to correct values")
      def testFiveB(self):
         self.assertEqual(sort_medal, [('United States', 121), ('China', 70), ('Russia', 56), ('Australia', 29), ('Italy', 28), ('South Korea', 21), ('Venezuela', 3)], "Testing if sort_medal is assigned to correct values")
      def testFiveC(self):
         self.assertEqual(sort_alpha, sorted(['Australia', 'China', 'Italy', 'Russia', 'South Korea', 'United States', 'Venezuela']), "Testing if sort_alpha is assigned to correct values")

   myTests().main()














​


