..  Copyright (C)  Brad Miller, David Ranum, Jeffrey Elkner, Peter Wentworth, Allen B. Downey, Chris
    Meyers, and Dario Mitchell.  Permission is granted to copy, distribute
    and/or modify this document under the terms of the GNU Free Documentation
    License, Version 1.3 or any later version published by the Free Software
    Foundation; with Invariant Sections being Forward, Prefaces, and
    Contributor List, no Front-Cover Texts, and no Back-Cover Texts.  A copy of
    the license is included in the section entitled "GNU Free Documentation
    License".

Dictionary methods
------------------

Dictionaries have a number of useful built-in methods.
The following table provides a summary and more details can be found in the
`Python Documentation <http://docs.python.org/py3k/library/stdtypes.html#mapping-types-dict>`_.

==========  ==============      =======================================================
Method      Parameters          Description
==========  ==============      =======================================================
keys        none                Returns a list of the keys in the dictionary
values      none                Returns a list of the values in the dictionary
items       none                Returns a list of the key-value pairs in the dictionary
get         key                 Returns the value associated with key; None otherwise
get         key,alt             Returns the value associated with key; alt otherwise
==========  ==============      =======================================================

As we saw earlier with strings and lists, dictionary methods use dot notation,
which specifies the name of the method to the right of the dot and the name of
the object on which to apply the method immediately to the left of the dot. The empty
parentheses in the case of ``keys`` indicate that this method takes no parameters.
If ``x`` is a variable whose value is a dictionary, ``x.keys`` is the method object, and ``x.keys()`` invokes the method, returning a value.

The keys method returns a list of the keys, not necessarily in the same order they were added to the dictionary or any other particular order.

.. activecode:: chp12_dict6
    
    inventory = {'apples': 430, 'bananas': 312, 'oranges': 525, 'pears': 217}  
  
    for akey in inventory.keys():     # the order in which we get the keys is not defined
       print "Got key", akey, "which maps to value", inventory[akey]     
       
    ks = list(inventory.keys())
    print ks

    
It's so common to iterate over the keys in a dictionary that you can
omit the ``keys`` method call in the ``for`` loop --- iterating over
a dictionary implicitly iterates over its keys.

.. activecode:: chp12_dict7
    
    inventory = {'apples': 430, 'bananas': 312, 'oranges': 525, 'pears': 217}  
    
    for k in inventory:     
       print "Got key", k

 
The ``values`` and ``items`` methods are similar to ``keys``. They return lists of objects which can be iterated over.  Note that the item objects are tuples containing the key and the associated value.

.. activecode:: chp12_dict8
    
    inventory = {'apples': 430, 'bananas': 312, 'oranges': 525, 'pears': 217}  
    
    print list(inventory.values())
    print list(inventory.items())

    for k in inventory:
        print "Got",k,"that maps to",inventory[k]
    
    
The ``in`` and ``not in`` operators can test if a key is in the dictionary:

.. activecode:: chp12_dict9
    
    inventory = {'apples': 430, 'bananas': 312, 'oranges': 525, 'pears': 217}
    print 'apples' in inventory
    print 'cherries' in inventory

    if 'bananas' in inventory:
        print inventory['bananas']
    else:
        print "We have no bananas"
     

This operator can be very useful since looking up a non-existent key in a
dictionary causes a runtime error.

The ``get`` method allows us to access the value associated with a key, similar to the ``[ ]`` operator.
The important difference is that ``get`` will not cause a runtime error if the key is not present.  It
will instead return None.  There exists a variation of ``get`` that allows a second parameter that serves as an alternative return value
in the case where the key is not present.  This can be seen in the final example below.  In this case, since "cherries" is not a key, return 0 (instead of None).

.. activecode:: chp12_dict10
    
    inventory = {'apples': 430, 'bananas': 312, 'oranges': 525, 'pears': 217}
    
    print inventory.get("apples")
    print inventory.get("cherries")

    print inventory.get("cherries",0)




.. note::

    This workspace is provided for your convenience.  You can use this activecode window to try out anything you like.

    .. activecode:: scratch_11_02


**Check your understanding**

   
.. mchoicemf:: test_question11_3_2
   :answer_a: 2
   :answer_b: 0.5
   :answer_c: bear
   :answer_d: Error, divide is not a valid operation on dictionaries.
   :correct: a
   :feedback_a: get returns the value associated with a given key so this divides 12 by 6.
   :feedback_b: 12 is divided by 6, not the other way around.
   :feedback_c: Take another look at the example for get above.  get returns the value associated with a given key.
   :feedback_d: The integer division operator is being used on the values returned from the get method, not on the dictionary.
   
   
   What is printed by the following statements?
   
   .. sourcecode:: python

     mydict = {"cat":12, "dog":6, "elephant":23, "bear":20}
     answer = mydict.get("cat")//mydict.get("dog")
     print answer

   
   
.. mchoicemf:: test_question11_3_3
   :answer_a: True
   :answer_b: False
   :correct: a
   :feedback_a: Yes, dog is a key in the dictionary.
   :feedback_b: The in operator returns True if a key is in the dictionary, False otherwise.
   
   What is printed by the following statements?
   
   .. sourcecode:: python

     mydict = {"cat":12, "dog":6, "elephant":23, "bear":20}
     print "dog" in mydict



.. mchoicemf:: test_question11_3_4
   :answer_a: True
   :answer_b: False
   :correct: b
   :feedback_a: 23 is a value in the dictionary, not a key.  
   :feedback_b: Yes, the in operator returns True if a key is in the dictionary, False otherwise.
   
   What is printed by the following statements?
   
   .. sourcecode:: python

      mydict = {"cat":12, "dog":6, "elephant":23, "bear":20}
      print 23 in mydict



.. mchoicemf:: test_question11_3_5
   :answer_a: 18
   :answer_b: 43
   :answer_c: 0
   :answer_d: 61
   :correct: b
   :feedback_a: Add the values that have keys longer than 3 characters, not those with exactly 3 characters.
   :feedback_b: Yes, the for statement iterates over the keys.  It adds the values of the keys that have length greater than 3.
   :feedback_c: This is the accumulator pattern.  Total starts at 0 but then changes as the iteration proceeds.
   :feedback_d: Not all the values are added together.  The if statement only chooses some of them.
   
   
   What is printed by the following statements?
   
   .. sourcecode:: python

      total = 0
      mydict = {"cat":12, "dog":6, "elephant":23, "bear":20}
      for akey in mydict:
         if len(akey) > 3:
            total = total + mydict[akey]
      print total
   


.. index:: aliases

