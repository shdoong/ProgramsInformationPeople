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

.. datafile:: files_extra.txt
   :hide:

   This summer I will be travelling.
   I will go to...
   Italy: Rome
   Greece: Athens
   England: London, Manchester
   France: Paris, Nice, Lyon
   Spain: Madrid, Barcelona, Granada
   Austria: Vienna
   I will probably not even want to come back! 
   However, I wonder how I will get by with all the different languages.
   I only know English!

1. The textfile, ``files_extra.txt``, contains the summer travel plans for someone with some commentary. Find the total number of characters in the file and save to the variable ``num``.

.. activecode:: ee_files_01
   :tags: Files/Iteratingoverlinesinafile.rst, Files/intro-WorkingwithDataFiles.rst

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(num, 316, "Testing that num value is assigned to correct value.")

   myTests().main()

2. Now, find the number of lines in the file, ``files_extra.txt``, and assign it to the variable ``num_lines``.

.. activecode:: ee_files_02
   :tags: Files/Iteratingoverlinesinafile.rst, Files/intro-WorkingwithDataFiles.rst
   
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testTwo(self):
         self.assertEqual(num_lines, 11, "Testing that num_lines is assigned to correct value.")

   myTests().main()

3. **Challenge** Assign the second word of every line to the list, ``second``.

.. activecode:: ee_files_03
   :tags:Files/Iteratingoverlinesinafile.rst, Files/intro-WorkingwithDataFiles.rst

   second = []
   
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testThree(self):
         self.assertEqual(second, ['summer', 'will', 'Rome', 'Athens', 'London,', 'Paris,', 'Madrid,', 'Vienna', 'will', 'I', 'only'], "Testing that second is assigned to correct value.")

   myTests().main()

4. **Challenge** Create a list called ``destination``. If the line in the file ``files_extra.txt`` has a colon (:), append that line to the list.

.. activecode:: ee_files_04
   :tags:Files/Iteratingoverlinesinafile.rst, Files/intro-WorkingwithDataFiles.rst
   

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testFour(self):
         self.assertEqual(destination, ['Italy: Rome\n', 'Greece: Athens\n', 'England: London, Manchester\n', 'France: Paris, Nice, Lyon\n', 'Spain: Madrid, Barcelona, Granada\n', 'Austria: Vienna\n'], "Testing that destination is assigned to correct values.")

   myTests().main()

5. Assign the first 33 characters from the textfile to the variable ``first_chars``.

.. activecode:: ee_files_05
   :tags:Files/intro-WorkingwithDataFiles.rst
   

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testFive(self):
         self.assertEqual(first_chars, "This summer I will be travelling.", "Testing that first_chars is assigned to correct value.")

   myTests().main()

