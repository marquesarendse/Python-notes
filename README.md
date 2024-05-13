# Python-notes
Python Introduction

How a computer works:
The memory on your computer is essentially a grid on which data and files are stored. In the computer's file directory, 
every file has a file name that appears as a clickable file icon. 
Information about the file, including its size, is saved in addition to its name. Additionally, the computer uses a pointer—an 
address that indicates where the file's contents are located in memory—to access a file's contents.

Zen of Python
Python is a sophisticated language that works well in the present day. For example, calling one function with a similar syntax is 
probably going to call another function with a similar syntax. 

When dealing with complex problems, where adding more complications is the last thing you want to do, Python's true potential is evident. 
"Import this," a hidden goal statement in Python, emphasizes this idea.

Type "Python" into a terminal window to open the Python command prompt. The prompt is prepared to receive a line of Python code when it is opened, 
as indicated by the three greater-than symbols.
Enter the command "import this" at this time to continue. "This" is the name of the module we're importing, and the "import" command is used to retrieve a useful module.

 
Basic data structure:
List:
The append() method can be used to append an item to the end of a list. For instance, we can type myList to append the value 5 to a 
list myList that already contains the values 1, 2, 3, and 4.append(5), after which myList is printed.

The insert() method can be used to insert an item at a specific location in the list. For example, we can type myList.insert(3, 10) 
and then print myList to insert the value 10 at position 3 in myList.

Items can be eliminated from a list in two different ways. The first method, remove(), eliminates an item by its value rather than its index. 
For example, we can type myList if we want to remove the value 5 from it.delete(5), print myList after that. On the other hand, an error will 
appear if we attempt to remove a value that isn't in the list.

Pop() is the second way to remove items from a list. The item at the end of the list is removed and returned using this method. As an illustration, 
let's type myList.The final item in myList will be deleted when you call pop() and print myList.

Tuples and Sets:
Curly brackets are used to define sets, as in this example: {'a', 'b', 'c'}, mySet. Another way to define a set is to pass any iterable object to the 
set class's constructor, as in this example: mySet = set(('a', 'b', 'c')).

Additionally, you can use the membership operator (in) to determine whether an element is in a set and the length() function to determine a set's length. Finally, 
a pop() function can be used on sets to remove and return any element from the set. 

Tuples:
Like lists, tuples are ordered and subscriptable, but there's a catch: you can't change them. Indexing allows you to retrieve elements from a tuple; however, modifying them will result in an error. 
Tuples are a better choice if you need to store a lot of data because they require less memory than lists, which makes them more efficient.

When a function needs to return more than one value, tuples are frequently used in this scenario.Though for readability, it's advised. A, B, C = myTuple is another way to break up a tuple's values into individual variables.

Dictionaries:
You can type the dictionary's name and the key enclosed in square brackets to access a particular key-value pair. You can use an assignment operator in a similar manner to add a new key-value pair. To modify an already-existing 
key-value pair, just access it and give it a new value. The.keys() and.values() methods can also be used to retrieve a dictionary's keys and values, respectively. 

A dictionary with a list of values is another typical pattern. It is easy to add to such a structure if the key is there already. Nevertheless, you can handle both scenarios with an if-else statement if you're not sure if the key exists. 
Lastly, remember that, like with lists and strings, you can use the len() function to find the length of a dictionary.

List Comprehensions:
Using a list comprehension, you can generate a for loop and return a copy of the list you're iterating over all in one line. It also lets you apply functions to each entry in a list or filter items.
You write a nested list comprehension to apply a function someFunc to all comments in a list of blog objects.
[[someFunc(comment) for comment in blog.comments] for blog in blogs]

By using the "split" function and creating our own "cleanWord" function, we can manipulate strings to fit our needs and create more useful data structures.

Dictionaries and Comprehensions:
#

Variables and Types:

Data Structures:
Data structures in Python make it possible to store a list of values in a single variable. A list is the first data structure we study, and it can hold any kind of data, 
including lists inside lists. The length function can be used to find the length of a list. A set is similar to a list, but it is declared using curly brackets and can only have unique elements.
 
Unlike a list, a set's elemental order is irrelevant. Lists and tuples are similar in that once they are declared, they cannot be changed. They are helpful for efficiently storing vast amounts of 
data in memory, such as pairs of X and Y coordinates. And last, just like a word and its meaning in a book, a dictionary is an assortment of key-value pairs. Curly braces are used to declare dictionaries, 
and keys are used to access them.

Operators:
The instructions that work with variables and values are called operators.
One type of arithmetic operator is addition, which returns two by adding one and one. Other arithmetic operators available in Python include the multiplication operator (marked by an asterisk) that 
multiplies two numbers together.

The forward slash operator can be used for division, and even if the outcome is a whole number, it yields a floating-point value. Programming-specific, the modulus operator yields the remainder following division. 

Operators can also be used to manipulate strings. While the multiplication operator can repeat a string a given number of times, the addition operator can concatenate or merge two strings together.

There are other operators in Python, such as membership, logical, identity, and comparison operators. Comparison operators assess two variables or values and return a true or false Boolean result. 

Boolean values govern how logical operators like "and," "or," and "not" function. While the "or" operator returns true if at least one operand is true, the "and" operator only returns true if both operands are true. 
The Boolean value that the "not" operator operates on is negated.

Control Flow:
One of the three primary control flow types in programming is the if statement, which lets you run a block of code only in response to specific conditions being met. The if statement in Python looks like this: "a = True, 
if a: print It is true." The code that is indented beneath the if statement will be executed if the condition is true. By indenting it further, you can add more code underneath the if statement.

Functions:
A function is similar to a machine that accepts inputs and outputs, such as a toaster that heats bread and makes toast. The toaster can retain its ability to toast even in the absence of bread. 
Functions can take one or more arguments, and they may or may not return a value. 


Fundaments of Working with Files:
Opening Files:
Python provides a built-in open() function to open files, this take two arguments:
the file path and the model in which you want to open the file('r' for reading, 'w' for
writing 'a' for appending, 'r' for reading and writing).
file = open('example.txt', 'r')

Reading from Files:
After opening a file in read mode('r'), you can read its contents using various methods like
read(), readline(), or 'readline()' or readlines().Eg:
content = file.read()

Writing to Files:
To write to a file, open it in the write mode('w') or append mode('a'), and then use the write()
method to add content. Eg:
file = open('example.txt', 'w')
file.write("Hello, World!")

Close Files: 
Its important to close files after you're done with them to free up system resources.Eg
file.close()

Using 'with' Statement:
This statement automatically closes the file when the block inside it exits, its smoother way 
to handle files. Eg:
with open('example.txt', 'r') as file:
content= file.read()

Working with CSV Files:
For handling CSV files, you can use the built-in 'csv' module, which provides a 'reader' and 'writer'
objects to easily read and write CSV files. Eg:
import csv

with open('data.csv', 'r') as file:
    csv_reader = csv.reader(file)
    for row in csv_reader:
        print(row)

Working with JSON Files: 
Working with JSON files is possible thanks to Python's built-in json module. JSON data can be written to a 
file using json.dump() and loaded from a file using json.load().

import json

# Reading JSON from a file
with open('data.json', 'r') as file:
    data = json.load(file)

# Writing JSON to a file
with open('data.json', 'w') as file:
    json.dump(data, file)





