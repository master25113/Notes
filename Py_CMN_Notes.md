# Day 1 - Python Marathon Part 1

## My_Notes:
```
* Topics:
    - Primitive Datatypes & Operators

    - Variables & Collections

    - Control flow & Iterables

    - Functions

    - Modules (Libs or Third part libs and others packages)

    - Class (OOPS)
        > Inheritance

    - Some Advanced Stuffs

* Python is High Level General Purpose Languages | About Python and Its History

* About Interpreter and Compile
    In INTERPRETER Clear Screen >>> import os
                                >>> os.system("clear)


* About Comments:
    - # Single line Comment
    
    -   """
        Multi line Comment
        """

* Numbers
    In interpreter >>> 1+2*3
                   >>> 9
                    
* Primitive Operators
    +, -, *, /(Float division), //(Int divison), %(Modulo), **(Exponent)

    Order Of Execution:
        BODMAS (Border/Function, Order/Exponent, Multiplication, Addition, Subtraction)

* BOOLEAN (0/1) [CASE SENSITIVE]
    In Interpreter >>>
        True 
        True 

        True + False
        1

* Comparision Operator:
    ==, !=, <, >, >=, <= 

    is ---> Checks if both var has same ref (only specific to Python)
        id - is the function for shows location it where stored
	Only numbers till 256 - This caching is done by Python's memory optimization to avoid creating multiple objects for frequently used small integers. 
        >>> id(a)
            10869672
    
    >>> a=10
    >>> id(a)
        10869672
    >>> b=10
    >>> id(b)
        10869672
    >>> a is b
        True

* Chaining Comparision:
    Gates : 
        AND - 1 & 1 (True & True)
        OR - 1 or 0 (True or False)
        NOT - not True -> False | O ---> 1 | 1 --->0 (True ---> False)

* Append 
    >>> a = [1,2]
    >>> a
        [1, 2]
    >>> a.append(4)
    >>> a
        [1, 2, 4]

```

## Code:
``` No Code Folder ```


___
---
***


# Day 2 - Python Marathon Part 2

## My_Notes:
```
* Data Types
    Core Datatypes - Int, Float, Boolean & String
    Collections - List, Tuple, Dictionary & Set
    
* Data Type Memory Management
   Mutable - Variable can modify (at same address) 
   unMutable - Variable cannot modify (at same address ) 

* Datatype:
    Int (1,2,3,4...)
    Float (1.0,1.1,...)
    Boolean (0 or 1)
    Single Line String - "Hi" or 'Hi' | ex: a = 'Hi'
    Multi Line String - """ Hello
                            Everyone"""


* id function in String:
    ex:
        >>> a = "hello"
        >>> b = "hello"
        >>> a is b
        True
    
    ex:
        >>> a = "hello Everyone"
        >>> b = "hello Everyone"
        >>> a is b
        False

    In string, Why Space after it changes of its address because of Python Identifiers
    In first 256 number - Satic Identifiers 

* String : Immutable
   Indexing
        a = "Hello World"
        a[0] = H
        a[6] = W
        a[5] = ' '
        a[-1] = d

* List : Mutable
    Indexing
        a = [1, 2, 3, 4]
        a[0] = 1
        a[1] = 2

* Memory Management : Datatype
    Int = Immutable
        Address = I
        Data = I
    
    Float = Immutable
        Address = I
        Data = I

    String = Immutable
        Address = M
        Data = I

    List = Mutable
        Address = I
        Data = M

    Here, Address = No Change & Value = Only Change ==> Mutable

    In String, You wont change single Character but you can change Entire String
        >>> a = "hello"
        >>> a
        'hello'
        >>> a[1]
        'e'
        >>> a[1] = f
        Traceback (most recent call last):
        File "<stdin>", line 1, in <module>
        NameError: name 'f' is not defined
        >>> a = "fello"
        >>> a
        'fello'

* In String 
    >>> name = "Batman"
    >>> msg = f"Bruce Wyane is {name}"      #f - format and this syntax is available after 3.6v of python
    >>> msg
    'Bruce Wyane is Batman'

    >>> msg = "Bruce Wyane is {name}".format(name=name)
    >>> msg
    'Bruce Wyane is Batman'

    >>> msg = "Bruce Wyane is {}".format(name)
    >>> msg
    'Bruce Wyane is Batman'

* String Contanination 
    >>> e = "hello" "world"
    >>> e
    'helloworld'

    >>> a = "hello"
    >>> b = "world"
    >>> c = a+b
    >>> c
    'helloworld'

    >>> d = a + " " + b
    >>> d
    'hello world'

    >>> f = a + "@" + c + ".com"
    >>> f
    'hello@helloworld.com'

    >>> b ="{host}"
    >>> a + "@" + b.format(host="google") + ".com"
    'hello@google.com'

```

## Code:
``` No Code Folder ```


___
---
***



# Day 3 - Python Marathon Part 3

## My_Notes:
```
* Sibi Bro refered W3S & Devdos for Learning & Reference

* How to find function?
    In Maths -> f(x) = x^2 ==> function of x

    print("Hi") | print --> function name | Hi --> Argument : String
    convertToPdf("map.pdf")

* Sibi bro refered devdocs.io website

* About input function #only supported in terminal environment
    >>> s = input("Say your name?")
    Say your name?kabil yugan
    >>> s
    'kabil yugan'

* Variables & Collections

    Variables: Variable can store data

    Collections : list, Tuple, Dictionary & Set
    Collections are not datatype and its a holder | It holds different datatypes
    It can store multiple variables
    But in Core dataypes only one variable can store

* Looking at OOPS
        
          Object 
         |      |
         |      |
      Methods  Members     
       
    Object:
    (1) Methods (Functions)
            tapToMute(), setLight()
            volumeSet(), noiseCancelation()
 
    (2) Members (Properties, Variable, other objects)  
        Inside Object It called as Properties & Outside Object It is called as variable
            Manufracture : Boat
            Interface : USB C
            Light : RGB
            Mode : A/B/C/D
            Color : RCB/White/Black

    In Python (OOPS)
        m = mic() | m is Object instance (variable) | mic() is Class
        print("Manufractue is {}",format(m.Manufracture))
        m.setAudioGain(50)

* Higher Order Function
    In Python, Higher Order Function means We in Outside then Object passed to Function
        ex:len(i) here len is higher order function and i is object 
    In Normal function, object is there then call onjects method
        ex:a.append here a is object and append id objects's method


    Its puposes is Type casting
    Ex: int(20) and here 20 is string and string to int convertion (typecasting)
    int()
    float()
    str()
    bool()
    list()
    tup()
    dict()
    set()

    type() function - it returns the datatype of the argument
        >>> a = 1
        >>> type(a)
        <class 'int'>

        >>> d = "1,2,3,4"
        >>> type(d)
        <class 'str'>
        >>> d = list(d)
        >>> d
        ['1', ',', '2', ',', '3', ',', '4']
        >>> 

        >>> i
        'boolean_text'
        >>> i = bool(i)
        >>> i
        True
        bool() typecast is used to find content is available or not in string

* Collections
    Lists:
            #Creating Empty List
            l = list or l = []      

            #Initialize With Contents
            >>> l = list([1,2,"hello",3.14,[12,13,14]])    
            >>> l
            [1, 2, 'hello', 3.14, [12, 13, 14]]

            >>> a = "hello"
            >>> a=list(a)
            >>> a
            ['h', 'e', 'l', 'l', 'o']

            #Accessing Elements in List       
            >>> l
            [1, 2, 'hello', 3.14, [12, 13, 14]]
            >>> l[2]
            'hello' 
            >>> l[2][1]
            'e'

            >>> l[-1][1]
            13

            len() function - To find length
                >>> len(l)
                5
                >>> len(l[4])
                3

                >>> a=1234
                >>> len(str(i))
                4
                
                >>> a=12.34
                >>> len(str(i))
                4

                >>> i = 10*"a"
                >>> i
                'aaaaaaaaaa'
                >>> len(i)
                10

            #list reverse
                >>> i = list("helloworld")
                >>> i
                ['h', 'e', 'l', 'l', 'o', 'w', 'o', 'r', 'l', 'd']
                >>> i.reverse()
                >>> i
                ['d', 'l', 'r', 'o', 'w', 'o', 'l', 'l', 'e', 'h']

            #Add items to End of a list
                >>> l.append(1)
                >>> l
                [1, 2, 'hello', 3.14, [12, 13, 14], 1]
                

            #Remove items in list
            >>> l
            [1, 'hello', 3.14, [12, 13, 14], 1]
            >>> l.pop() #it removes last element
            1
            >>> l.pop(2) #it removes 3rd element
            3.14
            >>> l
            [1, 'hello', [12, 13, 14]]

            #Adding Multiple elements
            >>> a
            ['h', 'e', 'l', 'l', 'o']
            >>> a.extend([1,2,3,4,'a'])
            >>> a   
            ['h', 'e', 'l', 'l', 'o', 1, 2, 3, 4, 'a']

            #Copy Function
                #Here Not using copy()
                >>> a
                ['h', 'e', 'l', 'l', 'o', 1, 2, 3, 4, 'a']
                >>> b =a
                >>> b
                ['h', 'e', 'l', 'l', 'o', 1, 2, 3, 4, 'a']
                >>> b.append(1)
                >>> b
                ['h', 'e', 'l', 'l', 'o', 1, 2, 3, 4, 'a', 1]
                >>> a
                ['h', 'e', 'l', 'l', 'o', 1, 2, 3, 4, 'a', 1]

                #Here using copy()
                >>> c = b.copy()
                >>> c.append("leo")
                >>> b
                ['h', 'e', 'l', 'l', 'o', 1, 2, 3, 4, 'a', 1]
                >>> c
                ['h', 'e', 'l', 'l', 'o', 1, 2, 3, 4, 'a', 1, 'leo']
``` 

## Code:

### inputFunction.py

``` Python
import os

while True:
    cmd = input("$ ") #Using Input function
    os.system(cmd)

"""
Output:
    $ python3 inputFunction.py 
        $ pwd
        /home/ky/Learning/SNA/sna-notes/PYTHON/day3/code
        $ ls
        inputFunction.py
""'
```



___
---
***



# Day 4 - Python Marathon Part 4

## My_Notes:
```
* Iterable - It has index and we can traverse | Traverse means a b c d are available we can move AtoB BtoC CtoD

* Slicing - If index available then slicing is possible
    #This syntax already we know because it is common thing
    var[index] => value
        >>> a
        [1, 2, 3, 4]
        >>> a[1]
        2

    #This is rare syntax because it is py only syntax
    var[start;stop-1:step] => list/collections 
    Default values - start=0, stop=len(), step=1
        >>> a
        [1, 2, 3, 4, 5, 6, 7, 8, 9]
        >>> a[1:5:1] #var[start;stop-1:step] 
        [2, 3, 4, 5]

        >>> a[1:5] #here not mentioned step value but step is default by 1
        [2, 3, 4, 5]
         
        >>> a[0:8:2] 
        [1, 3, 5, 7]

        >>> a[len(a):0:-1]
        [9, 8, 7, 6, 5, 4, 3, 2]

        >>> a[::-1]
        [9, 8, 7, 6, 5, 4, 3, 2, 1]

        >>> a[::1]
        [1, 2, 3, 4, 5, 6, 7, 8, 9]

        >>> a[1:len(a):1] 
        [2, 3, 4, 5, 6, 7, 8, 9]

        >>> a[0:len(a):1]
        [1, 2, 3, 4, 5, 6, 7, 8, 9]

    Copy() function alternative
        >>> a
        [1, 2, 3, 4, 5, 6, 7, 8, 9]
        >>> b=a
        >>> id(a)
        139642088357952
        >>> id(b)
        139642088357952
        >>> b = a.copy()
        >>> id(a)
        139642088357952
        >>> id(b)
        139642086991232

        #Alternative of copy
        >>> b=a[::1] #this process called deep copy or shadow copy
        >>> id(a)
        139642088357952
        >>> id(b)
        139642086972224

        copy() - is used for immutable things
        deepcopy() - is used for mutable things | import copy #its lib so import fist | it is deep layer copy
        
* Formating in string
    >>> s = "#{} : l->{}, ID->{}"
    >>> s
    '#{} : l->{}, ID->{}'
    >>> s.format(1, 2, 3)
    '#1 : l->2, ID->3'

* The 'del' keyword - it will delete an item
    #Removing item by value instead of index
    >>> u
    [1, 2, 3, 4, 5, [6, 66, 666], 7, 8, 9]
    >>> u.remove(3)
    >>> u
    [1, 2, 4, 5, [6, 66, 666], 7, 8, 9]

    #del keyword used to delete both items and variable also
    >>> u
    [1, 2, 3, 4, 5, [6, 66, 666], 7, 8, 9]
    >>> del u[8] #It delete by index of 8
    >>> u
    [1, 2, 3, 4, 5, [6, 66, 666], 7, 8]
 
    >>> u
    [1, 2, 3, 4, 5, [6, 66, 666], 7, 8]
    >>> u
    [1, 2, 3, 4, 5, [6, 66, 666], 7, 8]
    >>> del u #Delete a declared variable
    >>> u
    Traceback (most recent call last):
    File "<stdin>", line 1, in <module>
    NameError: name 'u' is not defined

* The 'in' keyword - value is in list or not
    >>> a = list(range(10))
    >>> a
    [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
    >>> 4 in a
    True
    >>> "hello" in a
    False

* + Operator with list - lists will merge
    >>> n = list([1,2,3,4,5,6])
    >>> m = list([5,6,7,8,9,0])
    >>> o = n+m
    >>> o
    [1, 2, 3, 4, 5, 6, 5, 6, 7, 8, 9, 0]

* CURD
    Items in list or tuples are example for Mutable and Immutable
    Create, Update/Edit, Read, Delete => Mutable
    Create & Read => Immutable

* Tuples - typle are the immutable list 
    #Create a Empty tuple
    >>> t = tuple()
    >>> t = ()

    #Create a tuple with single item
    >>> t = (1,) #why we use (1,) [comma] because python follow basic rule of bodmass ((1)) it prints 1 and it cannot break the rule
    >>> t
    (1,)

    >>> t = tuple((1,))
    >>> t
    (1,)

    #In tuple inside add the list and edit the list
    >>> t
    (1, 2, 3, 4, [5, 55, 555], 6, 7)
    >>> t[4]
    [5, 55, 555]
    >>> t[4].append(5555)
    >>> t
    (1, 2, 3, 4, [5, 55, 555, 5555], 6, 7)

    In Tuple brackets() not requied 
    >>> t = 1,2,3,4 #Here not used brackets()
    >>> type(t)
    <class 'tuple'>

    Packing and Unpacking: (This syntax will works on both tuples & lists)
        Packing - Becoming the tuple

        #Type 1 UNPACK
            a=0
            b=0
            c=0
            t=(1,2,3)
            a,b,c=t #3<-Unpack->3
            1,2,3=t | a=1,b=2,c=3
            #In Program
                >>> a=0
                >>> b=0
                >>> c=0
                >>> t=(1,2,3)
                >>> a,b,c=t
                >>> a
                1
                >>> b
                2
                >>> c
                3

        #Type 2 UNPACK
            >>> t=(1,2,3,4,5,6,7,8)
            >>> a,*b,c=t
            >>> a
            1
            >>> b
            [2, 3, 4, 5, 6, 7]
            >>> c
            8

        #Type 2 UNPACK
            #Swaping Variables A & B
                Ordinary Swap - Using Temporvary Variables
                    c=a
                    a=b
                    a=c

            #Swaping by Unpacking of tuple
                >>> a=1
                >>> b=2
                >>> a,b=(b,a) (or) >>> a,b=b,a
                >>> a
                2
                >>> b
                1

* Dictionaries 
    Dictionary is not iterable(not have  index) and only acces bt key value pair
    #Creating the empty Dictionaries
        >>> d = {}
        >>> d
        {}
        >>> d = dict()
        >>> d
        {}
        >>> type(d)
        <class 'dict'>
    
    #Creating Dictionary with data
        Key : Immutable datatype (int, float, string, Boolean & other immutables objects)
        >>> d[True]
        'yes'
        >>> d[0]
        'no'

        >>> d = { 1 : "vijay", 2 : "thalapthy"}
        >>> d[1]
        'vijay'
        >>> d[2]
        'thalapthy'

        >>> d = { True : "yes", False : "no", None : "nooo", "hello" : "hi"}
        >>> d[None]
        'nooo'
        >>> d["hello"]
        'hi'

        In Dictionary
            It is mutable (A:M, D:M)
            Every Key value (all immutable data types) must be hased and add extra table in hash table for To do Dictionary Operaton | { "user" : "kabil" : a81be4e9b20632860d20a64c054c4150} in dict hash table
            Hasing - Cannot reverse it and ONE way algorithm (like fingerprint)
                MD5 - 32bit
                >>> "a"*100
                'aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa'
                $ echo "aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa" | md5sum
                f363362e71acf8e1eaf7678cdb5c4928
            
             #"in" Keyword in Dictionary
                It is applied for only key not for value
                >>> d
                {'one': 1, 'two': 2}
                >>> "one" in d
                True

             #The keyword "del" in Dictionary
                It will delete the pair
                >>> d
                {'one': 1, 'two': 2}
                >>> del d["one"]
                >>> d
                {'two': 2}
                            
            #get() Method - pass key it give you a value
                >>> d.get(1)
                'one'
            
            #items() method in Dictionary
                >>> d.items()
                dict_items([(1, 'one'), (2, 'two'), (3, 'three')])
                >>> list(d.items())
                [(1, 'one'), (2, 'two'), (3, 'three')]

            #pop() method in Dictionary
                >>> d
                {1: 'one', 2: 'two', 3: 'three'}
                >>> d.pop(1)
                'one'
                >>> d
                {2: 'two', 3: 'three'}

            #update method in Dictionary
            >>> d
            {2: 'two', 3: 'three'}
            >>> d.update({2:"five"})
            >>> d
            {2: 'five', 3: 'three'}
            >>> d
            {2: 'five', 3: 'three'}

            >>> d['3'] = "seven"
            >>> d
            {2: 'five', 3: 'three', '3': 'seven'}


            #keys() & values() methods in Dictionary
            >>> d.keys()
            dict_keys([2, 3, '3'])
            >>> d.values()
            dict_values(['five', 'three', 'seven'])

            #packing & unpacking in Dictionary
                >>> d
                {1: 'one', 2: 'two', 3: 'three', 4: 'four'}
                >>> a,*b,c = d #In here only unpack keys
                >>> a
                1
                >>> b
                [2, 3]
                >>> c
                4

            #Adding 2nd Dictionary to 1st Dictionary
                >>> z = {'a':1,'b':2}
                >>> x = {'c':3}
                >>> z = {'a':1,'b':2, **x}
                >>> z
                {'a': 1, 'b': 2, 'c': 3}
 
                >>> z
                {'a': 1, 'b': 2, 'c': 3}
                >>> x = {'c':3, 'a':8, 'd':6}
                >>> z = {'a':1,'b':2, **x}
                >>> z
                {'a': 8, 'b': 2, 'c': 3, 'd': 6}

* Sets - These are just mathematical sets
    Value less Dictionary and duplicate items not possible
    values are immutable data types
        #Creating empty set
            >>> es = set()
            >>> type(es)
            <class 'set'>

        #Cannot store duplicates vlaues/items in sets
            >>> s = {1,2,3,4,5,1,2,3,6}
            >>> s
            {1, 2, 3, 4, 5, 6}
            >>> type(s)
            <class 'set'>

        #Add a new items in sets
            >>> s
            {1, 2, 3, 4, 5, 6}
            >>> s.add(7)
            >>> s
            {1, 2, 3, 4, 5, 6, 7}

    Set Operations:
        It is mutable (A:I, D:M)
        It is not Iterable
        Set Operations are done by following operators
            & -> Intersection (common items)
            | -> Union (combine items)
            - -> Difference (Only gets setA items and not get setB items and not common items)
            ^ -> Symmetric Difference (Except common items)
            >= -> Its superset | It take 2 operand sets and return boolean
            <= -> Its subset | It take 2 operand sets and return boolean
 
        #Intersection (&) in sets
            >>> s = {1,3,4,5,6,9}
            >>> d = {1,3,6,7,8,9}
            >>> type(s)
            <class 'set'>
            >>> type(d)
            <class 'set'>
            >>> s & d
            {1, 3, 6, 9}

        #Union (|) in sets
            >>> s | d
            {1, 3, 4, 5, 6, 7, 8, 9}

        #Difference (-) in sets
            >>> s - d
            {4, 5}

        #Symmetric Difference (^) in sets
            >>> s ^ d
            {4, 5, 7, 8}

        #superset & subset in set
            >>> {1,2} >= {1,2,3} #This is not superSet (setA is not superSet of setB)
            False

            >>> {1,2} <= {1,2,3} #This is subSet (setA is subset of setB)
            True

            >>> {1,2,3,4,5,6} >= {1,2,3} #This is SuperSet (setA is superset of setB)
            True

            >>> {1,2,3,4,5,6} <= {1,2,3} #This is not subset (setA is not subSet of setB)
            False
```

## Code:
``` No Code Folder ```



___
---
***



# Day 5 - Python Marathon Part 5

## My_Notes:
```
* Control flow & Iterables
    In If Else, Colon (:) - Block Of Code
    Indentation - It is a whitespaces(space or tab)

* Loops:
    For loop - Finite loops | For is used to deal with structured data
    While loop - Infinite & Finite Loops | While is used to deal with raw things and manual and unstructured data

    While loop - Infinite loops
        It will execute again and again untill the <condition> become False
        Loop shoud be constructed with 3 things
            (1) Initialize -> var = 10
            (2) Condition -> var <=10
            (3) Update Code -> var = var - 1

        #while Loop -> Infinite loop
            var = 10
            while var <=10 and var >= 0: #Infinite loops
                print("#{} Hello World".format(var))

            print("loop exited")

        ##while Loop -> Finite loop
            var = 10
            while var <=10 and var >= 0: #Finite loops
                print("#{} Hello World".format(var))
                var = var -1
            print("loop exited")

    For Loop
        #In here we can use it also without condition just with var i
            >>> for i in [1,2,3,4,5]:
            print(i)
            1
            2
            3
            4
            5

    range() function in loops
        >>> print(list(range(0,100)))
        [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33, 34, 35, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50, 51, 52, 53, 54, 55, 56, 57, 58, 59, 60, 61, 62, 63, 64, 65, 66, 67, 68, 69, 70, 71, 72, 73, 74, 75, 76, 77, 78, 79, 80, 81, 82, 83, 84, 85, 86, 87, 88, 89, 90, 91, 92, 93, 94, 95, 96, 97, 98, 99]
    
        for i in range(20,100):
        print(i)
    
    Break in Python loops
        for i in range(20,100):
        print(i)
        if i >=60:
            break
    
    Continue in Python loops - it used for skiping | 
        #skip even numbers
            for i in range(25,50):
                if i % 2 == 0: #Even Numbers
                    continue
                else:
                    print(i)
                    print("This is printed only for ODD numbers")

            print("loop exited")

    #Even number  printing in py
        for i in range(1,100):
            if i % 2 == 0:
                print("Even number : {}".format(i))

    #Odd number printing in py
        for i in range(1,100):
            if not i % 2 == 0:
                print("ODD number : {}".format(i))

* Enumeration
    L = ["a","b","c"]
          0   2   3
        
        l = ['a', 'b', 'c']

        #Enumeration in py
            for i, value in enumerate(l):
                print("{} {}".format(i,value))

            $ python3 enumeration.py 
            0 a
            1 b
            2 c

```

## Code:

### if_else.py
```Python
var = 10
if var > 10:
    print("It is greater than 10")
elif var < 10:
    print("It is less than 10")
else:
    print("what is this?")

"""
Output:
    $ python3 if_else.py 
    what is this?
"""
```

### if_else.py
```Python
var = 10
while var <=10 and var >= 0: #Finite loops
    print("#{} Hello World".format(var))
    var = var -1
print("loop exited")

"""
Output:
    var = 10
    while var <=10 and var >= 0: #infinite loops
        print("#{} Hello World",format(var))

    print("loop exited")
"""
```

### forLoop.py
```Python
l = ['apple', 'orange', 'banana']
#In here For loop, we can use it also without condition just with var i
for v in l:
    print("I am eating {}".format(v))

"""
Output:
    $ python3 forLoop.py 
    I am eating apple
    I am eating orange
    I am eating banana
"""
```

### break_in_python_loops.py
```python
for i in range(20,40):
        print(i)
        if i >=30:
            break

"""
Output:
    $ python3 break_in_python_Loops.py 
    20
    21
    22
    23
    24
    25
    26
    27
    28
    29
    30
"""
```
    
### continue_in_python_loops.py
```python
for i in range(25,50):
    if i % 2 == 0: #Even Numbers
        continue
    else:
        print(i)
        print("This is printed only for ODD numbers")

print("loop exited")

"""
Output:
    $ python3 continue_in_python.py 
    25
    This is printed only for ODD numbers
    27
    This is printed only for ODD numbers
    29
    This is printed only for ODD numbers
    31
    This is printed only for ODD numbers
    33
    This is printed only for ODD numbers
    35
    This is printed only for ODD numbers
    37
    This is printed only for ODD numbers
    39
    This is printed only for ODD numbers
    41
    This is printed only for ODD numbers
    43
    This is printed only for ODD numbers
    45
    This is printed only for ODD numbers
    47
    This is printed only for ODD numbers
    49
    This is printed only for ODD numbers
    loop exited
"""
```

### odd_even_in_loops.py
```python
for i in range(1,10):
    if i % 2 == 0:
        print("Even number : {}".format(i))

for i in range(1,10):
    if not i % 2 == 0:
        print("ODD number : {}".format(i))

"""
Output:
    Even number : 2
    Even number : 4
    Even number : 6
    Even number : 8
    ODD number : 1
    ODD number : 3
    ODD number : 5
    ODD number : 7
    ODD number : 9
"""
```

### enumeration.py
``` python
l = ['a', 'b', 'c']

for i, value in enumerate(l):
    print("{} {}".format(i,value))

"""
Output:
    $ python3 enumeration.py 
    0 a
    1 b
    2 c
"""
 ```



___
---
***



# Day 6 - Python Marathon Part 6

## My_Notes:
```
* Exception Handling:
    Error are the object and its a message

    try:
        code..  #In Here, The code which may rise errors
        ......
        ......
        
    except:
        code..
        ......
        ......

    #Sample Example : try except - error handling
        try:
        c = a + b
        except:
            print("some error happend")

* Pass in python
    It is used to continue the empty block
    It is used for skiping 

    try:
        .....
        .....
    except:
        pass


* Iterables:
    iter() - make the iterator out of an iterable datatype
    next() - gives the next in list


* File Handling:
    open() - It is Buit IN Function
        example:
        file_name = input("Enter file name or path to read : ")
        f = open(file_name, 'r')
        print(f.read())
        f.close()





```

## Code:

### try_except_errorHandling.py 
``` Python
try:
    c = a + b
except:
    print("some error happend")

"""
Output:
    $ python3 try_except_errorHandling.py 
    some error happend
""""
```

### try_except2.py 

```python
import sys

try:
    c= a+b
except:
    print("unexpected error: ",sys.exc_info()[0])

"""
Output
    $ python3 try_except2.py 
    unexpected error:  <class 'NameError'>
"""
```

### try_except3.py 

```python
import sys

a = 10
b = [1,2,3,4,5,6]
c = 5

def divide(a,b):
    if b == 0:
        raise Exception("Cannot divide by zero")
    return a/b
    
try:
    c = divide(5,0)
    print("The value of c is {}".format(c))
    raise IOError("This is sample error")

except NameError as e:
    print("Name error happened : {}".format(e))

except IndexError as e:
    print("Index error happened : {}".format(e))

except Exception as e:
    print("Something else... : {}".format(e))
    print("Error: {}".format(sys.exc_info()[0]))

else:
    print("All Good")

finally:
    print("Whatever the case is, I will works") #In finally block it is used for if i opened file then i want to close and something like this

"""
Output
    $ python3 try_except3.py 
    Something else... : Cannot divide by zero
    Error: <class 'Exception'>
    Whatever the case is, I will works
"""
```

### iter.py 

```python
l = [1,2,3,4,5]
d = {"a" : "b", "c" : "d", "e" : "f"}
for i in iter(l):
    print(i)
for i in iter(d):
    print(i)

"""
Output:
    python3 iter.py 
    1
    2
    3
    4
    5
    a
    c
    e
""""
```

### next.py 

```python
l = [1,2,3,4,5]
l = iter(l) #we want to wrap the l to iter method and then only it works

print(next(l))
print(next(l))
print(next(l))
print(next(l))
print(next(l))

"""
Output:
    $ python3 next.py 
    1
    2
    3
    4
    5
"""
```

### FileHandling_READ.py 

``` Python
file_name = input("Enter file name or path to read : ")
f = open(file_name, 'r')
print(f.read())
f.close()


"""
Output:
    $ python3 FileHandling_READ.py 
    Enter file name or path to read : temp.txt
    one
    two
    three
    four
    five
    six
    seven
    eight
    nine
    ten

    0
    1
    2
    3
"""
```

### FileHandling_READ2.py

```python
file_name = input("Enter file name or path to read : ")
f = open(file_name, 'r')
i = 0
while i<5:
    print(f.readline())
    i = i+1
f.close()


"""
Output:
$ python3 FileHandling_READ2.py 
    Enter file name or path to read : temp.txt
    one

    two

    three

    four

    five

"""
```

### FileHandling_READ3.py

``` python
file_name = input("Enter file name or path to read : ")
f = open(file_name, 'r')
i = 0
line =  f.readline()
while line:
    print(line, end='')
    i = i+1
    if i == 10:
        op = input("Read More or Not -> [n]: ")
        if op == 'n':
            print("Exiting.")
            break
        i = 0  # Reset counter to prompt every 10 lines
    line = f.readline()
f.close()


"""
Output:
    $ python3 FileHandling_READ3.py
    Enter file name or path to read : temp2.txt
    1
    2
    3
    4
    5
    6
    7
    8
    9
    10
    Read More or Not -> [n]: y
    11
    12
    13
    14
    15
    16
    17
    18
    19
    20
    Read More or Not -> [n]: n
    Exiting.
"""
```



___
---
***



# Day 7 - Python Marathon Part 7

## My_Notes:
```
* Functions
    - Group of Instructions given to a computer to do a meaningful task
    - Use "def" keyword to create new functions
        def add(x, y):
            z = x + y
            print("Result is {}".format(z))
            return z

* Variable Scopes - Local and Global
    Ex:
        x = 10
        def set_global_x(num):
        global x
        print("Before Set Globally x = {}".format(x))
        x = num
        print("Globally x = {}".format(x))

* First Class Functions
    - Function inside another function and its is called nested function in other programing lanugages
    - OOPS not known people use this First Class Functions
    - It looks like CLASS so its named First Class Function
        ex:
            def create_adder(x):
                def adder(y):
                    return x+y
                return adder
            add_40 = create_adder(40)   #A function instance with x=40 s created and saved
            print(add_40(100))

* Anonymous Function (Lambda Function)
    - It is used in Higher Order Function inside
        In Ordinary Function
            def check(x):
                return x > 3
            print(check(5))


        In Lambda Function
            >>> (lambda x : x>3)(5)
            True

            y = lambda x: x>3
            print(y(5))

* map()
    The map() function in Python applies a function to each item in an iterable (like a list) and returns a map object, which you can convert to a list or iterate over.

    print(list(map(add_40,l)))
   
    print(list(map((lambda x : x>3)(5))))

* filter()
     filter() is similar to map(), but instead of transforming items, it filters them based on a condition (a function that returns True or False)
        ex:
        def fil(x):
        return x >= 1000
        l = [100,500,1000,1024]
        print(list(filter(fil, l)))
        Output:
        [1000, 1024]
```

## Code:

### function_add.py
``` Python
#!/bin/bash

def add(x, y):
            z = x + y
            print("Result is {}".format(z))
            return z

a = int(input("Enter number 1 : "))
b = int(input("Enter number 2 : "))
print("Addition of {} and {} is {}".format(a, b, add(a,b)))

"""
Output:
    $ python3 function_add.py 
    Enter number 1 : 10
    Enter number 2 : 20
    Result is 30
    Addition of 10 and 20 is 30
"""
```

### function_basicMath.py
``` Python
def basicMath(x, y):
            a = x + y
            b = x - y
            c = x * y
            d = x / y
            #e = [a, b, c, d]
            #return e
            return a, b, c, d

a = int(input("Enter number 1 : "))
b = int(input("Enter number 2 : "))
print("Addition of {} and {} is {}".format(a, b, basicMath(a,b)))

"""
Output:
    $ python3 function_basicMath.py 
    Enter number 1 : 10
    Enter number 2 : 20
    Addition of 10 and 20 is (30, -10, 200, 0.5)
"""
```

### function_basicMath2.py 
``` Python
def basicMath(x, y):
            a = x + y
            b = x - y
            c = x * y
            d = x / y
            return {
                "Addition" : a,
                "Substraction" : b,
                "Multiplication" : c,
                "Divison" : d,
            }

a = int(input("Enter number 1 : "))
b = int(input("Enter number 2 : "))
print("Addition of {} and {} is {}".format(a, b, basicMath(a,b)))

d = basicMath(a, b)
#d = basicMath(b = x, a = y) #keyword arguments

for i in d.keys(): #d.keys() - it returns keys of dictionary d and It is the way to iterate the dictionary
    print("{} : {}".format(i, d[i]))

"""
Output:
$ python3 function_basicMath2.py 
    Enter number 1 : 20
    Enter number 2 : 10
    Addition of 20 and 10 is {'Addition': 30, 'Substraction': 10, 'Multiplication': 200, 'Divison': 2.0}
    Addition : 30
    Substraction : 10
    Multiplication : 200
    Divison : 2.0
"""
```

### function_math.py 
``` Python
def math(x, *y): #Note : In fuction , positional arguments not give *(unpacking) in first --> def math(*x, y) - it won't work
    print(x)
    print(y)

    r = 0 
    r = r + x
    for i in y:
        r = r + i
    return r

print("Addition Result is {}".format(math(10,20,30,40,50,60)))

"""
Output:
    $ python3 function_math.py 
    10
    (20, 30, 40, 50, 60) 
    Addition Result is 210
"""
```

### function_keywordArguments.py 
```python
def keyword_arguments(i, j, k, l=20, *x, **kw_args):    #Order -> Positional args, Keyword args, Variable Positional args, Variable Keyword args 
    print(i,j,k)
    print(l)
    print(x)
    print(kw_args)
    return kw_args

keyword_arguments(1,23,4,3,556,34,48,90,9,a=1,b=2,c=4,d=5)  #Order -> Positional args, Keyword args, Variable Positional args, Variable Keyword args 

"""
Output:
    $ python3 function_keywordArguments.py 
    1 23 4
    3
    (556, 34, 48, 90, 9)
    {'a': 1, 'b': 2, 'c': 4, 'd': 5}
"""
```

### variableScope.py
```python
x = 5
def set_x(num):
	x = num
	print("Locally x = {}".format(x))

def set_global_x(num):
	global x
	print("Before Set Globally x = {}".format(x))
	x = num
	print("Globally x = {}".format(x))

print("First x = {}".format(x))
set_x(50)
print("Ouside x = {}".format(x))
set_global_x(6)
print("Ouside x = {}".format(x))

"""
	Output:
	$ python3 variableScope.py 
	First x = 5
	Locally x = 50
	Ouside x = 5
	Before Set Globally x = 5
	Globally x = 6
	Ouside x = 6
"""
```

### first_class_function.py 
```python
def create_adder(x):
    def adder(y):
        return x+y
    return adder

add_40 = create_adder(40)   #A function instance with x=40 s created and saved
print(add_40(100))

"""
Output:
    $ python3 first_class_function.py 
    140
"""
```

### map_function.py
```python
def create_adder(x):
    def adder(y):
        return x+y
    def subtractor(y):
        return x-y
    return adder, subtractor

add_40, sub_40 = create_adder(40)
add_40, sub_40 = create_adder(50)

l = [100,200,3000,4000]
for v in l:
    print(add_40(v))
    print(sub_40(v))

print(list(map(add_40,l)))
print(list(map(sub_40,l)))

"""
Output:
    $ python3 map_function.py
    150
    -50
    250
    -150
    3050
    -2950
    4050
    -3950
    [150, 250, 3050, 4050]
    [-50, -150, -2950, -3950]
"""
```

### filter_function.py 
```python
def fil(x):
    return x >= 1000
l = [100,500,1000,1024]
print(list(filter(fil, l)))

"""
output:
    $ python3 filter_function.py 
    [1000, 1024]
"""
```



___
---
***



# Day 8 - Python Marathon Part 8

## My_Notes:
```
* Modules 
    - Consider a module to be the same as a code library | A file containing a set of functions you want to include in your application.

    - Sibi bro suggested website - pypi.org for Python Package Index

    - About import math & import img2pdf

    - About Custom module | he showed his GitlabCtl

* Advanced Python:
    * Generators in Python:
        yield -> keyword 
            - It is used in large data like csv that contain 10k number to loop inside print so it stores 10k number in memory and it slow down PC, So we use Yield -> that generate one at a time 

            - Normal Return ->  Iterating already available data
            - In yeild -> Generating the data on-demand
            - This concept is called Generators

    * About Decorators 
        A decorator in Python is a function that takes another function as input, adds some extra behavior to it, and returns a new function.


    * Enum
        An enum in Python is a class that defines a set of constant values, which are represented as unique, named members, making the code more readable and maintainable.

```

## Code:

### import_math.py
```python
import math

num = int(input("Enter a number for Square root : "))
print("Square Root of {} is {}".format(num,math.sqrt(num)))

#from math import sqrt
#print("Square Root of {} is {}".format(num,sqrt(num)))

#from math import sqrt as SR
#print("Square Root of {} is {}".format(num,SR(num)))

"""
Output:
    $ python3 import_math.py
    Enter a number for Square root : 9
    Square Root of 9 is 3.0
"""
```

### convert_img2pdf.py 
```python
""" 
# Create a virtual environment
$ python3 -m venv ~/venvs/myenv

# Activate it
$ source ~/venvs/myenv/bin/activate

# Install the package inside the virtual environment
$ pip install img2pdf
"""

import img2pdf

image = "/home/ky/Learning/SNA/sna-notes/PYTHON/day8/code/live_today.jpg"
output = "/home/ky/Learning/SNA/sna-notes/PYTHON/day8/code/live_today.pdf"

with open(output, "wb") as f:   #wb -> binary wirte mode (or) w -> write mode
    f.write(img2pdf.convert(image))
    f.close()

"""
Output:
    $ python3 convert_img2pdf.py 
    $ ls
    convert_img2pdf.py  import_math.py  live_today.jpg  live_today.pdf
"""
```

### binary_Pyfile
```python
#!/usr/bin/env python3
print("How Are you . . .")

"""
SETUP:
    # Change Name binary_Pyfile.py to binary_Pyfile
    $ sudo chmod +x binary_PyFile 

Path Variable Setup:
    $ a=1
    $ echo $a
        1

    $ echo $PATH
        /home/ky/venvs/myenv/bin:/home/ky/.local/bin:/home/ky/.local/bin:/home/ky/.local/bin:/home/ky/.local/bin:/home/ky/.local/bin:/usr/local/bin:/usr/bin:/bin:/usr/local/games:/usr/games
    $ PATH=$PATH:home/ky/Learning/SNA/sna-notes/PYTHON/day8/code/bin
    $ echo $PATH
        /home/ky/venvs/myenv/bin:/home/ky/.local/bin:/home/ky/.local/bin:/home/ky/.local/bin:/home/ky/.local/bin:/home/ky/.local/bin:/usr/local/bin:/usr/bin:/bin:/usr/local/games:/usr/games:home/ky/Learning/SNA/sna-notes/PYTHON/day8/code/bin
    * Not Working - Just chill because i am not have time and mind to fix
    
Output:
    $ ./binary_PyFile 
    How Are you . . . 

"""
```

### generator_yield.py 
```python
def double_numbers(iterable):
    for i in iterable:
        print("[] double data gen")
        yield i*2

def datagen():
    print("[] data gen")
    return [1,2,3]

# Generating the data on-demand
for i in double_numbers(range(6)):
    print(i)

# Iterating already available data
for i in datagen():
    print(i)

"""
Output:
    $ python3 generator_yield.py 
    [] double data gen
    0
    [] double data gen
    2
    [] double data gen
    4
    [] double data gen
    6
    [] double data gen
    8
    [] double data gen
    10
    [] data gen
    1
    2
    3
"""
```

### generator_yield2.py
```python
def double_numbers(iterable):
    for i in iterable:
        print("[] double data gen {}".format(i))
        yield i*2

i = double_numbers(range(1,5))

k = next(i)
while k:
    print(k)
    try:
        k = next(i)
    except:
        break

"""
Output:
    $ python3 generator_yield2.py
    [] double data gen 1
    2
    [] double data gen 2
    4
    [] double data gen 3
    6
    [] double data gen 4
    8
"""
```

### decorators.py
```python
from functools import wraps #Decorators

def beg(target_functions):
    @wraps(target_functions)
    def wrapper(*args, **kwargs):
        msg = target_functions(*args, **kwargs)
        return msg + "Please !!!"
    return wrapper

@beg
def say():
    msg = "Can you me buy me a Samosa? "
    return msg

print(say())

"""
    Output:
    $ python3 decorators.py 
    Can you me buy me a Samosa? Please !!!
"""
```

### decorators2.py
```python
from functools import wraps #Decorators

translations = {
    "samosa_buy" : {
        "ta" : "எனக்கு ஒரு சமோசா வாங்கித் தர முடியுமா?",
        "en" : "can you buy me a samosa",
        "sp" : "¿Puedes comprarme una samosa?",
        "ml" : "എനിക്ക് ഒരു സമോസ വാങ്ങിത്തരുമോ?"
    }
    
}

def translate(functions):
    @wraps(functions)
    def wrapper(*args, **kwargs):
        msg, lang = functions(*args, **kwargs)
        return translations[msg][lang] + "Please !!!"
    return wrapper

@translate
def say(lang="en"):
    msg = "samosa_buy"
    return msg, lang

print(say("en"))
print(say("ta"))
print(say("ml"))
print(say("sp"))

"""
    Output:
    $ python3 decorators2.py 
    can you buy me a samosaPlease !!!
    எனக்கு ஒரு சமோசா வாங்கித் தர முடியுமா?Please !!!
    എനിക്ക് ഒരു സമോസ വാങ്ങിത്തരുമോ?Please !!!
    ¿Puedes comprarme una samosa?Please !!!
"""
```

### enum.py 
```python
l = ["apple", "bannana", "mango", "beery"]

# Enum Way
for i,d in enumerate(l):
    print("{} {}".format(i,d))

# Ordinary Way
c=0
for i in l:
    print(i)
    c+=1
    if(c==2):
        break


"""
Output:
    $ python3 enum.py 
    0 apple
    1 bannana
    2 mango
    3 beery
    apple
    bannana
"""
```



___
---
***



# Day 9 - Python Marathon Part 9

## My_Notes:
```
* Modules - Libraries
    - About Creating Our Own Modules

* Class
    - It is In General Looks like Classification
    - No, a class is not the same as classification, but they are related.
        Class (in OOP) is a blueprint for creating objects.
        Classification is the process of grouping things based on characteristics.

        Parent Class    -> Automative
        Child Class     -> Car | Bike | Cycle | Truck
        Objects         -> Cars | Bikes

* Object Oriented Programming
           Class
          /     \
   Members      Methods
        \         /
         \       /
          \     /
           Object

    - About Objects and its Properties and Functions
        Class Car -> Object (Car)
                Members or Properties  -> Color | Model | Tyre Type | Glass | Engine | Battery % 
                    - Properties may static or variable
                Methods or Functions   -> Drive | Break | Steer | Change Gear | Indicator On Off 

        Constructor - Its the first function that executes when you initilize class into an object
        
        About Instance - something created from class

        About @classmethod
            @classmethod is a decorator used to define a method that belongs to the class rather than an instance of the class.

            A classmethod receives the class itself as the first argument, traditionally named cls.

        About @staticmethod
            @staticmethod is a decorator that defines a method that does not take self or cls as the first argument. It behaves just like a regular function but lives inside the class's namespace

        About Getter & Setter & Deleter
            - A getter is used to read an attribute.
           -  A setter is used to update or validate an attribute

        About Inheritance - Inheritance allows a class (child) to reuse and extend the properties and behaviors of another class (parent).

``` 

## Code:
### __init__.py
```python
def add(x,y):
    return x+y
```

### Add.py
```python
def add(x,y):
    return x+y
```

### User.py
```python
def get_user(x):
    return "Hi {}".format(x)
```

### import_module.py
```python
import snalib
print(snalib.add(10,30))

"""
Output:
    $ python3 import_module.py
    40
"""
```

### import_module2.py
```python
from snalib.User import get_user

print(get_user("TVK Vijay"))

"""
Output:
    $ python3 import_module2.py
    Hi TVK Vijay
"""
```

### Car.py
```python
class Car:

    #Class Attribute
    type = "Sedan"

    #Constructor - Its the first function that executes when you initilize class into an object
    def __init__(self, make, model, regNo):  #self is like "this" in PHP
        #Instance Attributes
        self._make = make # Or self.make = make
        self.model = model
        self.regNo = regNo
        self.batt = 0
        if self.type == "Sedan":
            self.breakPow = "100%"
        elif self.type == "Hatchback":
            self.breakPow = "75%"
    
    def start(self):    # In class inside, create function and that function does not need single argument and it is mandatory to give self  | If you dont want self then define as Static method 
        print("Vrrmmmmm..... {} {} {} is ready for Drive".format(self.make, self.model, self.regNo))

    def get_battery(self):
        print("Batter : {}%".format(self.batt))

    @classmethod #A classmethod receives the class itself as the first argument, traditionally named cls.
    def get_type(cls):
        g = cls("Astron Marton", "DB11", "TN40BS2077")
        g.start()
        return g

    @classmethod
    def build_aston(cls, regNo):
        g = cls("Astron Marton", "DB11", regNo)
        g.start()
        return g

    @staticmethod #It behaves just like a regular function but lives inside the class's namespace
    def build_pd7(regNo):
        cls = Car
        g = cls("Astron Marton", "PD7", regNo)
        g.start()
        return g

    @property
    def make(self):
        return self._make

    @make.getter
    def make(self):
        print("Returning {}".format(self._make))

    @make.setter
    def make(self, make):
        self._make = make

    @make.deleter
    def make(self):
        print("Deleting {}....".format(self.regNo))
        del self._make

def get_anything():
        print("I am independent car's @staticmethod") 
```

### oops.py
```python
from snalib.Car import Car
from snalib.Car import get_anything

# Initilize
x = Car("BMW", "M2025", "TN40AN1155")
y = Car("BMW", "Zi4", "TN40PM4050")

x.start()
y.start()

x.batt = 100

#Call with Object instance
x.get_battery()

#Call with class
Car.get_battery(x)
print(Car.type)
Car.get_type()

#Outside class and Its a function
get_anything()

a = Car.build_aston("TN40BS2040")   #Class method
b = Car.build_pd7( "TN40LV1503")     #Static method

#del y.batt
y.get_battery()

print(a.make)
a.make = "Hello"
a.model = "Test"

print(a.make)
a.start()

del a.make

print("A's type :" + a.type)
Car.type = "Hatchback"
q = Car.build_aston("TN40BS3040")
q = Car.build_pd7( "TN40LV2004")

print("Q's type :" + q.type)
print(q.type)
print(Car.type)

"""
Output:
$ python3 oops.py 
    Returning BMW
    Vrrmmmmm..... None M2025 TN40AN1155 is ready for Drive
    Returning BMW
    Vrrmmmmm..... None Zi4 TN40PM4050 is ready for Drive
    Batter : 100%
    Batter : 100%
    Sedan
    Returning Astron Marton
    Vrrmmmmm..... None DB11 TN40BS2077 is ready for Drive
    I am independent car's @staticmethod
    Returning Astron Marton
    Vrrmmmmm..... None DB11 TN40BS2040 is ready for Drive
    Returning Astron Marton
    Vrrmmmmm..... None PD7 TN40LV1503 is ready for Drive
    Batter : 0%
    Returning Astron Marton
    None
    Returning Hello
    None
    Returning Hello
    Vrrmmmmm..... None Test TN40BS2040 is ready for Drive
    Deleting TN40BS2040....
    A's type :Sedan
    Returning Astron Marton
    Vrrmmmmm..... None DB11 TN40BS3040 is ready for Drive
    Returning Astron Marton
    Vrrmmmmm..... None PD7 TN40LV2004 is ready for Drive
    Q's type :Hatchback
    Hatchback
    Hatchback
"""
```

### Automobile.py
```python
class Automobile:
    #Constructor
    def __init__(self, make, model, regno):
        #Instance Attributes
        self._make = make
        self.model = model
        self.regNo = regno

    @property
    def make(self):
        return self._make

    @make.getter
    def make(self):
        print("Returning {}".format(self.model))
        return self._make

    @make.setter
    def make(self, make):
        print("Setting make to {}".format(make))
        self._make = make

    @make.deleter
    def make(self):
        print("Deleting {}...".format(self.regNo))
        del self._make
```

### Car0.py
```python
from .Automobile import Automobile

class Car0(Automobile): #Inheritance allows a class (child) to reuse and extend the properties and behaviors of another class (parent)
    #Class Attribute
    type = "Sedan"

    #Constructor
    def __init__(self, make, model, regNo): 
        #Instance Attributes
        super().__init__(make, model, regNo) #Inheritance
        self.batt = 0
        if self.type == "Sedan":
            self.breakPow = "100%"
        elif self.type == "Hatchback":
            self.breakPow = "75%"
    
    #Type Casting and python not have type casting
    @classmethod
    def build_from_automobile(cls, d: Automobile):
        c = cls(d.make, d.model, d.regNo)
        return c

    
    def start(self):
        print("Vrrmmmmm..... {} {} {} is ready for Drive".format(self.make, self.model, self.regNo))

    def get_battery(self):
        print("Batter : {}%".format(self.batt))

    @classmethod
    def get_type(cls):
        g = cls("Astron Marton", "DB11", "TN40BS2077")
        g.start()
        return g

    @classmethod
    def build_aston(cls, regNo):
        g = cls("Astron Marton", "DB11", regNo)
        g.start()
        return g

    @staticmethod
    def build_pd7(regNo):
        cls = Car0
        g = cls("Astron Marton", "PD7", regNo)
        g.start()
        return g

def get_anything():
        print("I am independent car's @staticmethod")

"""
Output:
$ python3 oops1.py 
    Returning BMW
    Vrrmmmmm..... None M2025 TN40AN1155 is ready for Drive
    Returning BMW
    Vrrmmmmm..... None Zi4 TN40PM4050 is ready for Drive
    Batter : 100%
    Batter : 100%
    Sedan
    Returning Astron Marton
    Vrrmmmmm..... None DB11 TN40BS2077 is ready for Drive
    I am independent car's @staticmethod
    Returning Astron Marton
    Vrrmmmmm..... None DB11 TN40BS2040 is ready for Drive
    Returning Astron Marton
    Vrrmmmmm..... None PD7 TN40LV1503 is ready for Drive
    Batter : 0%
    Returning Astron Marton
    None
    Returning Hello
    None
    Returning Hello
    Vrrmmmmm..... None Test TN40BS2040 is ready for Drive
    Deleting TN40BS2040....
    A's type :Sedan
    Returning Astron Marton
    Vrrmmmmm..... None DB11 TN40BS3040 is ready for Drive
    Returning Astron Marton
    Vrrmmmmm..... None PD7 TN40LV2004 is ready for Drive
    Q's type :Hatchback
    Hatchback
    Hatchback
"""
```

### Bike.py
```python
from .Automobile import Automobile

class Bike(Automobile): #Inheritance

    #Constructor
    def __init__(self, make, model, regNo): 
        #Instance Attributes
        super().__init__(make, model, regNo) #Inheritance
```

### oops1.py
```python
from snalib.Car0 import Car0
from snalib.Car0 import get_anything
from snalib.Bike import Bike
from snalib.Automobile import Automobile

# Initilize
x = Car0("BMW", "M2025", "TN40AN1155")
y = Car0("BMW", "Zi4", "TN40PM4050")

x.start()
y.start()

x.batt = 100

#Call with Object instance
x.get_battery()

#Call with class
Car0.get_battery(x)
print(Car0.type)
Car0.get_type()

#Outside class and Its a function
get_anything()

a = Car0.build_aston("TN40BS2040")   #Class method
b = Car0.build_pd7( "TN40LV1503")     #Static method

#del y.batt
y.get_battery()

print(a.make)
a.make = "Hello"
a.model = "Test"

print(a.make)
a.start()

del a.make

print("A's type :" + a.type)
Car0.type = "Hatchback"
q = Car0.build_aston("TN40BS3040")
q = Car0.build_pd7( "TN40LV2004")

print("Q's type :" + q.type)
print(q.type)
print(Car0.type)

d = Bike("KTM", "Duke", "TN40UE2100")
d.make = "KTM TM"
print(d.make)

d = Automobile("KTM", "Duke 250", "TN40VJ2026")
d.make = "KTM NEW"
print(d.make)

c = Car0.build_from_automobile(d)
c.start()


"""
Output:
$ python3 oops1.py 
    Returning M2025
    Vrrmmmmm..... BMW M2025 TN40AN1155 is ready for Drive
    Returning Zi4
    Vrrmmmmm..... BMW Zi4 TN40PM4050 is ready for Drive
    Batter : 100%
    Batter : 100%
    Sedan
    Returning DB11
    Vrrmmmmm..... Astron Marton DB11 TN40BS2077 is ready for Drive
    I am independent car's @staticmethod
    Returning DB11
    Vrrmmmmm..... Astron Marton DB11 TN40BS2040 is ready for Drive
    Returning PD7
    Vrrmmmmm..... Astron Marton PD7 TN40LV1503 is ready for Drive
    Batter : 0%
    Returning DB11
    Astron Marton
    Setting make to Hello
    Returning Test
    Hello
    Returning Test
    Vrrmmmmm..... Hello Test TN40BS2040 is ready for Drive
    Deleting TN40BS2040...
    A's type :Sedan
    Returning DB11
    Vrrmmmmm..... Astron Marton DB11 TN40BS3040 is ready for Drive
    Returning PD7
    Vrrmmmmm..... Astron Marton PD7 TN40LV2004 is ready for Drive
    Q's type :Hatchback
    Hatchback
    Hatchback
    Setting make to KTM TM
    Returning Duke
    KTM TM
    Setting make to KTM NEW
    Returning Duke 250
    KTM NEW
    Returning Duke 250
    Returning Duke 250
    Vrrmmmmm..... KTM NEW Duke 250 TN40VJ2026 is ready for Drive
"""
```



___
---
***

```END...```