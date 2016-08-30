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

1. The class, ``Pokemon``, is provided below and describes a Pokemon and its leveling and evolving characteristics. An instance of the class is one pokemon that you create. ``Grass`` is a subclass that inherits from ``Pokemon`` but changes some aspects, for instance, the boost values are different. For the subclass ``Grass``, add another method called ``action`` that returns the string "[name of pokemon] knows a lot of different moves!". Call an instance of this class with the name as "Belle". Assign this instance to the variable ``p1``.

.. activecode:: ee_inheritance_01
   :tags:Inheritance/inheritVarsAndMethods.rst

   class Pokemon():
       attack = 12
       defense = 10
       hp = 15
    
       def __init__(self, name, level = 5):
           self.name = name
           self.p_type = "Normal"
           self.level = level
       
       def train(self):
           self.update()
           self.attack_up()
           self.defense_up()
           self.hp_up()
           self.level = self.level + 1
           if self.level%self.evolve == 0:
               return self.level, "Evolved!"
           else:
               return self.level
    
       def attack_up(self):
           self.attack = self.attack + self.attack_boost
           return self.attack
    
       def defense_up(self):
           self.defense = self.defense + self.defense_boost
           return self.defense
    
       def hp_up(self):
           self.hp = self.hp + self.hp_boost
           return self.hp

       def update(self):
           self.hp_boost = 5
           self.attack_boost = 3
           self.defense_boost = 2
           self.evolve = 10
        
       def __str__(self):
           self.update()
           return "Pokemon name: {}, Type: {}, Level: {}".format(self.name, self.p_type, self.level)

   class Grass(Pokemon):
       attack = 15
       defense = 14
       hp = 12
    
       def update(self):
           self.hp_boost = 6
           self.attack_boost = 2
           self.defense_boost = 3
           self.evolve = 12
        
       def moves(self):
           self.p_moves = ["razor leaf", "synthesis", "petal dance"]


   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOneA(self):
         self.assertEqual(p1.action(), "Belle knows a lot of different moves!", "Testing that action method is correct and p1 assigned to correct value")
      
   myTests().main()

2. The attack strength for grass Pokemon does not change until they reach level 10. At level 10 and up, their attack strength increases by the attack_boost amount when they level. Modify the ``Grass`` class to reflect this change. To test, create an instance of the class with the name as "Bulby". Assign the instance to the variable ``p2``. Then, train the Pokemon until it reaches level 10.

.. activecode:: ee_inheritance_02
   :tags:Inheritance/inheritVarsAndMethods.rst,Inheritance/OverrideMethods.rst

   class Pokemon():
       attack = 12
       defense = 10
       hp = 15
    
       def __init__(self, name, level = 5):
           self.name = name
           self.p_type = "Normal"
           self.level = level
       
       def train(self):
           self.update()
           self.attack_up()
           self.defense_up()
           self.hp_up()
           self.level = self.level + 1
           if self.level%self.evolve == 0:
               return self.level, "Evolved!"
           else:
               return self.level
    
       def attack_up(self):
           self.attack = self.attack + self.attack_boost
           return self.attack
    
       def defense_up(self):
           self.defense = self.defense + self.defense_boost
           return self.defense
    
       def hp_up(self):
           self.hp = self.hp + self.hp_boost
           return self.hp

       def update(self):
           self.hp_boost = 5
           self.attack_boost = 3
           self.defense_boost = 2
           self.evolve = 10
        
       def __str__(self):
           return "Pokemon name: {}, Type: {}, Level: {}".format(self.name, self.p_type, self.level)

   class Grass(Pokemon):
       attack = 15
       defense = 14
       hp = 12
    
       def update(self):
           self.hp_boost = 6
           self.attack_boost = 2
           self.defense_boost = 3
           self.evolve = 12
           self.p_type = "Grass"
        
       def moves(self):
           self.p_moves = ["razor leaf", "synthesis", "petal dance"]
           

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOneA(self):
         self.assertEqual(p2.__str__(), "Pokemon name: Bulby, Type: Grass, Level: 5", "Testing that p2 is assigned to correct value.")
      def testOneB(self):
         self.assertEqual(p2.attack_up(), 17, "Testing that attack value is assigned to correct value at level 10.")
      
   myTests().main()

3. Create a new subclass for ghost type Pokemon called ``Ghost``. It should inherit from the Pokemon parent class. The starting attack value for ghost pokemon is 15, defense value is 12, and hp remains the same at 15. In addition, the ghost class should also have an additional variable called ``item`` that will either have the value "Yes" or "No". If the pokemon has an item, they are able to gain XP faster so they will level every 8 levels. If they do not have an item, they gain XP much slower and evolve every 20 levels at level 20, 40, etc. In addition, they gain a 3 HP, 4 attack, and 3 defense boost when they level. Also remember to update the p_type to "Ghost". Create two instances of the class with the first name as "Ghastly" and it does have an item. Assign this instance to the variable ``g1``. The second should be named "Drifloon" and it does not have an item. Assign the second instance to the variable ``g2``.Train both "Ghastly" and "Drifloon" two times.

.. activecode:: ee_inheritance_03
   :tags:Inheritance/inheritVarsAndMethods.rst,Inheritance/OverrideMethods.rst,Inheritance/InvokingSuperMethods.rst

   class Pokemon():
       attack = 12
       defense = 10
       hp = 15
    
       def __init__(self, name, level = 5):
           self.name = name
           self.p_type = "Normal"
           self.level = level
       
       def train(self):
           self.update()
           self.attack_up()
           self.defense_up()
           self.hp_up()
           self.level = self.level + 1
           if self.level%self.evolve == 0:
               return self.level, "Evolved!"
           else:
               return self.level
    
       def attack_up(self):
           self.attack = self.attack + self.attack_boost
           return self.attack
    
       def defense_up(self):
           self.defense = self.defense + self.defense_boost
           return self.defense
    
       def hp_up(self):
           self.hp = self.hp + self.hp_boost
           return self.hp

       def update(self):
           self.hp_boost = 5
           self.attack_boost = 3
           self.defense_boost = 2
           self.evolve = 10
        
       def __str__(self):
           return "Pokemon name: {}, Type: {}, Level: {}".format(self.name, self.p_type, self.level)

   class Grass(Pokemon):
       attack = 15
       defense = 14
       hp = 12
    
       def update(self):
           self.hp_boost = 6
           self.attack_boost = 2
           self.defense_boost = 3
           self.evolve = 12
           self.p_type = "Grass"
        
       def moves(self):
           self.p_moves = ["razor leaf", "synthesis", "petal dance"]

   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOneA(self):
         self.assertEqual(g1.__str__(), "Pokemon name: Ghastly, Type: Ghost, Level: 7", "Testing that g1 is assigned to correct value.")
      def testOneB(self):
         self.assertEqual(g2.__str__(), "Pokemon name: Drifloon, Type: Ghost, Level: 7", "Testing that g2 is assigned to correct value.")
      def testOneC(self):
         self.assertEqual(g1.train(), (8, "Evolved!"), "Testing that g1 evolves at level 8.")
      def testOneD(self):
         self.assertEqual(g2.train(), 8, "Testing that g2 does not evolve at level 8.")
      
   myTests().main()

4. Create another subclass called ``GrassBug`` that inherits from the Grass subclass. Everything will remain the same as the grass pokemon, however, the moves method will change. In addition to all the grass moves from the Grass subclass, Grass and Bug pokemon also have an additional three moves added to the list, p_moves: "poison sting", "stun spore", and "acid". Call the moves method from the Grass subclass in the moves method of the new ``GrassBug`` sub class and add the additional moves. 

.. activecode:: ee_inheritance_04
   :tags:Inheritance/inheritVarsAndMethods.rst,Inheritance/InvokingSuperMethods.rst,Inheritance/OverrideMethods.rst

   class Pokemon():
       attack = 12
       defense = 10
       hp = 15
    
       def __init__(self, name, level = 5):
           self.name = name
           self.p_type = "Normal"
           self.level = level
       
       def train(self):
           self.update()
           self.attack_up()
           self.defense_up()
           self.hp_up()
           self.level = self.level + 1
           if self.level%self.evolve == 0:
               return self.level, "Evolved!"
           else:
               return self.level
    
       def attack_up(self):
           self.attack = self.attack + self.attack_boost
           return self.attack
    
       def defense_up(self):
           self.defense = self.defense + self.defense_boost
           return self.defense
    
       def hp_up(self):
           self.hp = self.hp + self.hp_boost
           return self.hp

       def update(self):
           self.hp_boost = 5
           self.attack_boost = 3
           self.defense_boost = 2
           self.evolve = 10
        
       def __str__(self):
           return "Pokemon name: {}, Type: {}, Level: {}".format(self.name, self.p_type, self.level)

   class Grass(Pokemon):
       attack = 15
       defense = 14
       hp = 12
    
       def update(self):
           self.hp_boost = 6
           self.attack_boost = 2
           self.defense_boost = 3
           self.evolve = 12
           self.p_type = "Grass"
        
       def moves(self):
           self.p_moves = ["razor leaf", "synthesis", "petal dance"]
        
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOneA(self):
         self.assertEqual(GrassBug("Buggy").moves(), ['razor leaf', 'synthesis', 'petal dance', 'poison sting', 'stun spore', 'acid'], "Testing that g1 is assigned to correct value.")
     
   myTests().main()


5. **Challenge** Along with the Pokemon parent class, we have also provided several subclasses. Write another method in the parent class that will be inherited by the subclasses called ``opponent`` that will show which type of pokemon the current type is weak against and strong against. For instance, if the p_type of the subclass is grass, fire will be assigned to the variable ``weak`` and water will be assigned to the variable ``strong``. Grass is weak against fire, but strong against water. Ghost is weak against dark but strong against psychic. Fire is weak against water but strong against grass. Finally, flying is weak against electric but strong against fighting.

.. activecode:: ee_inheritance_05
   :tags:Inheritance/inheritVarsAndMethods.rst

   class Pokemon():
       attack = 12
       defense = 10
       hp = 15
    
       def __init__(self, name,level = 5):
           self.name = name
           self.p_type = "Normal"
           self.level = level
           self.weak = "Normal"
           self.strong = "Normal"
    
       def train(self):
           self.update()
           self.attack_up()
           self.defense_up()
           self.hp_up()
           self.level = self.level + 1
           if self.level%self.evolve == 0:
               return self.level, "Evolved!"
           else:
               return self.level
    
       def attack_up(self):
           self.attack = self.attack + self.attack_boost
           return self.attack
    
       def defense_up(self):
           self.defense = self.defense + self.defense_boost
           return self.defense
    
       def hp_up(self):
           self.hp = self.hp + self.hp_boost
           return self.hp

       def update(self):
           self.hp_boost = 5
           self.attack_boost = 3
           self.defense_boost = 2
           self.evolve = 10
        
       def __str__(self):
           self.update()
           return "Pokemon name: {}, Type: {}, Level: {}".format(self.name, self.p_type, self.level)

       def opponent(self):
           self.update()
           if self.p_type == "Grass":
               self.weak = "fire"
               self.strong = "water"
           elif self.p_type == "Ghost":
               self.weak = "dark"
               self.strong = "psychic"
           elif self.p_type == "Fire":
               self.weak = "water"
               self.strong = "grass"
           elif self.p_type == "Flying":
               self.weak = "electric"
               self.strong = "fighting"
           return self.weak, self.strong
    
   class Grass(Pokemon):
       attack = 15
       defense = 14
       hp = 12
    
       def update(self):
           self.hp_boost = 6
           self.attack_boost = 2
           self.defense_boost = 3
           self.evolve = 12
           self.p_type = "Grass"
    
   class Ghost(Pokemon):
        
       def update(self):
           self.hp_boost = 3
           self.attack_boost = 4
           self.defense_boost = 3
           self.p_type = "Ghost"
        
   class Fire(Pokemon):
        
       def update(self):
           Pokemon.update(self)
           self.p_type = "Fire"

   class Flying(Pokemon):
       def update(self):
           Pokemon.update(self)
           self.p_type = "Flying"
  
   =====

   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

      def testOneA(self):
         self.assertEqual(Grass("Buggy").opponent(), ("fire", "water"), "Testing that Grass weak and strong are assigned to correct values.")
      def testOneB(self):
         self.assertEqual(Fire("Buggy").opponent(), ("water", "grass"), "Testing that Fire weak and strong are assigned to correct values.")
      def testOneC(self):
         self.assertEqual(Ghost("Buggy").opponent(), ("dark", "psychic"), "Testing that Ghost weak and strong are assigned to correct values.")
      def testOneD(self):
         self.assertEqual(Flying("Buggy").opponent(), ("electric", "fighting"), "Testing that Flying weak and strong are assigned to correct values.")

   myTests().main()




​


