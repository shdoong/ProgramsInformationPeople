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

1. Using string interpolation, fill out the parameters so that "I go to UM and I am in SI 106" is assigned to ``str1``.

.. activecode:: ee_interpolation_01
   :tags:StringFormatting/Interpolation.rst

   str1 = "I go to {} and I am in {}".format()
      
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(str1, "I go to UM and I am in SI 106", "Testing that str1 is assigned to correct value")

   myTests().main()


1.1 Using string interpolation, fill out the parameters so that 'This book teaches students python.' is assigned to ``info``.

.. activecode:: ee_interpolation_011
   :tags: StringFormatting/Interpolation.rst

   info = "This book {} students {}.".format()

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(info, "This book teaches students python.", "Testing that info has the correct value.")

   myTests().main()

2. Use string formatting to complete the string given. The blanks should correspond to variable ``name`` and ``breed``.  

.. activecode:: ee_interpolation_02
   :tags:StringFormatting/Interpolation.rst

   name = "Oreo"
   breed = "poodle"
   str1 = "This is {}, he is a {}."
      
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(str1, "This is Oreo, he is a poodle.", "Testing that str1 is assigned to correct value")

   myTests().main()

2.1 Using string interpolation, assign the correct value to the variable ``names`` so that the value assigned to the variable ``sent`` is "Paul, Jackie, and Stephen have taught or are teaching this class."

.. activecode:: ee_interpolation_021
   :tags: StringFormatting/Interpolation.rst

   sent = "{}, {}, and {} have taught or are teaching this class.".format()

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(sent, "Paul, Jackie, and Stephen have taught or are teaching this class.", "Testing that sent has the correct value.")
         self.assertEqual(names, ['Paul', 'Jackie', 'Stephen'], "Testing that names has the correct values assigned")

   myTests().main()

3. Provided is a list of tuples, the first is a country, the second is their medal count. Create a new list called ``medals`` using these tuples so that if the tuple was ('USA', 121), then what is added to medals is the string "USA won 121 medals". Do so using string interpolation.

.. activecode:: ee_interpolation_03
   :tags:StringFormatting/Interpolation.rst

   countries = [('Jamaica', 11), ('Malaysia',5), ('Japan', 41), ('Sweden', 11), ('Serbia', 8)]

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(medals, ['Jamaica won 11 medals', 'Malaysia won 5 medals', 'Japan won 41 medals', 'Sweden won 11 medals', 'Serbia won 8 medals'], "Testing that medals is assigned to correct values")

   myTests().main()

3.1 Provided is a list of tuples, the first is a name, the second is a city. Create a new list called ``user_info`` using these tuples so that if the tuple was ('Ashley', 'Kalamazoo'), then what is added to user_info is the string "Ashley is from Kalamazoo". Do so using string interpolation.

.. activecode:: ee_interpolation_031
   :tags: StringFormatting/Interpolation.rst

   info = [('Sarah', 'Mattawan'), ("Grace", "Kalamazoo"), ('Mariana', "Sao Paulo"), ('Kevin', 'Melbourne'), ('Srishti', 'Dubai'), ('Kathleen', 'Bagota'), ('Ann', 'Excel')]


   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(user_info, ['Sarah is from Mattawan', 'Grace is from Kalamazoo', 'Mariana is from Sao Paulo', 'Kevin is from Melbourne', 'Srishti is from Dubai', 'Kathleen is from Bagota', 'Ann is from Excel'], "Testing that user_info has the correct value.")
         
   myTests().main()

4.  Write a function called ``pokemon`` that takes in a list of an integer and string. The integer is the level of the trainer and the string is where the trainer plays. If the player is level five or below, they have the most rattatas. If they are between level 6 and 10, they have the most zubats. If they are higher than level 10, they have the most eevees. Return the string "I'm level __ and I caught a bunch of __ in the __!" where the first blank is the player level, the second is the pokemon, and the third is the location where they play. For instance, if the inputted list is [2, "city"], the returned string should be "I'm level 2 and I caught a bunch of rattatas in the city!" Do this using string interpolation.

.. activecode:: ee_interpolation_04
   :tags:StringFormatting/Interpolation.rst
      

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testFour(self):
         self.assertEqual(pokemon([4, "suburbs"]), "I'm level 4 and I caught a bunch of rattatas in the suburbs!", "Testing that pokemon[4, 'suburbs'] returns 'I'm level 4 and I caught a bunch of rattatas in the suburbs!'.")
         self.assertEqual(pokemon([25, "field"]), "I'm level 25 and I caught a bunch of eevees in the field!", "Testing that pokemon[25, 'field'] returns 'I'm level 25 and I caught a bunch of eevees in the field!'.")
         self.assertEqual(pokemon([10, "city"]), "I'm level 10 and I caught a bunch of zubats in the city!", "Testing that pokemon[10, 'city'] returns 'I'm level 10 and I caught a bunch of zubats in the city!'.")

   myTests().main()

5. The list of tuples, ``order``, contains information about pizza orders. It contains information on whether or not the order is a pickup or delivery, how many pizzas were ordered, the kind of pizzas, and in how many minutes they need to be ready. Create a list called ``response`` that gives a response to each order. For a delivery, if the order input is ("delivery", 1, "cheese", 10), the response should be "Your 1 cheese pizza will be delivered in 10 minutes". If the order is a pickup, the response should be "Come pick up your 1 cheese pizza in 10 minutes". 

.. activecode:: ee_interpolation_05
   :tags:StringFormatting/Interpolation.rst

   order = [("delivery", 3, "pepperoni", 20), ("pickup", 4, "cheese", 10), ("pickup", 2, "combo", 5), ("delivery", 10, "cheese", 15), ("delivery", 1, "supreme", 60)]

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testFive(self):
         self.assertEqual(response, ['Your 3 pepperoni pizzas will be delievered in 20 minutes', 'Come pick up your 4 cheese pizzas in 10 minutes', 'Come pick up your 2 combo pizzas in 5 minutes', 'Your 10 cheese pizzas will be delievered in 15 minutes', 'Your 1 supreme pizzas will be delievered in 60 minutes'], "Testing if response is assigned to correct values")

   myTests().main()

5.1 Provided is a list of dictionaries of pokemon trainers. If they have walked less than 2 kilometers, then they should have their name and the message "you are so close to hatching a 2 km egg, you've gone ___ km so far!" added to a new list called ``trainer_data``. If they have walked less than 5 km, they should have the same messaged printed, but with 5km, not 2km. The same for a 10 km egg. If they have walked more than 10 km, then it should print their name, plus the message "you could have hatched a 10 km egg or more! You walked ___ km!" (example, a trainer with the name of Nurse Joy who has walked 1.3, would have "Nurse Joy, you are so close to hatching a 2 km egg, you've gone 1.3 km so far!")

.. activecode:: ee_interpolation_051
   :tags:StringFormatting/Interpolation.rst

   lst = [{'trainer_name': "Ash", 'distance_traveled': 8.9, 'pokemon_caught': 17}, {'trainer_name': "Mysti", "distance_traveled": 4.7, 'pokemon_caught': 9}, {'trainer_name': "Brock", 'distance_traveled': 20.2, 'pokemon_caught': 39}, {'trainer_name': "Gary", 'distance_traveled': 1.8, 'pokemon_caught': 89}]


   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(trainer_data, ["Ash, you are so close to hatching a 10 km egg, you've gone 8.9 km so far!", "Mysti, you are so close to hatching a 5 km egg, you've gone 4.7 km so far!", 'Brock, you could have atched a 10 km egg or more! You walked 20.2 km!', "Gary, you are so close to hatching a 2 km egg, you've gone 1.8 km so far!"], "Testing that trainer_data has the correct value.")
         
   myTests().main()















​


