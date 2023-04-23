# Python

## Typing

### Types of typing

- Static - typing, in which the variable is associated with the type at the moment of declaration, and the type cannot be changed later.

- Dynamic - typing, in which the type of the variable is set at the moment of assigning a value, and not at the moment of declaration, and so on. may be changed later.

static typing example (GO):

```golang
var x int = 5
x = 'abc' // here the GO compiler will swear
```

dynamic typing example (Python):

```python
x = 5
x = 'abc' # here the interpreter does not swear, since the typing is dynamic
```

- Strict - no automatic casts to another type (implicit conversions).
- Non-strict - the presence of those.

strong typing example (Python):

```python
a = [5, 6]
print(",".join(a)) # here the interpreter complains because join() expects a list of strings as input
```

loose typing example (Javascript):

```javascript
let a = "hello";
let b = 100;
let c = a + b;
console.log(c); // "hello100"
```

- Explicit - we specify types everywhere by hand.
- Implicit - the compiler/interpreter does this itself.

explicit typing example (C++):

```C++
int x = 5;
y = 6; // here the compiler will swear
```

implicit typing example (Python):

```python
a = 1
```

Important: the most rational and optimal memory is used in the case of strict static typing.

Python typing : dynamic, strict, implicit.

## Types of data types that are in python

1. mutable

- Lists(list)
- Dictionaries (dict)
- Sets(set)
- Bytearray
- Queues(queue)
- Stacks(stack)
- Trees(tree)
- Graphs(graph)

2. immutable

- Numbers (int, float, complex)
- Boolean values (bool)
- Strings
- Tuples
- File objects (file)
- Frozenset
- bytes
- None

1. Mutable

- Lists

In Python, lists are ordered collections of elements that can be of various data types, including other lists.
They are mutable data types, meaning items in a list can be added, removed, or modified after it's been created.
The list is created using square brackets [], where the list items are separated by commas.

```python
my_list = [1, 2, 3, 4, 5]
```

The elements of a list can be accessed by an index that starts at 0.

```python
first_element = my_list[0]
```

List elements can be modified by assigning new values to them by index.

```python
my_list[1] = 10
```

Lists also support many methods for working with list items, such as adding new items, removing items, sorting, and so on. All of these methods make lists a very handy tool for storing and manipulating collections of data in Python.

- Dictionaries

In Python, dictionaries are unordered collections of key-value pairs. They are also known as associative arrays or hash maps in other programming languages. Dictionaries are mutable data types, which means that their contents can be changed after creation.
A dictionary is created using curly braces {} or the built-in dict() function. Each key-value pair in the dictionary is separated by a colon : and individual pairs are separated by commas.

```python
my_dict = {'apple': 1, 'banana': 2, 'orange': 3}
```

Keys in a dictionary must be unique, but values can be duplicated.
Values in a dictionary can be accessed by referencing their corresponding keys using square brackets [].

```python
my_dict['banana']
```

Dictionaries also have a variety of built-in methods for working with their contents, such as adding or removing key-value pairs, checking if a key is in the dictionary, and iterating over the keys or values. They are a powerful tool for storing and manipulating data in Python.

- Sets

In Python, a set is an unordered collection of unique elements. They are similar to lists and tuples, but unlike lists and tuples, sets cannot contain duplicate elements. Sets are mutable data types, which means that their contents can be changed after creation.
Sets can be created using curly braces {} or the built-in set() function. Elements in a set are separated by commas.

```python
my_set = {1, 2, 3, 4, 5}
```

Sets support mathematical set operations like union, intersection, and difference. For example, to create a union of two sets, we can use the "|" operator.

```python
set1 = {1, 2, 3}
set2 = {3, 4, 5}
union_set = set1 | set2
print(union_set) # Output: {1, 2, 3, 4, 5}
```

We can also add or remove elements from a set using the add() and remove() methods, respectively.

```python
my_set.add(6)
my_set.remove(3)
```

In addition to the built-in methods, sets also support iteration over their elements using a for loop. Overall, sets are a useful data structure for efficiently storing and manipulating unique collections of data in Python.

- Bytearray

In Python, bytearray is a built-in data type used to represent sequences of bytes. bytearray objects are similar to bytes objects, but they can be modified.

```python
ba = bytearray(b'hello')
```

Like other sequence types in Python, you can access individual bytes in a bytearray object using indexing.
You can also slice a bytearray object to get a new bytearray object containing a subset of the original bytes:

Одним из преимуществ bytearray над bytes является то, что вы можете изменять отдельные байты объекта bytearray с помощью индексации:

```python
ba[1] = 111  # changes the second byte to the ASCII code for 'o'
```

- Queues

In Python, queues are a type of data structure used to store and manage a collection of elements in a first-in, first-out (FIFO) order. Queues are commonly used in computer science and software engineering to manage tasks or events that need to be processed in the order in which they were received.

Python provides a built-in module called queue that contains several classes for implementing different types of queues. One of the most commonly used classes is Queue, which is a basic FIFO queue. Other classes in the queue module include LifoQueue, which is a last-in, first-out (LIFO) queue, and PriorityQueue, which is a queue that stores elements with associated priorities.

To use a Queue object in Python, you must first create an instance of the class:

```python
import queue
my_queue = queue.Queue()
```

Once the queue is created, you can add elements to the queue using the put() method and remove elements from the queue using the get() method:

```python
my_queue.put(1)
my_queue.put(2)
my_queue.put(3)

print(my_queue.get()) # Output: 1
print(my_queue.get()) # Output: 2
```

The put() method adds an element to the end of the queue, while the get() method removes and returns the element at the front of the queue.
Queues in Python are thread-safe, which means that they can be safely accessed and modified by multiple threads in a concurrent program. This makes them a useful tool for managing task queues and message queues in multi-threaded applications.

- Stacks

In Python, a stack is a type of data structure that stores and manages a collection of elements in a last-in, first-out (LIFO) order. Stacks are commonly used in computer science and software engineering to manage program memory, function calls, and other types of data.
Python provides a built-in list data type that can be used to implement a stack. To use a list as a stack, you can use the append() method to add elements to the top of the stack and the pop() method to remove elements from the top of the stack:

```python
my_stack = []

my_stack.append(1)
my_stack.append(2)
my_stack.append(3)

print(my_stack.pop()) # Output: 3
print(my_stack.pop()) # Output: 2
```

Python also provides a built-in module called queue that contains a class called LifoQueue, which is a last-in, first-out (LIFO) queue. LifoQueue can be used to implement a stack, and provides the same methods as a regular Queue object (put(), get(), etc.):

```python
import queue

my_stack = queue.LifoQueue()

my_stack.put(1)
my_stack.put(2)
my_stack.put(3)

print(my_stack.get()) # Output: 3
print(my_stack.get()) # Output: 2
```

In general, stacks are a useful tool for managing collections of data in a last-in, first-out (LIFO) order. They are commonly used in algorithm design, programming language implementations, and other areas of computer science.

- Trees

In Python, a tree is a type of data structure used to represent hierarchical relationships between elements. Trees consist of nodes, which are connected by edges to form a hierarchical structure. The topmost node in a tree is called the root, and nodes without any child nodes are called leaves.

Trees are commonly used in computer science and software engineering for organizing and managing data, such as file systems, search trees, and decision trees. There are several different types of trees in Python, including binary trees, n-ary trees, and balanced trees.

- Graphs

In Python, a graph is a data structure used to represent a collection of interconnected nodes, called vertices or nodes, and the edges that connect them. Graphs are commonly used in computer science and software engineering to represent complex networks, such as social networks, transportation networks, and communication networks.
In a graph, each node is represented as an object or a data structure, and each edge is represented as a pair of nodes that are connected. Edges can be directed or undirected, depending on whether they represent a one-way or two-way connection between nodes. Graphs can also be weighted, meaning that each edge has a weight or a value associated with it.
Python provides several libraries and modules for working with graphs, such as the networkx library for creating and analyzing graphs, and the graph-tool library for performing advanced graph operations.

```python
import networkx as nx

# create an empty graph
G = nx.Graph()

# add nodes to the graph
G.add_node(1)
G.add_node(2)
G.add_node(3)

# add edges to the graph
G.add_edge(1, 2)
G.add_edge(2, 3)
G.add_edge(3, 1)

# print information about the graph
print(nx.info(G))
```

Overall, graphs are a powerful data structure for representing complex networks and relationships, and Python provides several tools and libraries for working with them effectively.

2. Immutable

- Numbers

In Python, there are several different types of numbers that can be used in mathematical operations and calculations. These include:

Integers (int): Integers are whole numbers, both positive and negative, that do not have a fractional component. They can be represented in Python using the int type.

Floating-point numbers (float): Floating-point numbers are numbers that have a fractional component. They can be represented in Python using the float type.

Complex numbers (complex): Complex numbers are numbers that have a real and imaginary component. They can be represented in Python using the complex type.

In addition to these basic number types, Python also provides several modules and libraries for working with more advanced mathematical operations, such as trigonometric functions, logarithms, and random number generation. These include the math module and the random module.

- Boolean values

In Python, boolean values are used to represent the truth values of logical expressions. Boolean values can have two possible values: True or False.

Boolean values are typically used in conditional statements and loops to determine the flow of program execution based on the evaluation of a logical expression. In Python, the boolean values True and False are keywords that represent the truth values of logical expressions.

- Strings

In Python, a string is an ordering sequence of characters. Strings are used to represent text-based data, such as words, sentences, and paragraphs.

Strings are a type of object in Python and are represented using the str type. Strings can be created using single quotes ('...') or double quotes ("...") and can contain letters, digits, and special characters.

In Python3, the default string is Unicode, which eliminates the problems of working and displaying Cyrillic characters and various rare encodings.
If you want to add characters to an existing string, you will have to create a new string, with a new address in memory:

```python
a = "hello"
id(a) # 2044344987401
a = "hello world"
id(a) # 2044334957804
```

- Tuples

In Python, a tuple is a collection of ordered, immutable elements. Tuples are similar to lists, but the main difference is that tuples cannot be modified once they are created.

Tuples are defined using parentheses () and can contain elements of any data type, including other tuples. Since tuples are immutable, you cannot add, remove, or modify elements once they are defined.

Since tuples are immutable, they are often used to represent collections of values that should not be modified. For example, tuples can be used to represent the coordinates of a point in a two-dimensional space, or the RGB values of a color.

```python
a = (1,2)
id(a) # 2044370285184
a = (1,2,3)
id(a) # 2044369999872
```

- File objects

In Python, a file object is used to represent a file on disk or any other file-like input/output stream. File objects are created by the built-in open() function, which returns a file object that can be used to read from or write to a file.

File objects have a number of methods for reading and writing data, as well as manipulating the file itself. Here are some common methods for file objects in Python:

- read(size): reads and returns up to size bytes of data from the file.
- readline(): reads and returns one line of data from the file.
- readlines(): reads and returns a list of lines from the file.
- write(string): writes string to the file.
- writelines(lines): writes a list of strings to the file.
- close(): closes the file.

```python
# opening a file for writing
f = open('myfile.txt', 'w')

# writing data to the file
f.write('Hello, world!\n')
f.write('This is a test\n')

# closing the file
f.close()

# opening a file for reading
f = open('myfile.txt', 'r')

# reading data from the file
data = f.read()
print(data)

# closing the file
f.close()
```

- Frozenset

In Python, a frozenset is an immutable version of the built-in set type. Like sets, frozenset objects contain a collection of unique, hashable elements, but unlike sets, frozenset objects cannot be modified once they are created.

```python
# creating a frozenset
s = frozenset([1, 2, 3, 3, 4])
print(s)  # output: frozenset({1, 2, 3, 4})
```

Since frozenset objects are immutable, they can be used as keys in dictionaries or elements in other sets, whereas regular sets cannot. This is because mutable objects such as sets are not hashable, and therefore cannot be used as dictionary keys or set elements.

Overall, frozenset objects provide a way to create an immutable set of elements that can be used in situations where mutability is not desired, such as in dictionary keys or set elements.

- Bytes

In Python, bytes is a built-in data type used to represent sequences of bytes. bytes objects are immutable, meaning that their contents cannot be changed once they are created.
Like other sequence types in Python, you can access individual bytes in a bytes object using indexing.
Here are some common methods for bytes objects:

decode(encoding='utf-8', errors='strict'): decodes the bytes object using the specified character encoding and returns a str object.
hex(): returns a string containing the hexadecimal representation of the bytes object.
bytes objects are commonly used in applications that require working with binary data, such as cryptography, data serialization, and network protocols. Since bytes objects are immutable, they are also useful for representing data that should not be changed accidentally or maliciously.

- None

In Python, None is a built-in constant that represents the absence of a value. It is often used to indicate that a variable or argument has not been assigned a value or that a function does not return a value.

None is a singleton object, meaning that there is only one instance of it in memory at any given time. You can assign None to a variable or return it from a function like any other value:

```python
x = None

def my_func():
    return None
```

None is often used as a default return value for functions that don't return anything useful, or as a sentinel value to indicate that a function encountered an error.

## Sequences

### What is sequence

A sequence in Python is an iterable object that supports efficient element access using integer indices through a special `__getitem__()` method and supports a `__len__()` method that returns the length of the sequence.
The main built-in sequence types are list, tuple, range, str, bytes and bytearray.

Sequences can also optionally implement the `count()`, `index()`, `__contains__()` and `__reversed__()` methods and others.

### Which operations are supported by most sequences

- `x in s`, `x not in s` - whether element x is in sequence s (for strings and byte sequences - whether x is a substring of s)
- `s + t` - sequence concatenation
- `s * n, n * s` - concatenation of n non-recursive copies of the sequence s
- `s[i]` - i-th element of the sequence s
- `s[i:j]` – slice of sequence s from i to j
- `s[i:j:k]` - cut sequence s from i to j with step k
- `len(s)` - sequence length
- `min(s)` - the minimum element of the sequence
- `max(s)` - the maximum element of the sequence
- `s.index(x[, i[, j]])` - index of the first occurrence of x (optional - starting from position i to position j)
- `s.count(x)` is the total number of occurrences of x in s
- `sum(s)` - the sum of the elements of the sequence

Immutable sequences usually implement the hash(s) operation, the hash value of an object.

- `s[i] = x` – элемент с индексом i заменяется на x
- `s[i:j] = t`, `s[i:j:k] = t` – элементы с индексами от i до j (с шагом k) заменяются содержимым итерабельного объекта t
- `del s[i:j]`, `del s[i:j:k]` – удаление соответствующих элементов из последовательности
- `s.append(x)` – добавление x в конец последовательности
- `s.clear()` – удаление всех элементов последовательности
- `s.copy()` – нерекурсивная копия последовательности
- `s.extend(t)` – добавление всех элементов итерабельного объекта в конец последовательности
- `s.insert(i, x)` – вставка элемента x по индексу i
- `s.pop()`, `s.pop(i)` – возврат значения по индексу i (по умолчанию – последний элемент) и удаление его из последовательности
- `s.remove(x)` – удаление первого вхождения x
- `s.reverse()` – разворот последовательности в обратном порядке

### What kinds of strings are there in python

Depends on the version of Python. In the second branch, two types: single-byte strings and Unicode are represented by the str and unicode classes, respectively. Python 3 has one kind of string, str, which is Unicode. There are no single-byte strings, instead of them there is a bytes type, that is, a chain of bytes.

### Is it possible to change a single character within a string

No, strings are immutable. The replace, format, and concatenation operations return a new string.

### How to concatenate a list of strings into one. How to split a string into a list of strings

To join, you need the `.join()` string method. To split, the `.split()` method.

### How to encode and decode strings

Encode - translate Unicode into a byte string. Call the `.encode()` method on a string.

Decode - recover a string from a string of bytes. Call the `.decode()` method on the `str` or `bytes` object (Python 2 and 3 respectively).

In both cases, explicitly pass the encoding, otherwise the one defined in the system by default will be used. Be prepared to catch `UnicodeEncodeError`, `UnicodeDecodeError` exceptions.

### How is a list different from a tuple

Lists are mutable sequences, typically used to store data of the same type (although Python doesn't prohibit storing data of different types in them). Represented by the list class.

Tuples are immutable sequences commonly used to store heterogeneous data. Represented by the tuple class.

At the language level, they differ in that you cannot add or remove an element to a tuple. There are no differences at the interpreter level. Both collections are represented by an array of pointers to a `PyObject` structure.

For a list, functions are defined that add a new element to such an array, remove an existing one, and merge two arrays into one. They are called by the list methods `.append()`, `.pop()`, `.sort()`, and so on.

### What is a range

Ranges are immutable sequences of numbers that are specified by start, end and step. Represented by the class range (in Python 2, xrange; range in Python 2 is a function that returns a list).
Constructor parameters must be integers (either int class instances or any object with an `__index__` method)
Supports all operations common to sequences, except for concatenation and repetition, and, in versions of Python prior to 3.2, slicing and negative indexes.

### How to make a list unique (no duplicate elements)

Set variant. Does not guarantee the order of elements. The order is preserved only for small lists.

```python
list(set([1, 2, 2, 2, 3, 3, 1]))
>>> [1, 2, 3]
```

Variant with OrderedDict. Guarantees the order of elements.

```python
>>> from collections import OrderedDict
>>> list(OrderedDict.fromkeys([1, 2, 2, 2, 3, 3, 1]))
[1, 2, 3]
```

Loop option. Slowly, but it guarantees order. Suitable if elements cannot be placed inside a set (for example, dictionaries).

```python
res = []
for x in [1, 2, 2, 2, 3, 3, 1]:
     if x not in res:
         res append(x)
>>> [1, 2, 3]
```

### There is a tuple of three elements. Assign variables a, b, c their values

`a, b, c = (1, 2, 3)`

### How sequences are compared

Two sequences are equal if they have the same type, the same length, and the corresponding elements of both sequences are equal.

Sequences of the same types can be compared. Comparisons occur in lexicographic order: a sequence of smaller length is less than a sequence of larger length, but if their lengths are equal, then the result of the comparison is equal to the result of comparing the first differing elements.
