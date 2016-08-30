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

1. The code below takes the list of country, ``country``, and searches to see if it is in the dictionary ``gold`` which shows some countries who won gold during the Olympics. However, this code currently does not work. Correctly add try/except clause in the code so that it will correctly populate the list, ``country_gold``, with either the number of golds won or the string "Did not get gold".

.. activecode:: ee_exceptions_01
   :tags:Exceptions/intro-exceptions.rst

   gold = {"US":46, "Fiji":1, "Great Britain":27, "Cuba":5, "Thailand":2, "China":26, "France":10}
   country = ["Fiji", "Chile", "Mexico", "France", "Norway", "US"]
   country_gold = []

   for x in country:
        country_gold.append(gold[x])
        country_gold.append("Did not get gold")

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOneA(self):
         self.assertEqual(country_gold, [1, 'Did not get gold', 'Did not get gold', 10, 'Did not get gold', 46], "Testing that country_gold is assigned to correct values")
      
   myTests().main()

2. The list, ``numb``, contains integers. Write code that populates the list ``remainder`` with the remainder of 36 divided by each number in ``numb``. For example, the first element should be 0, because 36/6 has no remainder. If there is an error, have the string "Error" appear in the ``remainder``.

.. activecode:: ee_exceptions_02
   :tags:Exceptions/intro-exceptions.rst

   numb = [6, 0, 36, 8, 2, 36, 0, 12, 60, 0, 45, 0, 3, 23]

   remainder = []

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOneA(self):
         self.assertEqual(remainder, [0, 'Error', 0, 4, 0, 0, 'Error', 0, 36, 'Error', 36, 'Error', 0, 13], "Testing that remainder is assigned to correct values.")
     
   myTests().main()

3. The code below assigns the 5th letter of each word in ``food`` to the new list ``fifth``. However, the code currently produces errors. Insert a try/except clause that will allow the code to run and produce of list of the 5th letter in each word. If the word is not long enough, it should not print anything out. Note: The pass statement is a null operation; nothing will happen when it executes.

.. activecode:: ee_exceptions_03
   :tags:Exceptions/intro-exceptions.rst

   food = ["chocolate", "chicken", "corn", "sandwich", "soup", "potatoes", "beef", "lox", "lemonade"]
   fifth = []

   for x in food:
      
           fifth.append(x[4])

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOneA(self):
         self.assertEqual(fifth, ['o', 'k', 'w', 't', 'n'], "Testing that fifth is assigned to correct values.")
     
      
   myTests().main()

4. The buggy code below prints out the value of the sport in the list ``sport``. Use try/except so that the code will run properly. If the sport is not in the dictionary, ``ppl_play``, add it in with the value of 1.

.. activecode:: ee_exceptions_04
   :tags:Exceptions/intro-exceptions.rst

   sport = ["hockey", "basketball", "soccer", "tennis", "football", "baseball"]

   ppl_play = {"hockey":4, "soccer": 10, "football": 15, "tennis": 8}

   for x in sport:
      
        print ppl_play[x]
       
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOneA(self):
         self.assertEqual(sorted(ppl_play.items()), [('baseball', 1), ('basketball', 1), ('football', 15), ('hockey', 4), ('soccer', 10), ('tennis', 8)], "Testing that ppl_play is assigned to correct values.")
     
   myTests().main()



