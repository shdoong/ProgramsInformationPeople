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

1. Assign the value of the 34st element of ``lst`` to the variable ``output``.

.. activecode:: ee_ch9_01
   :tags:Iteration/TraversalandtheforLoopByIndex.rst

   lst = ["hi", "morning", "dog", "506", "caterpillar", "balloons", 106, "yo-yo", "python", "moon", "water", "sleepy", "daffy", 45, "donald", "whiteboard", "glasses", "markers", "couches", "butterfly", "100", "magazine", "door", "picture", "window", ["Olympics", "handle"], "chair", "pages", "readings", "burger", "juggle", "craft", ["store", "poster", "board"], "laptop", "computer", "plates", "hotdog", "salad", "backpack", "zipper", "ring", "watch", "finger", "bags", "boxes", "pods", "peas", "apples", "horse", "guinea pig", "bowl", "EECS"]
   
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(output, "laptop", "Testing that output value is assigned to correct value.")

   myTests().main()

2. Assign the number of elements in ``lst`` to the variable ``output``.

.. activecode:: ee_ch9_02
  
   lst = ["hi", "morning", "dog", "506", "caterpillar", "balloons", 106, "yo-yo", "python", "moon", "water", "sleepy", "daffy", 45, "donald", "whiteboard", "glasses", "markers", "couches", "butterfly", "100", "magazine", "door", "picture", "window", ["Olympics", "handle"], "chair", "pages", "readings", "burger", "juggle", "craft", ["store", "poster", "board"], "laptop", "computer", "plates", "hotdog", "salad", "backpack", "zipper", "ring", "watch", "finger", "bags", "boxes", "pods", "peas", "apples", "horse", "guinea pig", "bowl", "EECS"]
   
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testTwo(self):
         self.assertEqual(output, 52, "Testing that output value is assigned to correct value.")

   myTests().main()

3. Assign the value of the last element of ``lst`` to the variable the variable ``output``. Do this so that it doesn't matter the length of lst. 

.. activecode:: ee_ch9_03
   
   lst = ["hi", "morning", "dog", "506", "caterpillar", "balloons", 106, "yo-yo", "python", "moon", "water", "sleepy", "daffy", 45, "donald", "whiteboard", "glasses", "markers", "couches", "butterfly", "100", "magazine", "door", "picture", "window", ["Olympics", "handle"], "chair", "pages", "readings", "burger", "juggle", "craft", ["store", "poster", "board"], "laptop", "computer", "plates", "hotdog", "salad", "backpack", "zipper", "ring", "watch", "finger", "bags", "boxes", "pods", "peas", "apples", "horse", "guinea pig", "bowl", "EECS"]
   
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testThree(self):
         self.assertEqual(output, "EECS", "Testing that output value is assigned to correct value.")

   myTests().main()

4. Create a new list of the 6th through 14th elements of ``lst`` and assign it to the variable ``output``.

.. activecode:: ee_ch9_04
   
   lst = ["swimming", 2, "water bottle", 44, "lollipop", "shine", "marsh", "winter", "donkey", "rain", ["Rio", "Beijing", "London"], [1,2,3], "gold", "bronze", "silver", "mathematician", "scientist", "actor", "actress", "win", "cell phone", "leg", "running", "horse", "socket", "plug", ["Phelps", "le Clos", "Lochte"], "drink", 22, "happyfeet", "penguins"]

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testFour(self):
         self.assertEqual(output, ["shine", "marsh", "winter", "donkey", "rain", ["Rio", "Beijing", "London"], [1,2,3], "gold"], "Testing that output value is assigned to correct value.")

   myTests().main()

5. Create a new string of ``str1`` but lowercase and assign it to the variable ``output``. Do not hard code this.

.. activecode:: ee_ch9_05
      
   str1 = "OH THE PLACES YOU WILL GO"

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testFive(self):
         self.assertEqual(output, "oh the places you will go", "Testing that output value is assigned to correct value.")

   myTests().main()

6. Create a variable ``output`` and assign it to a list whose elements are the words in the string ``str1``. 

.. activecode:: ee_ch9_06
      
   str1 = "OH THE PLACES YOU'LL GO"

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testSix(self):
         self.assertEqual(output, ["OH", "THE", "PLACES", "YOU'LL", "GO"], "Testing that output value is assigned to correct value.")

   myTests().main()

7. Add the pet "goldfish" to the end of the list of pets, ``pets``. Do this using a list method.

.. activecode:: ee_ch9_07
    
   pets = ["cat", "dog", "lizard", "parrot", "hamster"]

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testSeven(self):
         self.assertEqual(pets, ["cat", "dog", "lizard", "parrot", "hamster", "goldfish"], "Testing that pets value is assigned to correct value.")

   myTests().main()

8. Get rid of all values of 7 from the list, ``numbers``. 

.. activecode:: ee_ch9_08

   numbers = [1, 1, 2, 2, 3, 3, 6, 6, 7, 7, 7, 7, 8, 8, 12, 15]

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testEight(self):
         self.assertEqual(numbers, [1, 1, 2, 2, 3, 3, 6, 6, 8, 8, 12, 15], "Testing that output value is assigned to correct value.")

   myTests().main()

9. **Challenge** Please get rid of the pet "cat" from the list ``pets``. Add the pet "dog" in its place.

.. activecode:: ee_ch9_09

   pets = ["goldfish", "cat", "parrot", "hamster"]

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testNine(self):
         self.assertEqual(pets[1], "dog", "Testing that dog is in correct location.")
         self.assertEqual(pets, ["goldfish", "dog", "parrot", "hamster"], "Testing that output value is assigned to correct value.")

   myTests().main()

10. **Challenge** Create a list made up of the 5th and 37th element from the list ``words`` and assign it to the variable ``output``.

.. activecode:: ee_ch9_10

   words = ["hi", "morning", "dog", "506", "caterpillar", "balloons", 106, "yo-yo", "python", "moon", "water", "sleepy", "daffy", 45, "donald", "whiteboard", "glasses", "markers", "couches", "butterfly", "100", "magazine", "door", "picture", "window", ["Olympics", "handle"], "chair", "pages", "readings", "burger", "juggle", "craft", ["store", "poster", "board"], "laptop", "computer", "plates", "hotdog", "salad", "backpack", "zipper", "ring", "watch", "finger", "bags", "boxes", "pods", "peas", "apples", "horse", "guinea pig", "bowl", "EECS"]
   
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testTen(self):
         self.assertEqual(output, ["caterpillar", "hotdog"], "Testing that output value is assigned to correct value.")

   myTests().main()

11. **Challenge** Create a new list, ``newlist``, that is made up of the last 6 elements of ``lst``. Then assign the fourth element of the new list to the variable ``output``. Note: This should work regardless of the length of the list.

.. activecode:: ee_ch9_11

   lst = ["swimming", 2, "water bottle", 44, "lollipop", "shine", "marsh", "winter", "donkey", "rain", ["Rio", "Beijing", "London"], [1,2,3], "gold", "bronze", "silver", "mathematician", "scientist", "actor", "actress", "win", "cell phone", "leg", "running", "horse", "socket", "plug", ["Phelps", "le Clos", "Lochte"], "drink", 22, "happyfeet", "penguins"]
   
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testElevenA(self):
         self.assertEqual(newlist, ["plug", ["Phelps", "le Clos", "Lochte"], "drink", 22, "happyfeet", "penguins"], "Testing that newlist value is assigned to correct value.")

      def testElevenB(self):
         self.assertEqual(output, 22, "Testing that output value is assigned to correct value.")

   myTests().main()

12. **Challenge** Remove the whitespace from ``str1`` and assign the new string to variable ``newstring``. Then save the number of characters of ``newstring`` to ``newlength``. Next, split ``newstring`` on every occurrence the letter 'p' and assign to ``output``.

.. activecode:: ee_ch9_12

   str1 = "     peter piper picked a peck of pickled peppers.               "
   
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testTwelveA(self):
         self.assertEqual(newstring, "peter piper picked a peck of pickled peppers.", "Testing that newstring value is assigned to correct value.")

      def testTwelveB(self):
         self.assertEqual(newlength, 45, "Testing that newlength value is assigned to correct value.")

      def testTwelveC(self):
         self.assertEqual(output, ['', 'eter ', 'i', 'er ', 'icked a ', 'eck of ', 'ickled ', 'e', '', 'ers.'], "Testing that output value is assigned to correct value.")

   myTests().main()
