Extra Exercises
================

1. Write code to assign to the variable ``map_testing`` all the elements in lst_check while adding the string "Fruit: " to the beginning of each element using mapping.

.. activecode:: ee_listcomp_01
   :tags:

   lst_check = ['plums', 'watermelon', 'kiwi', 'strawberries', 'blueberries', 'peaches', 'apples', 'mangos', 'papaya']

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(map_testing, ['Fruit: plums', 'Fruit: watermelon', 'Fruit: kiwi', 'Fruit: strawberries', 'Fruit: blueberries', 'Fruit: peaches', 'Fruit: apples', 'Fruit: mangos', 'Fruit: papaya'], "Testing that map_testing has the correct values.")

   myTests().main()

2. Write code to assign to the variable ``filter_testing`` all the elements in lst_check that have a w in them using filter.

.. activecode:: ee_listcomp_02
  

   lst_check = ['plums', 'watermelon', 'kiwi', 'strawberries', 'blueberries', 'peaches', 'apples', 'mangos', 'papaya']

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(filter_testing, ['watermelon', 'kiwi', 'strawberries'], "Testing that filter_testing has the correct values.")

   myTests().main()

3. Write code to assign to the variable ``reducing_testing`` all the elements in lst_check and compiling them in a string that begins with "Fruits: " and has a comma and a space between each element using reduce.

.. activecode:: ee_listcomp_03
   

   lst_check = ['plums', 'watermelon', 'kiwi', 'strawberries', 'blueberries', 'peaches', 'apples', 'mangos', 'papaya']

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(reducing_testing, "Fruits: plums, watermelon, kiwi, strawberries, blueberries, peaches, apples, mangos, papaya", "Testing that reducing_testing has the correct value.")

   myTests().main()

4. Write code to assign to the variable ``compri`` all the values of the key name in the dictionary ``tester``. Do this using list comprehension.

.. activecode:: ee_listcomp_04
   :tags:

   tester = {'info': [{"name": "Lauren", 'class standing': 'Junior', 'major': "Information Science"},{'name': 'Ayo', 'class standing': "Bachelor's", 'major': 'Information Science'}, {'name': 'Kathryn', 'class standing': 'Senior', 'major': 'Sociology'}, {'name': 'Nick', 'class standing': 'Junior', 'major': 'Computer Science'}, {'name': 'Gladys', 'class standing': 'Sophomore', 'major': 'History'}, {'name': 'Adam', 'major': 'Violin Performance', 'class standing': 'Senior'}]}


   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(sorted(compri), sorted(['Lauren', 'Ayo', 'Kathryn', 'Nick', 'Gladys', 'Adam']), "Testing that compri has the correct values.")

   myTests().main()

5. Write code to assign to the variable ``compri_sample`` all the values of the key name in the dictionary ``tester`` if they are juniors or seniors. Do this using list comprehension.

.. activecode:: ee_listcomp_05


   tester = {'info': [{"name": "Lauren", 'class standing': 'Junior', 'major': "Information Science"},{'name': 'Ayo', 'class standing': "Bachelor's", 'major': 'Information Science'}, {'name': 'Kathryn', 'class standing': 'Senior', 'major': 'Sociology'}, {'name': 'Nick', 'class standing': 'Junior', 'major': 'Computer Science'}, {'name': 'Gladys', 'class standing': 'Sophomore', 'major': 'History'}, {'name': 'Adam', 'major': 'Violin Performance', 'class standing': 'Senior'}]}


   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(sorted(compri_sample), sorted(['Lauren', 'Nick']), "Testing that compri_sample has the correct values.")

   myTests().main()

6. Write code using zip and filter so that these lists (l1 and l2) are combined into one big list and assigned to the variable ``opposites`` if they are both longer than 3 characters each.

.. activecode:: ee_listcomp_06
   :tags:
   
   l1 = ['left', 'up', 'front']
   l2 = ['right', 'down', 'back']

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(opposites, [('left','right'), ('up', 'down'), ('front','back')], "Testing that opposites has the correct list of tuples.")

   myTests().main()

7.  Write code to assign to the variable ``class_sched`` all the values of the key ``important classes``. Do this using list comprehension.

.. activecode:: ee_listcomp_07
   :tags:

   tester = {'info': [
            {"name": "Lauren", 'class standing': 'Junior', 'major': "Information Science", 'important classes': ['SI 106', 'ENGLISH 125', 'SI 110', 'AMCULT 202']},
            {'name': 'Ayo', 'class standing': "Bachelor's", 'major': 'Information Science', "important classes": ['SI 106', 'SI 410', 'PSYCH 111']}, 
            {'name': 'Kathryn', 'class standing': 'Senior', 'major': 'Sociology', 'important classes': ['WOMENSTD 220', 'SOC 101', 'ENS 384']}, 
            {'name': 'Nick', 'class standing': 'Junior', 'major': 'Computer Science', "important classes": ['SOC 101', 'AMCULT 334', 'EECS 281']}, 
            {'name': 'Gladys', 'class standing': 'Sophomore', 'major': 'History', 'important classes': ['ENGLISH 125', 'HIST 259', 'ENGLISH 130']}, 
            {'name': 'Adam', 'major': 'Violin Performance', 'class standing': 'Senior', 'important classes': ['PIANO 101', 'STUDIO 300', 'THEORY 229', 'MUSC 356']}]}


   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOne(self):
         self.assertEqual(sorted(class_sched), sorted(['SI 106', 'ENGLISH 125', 'SI 110', 'AMCULT 202','SI 106', 'SI 410', 'PSYCH 111', 'WOMENSTD 220', 'SOC 101', 'ENS 384', 'SOC 101', 'AMCULT 334', 'EECS 281', 'ENGLISH 125', 'HIST 259', 'ENGLISH 130', 'PIANO 101', 'STUDIO 300', 'THEORY 229', 'MUSC 356']), "Testing that class_sched has the correct list.")

   myTests().main()
