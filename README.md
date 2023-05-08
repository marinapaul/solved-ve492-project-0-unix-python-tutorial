Download Link: https://assignmentchef.com/product/solved-ve492-project-0-unix-python-tutorial
<br>
<h1></h1>

The goal of this project is to help you get familiar with Unix commands and Python grammar. The grade of this project will not count into your total grade. But failing to submit it before the deadline will cause a deduction.

<h1>Introduction</h1>

The projects for this class assume you use Python 3.6. Project 0 will cover the following:

<ul>

 <li>A mini-UNIX tutorial</li>

 <li>Instructions on how to set up the right Python version,</li>

 <li>A mini-Python tutorial.</li>

</ul>

<h1>Part 1: Unix Basics</h1>

Here are basic commands to navigate UNIX and edit files.

<h2>File/Directory Manipulation</h2>

When you open a terminal window, you’re placed at a command prompt: <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="cabcaffef3f8e7beab8aa7b39a89">[email protected]</a>:~$

The prompt generally shows your username, the host you are logged onto, and your current location in the directory structure (your path). The tilde character is shorthand for your home directory. Note your prompt may look slightly different. To make a directory, use the mkdir command. Use cd to change to that directory:

<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="addbc899949f80d9ccedc0d4fdee">[email protected]</a>:~$ mkdir foo <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="ec9a89d8d5dec1988dac8195bcaf">[email protected]</a>:~$ cd foo <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="8ef8ebbab7bca3faefcee3f7decd">[email protected]</a>:~/foo$

Use ls to see a listing of the contents of a directory, and touch to create an empty file:

<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="374152030e051a4356775a4e6774">[email protected]</a>:~$ ls <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="82f4e7b6bbb0aff6e3c2effbd2c1">[email protected]</a>:~$ touch alloha <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="d8aebdece1eaf5acb998b5a1889b">[email protected]</a>:~/foo$ ls alloha <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="1d6b7829242f30697c5d70644d5e">[email protected]</a>:~/foo$ cd ..

<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="a3d5c6979a918ed7c2e3cedaf3e0">[email protected]</a>:~$

Download python_basics.zip from <a href="https://umjicanvas.com/files/204949/download?download_frd=1">Canvas</a> into your home directory (note: the zip file’s name may be slightly different when you download it). Use unzip to extract the contents of the zip file:

<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="265043121f140b5247664b5f7665">[email protected]</a>:~$ ls *.zip python_basics.zip <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="8cfae9b8b5bea1f8edcce1f5dccf">[email protected]</a>:~$ unzip python_basics.zip <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="6016055459524d1401200d193023">[email protected]</a>:~/foo$ cd python_basics <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="245241101d1609504564495d7467">[email protected]</a>:~/foo$ ls foreach.py helloWorld.py listcomp.py listcomp2.py quickSort.py shop.py shopTest.py

Some other useful Unix commands:

<ul>

 <li>cp copies a file or files</li>

 <li>rm removes (deletes) a file</li>

 <li>mv moves a file (i.e., cut/paste instead of copy/paste)</li>

 <li>man displays documentation for a command</li>

 <li>pwd prints your current path</li>

 <li>Press <strong>Ctrl-c </strong>to kill a running process</li>

 <li>Append the character &amp; to a command to run it in the background</li>

 <li>fg brings a program running in the background to the foreground</li>

</ul>

<h1>Part 2: Python Installation</h1>

Many of you may not have Python 3.6 already installed on your computers. Conda is an easy way to manage many different environments, each with its own Python version and dependencies. This allows us to avoid conflicts between our preferred Python version and that of other classes. We’ll walk through how to set up and use a conda environment.

<strong>Prerequisite: </strong><a href="https://docs.anaconda.com/anaconda/install/">Anaconda</a><a href="https://docs.anaconda.com/anaconda/install/">.</a> If you haven’t installed it, install it through the previous link.

<strong>Creating a Conda Environment </strong>The command for creating a conda environment with Python 3.6 is:

<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="6f190a5b565d421b0e2f02163f2c">[email protected]</a>:~$ conda create –name &lt;env-name&gt; python=3.6

For us, we decide to name our environment ve492, so we run the following command, and press <strong>y </strong>to confirm installing any missing packages.

<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="a4d2c1909d9689d0c5e4c9ddf4e7">[email protected]</a>:~/python_basics$ conda create –name ve492 python=3.6

<strong>Entering the Environment </strong>To enter the conda environment that we just created, do the following. Note that the Python version within the environment is 3.6, just what we want. The tag (&lt;env-name&gt;) shows you the name of the conda environment that is active. In our case, we have (ve492), as what we’d expect.

<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="641201505d5649100524091d3427">[email protected]</a>:~/python_basics$ source activate ve492 (ve492) <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="1a6c7f2e2328376e7b5a77634a59">[email protected]</a>:~/python_basics$ python -V Python 3.6.6 :: Anaconda, Inc.

<strong>Leaving the Environment        </strong>Leaving the environment is just as easy.

(ve492) <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="2056451419120d5441604d597063">[email protected]</a>:~/python_basics$ source deactivate <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="d6a0b3e2efe4fba2b796bbaf8695">[email protected]</a>:~/python_basics$ python -V Python 3.7.4

Our python version has now returned to whatever the system default is!

<h1>Part3: Python Basics</h1>

<strong>Prerequisite: </strong>python_basics.zip from <a href="https://umjicanvas.com/files/204949/download?download_frd=1">Canvas</a><a href="https://umjicanvas.com/files/204949/download?download_frd=1">.</a>

The programming assignments in this course will be written in Python, an interpreted, object-oriented language that shares some features with both C++ and Matlab. This tutorial will walk through the primary syntactic constructions in Python, using short examples.

We encourage you to type all python code shown in the tutorial onto your own machine. Make sure it responds the same way. You may find the

Troubleshooting section helpful if you run into problems.

<h2>Invoking the Interpreter</h2>

Python can be run in one of two modes. It can either be used interactively, via an interpreter, or it can be called from the command line to execute a script. We will first use the Python interpreter interactively.

You invoke the interpreter using the command python at the Unix command prompt; or if you are using Windows that doesn’t work for you in Git Bash, using python -i.

(ve492) <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="0d7b6839343f20796c4d60745d4e">[email protected]</a>:~/python_basics$ python

Python 3.6.6 |Anaconda, Inc.| (default, Sept 3 2019, 23:11:49) [GCC 4.2.1 Compatible Clang 4.0.1 (tags/RELEASE_401/final)] on darwin

Type “help”, “copyright”, “credits” or “license” for more information. &gt;&gt;&gt;

<h2>Operators</h2>

The Python interpreter can be used to evaluate expressions, for example simple arithmetic expressions. If you enter such expressions at the prompt (&gt;&gt;&gt;) they will be evaluated and the result will be returned on the next line.

&gt;&gt;&gt; 1 + 1

2

&gt;&gt;&gt; 2 * 3

6

Boolean operators also exist in Python to manipulate the primitive True and False values.

&gt;&gt;&gt; 1 == 0

False

&gt;&gt;&gt; not (1 == 0)

True

&gt;&gt;&gt; (2 == 2) and (2 == 3)

False

&gt;&gt;&gt; (2 == 2) or (2 == 3)

True

<h2>Strings</h2>

Python has a built-in string type. The + operator is overloaded to do string concatenation on string values.

&gt;&gt;&gt; ‘artificial’ + “intelligence” ‘artificialintelligence’

There are many built-in methods which allow you to manipulate strings.

&gt;&gt;&gt; ‘artificial’.upper()

‘ARTIFICIAL’

&gt;&gt;&gt; ‘HELP’.lower()

‘help’

&gt;&gt;&gt; len(‘Help’)

4

Notice that we can use either single quotes ‘ ‘ or double quotes ” ” to surround string. This allows for easy nesting of strings. We can also store expressions into variables.

&gt;&gt;&gt; s = ‘hello world’ &gt;&gt;&gt; print(s) hello world &gt;&gt;&gt; s.upper()

‘HELLO WORLD’

&gt;&gt;&gt; len(s.upper())

11

&gt;&gt;&gt; num = 8.0

&gt;&gt;&gt; num += 2.5 &gt;&gt;&gt; print(num)

10.5

In Python, you do not have to declare variables before you assign to them.

<h2>Exercise: Dir and Help</h2>

Learn about the methods Python provides for strings. To see what methods Python provides for a datatype, use the dir and help commands:

&gt;&gt;&gt; s = ‘abc’

&gt;&gt;&gt; dir(s)

[‘__add__’, ‘__class__’, ‘__contains__’, ‘__delattr__’, ‘__doc__’, ‘__eq__’,

‘__ge__’,’__getattribute__’, ‘__getitem__’, ‘__getnewargs__’,

‘__getslice__’, ‘__gt__’, ‘__hash__’, ‘__init__’, ‘__le__’, ‘__len__’,

‘__lt__’, ‘__mod__’, ‘__mul__’, ‘__ne__’, ‘__new__’, ‘__reduce__’, ‘__reduce_ex__’, ‘__repr__’, ‘__rmod__’, ‘__rmul__’, ‘__setattr__’,

‘__str__’, ‘capitalize’, ‘center’, ‘count’, ‘decode’, ‘encode’,

‘endswith’, ‘expandtabs’, ‘find’, ‘index’, ‘isalnum’, ‘isalpha’,

‘isdigit’, ‘islower’, ‘isspace’, ‘istitle’, ‘isupper’, ‘join’, ‘ljust’,

‘lower’, ‘lstrip’, ‘replace’, ‘rfind’, ‘rindex’, ‘rjust’, ‘rsplit’, ‘rstrip’, ‘split’, ‘splitlines’, ‘startswith’, ‘strip’, ‘swapcase’,

‘title’, ‘translate’, ‘upper’, ‘zfill’]

&gt;&gt;&gt; help(s.find)

Help on built-in function find:

find(…) method of builtins.str instance

S.find(sub[, start[, end]]) -&gt; int

Return the lowest index in S where substring sub is found, such that sub is contained within S[start:end]. Optional arguments start and end are interpreted as in slice notation.

Return -1 on failure.

&gt;&gt;&gt; s.find(‘b’)

1

Try out some of the string functions listed in dir (ignore those with underscores ’ ’ around the method name).

<h2>Built-in Data Structures</h2>

Python comes equipped with some useful built-in data structures, broadly similar to C++ STL Containers.

<strong>Lists     </strong>Lists store a sequence of mutable items:

&gt;&gt;&gt; fruits = [‘apple’, ‘orange’, ‘pear’, ‘banana’]

&gt;&gt;&gt; fruits[0] ‘apple’

We can use the + operator to do list concatenation:

&gt;&gt;&gt; otherFruits = [‘kiwi’, ‘strawberry’]

&gt;&gt;&gt; fruits + otherFruits

&gt;&gt;&gt; [‘apple’, ‘orange’, ‘pear’, ‘banana’, ‘kiwi’, ‘strawberry’]

Python also allows negative-indexing from the back of the list. For instance, fruits[-1] will access the last element ‘banana’:

&gt;&gt;&gt; fruits[-2]

‘pear’

&gt;&gt;&gt; fruits.pop()

‘banana’

&gt;&gt;&gt; fruits

[‘apple’, ‘orange’, ‘pear’]

&gt;&gt;&gt; fruits.append(‘grapefruit’)

&gt;&gt;&gt; fruits

[‘apple’, ‘orange’, ‘pear’, ‘grapefruit’]

&gt;&gt;&gt; fruits[-1] = ‘pineapple’

&gt;&gt;&gt; fruits

[‘apple’, ‘orange’, ‘pear’, ‘pineapple’]

We can also index multiple adjacent elements using the slice operator. For instance, fruits[1:3], returns a list containing the elements at position 1 and 2. In general fruits[start:stop] will get the elements in start, start+1, …, stop-1. We can also do fruits[start:] which returns all elements starting from the start index. Also fruits[:end] will return all elements before the element at position end:

&gt;&gt;&gt; fruits[0:2]

[‘apple’, ‘orange’]

&gt;&gt;&gt; fruits[:3]

[‘apple’, ‘orange’, ‘pear’]

&gt;&gt;&gt; fruits[2:]

[‘pear’, ‘pineapple’]

&gt;&gt;&gt; len(fruits)

4

The items stored in lists can be any Python data type. So for instance we can have lists of lists:

&gt;&gt;&gt; lstOfLsts = [[‘a’, ‘b’, ‘c’], [1, 2, 3], [‘one’, ‘two’, ‘three’]]

&gt;&gt;&gt; lstOfLsts[1][2]

3

&gt;&gt;&gt; lstOfLsts[0].pop()

‘c’

&gt;&gt;&gt; lstOfLsts

[[‘a’, ‘b’], [1, 2, 3], [‘one’, ‘two’, ‘three’]]

<h2>Exercise: Lists</h2>

Play with some of the list functions. You can find the methods you can call on an object via the dir and get information about them via the help command:

&gt;&gt;&gt; dir(list)

[‘__add__’, ‘__class__’, ‘__contains__’, ‘__delattr__’, ‘__delitem__’,

‘__delslice__’, ‘__doc__’, ‘__eq__’, ‘__ge__’, ‘__getattribute__’,

‘__getitem__’, ‘__getslice__’, ‘__gt__’, ‘__hash__’, ‘__iadd__’, ‘__imul__’,

‘__init__’, ‘__iter__’, ‘__le__’, ‘__len__’, ‘__lt__’, ‘__mul__’, ‘__ne__’,

‘__new__’, ‘__reduce__’, ‘__reduce_ex__’, ‘__repr__’, ‘__reversed__’,

‘__rmul__’, ‘__setattr__’, ‘__setitem__’, ‘__setslice__’, ‘__str__’,

‘append’, ‘count’, ‘extend’, ‘index’, ‘insert’, ‘pop’, ‘remove’, ‘reverse’,

‘sort’]

&gt;&gt;&gt; help(list.reverse)

Help on built-in function reverse:

reverse(…)

L.reverse() — reverse *IN PLACE*

&gt;&gt;&gt; lst = [‘a’, ‘b’, ‘c’]

&gt;&gt;&gt; lst.reverse()

&gt;&gt;&gt; [‘c’, ‘b’, ‘a’]

Press <strong>q </strong>to back out of a help screen.

<h2>Tuples</h2>

A data structure similar to the list is the tuple, which is like a list except that it is immutable once it is created (i.e., you cannot change its content once created). Note that tuples are surrounded with parentheses while lists have square brackets.

&gt;&gt;&gt; pair = (3, 5)

&gt;&gt;&gt; pair[0]

3

&gt;&gt;&gt; x, y = pair

&gt;&gt;&gt; x

3

&gt;&gt;&gt; y

5

&gt;&gt;&gt; pair[1] = 6

TypeError: object does not support item assignment

The attempt to modify an immutable structure raised an exception. Exceptions indicate errors: index out of bounds errors, type errors, and so on will all report exceptions in this way.

<h2>Sets</h2>

A set is another data structure that serves as an unordered list with no duplicate items. Below, we show how to create a set:

&gt;&gt;&gt; shapes = [‘circle’, ‘square’, ‘triangle’, ‘circle’]

&gt;&gt;&gt; setOfShapes = set(shapes)

Another way of creating a set is shown below:

&gt;&gt;&gt; setOfShapes = {‘circle’, ‘square’, ‘triangle’, ‘circle’}

Next, we show how to add things to the set, test if an item is in the set, and perform common set operations (difference, intersection, union):

&gt;&gt;&gt; setOfShapes set([‘circle’, ‘square’, ‘triangle’])

&gt;&gt;&gt; setOfShapes.add(‘polygon’)

&gt;&gt;&gt; setOfShapes set([‘circle’, ‘square’, ‘triangle’, ‘polygon’])

&gt;&gt;&gt; ‘circle’ in setOfShapes

True

&gt;&gt;&gt; ‘rhombus’ in setOfShapes

False

&gt;&gt;&gt; favoriteShapes = [‘circle’, ‘triangle’, ‘hexagon’]

&gt;&gt;&gt; setOfFavoriteShapes = set(favoriteShapes) &gt;&gt;&gt; setOfShapes – setOfFavoriteShapes set([‘square’, ‘polygon’]) &gt;&gt;&gt; setOfShapes &amp; setOfFavoriteShapes set([‘circle’, ‘triangle’]) &gt;&gt;&gt; setOfShapes | setOfFavoriteShapes

set([‘circle’, ‘square’, ‘triangle’, ‘polygon’, ‘hexagon’])

Note that the objects in the set are unordered; you cannot assume that their traversal or print order will be the same across machines!

<h2>Dictionaries</h2>

The last built-in data structure is the dictionary which stores a map from one type of object (the key) to another (the value). The key must be an immutable type (string, number, or tuple). The value can be any Python data type.

Note: In the example below, the printed order of the keys returned by Python could be different than shown below. The reason is that unlike lists which have a fixed ordering, a dictionary is simply a hash table for which there is no fixed ordering of the keys (like unordered_map in C++). The order of the keys depends on how exactly the hashing algorithm maps keys to buckets, and will usually seem arbitrary. Your code should not rely on key ordering, and you should not be surprised if even a small modification to how your code uses a dictionary results in a new key ordering.

&gt;&gt;&gt; studentIds = {‘knuth’: 42.0, ‘turing’: 56.0, ‘nash’: 92.0}

&gt;&gt;&gt; studentIds[‘turing’]

56.0

&gt;&gt;&gt; studentIds[‘nash’] = ‘ninety-two’

&gt;&gt;&gt; studentIds

{‘knuth’: 42.0, ‘turing’: 56.0, ‘nash’: ‘ninety-two’}

&gt;&gt;&gt; del studentIds[‘knuth’]

&gt;&gt;&gt; studentIds

{‘turing’: 56.0, ‘nash’: ‘ninety-two’}

&gt;&gt;&gt; studentIds[‘knuth’] = [42.0, ‘forty-two’]

&gt;&gt;&gt; studentIds

{‘knuth’: [42.0, ‘forty-two’], ‘turing’: 56.0, ‘nash’: ‘ninety-two’}

&gt;&gt;&gt; studentIds.keys()

[‘knuth’, ‘turing’, ‘nash’]

&gt;&gt;&gt; studentIds.values()

[[42.0, ‘forty-two’], 56.0, ‘ninety-two’]

&gt;&gt;&gt; studentIds.items()

[(‘knuth’, [42.0, ‘forty-two’]), (‘turing’,56.0), (‘nash’, ‘ninety-two’)]

&gt;&gt;&gt; len(studentIds)

3

As with nested lists, you can also create dictionaries of dictionaries.

<strong>Exercise: Dictionaries</strong>

Use dir and help to learn about the functions you can call on dictionaries.

<h2>Writing Scripts</h2>

Now that you’ve got a handle on using Python interactively, let’s write a simple Python script that demonstrates Python’s for loop. Open the file called foreach.py, which should contain the following code:

<em># This is what a comment looks like </em>fruits = [‘apples’, ‘oranges’, ‘pears’, ‘bananas’] for fruit in fruits: print(fruit + ‘ for sale’)

fruitPrices = {‘apples’: 2.00, ‘oranges’: 1.50, ‘pears’: 1.75} for fruit, price in fruitPrices.items():

if price &lt; 2.00:

print(‘%s cost %f a pound’ % (fruit, price))

else: print(fruit + ‘ are too expensive!’)

At the command line, use the following command in the directory containing foreach.py:

<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="c1b7a4f5f8f3ecb5a081acb89182">[email protected]</a>:~/tutorial$ python foreach.py apples for sale oranges for sale pears for sale bananas for sale apples are too expensive! oranges cost 1.500000 a pound pears cost 1.750000 a pound

Remember that the print statements listing the costs may be in a different order on your screen than in this tutorial; that’s due to the fact that we’re looping over dictionary keys, which are unordered. To learn more about control structures (e.g., if and else) in Python, check out the official <a href="https://docs.python.org/3.6/tutorial/">Python </a><a href="https://docs.python.org/3.6/tutorial/">tutorial section on this topic</a><a href="https://docs.python.org/3.6/tutorial/">.</a>

If you like functional programming you might also like map and filter:

&gt;&gt;&gt; list(map(lambda x: x * x, [1, 2, 3]))

[1, 4, 9]

&gt;&gt;&gt; list(filter(lambda x: x &gt; 3, [1, 2, 3, 4, 5, 4, 3, 2, 1]))

[4, 5, 4]

The next snippet of code demonstrates Python’s list comprehension construction:

nums = [1, 2, 3, 4, 5, 6] plusOneNums = [x + 1 for x in nums] oddNums = [x for x in nums if x % 2 == 1]

print(oddNums)

oddNumsPlusOne = [x + 1 for x in nums if x % 2 == 1]

print(oddNumsPlusOne)

This code is in a file called listcomp.py, which you can run:

<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="d3a5b6e7eae1fea7b293beaa8390">[email protected]</a>:~/tutorial$ python listcomp.py

[1, 3, 5]

[2, 4, 6]

<h2>Exercise: List Comprehensions</h2>

Write a list comprehension which, from a list, generates a lowercased version of each string that has length greater than five. You can find the solution in listcomp2.py.

<strong>Beware of Indendation!</strong>

Unlike many other languages, Python uses the indentation in the source code for interpretation. So for instance, for the following script:

if 0 == 1:

print(‘We are in a world of arithmetic pain’)

print(‘Thank you for playing’)

will output: Thank you for playing But if we had written the script as

if 0 == 1:

print(‘We are in a world of arithmetic pain’) print(‘Thank you for playing’)

there would be no output. The moral of the story: be careful how you indent! It’s best to use four spaces for indentation – that’s what the course code uses.

<strong>Tabs vs Spaces </strong>Because Python uses indentation for code evaluation, it needs to keep track of the level of indentation across code blocks. This means that if your Python file switches from using tabs as indentation to spaces as indentation, the Python interpreter will not be able to resolve the ambiguity of the indentation level and throw an exception. Even though the code can be lined up visually in your text editor, Python “sees” a change in indentation and most likely will throw an exception (or rarely, produce unexpected behavior).

This most commonly happens when opening up a Python file that uses an indentation scheme that is opposite from what your text editor uses (aka, your text editor uses spaces and the file uses tabs). When you write new lines in a code block, there will be a mix of tabs and spaces, even though the whitespace is aligned. For a longer discussion on tabs vs spaces, see <a href="https://stackoverflow.com/questions/119562/tabs-versus-spaces-in-python-programming">this </a>discussion on StackOverflow.

<h2>Writing Functions</h2>

As in C++, in Python you can define your own functions:

fruitPrices = {‘apples’: 2.00, ‘oranges’: 1.50, ‘pears’: 1.75}

def buyFruit(fruit, numPounds):

if fruit not in fruitPrices:

print(“Sorry we don’t have %s” % (fruit))

else:

cost = fruitPrices[fruit] * numPounds print(“That’ll be %f please” % (cost))

<em># Main Function </em>if __name__ == ‘__main__’: buyFruit(‘apples’, 2.4) buyFruit(‘coconuts’, 2)

Rather than having a main function as in Java, the __name__ == ‘__main__’ check is used to delimit expressions which are executed when the file is called as a script from the command line. The code after the main check is thus the same sort of code you would put in a main function in C++. Save this script as fruit.py and run it:

<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="681e0d5c515a451c09280511382b">[email protected]</a>:~/tutorial$ python fruit.py

That’ll be 4.800000 please

Sorry we don’t have coconuts

<h2>Advanced Exercise</h2>

Write a quickSort function in Python using list comprehensions. Use the first element as the pivot. You can find the solution in quickSort.py.

<h2>Object Basics</h2>

Although this isn’t a class in object-oriented programming, you’ll have to use some objects in the programming projects, and so it’s worth covering the basics of objects in Python. An object encapsulates data and provides functions for interacting with that data.

<strong>Defining Classes       </strong>Here’s an example of defining a class named FruitShop:

class FruitShop:

def __init__(self, name, fruitPrices):

<em>“”” name: Name of the fruit shop</em>

<em>fruitPrices: Dictionary with keys as fruit strings and prices for values e.g.</em>

<em>{‘apples’: 2.00, ‘oranges’: 1.50, ‘pears’: 1.75}</em>

<em>“”” </em>self.fruitPrices = fruitPrices self.name = name print(‘Welcome to %s fruit shop’ % (name))

def getCostPerPound(self, fruit):

<em>“”” fruit: Fruit string</em>

<em>Returns cost of ‘fruit’, assuming ‘fruit’ is in our inventory or None otherwise</em>

<em>“”” </em>if fruit not in self.fruitPrices: return None

return self.fruitPrices[fruit]

def getPriceOfOrder(self, orderList):

<em>“””</em>

<em>orderList: List of (fruit, numPounds) tuples</em>

<em>Returns cost of orderList, only including the values of fruits that this fruit shop has.</em>

<em>“”” </em>totalCost = 0.0 for fruit, numPounds in orderList:

costPerPound = self.getCostPerPound(fruit) if costPerPound != None:

totalCost += numPounds * costPerPound

return totalCost

def getName(self): return self.name

The FruitShop class has some data, the name of the shop and the prices per pound of some fruit, and it provides functions, or methods, on this data. What advantage is there to wrapping this data in a class?

<ul>

 <li>Encapsulating the data prevents it from being altered or used inappropriately,</li>

 <li>The abstraction that objects provide make it easier to write generalpurpose code.</li>

</ul>

<strong>Using Objects </strong>So how do we make an object and use it? Make sure you have the FruitShop implementation in shop.py. We then import the code from this file (making it accessible to other scripts) using import shop, since shop.py is the name of the file. Then, we can create FruitShop objects as follows:

import shop

shopName = ‘the Berkeley Bowl’

fruitPrices = {‘apples’: 1.00, ‘oranges’: 1.50, ‘pears’: 1.75} berkeleyShop = shop.FruitShop(shopName, fruitPrices) applePrice = berkeleyShop.getCostPerPound(‘apples’) print(applePrice)

print(‘Apples cost $%.2f at %s.’ % (applePrice, shopName))

otherName = ‘the Stanford Mall’ otherFruitPrices = {‘kiwis’: 6.00, ‘apples’: 4.50, ‘peaches’: 8.75} otherFruitShop = shop.FruitShop(otherName, otherFruitPrices) otherPrice = otherFruitShop.getCostPerPound(‘apples’) print(otherPrice) print(‘Apples cost $%.2f at %s.’ % (otherPrice, otherName)) print(“My, that’s expensive!”)

This code is in shopTest.py; you can run it like this:

<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="0e786b3a373c237a6f4e63775e4d">[email protected]</a>:~/tutorial$ python shopTest.py

Welcome to the Berkeley Bowl fruit shop 1.0

Apples cost $1.00 at the Berkeley Bowl.

Welcome to the Stanford Mall fruit shop 4.5

Apples cost $4.50 at the Stanford Mall. My, that’s expensive!

So what just happened? The import shop statement told Python to load all of the functions and classes in shop.py.

The line berkeleyShop = shop.FruitShop(shopName, fruitPrices) constructs an instance of the FruitShop class defined in shop.py, by calling the __init__ function in that class. Note that we only passed two arguments in, while __init__ seems to take three arguments: (self, name, fruitPrices). The reason for this is that all methods in a class have self as the first argument. The self variable’s value is automatically set to the object itself; when calling a method, you only supply the remaining arguments. The self variable contains all the data (name and fruitPrices) for the current specific instance (similar to this in C++). The print statements use the substitution operator (described in the <a href="https://docs.python.org/2/library/stdtypes.html#string-formatting">Python docs</a> if you’re curious).

<strong>Static vs Instance Variables </strong>The following example illustrates how to use static and instance variables in Python.

Create the person_class.py containing the following code:

class Person: population = 0

def __init__(self, myAge): self.age = myAge Person.population += 1

def get_population(self):

return Person.population

def get_age(self): return self.age We first compile the script:

<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="ef998adbd6ddc29b8eaf8296bfac">[email protected]</a>:~/tutorial$ python person_class.py Now use the class as follows:

&gt;&gt;&gt; import person_class

&gt;&gt;&gt; p1 = person_class.Person(12)

&gt;&gt;&gt; p1.get_population()

1

&gt;&gt;&gt; p2 = person_class.Person(63)

&gt;&gt;&gt; p1.get_population() 2

&gt;&gt;&gt; p2.get_population()

2

&gt;&gt;&gt; p1.get_age() 12

&gt;&gt;&gt; p2.get_age()

63

In the code above, age is an instance variable and population is a static variable. population is shared by all instances of the Person class whereas each instance has its own age variable.

<h2>More Python Tips and Tricks</h2>

This tutorial has briefly touched on some major aspects of Python that will be relevant to the course. Here are some more useful tidbits:

<ul>

 <li>Use range to generate a sequence of integers, useful for generating traditional indexed for loops:</li>

</ul>

for index in range(3): print(index)

<ul>

 <li>After importing a file, if you edit a source file, the changes will not be immediately propagated in the interpreter. For this, use the reload command:</li>

</ul>

&gt;&gt;&gt; reload(shop)

<h2>Troubleshooting</h2>

These are some problems (and their solutions) that new Python learners commonly encounter.

<ul>

 <li><strong>Problem: </strong>ImportError: No module named py</li>

</ul>

<strong>Solution: </strong>For import statements with import &lt;package-name&gt;, do not include the file extension (i.e. the .py string). For example, you should use: import shop NOT: import shop.py

<ul>

 <li><strong>Problem: </strong>NameError: name ’MY VARIABLE’ is not defined. Even after importing you may see this.</li>

</ul>

<strong>Solution: </strong>To access a member of a module, you have to type

MODULE NAME.MEMBER NAME, where MODULE NAME is the name of the .py file, and MEMBER NAME is the name of the variable (or function) you are trying to access.

<ul>

 <li><strong>Problem: </strong>TypeError: ’dict’ object is not callable</li>

</ul>

<strong>Solution: </strong>Dictionary looks up are done using square brackets: [ and ]. NOT parenthesis: ( and ).

<ul>

 <li><strong>Problem: </strong>ValueError: too many values to unpack</li>

</ul>

<strong>Solution: </strong>Make sure the number of variables you are assigning in a for loop matches the number of elements in each item of the list. Similarly for working with tuples.

For example, if pair is a tuple of two elements (e.g. pair =(‘apple’, 2.0)) then the following code would cause the “too many values to unpack error”:

(a, b, c) = pair

Here is a problematic scenario involving a for loop:

pairList = [(‘apples’, 2.00), (‘oranges’, 1.50), (‘pears’, 1.75)] for fruit, price, color in pairList: print(‘%s fruit costs %f and is the color %s’ % (fruit, price, color))

<ul>

 <li><strong>Problem: </strong>AttributeError: ’list’ object has no attribute ’length’ (or something similar)</li>

</ul>

<strong>Solution: </strong>Finding length of lists is done using len(NAME OF LIST).

<ul>

 <li><strong>Problem: </strong>Changes to a file are not taking effect.</li>

</ul>

<strong>Solution: </strong>Make sure you are saving all your files after any changes. If you are editing a file in a window different from the one you are using to execute python, make sure you reload(_YOUR_MODULE_) to guarantee your changes are being reflected. reload works similarly to import.

<h2>More References</h2>

<ul>

 <li>The place to go for more Python information: <a href="https://www.python.org/">python.org</a></li>

 <li>A good reference book: Learning Python</li>

</ul>

<h1>Part 4: Question 1: Addition</h1>

Open addition.py and look at the definition of add:

def add(a, b):

“Return the sum of a and b” “*** YOUR CODE HERE ***” return 0

The tests called this with a and b set to different values, but the code always returned zero. Modify this definition.

<h1>Part 5: Question 2: buyLotsOfFruit function</h1>

Add a buyLotsOfFruit(orderList) function to buyLotsOfFruit.py which takes a list of (fruit,pound) tuples and returns the cost of your list. If there is some fruit in the list which doesn’t appear in fruitPrices it should print an error message and return None. Please do not change the fruitPrices variable.

<h1>Part 6: Question 3: shopSmart function</h1>

Fill in the function shopSmart(orders,shops) in shopSmart.py, which takes an orderList (like the kind passed in to FruitShop.getPriceOfOrder) and a list of FruitShop and returns the FruitShop where your order costs the least amount in total. Don’t change the file name or variable names, please. Note that we will provide the shop.py implementation as a “support” file, so you don’t need to submit yours.


