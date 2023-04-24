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

Strict typing example (Python):

```python
a = [5, 6]
print(",".join(a)) # here the interpreter complains because join() expects a list of strings as input
```

Non-strict typing example (Javascript):

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

One advantage of bytearray over bytes is that you can change individual bytes of a bytearray object using indexing:

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

Most mutable sequences support the following operations:

- `s[i] = x` - element with index i is replaced by x
- `s[i:j] = t`, `s[i:j:k] = t` - elements with indexes from i to j (in increments of k) are replaced by the contents of the iterable object t
- `del s[i:j]`, `del s[i:j:k]` - remove matching elements from sequence
- `s.append(x)` - append x to the end of the sequence
- `s.clear()` - remove all elements of the sequence
- `s.copy()` - non-recursive copy of a sequence
- `s.extend(t)` - add all elements of an iterable object to the end of the sequence
- `s.insert(i, x)` - insert element x at index i
- `s.pop()`, `s.pop(i)` - return the value at index i (default is the last element) and remove it from the sequence
- `s.remove(x)` - remove the first occurrence of x
- `s.reverse()` - reverse the sequence

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

## Sets and mappings

### How to understand if an object is hashable

An object is said to be hashable if it has a hash value (an integer) that never changes during its life cycle and is returned by the `__hash__()` method, and can be compared with other objects (implements the `__eq__()` method). Equal hashable objects must have equal hash values.
All standard immutable objects are hashable. All standard mutable objects are not hashable.

### What is a set

A set is an unordered collection of hashable objects that do not repeat.
Sets have no concept of element position. Accordingly, they do not support indexing and slicing.
Built-in set classes: set (mutable set), frozenset (immutable set).

### What sets are used for

Commonly used to test an element for membership in a set and remove repetitions of elements and perform operations such as union, intersection, difference, and symmetrical difference

### What operations can be performed on sets

- `set([iterable])`, `frozenset([iterable])` - creating a set (empty or from elements of an iterable object)
- `len(s)` - the number of elements in the set
- `x in s`, `x not in s` - checking if an element is in the set
- `s.isdisjoint(t)` - checking that the given set has no common elements with the given
- `s.issubset(t)`, `s <= t` - checking that all elements of set s are elements of set t
- `s < t` - check that s <= t and s != t
- `s.isuperset(t)`, `s >= t` - checking that all elements of set t are elements of set s
- `s > t` - check that `s >= t` and `s != t`
- `s.union(t, ...)`, `s | t | ...` – creation of a new set, which is the union of the given sets
- `s.intersection(t, ...)`, `s & t & ...` - create a new set that is the intersection of the given sets
- `s.difference(t, ...)`, `s - t - ...` - create a new set, which is the difference of given sets
- `s.symmetric_difference(t)`, `s ^ t` - create a new set that is the symmetric difference of the given sets (i.e., the difference between union and intersection of sets)
- `s.copy()` is an incomplete copy of the set s

Set operations, which are methods, take any iterable objects as arguments. Set operations written as binary operations require that the second operand of the operation is also a set and return a set of the same type as the first set.

Operations on mutable sets:

- `s.update(t, ...)`, `s |= t | ...` – add elements from other sets to the given set
- `s.intersection_update(t, ...)`, `s &= t & ...` - leave in this set only those elements that are in other sets
- `s.difference_update(t, ...)`, `s -= t | ...` - remove from the given set those elements that are in other sets
- `s.symmetric_difference_update(t)`, `s ^= t` - keep or add to s elements that are either in s or t, but not in both sets
- `s.add(element)` - add a new element to the set
- `s.remove(element)` - remove an element from the set; if there is no such element, a KeyError exception is thrown
- `s.discard(element)` - remove an element from the set if it is in it
- `s.pop()` - remove from the set and return an arbitrary element; if the set is empty, a KeyError exception is thrown
- `s.clear()` - remove all elements of the set.

### How sets are checked for equality

Sets are checked for equality element by element, regardless of the types of sets.

### What is mapping

Mapping is a container object that supports random access to elements by keys and describes all methods described in the abstract base class `collections.Mapping` (`get()`, `items()`, `keys() `, `values()`) or `collections.MutableMapping` (`clear()`, `get()`, `items()`, `keys()`, `pop()`, `popitem()` , `setdefault()`, `update()`, `values()`).
Mappings include the `dict`, `collections.defaultdict`, `collections.OrderedDict` and `collections.Counter` classes.

### What are the nuances in using numbers as keys

Numeric keys in dictionaries follow the rules for comparing numbers. Thus, `int(1)` and `float(1.0)` are considered the same key. However, because float values are stored approximately, it is not recommended to use them as keys.

```python
>>> {True: 'yes', 1: 'no', 1.0: 'maybe'}
{True: 'maybe'}
```

### What operations can be performed on mappings

- `len(d)` is the number of elements.
- `d[key]` - get value with key key. If no such key exists and the mapping implements the `__missing__(self, key)` special method, then it is called. If the key does not exist and the `__missing__` method is not defined, a KeyError exception is thrown.
- `d[key] = value` - change the value or create a new key-value pair if the key does not exist.
- `key in d`, `key not in d` – check if the key is present in the display.
- `iter(d)` is the same as iter(d.keys()).
- `clear()` - remove all elements of the dictionary.
- `copy()` - create an incomplete copy of the dictionary.
- `(class method) dict.fromkeys(sequence[, value])` – creates a new dictionary with keys from the sequence sequence and the given value (default is None).
- `d.get(key[, default])` - safely get value by key (never throws KeyError). If the key is not found, the default value is returned (the default is None).
- `d.items()` - in Python 3, returns a dictionary representation object corresponding to pairs (two-tuples) of the form (key, value). In Python 2, it returns the corresponding list, and the iteritems() method returns an iterator. The equivalent method in Python 2.7 is viewitems().
- `d.keys()` - in Python 3, returns a dictionary view object corresponding to the keys of the dictionary. In Python 2, it returns the corresponding list, and the iterkeys() method returns an iterator. The equivalent method in Python 2.7 is viewkeys().
- `d.pop(key[, default])` - if the key key exists, removes the element from the dictionary and returns its value. If the key does not exist and default is set, then that value is returned, otherwise a KeyError exception is thrown.
- `d.popitem()` - removes an arbitrary key-value pair and returns it. If the dictionary is empty, a KeyError exception is thrown. The method is useful for algorithms that traverse the dictionary by removing already processed values (for example, certain algorithms related to graph theory).
- `d.setdefault(key[, default])` - if the key key exists, returns the corresponding value. Otherwise, it creates an element with key key and default value. default is None by default.
- `d.update(mapping)` - accepts either another dictionary or mapping, or an iterable object consisting of iterable objects - key-value pairs, or named arguments. Adds matching elements to the dictionary, overwriting elements with existing keys.
- `d.values()` - in Python 3, returns a dictionary view object corresponding to the values. In Python 2, it returns the corresponding list, and the itervalues() method returns an iterator. The equivalent method in Python 2.7 is viewvalues().

### What the items method returns

The objects returned by the `items()`, `keys()` and `values()` methods (`viewitems()`, `viewkeys()`, `viewvalues()` in Python 2.7) are _dictionary view_ objects . They provide a dynamic view of dictionary elements, that is, changes to this dictionary are automatically reflected on these objects as well.

Operations with dictionary representations:

- `iter(dictview)` - Get an iterator over keys, values, or key/value pairs. All dictionary views, when iterated, return the elements of the dictionary in the same order. Trying to modify a dictionary while iterating may throw a RuntimeError exception
- `len(dictview)` is the number of elements in the dictionary.
- `x in dictview` - Check if a key, value, or key-value pair exists in the dictionary.

### How to sort a list of dictionaries by a specific field

The list method `.sort()` and the built-in function `sorted()` take a `key` parameter. It should be a callable object that takes the next element (in our case, a dictionary) and returns a sorting criterion value.

The code below shows how to sort a list of people by age:

```python
users = [{'age': 30}, {'age': 20}, {'age': 10}]
users.sort(key=lambda user: user['age'])
>>> [{'age': 10}, {'age': 20}, {'age': 30}]
```

### What can be a dictionary key. What can't. Why

A dictionary key can be any hashable immutable object: a number, a string, a datetime, a function, and even a module. Such objects have a `__hash__()` method that unambiguously maps the object to some number. By this number, the dictionary looks up the value for the key.

Lists, dictionaries, and sets are mutable and have no hashing method. When substituting them into a dictionary, an error will occur.

The hash of a tuple is calculated recursively over all elements. Yes, tuple

`(1, (True, (42, ('hello', ))))`
consists only of immutable elements, so it can be a key. However, such a tuple

`(1, (True, (42, ({'hello': 'world'}, ))))`
contains a dictionary deep inside, so the hash cannot be calculated.

### There are two lists - keys and values. How to make a dictionary out of them

```python
keys = ['foo', 'bar', 'baz']
vals = [1, 2, 3]
dict(zip(keys, vals))
>>> {'baz': 3, 'foo': 1, 'bar': 2}
```

The `zip` function returns a list of pairs of Nth elements. The `dict` constructor takes a list of pairs. It treats each pair as a key and a value, respectively.

### How a hash table works

A hash table is a sparse array (an array that has empty positions). In standard English textbooks, hash table cells are called "bucket". In the dict hash table, each element corresponds to a cell containing two fields: a reference to the key and a reference to the element's value. Since the size of all cells is the same, an individual cell is accessed by offset.

Python tends to leave at least a third of the cells empty; if the hash table becomes too full, it is copied to a new location in memory where there is room for more cells.

To put an element into a hash table, the first step is to calculate the hash value of the element's key. This is done by the `hash()` built-in function.

To select a value using the `my_dict[search_key]` expression, Python calls the `hash(search_key)` function to get the search*key hash value, and uses the few least significant bits of the resulting number as a cell offset from the beginning of the hash table (exactly how many bits depends from the current table size). If the found cell is empty, a `KeyError` exception is raised. Otherwise, there is some element in the found cell - a `key:value` pair - and then Python checks if search_key == found_key is true. If yes, then the element is found and found_value is returned. If search_key and found_key do not match, then there is a \_hash collision*. To resolve a collision, the algorithm takes various bits of the hash value, performs certain actions on them, and uses the result as an offset to another cell.

### What is a collision

When a hash function returns the same answer for different data.

### Where search will be faster, and where search and why: dict, list, set, tuple

The lookup will be faster in dict and set because they are hash tables and element access takes O(1). For list and tuple, the search will be performed in O(n) on average.

The exception only works for very small lists up to 5 elements long. In this case, it will be faster for the interpreter to run through the list than to calculate the hash.

In Python 2, the `keys`, `values`, `items` dictionary methods return a list. That is, before iterating over a dictionary (or set), the interpreter first creates a new list, which takes additional time and memory, but after creation it is already an ordinary list. That is, in Python 2, iteration over dictionaries and sets takes longer, by creating a new list and copying elements into it.

In Python 3, these methods create a representation object. This is definitely faster than creating a new list in Python2. But iteration over such a representation should take a little longer than over the list due to the fact that data in dictionaries is stored sparsely (rarely, sparsely). In support of the above (Python 3):

```python
>>> l = list(range(1000000))
>>> d = dict.fromkeys(l)
>>> s = set(l)
>>>def iter_list():
... for i in l:
... pass
...
>>>def iter_dict():
... for i in d:
... pass
...
>>>def iter_set():
... for i in s:
... pass
...
>>> timeit.timeit(iter_list, number=1000)
  6.727667486004066
>>> timeit.timeit(iter_dict, number=1000)
  9.293120226997416
>>> timeit.timeit(iter_set, number=1000)
  8.627948219014797
```

## Functions

### What are args, kwargs. When are they required?

The expressions `*args` and `**kwargs` are declared in the function signature. They mean that variables named `args` and `kwargs` (without asterisks) will be available inside the function. You can use other names, but this is considered bad form.

`args` is a tuple that accumulates positional arguments. `kwargs` is a dictionary of named arguments, where key is the name of the parameter, value is the value of the parameter.

**Important:** if no parameters are passed to the function, the variables will be equal to an empty tuple and an empty dictionary, respectively, and not `None`.

Please don't confuse a tuple with a list. The next question explains why.

### Why using mutable objects as default parameters is bad. Give an example of a bad case. How to fix

The function is created once when the module is loaded. Named parameters and their default values are also created once and stored in one of the function object's fields.

In our example, `bar` is equal to the empty list. The list is a mutable collection, so the value of `bar` can change from call to call. Example:

```python
def foo(bar=[]):
     bar append(1)
     return bar
foo()
>>> [1]
foo()
[eleven]
foo()
>>> [1, 1, 1]
```

It is considered good practice to specify an empty immutable value for the parameter, for example `0`, `None`, `''`, `False`. In the body of the function, check for fullness and create a new collection:

```python
def foo(bar=None):
     if bar is None:
         bar = []
     bar append(1)
     return bar
foo()
>>> [1]
foo()
>>> [1]
foo()
>>> [1]
```

The above is relevant incl. for sets and dictionaries.

### Is it possible to pass a function as an argument to another function

Yes, in Python it is possible to pass functions as arguments to another function. A function in Python is a first-order object, it allows: assignment, transfer to a function, deletion.
This approach is called function argument passing or using functional programming.
This is a very powerful tool that allows you to create more flexible and abstract functions that can take different actions as arguments in order to perform different operations.

Example:

```python
def apply_function(func, lst):
    result = []
    for item in lst:
        result.append(func(item))
    return result

def square(x):
    return x**2

numbers = [1, 2, 3, 4, 5]
squares = apply_function(square, numbers)
print(squares)
```

### Is it possible to declare a function inside another function. Where will she be seen?

Can. Such a function will only be visible inside the first function.

### What are lambdas. What are their features

Lambda functions in Python are unnamed functions that can be defined and passed as arguments to other functions. They are commonly used in places where you need to quickly define a function without having to create a separate name for it.

Main features of lambda functions in Python:

They are defined using the lambda keyword, followed by a comma-separated list of arguments, followed by a colon, and then the body of the function.

They return the result of their work using an expression that is specified in the function body.

They can be used anywhere a function is expected, including as function arguments.

They can be called directly, but it's better to use them as arguments to other functions.

```python
# Define a lambda function to calculate the square of a number
square = lambda x: x ** 2

# Use a lambda function as an argument to another function
numbers = [1, 2, 3, 4, 5]
squares = map(lambda x: x ** 2, numbers)

print(square(5))   # Output: 25
print(list(squares))   # Output: [1, 4, 9, 16, 25]
```

Thus, lambda functions in Python can be very handy when you need to quickly define a small function without creating a separate name for it. However, their use should be limited only to those places where it is really convenient and improves the readability and maintainability of the code.

### Are the following expressions allowed?

- `nope=lambda:pass`
- `riser = lambda x: raise Exception(x)`

No, loading the module will throw a `SyntaxError` exception. In the lambda body,
be just an expression. `pass` and `raise` are operators.

### How argument values are passed to a function or method

In languages such as C++, there are variables stored on the stack and in dynamic memory. When a function is called, we push all the arguments onto the stack, after which we transfer control to the function. She knows the sizes and offsets of variables on the stack, and accordingly can interpret them correctly.
In this case, we have two options: copy the memory of the variable onto the stack or put a reference to the object in dynamic memory (or at higher stack levels).
It is obvious that when the values on the function stack change, the values in the dynamic memory will not change, and when the memory area changes by reference, we modify the shared memory, so all references to the same memory area will “see” the new value.

In python, this mechanism has been abandoned, the replacement is the _assignment_ mechanism of a variable name with an object, for example, when creating a variable:
`var="john"`

The interpreter creates a "john" object and a "name" var, and then associates the object with the given name.
When a function is called, no new objects are created, instead a name is created in its scope that is associated with an existing object.
But in python there are mutable and immutable types. The latter, for example, include numbers: during arithmetic operations, existing objects do not change, but a new object is created, with which the existing name is then associated. If no name is associated with the old object after that, it will be removed using the reference counting mechanism.
If the name is associated with a variable of a mutable type, then during operations with it, the object's memory changes, respectively, all names associated with this memory area will "see" the changes.

### What is a closure

In Python, a closure is a function object that has access to variables in its enclosing lexical scope, even when the function is called outside that scope. This means a closure can remember and access values from the outer function even if the outer function has completed execution. Closures are created when a nested function references a value from its enclosing scope. The nested function can be returned as a closure, allowing the referenced value to be accessed even after the outer function has completed execution. Closures are commonly used in situations where a value needs to be accessed and updated by multiple functions or methods.

## Iterators and generators

- [Iterators and generators(rus)](https://xakep.ru/2014/10/06/generatora-iteratory-python/)
- [Iterable object, iterator and generator](https://habr.com/ru/post/337314/)

### What is a container

A container is a data type that encapsulates values of other types. Lists, tuples, sets, dictionaries, etc. are containers.

### What is an iterable object

_An iterable object_ is an object that can return values one at a time.
Examples: all containers and sequences (lists, strings, etc.), files, and instances of any classes that have an `__iter__()` or `__getitem__()` method defined.
Iterables can be used inside a `for` loop, as well as in many other cases where a sequence is expected (functions `sum()`, `zip()`, `map()`, etc.).

**More**:

Consider an iterable object (`Iterable`). In the standard library, it is declared as an abstract class `collections.abc.Iterable`:

```python
class Iterable(metaclass=ABCMeta):

    __slots__ = ()

    @abstractmethod
    def __iter__(self):
        while False:
            yield None

    @classmethod
    def __subclasshook__(cls, C):
        if cls is Iterable:
            return _check_methods(C, "__iter__")
        return NotImplemented
```

It has an abstract `__iter__` method which should return an iterator object. And the `__subclasshook__` method which checks if the class has the `__iter__` method. Thus, it turns out that an iterable object is any object that implements the `__iter__` method.

```python
class SomeIterable1(collections.abc.Iterable):
    def __iter__(self):
        pass

class SomeIterable2:
    def __iter__(self):
        pass

print(isinstance(SomeIterable1(), collections.abc.Iterable))
# True
print(isinstance(SomeIterable2(), collections.abc.Iterable))
# True
```

But there is one point, this is the `iter()` function. It is this function that is used, for example, by the for loop to obtain an iterator. The `iter()` function first calls its `__iter__` method to get an iterator from an object. If the method is not implemented, then it checks for the presence of the `__getitem__` method, and if it is implemented, then an iterator is created based on it. `__getitem__` must accept a zero-based index. If none of these methods are implemented, then a `TypeError` exception will be thrown.

```python
from string import ascii_letters

class SomeIterable3:
    def __getitem__(self, key):
        return ascii_letters[key]

for item in SomeIterable3():
    print(item)
```

### What is an iterator

_Iterator_ (iterator) is an object that represents a stream of data. Repeatedly calling the `__next__()` (`next()` in Python 2) method of an iterator, or passing it to the `next()` built-in function, returns the subsequent elements of the stream.

If there is no more data left, a `StopIteration` exception is thrown. After that, the iterator is exhausted and any subsequent calls to its `__next__()` method again throw a `StopIteration` exception.

Iterators are required to have a `__iter__` method that returns the iterator object itself, so any iterator is also an iterable object and can be used almost anywhere that iterable objects are accepted.

**Details:**

Iterators are represented by the abstract class `collections.abc.Iterator`:

```python
class Iterator(Iterable):

     __slots__ = ()

     @abstractmethod
     def __next__(self):
         'Return the next item from the iterator. When exhausted, raise StopIteration'
         raise StopIteration

     def __iter__(self):
         return self

     @classmethod
     def __subclasshook__(cls, C):
         if cls is Iterator:
             return _check_methods(C, '__iter__', '__next__')
         return NotImplemented
```

`__next__` Returns the next available element and throws a `StopIteration` exception when there are no more elements left.
`__iter__` Returns `self`. This allows an iterator to be used where an iterable object is expected, such as `for`.
`__subclasshook__` Checks if the class has a method `__iter__` and `__next__`

### What is a generator

Depending on the context, it can mean either a generator function or a generator iterator (most often the latter).
The `__iter__` and `__next__` methods for generators are created automatically.

From an implementation point of view, a _generator_ in Python is a language construct that can be implemented in two ways: as a function with the `yield` keyword, or as a generator expression. As a result of calling a function or evaluating an expression, we get a generator object of type `types.GeneratorType`. The canonical example is a generator generating a sequence of Fibonacci numbers that, being infinite, could not fit into any collection. Sometimes the term is applied to the generator function itself, and not just the object returned to it as a result.

Since the `__next__` and `__iter__` methods are defined in the generator object, that is, the iterator protocol is implemented, from this point of view, in Python, any generator is an iterator.

When the generator function terminates (by using the `return` keyword or reaching the end of the function), a `StopIteration` exception is thrown.

### What is a generator function

_Generator function_ - a function whose body contains the `yield` keyword. When called, such a function returns a generator object (generator iterator).

### What yield does

`yield` freezes the state of the generator function and returns the current value. After the next call to `__next__()`, the generator function continues its execution from where it left off.

### What is the difference between \[x for x in y\] and (x for x in y)

The first expression returns a list (list inclusion), the second is a generator.

### What is special about the generator

The generator does not store all elements in memory, but only the internal state for calculating the next element. At each step, only the next element can be calculated, but not the previous one. You can only loop through the generator once.

### How to declare a generator

- use `(x for x in seq)` syntax
- `yield` operator in function body instead of `return`
  is the `iter` built-in function that calls the `__iter__()` method of an object. This method must return a generator.

### How to get a list from a generator

Pass it to the list constructor: `list(x for x in some_seq)`. It is important that after that it will no longer be possible to iterate over the generator.

### What is a subgenerator

In Python 3, there are so-called subgenerators. If a pair of keywords `yield from` occurs in a generator function, followed by a generator object, then this generator delegates access to the subgenerator until it completes (its values run out), after which it continues its execution.

Actually `yield` is an expression. It can take values that are sent to the generator. If no values are sent to the generator, the result of this expression is `None`.

`yield from` is also an expression. Its result is the value that the subgenerator returns in the `StopIteration` exception (for this, the value is returned using the `return` keyword).

### What methods do generators have

- `__next__()` - starts or continues execution of the generator function. The result of the current yield expression will be None. Execution then continues to the next yield expression, which passes the value to where `__next__` was called. If the generator terminates without returning a value with `yield`, a `StopIteration` exception is thrown. The method is usually called implicitly, i.e. by a `for` loop or the built-in `next()` function.
- `send(value)` - continues execution and sends the value to the generator function. The value argument becomes the value of the current yield expression. The `send()` method returns the next value returned by the generator, or throws a `StopIteration` exception if the generator terminates without returning a value. If `send()` is used to start a generator, then the only valid value is `None`, since no yield expression has yet been executed that can be assigned that value.
- `throw(type[, value[, traceback]])` - throws an exception of type type at the place where the generator was stopped and returns the next value of the generator (or throws `StopIteration`). If the generator does not handle the given exception (or throws another exception), then it is thrown at the call site.
- `close()` - Throws a `GeneratorExit` exception at the location where the generator was suspended. If a generator throws `StopIteration` (by terminating normally or because it is already closed) or `GeneratorExit` (by not handling the given exception), `close` simply returns to the place of the call. If the generator returns another value, a `RuntimeError` exception is thrown. The `close()` method does nothing if the generator has already completed.

### Is it possible to extract a generator element by index

No, there will be an error. The generator does not support the `__getitem__` method.

### What does iterating over a dictionary return

Key. The order of the keys is not guaranteed (in 3.6 it is unofficially guaranteed, in 3.7 it is guaranteed). For small dictionaries, the order will be the same as in the declaration. For larger ones, the order depends on the location of the elements in memory. The special class `OrderedDict` respects the order in which keys are added.

```python
for key in {'foo': 1, 'bar': 2}:
     process_key(key)
```

### How to iterate a dictionary over key-value pairs

The `.items()` dictionary method returns a generator of `(key, value)` tuples.

### What is a coroutine

A coroutine is a program component that generalizes the concept of a subroutine, which additionally supports multiple entry points (rather than one, like a subroutine) and stopping and continuing execution while maintaining a certain position.
The advanced features of generators in Python (yield and yield from expressions, sending values to generators) are used to implement coroutines.
Coroutines are useful for implementing asynchronous non-blocking operations and cooperative multitasking on the same thread without using callback functions and writing asynchronous code in a synchronous style.
Python 3.5 includes support for coroutines at the language level. The async and await keywords are used for this.

## Classes, objects

### How to get a list of object attributes

The `dir` function returns a list of strings - fields of the object. The `__dict__` field contains a dictionary of the form `{field -> value}`.

### What are magic methods, what are they for?

Magic methods are methods whose names begin and end with a double underscore. They are magical because they are almost never called explicitly. They are called by built-in functions or syntactic constructs. For example, the `len()` function calls the `__len__()` method of the passed object. The `__add__(self, other)` method is called automatically when added with the `+` operator.

Here are some magical methods:

- `__init__`: class initializer
- `__new__`: called when an instance of a class is created and returns a new object of that class. It is called before the `__init__` method and allows you to create and configure an object before it is initialized.
- `__add__`: addition with another object
- `__eq__`: check for equality with another object
- `__iter__`: returns an iterator

### How to refer to the parent class in a class

The `super` function takes a class and an instance:

```python
class NextClass(FirstClass):
     def __init__(self, x):
         super(NextClass, self).__init__()
         self.x = x
```

### Is it possible to have multiple inheritance

Yes, you can specify more than one parent in a child class.

### What is MRO

_MRO_ – method resolution order, method resolution order. The algorithm by which the method should be searched if the class has two or more parents.

In classical classes, the search for inheritance by references to names is carried out in the following order:

1. Instance first
2. Then his class
3. Next, all superclasses of its class, first by depth, and then from left to right

The first occurrence found is used. This order is called DFLR (Depth Traversal Left to Right).

When inheriting new-style classes, the MRO (method resolution order) rule is applied, i.e. linearized traversal of the class tree, with the nested inheritance element made available in the `__mro__` attribute of the class. Such an algorithm is called _C3-linearization_. Inheritance according to the MRO rule is carried out approximately in the following order.

1. Enumeration of all classes inherited by the instance, according to the DFLR search rule for classical classes, and the class is included in the search result as many times as it occurs during the traversal.
2. View in the resulting list of duplicate classes, from which all are removed, except for the last (rightmost) duplicate in the list.

MRO ordering is used in inheritance and invocation of the super() built-in function, which always calls the next MRO class (relative to the call point).

**Example of inheritance in non-diamond hierarchical trees:**

```python
class D: attr = 3 # D:3 E:2
class B(D) pass # | |
class E: attr = 2 # B C:1
class C(E): attr = 1 # / /
class A(B, C): pass # A
X = A() # |
print(X.attr) # X

#DFLR = [X, A, B, D, C, E]
# MRO = [X, A, B, D, C, E, object]
# Both in version 3.x and in version 2.x (always) prints the string "3"
```

**An example of inheritance in diamond-shaped hierarchical trees:**

```python
class D: attr = 3 # D:3 D:3
class B(D) pass # | |
class C(D): attr = 1 # B C:1
class A(B, C): pass # / /
X = A() # A
print(X.attr) # |
                                 # X

#DFLR = [X, A, B, D, C, D]
# MRO = [X, A, B, C, D, object] (keeps only the last duplicate of D)
# Output string "1" in version 3.x, string "3" in version 2.x ("1" if D(object))
```

### What is Diamond problem

With diamond inheritance, determine which class method should be called

### What are mixins

Mixin (mix-in, English “mixture”), a design pattern in OOP, when a small helper class is added to the inheritance chain. For example, there is a class

```python
class NowMixin(object):
     def now():
         return datetime.datetime.utcnow()
```

Then any class inherited with this mixin will have a `now()` method.

It is customary to add the word `Mixin` to mixin names, since there is no mechanism for understanding whether this is a full-fledged class or mixin. A mixin is technically the most common class.

### What is a context manager. How to write your

Python has the `with` operator. The code placed inside is executed with a peculiarity: before and after, the events of entering and exiting the `with` block are guaranteed to fire. The object that defines this logic is called the context manager.

Block entry and exit events are defined by the `__enter__` and `__exit__` methods. The first is triggered at the moment when the program execution flow goes inside `with`. The method can return a value. It will be available to the underlying code inside the `with` block.

`__exit__` fires at the moment of exit from the block, incl. and because of the exception. In this case, the triple of values `(exc_class, exc_instance, traceback)` will be passed to the method.

The most common context manager is the class generated by the `open` function. It guarantees that the file will be closed even if an error occurs inside the block.

You should try to exit the context manager as quickly as possible to free the context and resources.

```python
with open('file.txt') as f:
     data = f.read()
process_data(data)
```

An example of implementing your context manager based on a class:

```python
class Printable:
     def __enter__(self):
         print('enter')

     def __exit__(self, type, value, traceback):
         print('exit')
```

An example of implementing your own context manager using the built-in contextlib library:

```python
from contextlib import contextmanager

@contextmanager
def printable():
     print('enter')
     try:
       yield
     finally:
       print('exit')
```

Context managers can also be used to temporarily replace parameters, environment variables, database transactions.

### Comment out the expression

`object() == object()`

Always false, because by default objects are compared by their id (memory address) field, unless the `__eq__` method is overridden.

### What is \_\_slots\_\_. Pros, cons

Classes store fields and their values in a secret `__dict__` dictionary. Since the dictionary is a mutable structure, you can add and remove fields from the class on the fly. The `__slots__` parameter on the class hard-codes the set of class fields. Slots are used when a class can have a lot of fields, such as in some `ORM`s, or when performance is critical because slot access is faster than dictionary lookups, or when millions of class instances are created during program execution, using ` __slots__` will save memory.

Slots are actively used in the `requests` and `falcon` libraries.

Drawback: You can't assign a field to a class that isn't in the slots. The `__getattr__` and `__setattr__` methods do not work.
Solution: include `__dict_ element in `**slots**`

### What is the meaning of \_value, \_\_value parameters

A class field with a single leading underscore indicates that the parameter is only used within the class. At the same time, it is available for external access. This access restriction is at the agreement level only.

```python
class Foo(object):
     def __init__(self):
         self._bar = 42

Foo()._bar
>>> 42
```

Modern IDEs like `PyCharm` will highlight field access with an underscore, but there will be no runtime error.

Double underscore fields are available inside the class, but are not available from outside. This is achieved by a tricky trick: the interpreter assigns names like `_<ClassName>__<fieldName>` to such fields. The described mechanism is called _name mangling_ or _name decoration_

```python
class Foo(object):
     def __init__(self):
         self.__bar = 42

Foo().__bar
>>> AttributeError: 'Foo' object has no attribute '__bar'
Foo()._Foo__bar
>>> 42
```

### What is \_\_new\_\_. And how is it different from \_\_init\_\_. In what order are they executed?

The main difference between the two methods is that `__new__` handles object creation, while `__init__` handles object initialization.

`__new__` is called automatically when the class name is called (when an instance is created), while `__init__` is called every time a class instance returns `__new__`, passing the returned instance to `__init__` as the `self` parameter, so even if you saved an instance somewhere globally/statically and returned it every time from `__new__`, it will still call `__init__` every time.

It follows from the above that `__new__` is called first, and then `__init__`

### What is and how old-style differs from new-style classes

The new-style classes (3.x are the only ones available, in 2.x when inheriting from `object`) differ from the classic ones (the default in 2.x) in the following ways:

- The reason for the creation of new style classes was the idea to remove the difference between built-in types and user-defined types. [Unifying types and classes in Python 2.2](https://www.python.org/download/releases/2.2.3/descrintro/)
- Diamond patterns of multiple inheritance have a slightly different search order. They are searched in breadth rather than depth before starting from bottom to top (see question about MRO)
- Classes now stand for types, and types are classes. Thus, calling the built-in function `type(I)` returns the class from which the instance is obtained, not the type of the instance, which is usually equivalent to the expression `I.__class__`. The class `type` can be subclassed to create special classes. All classes inherit from the built-in `object` class, which provides a small set of methods by default

### What is duck typing

Implicit typing, latent typing or _duck typing_ (eng. Duck typing) is a type of dynamic typing used in some programming languages (Perl, Smalltalk, Python, Objective-C, Ruby, JavaScript, Groovy, ColdFusion, Boo, Lua, Go , C#), when the scope of an object's use is determined by its current set of methods and properties, as opposed to inheriting from a particular class.
That is, an object is considered to implement an interface if it contains all the methods of this interface, regardless of the relationships in the inheritance hierarchy and belonging to any particular class.

Duck typing solves hierarchical typing problems such as:

- the inability to explicitly indicate (by inheritance) the compatibility of an interface with all present and future interfaces with which it is ideologically compatible;
- an exponential increase in the number of relationships in the type hierarchy with at least a partial attempt to do this.

## Modules, packages

### What is a module

A module is a functionally complete fragment of a program, designed as a separate file with source code or a named continuous part of it. Modules allow complex tasks to be broken down into smaller ones in accordance with the principle of modularity.
A file that contains Python source code is a module.
Modules can be combined into packages and, further, into libraries.

### How can I get the module name

The name of the module is available in its global variable `__name__`. If the module is not imported but is run as a script, then `__name__` is set to `"__main__"`.

### What is modular programming

Modular programming is the organization of a program as a collection of small independent blocks called modules, the structure and behavior of which are subject to certain rules. The use of modular programming makes it easier to test the program and find errors. Hardware-dependent subtasks can be strictly separated from other subtasks, which improves the portability of the created programs.

### How Python looks for modules on import

When importing modules, the Python interpreter looks for them in directories and archives, the list of which is available both for reading and for modification in the form of the path variable of the built-in module sys.
By default, sys.path consists of the directory with the script being run, the contents of the PYTHONPATH environment variable, and the standard location of modules specific to a particular platform and interpreter.

### What is a package

Modules can be combined into packages. Packages serve as namespaces for modules and a way to structure them.
Every package is a module, but not every module is a package.
As a rule, modules are represented as files, and packages are represented as directories in the file system (but not always).
For a directory to be a package, it must contain an `__init__.py` file. It is automatically executed when the corresponding module is imported and may contain certain actions for initialization or be empty.

### What can you say about the import package.item construct

When using the from package import item statement, item can be a package, a module, or any name declared in the package. When using the import package.item statement, item must be a module or a package.

## Exceptions

### What is exception handling

Handling _exceptional situations_ or handling _exceptions_ (eng. exception handling) - a programming language mechanism designed to describe the reaction of a program to run-time errors and other possible problems (exceptions) that may arise during program execution and lead to impossibility (meaninglessness) ) further development by the program of its basic algorithm.

Python code can throw an exception using the raise keyword. After it, the object of the exception is indicated. You can also specify the class of the exception, in which case the constructor without parameters will be automatically called. raise can only throw instances of the BaseException class and its descendants, and (in Python 2) instances of old-type classes as exceptions.

### Why they can use the try finally construct without except

```python
try:
     # some code
finally:
     # some code
```

If an error occurs in the try block, then the finally block will still be executed and you can do a "cleanup" inside it, for example.

It should be noted:
The `finally` block in a `try/except/finally` construct in Python always fires, except when the Python interpreter stops or a fatal error occurs, such as a syntax violation or low-level I/O errors.

Also, the `finally` block can be skipped if an unhandled exception of type `SystemExit`, `KeyboardInterrupt`, or `GeneratorExit` occurs, which can be thrown when the user stops the program or for other reasons that require the program to terminate immediately.

Otherwise, the `finally` block will be executed regardless of whether an exception was thrown or not.

### How to properly handle exceptions differently

Except blocks are processed from top to bottom and control is transferred to no more than one handler. Therefore, if you need to handle exceptions that are in the inheritance hierarchy differently, you must first specify handlers for less common exceptions, and then for more common ones.
This is also why _bare except_ can only be the last one (aka SyntaxError). Moreover, if you first place handlers for more general exceptions, then less general exception handlers will simply be ignored.

### What happens if the error is not handled by the except block

If none of the given except blocks catches the thrown exception, then it will be caught by the nearest outer try/except block that has a corresponding handler. If the program does not catch the exception at all, then the interpreter terminates the program and prints information about the exception to the standard error stream sys.stderr.
There are two exceptions to this rule:

- If an exception occurs in an object's destructor, program execution is not terminated and an "Exception ignored" warning is printed to the standard error stream with information about the exception.
- When an exception SystemExit occurs, only the program is terminated without displaying information about the exception on the screen (does not apply to the previous paragraph, in the destructor the behavior of this exception will be the same as the others).

### What to do if you need to catch an exception, perform actions and raise the same exception again

In order to perform certain actions in the exception handler, and then pass the exception further, one level of handlers higher (that is, throw the same exception again), the raise keyword is used without parameters.

```python
try:
     10
except ZeroDivisionError:
   # some logic
   raise
```

### What is exception chaining

In Python 3, when an exception is raised in an except block, the old exception is stored in the `__context__` data attribute, and if the new exception is not handled, it will print out that the new exception was thrown while handling the old one ("During handling of the above exception, another exception occurred:").
Also, you can chain exceptions into one chain or replace old ones with new ones. To do this, use the construct `raise new_exception from old_exception` or `raise new_exception from None`.
In the first case, the specified exception is stored in the `__cause__` attribute and the `__suppress_context__` attribute (which suppresses the exception being thrown from `__context__`) is set to True. Then, if the new exception is not handled, information will be displayed that the old exception is the cause of the new one ("The above exception was the direct cause of the following exception:").
In the second case, `__suppress_context__` is set to True and `__cause__` to None. Then, when an exception is thrown, it will actually be replaced by a new one (although the old exception is still stored in `__context__`).

There is no exception chaining in Python 2. Any exception thrown in the except block replaces the old one.

### Why the else block is needed

The else block is executed if no exceptions were thrown during the execution of the try block. It is intended to separate code that might throw an exception that should be handled in a given try/except block from code that might throw an exception of the same class that should be caught at a higher level, and to minimize the number of statements in the try block.

### What can be passed to the exception constructor

Exceptions can take any unnamed arguments as a constructor parameter. They are placed in the args data attribute as a tuple (an immutable list). The most common use is a single string parameter that contains the error message. All exceptions define a `__str__` method that calls str(self.args) by default.
Python 2 also has a message attribute that puts `args[0]` if `len(args) == 1`

### What are the exception classes

- Basic:
  - BaseException is the base class for all exceptions.
  - Exception is a subclass of BaseException, the base class for all standard exceptions that do not indicate mandatory program termination, and all user-defined exceptions.
  - StandardError (Python 2) - Base class for all built-in exceptions except StopIteration, GeneratorExit, KeyboardInterrupt and SystemExit.
  - ArithmeticError is the base class for all exceptions related to arithmetic operations.
  - BufferError is the base class for exceptions related to buffer operations.
  - LookupError is the base class for exceptions related to an invalid collection key or index.
  - EnvironmentError (Python 2) - base class for exceptions related to errors that occur outside the Python interpreter. In Python 3, its role is played by OSError.
- Some of the specific standard exceptions:
  - AssertionError - failure of the condition in the assert statement.
  - AttributeError – attribute access error.
  - FloatingPointError – operation error on floating point numbers.
  - ImportError - error importing a module or a name from a module.
  - IndexError - invalid index of a sequence (for example, a list).
  - KeyboardInterrupt - termination of the program by pressing Ctrl + C in the console.
  - MemoryError - lack of memory.
  - NameError - name not found.
  - NotImplementedError – action not implemented. Intended, among other things, to create abstract methods.
  - OSError – system error.
  - OverflowError - the result of an arithmetic operation is too large to be represented.
  - RuntimeError is a generic runtime error that does not fit into any of the categories.
  - SyntaxError - syntax error.
  - IndentationError - a subclass of SyntaxError - invalid indentation.
  - TabError - subclass of IndentationError - mixed use of tabs and spaces.
  - SystemError - non-critical internal error of the interpreter. If this exception occurs, please file a bug report at [bugs.python.org](https://bugs.python.org/)
  - SystemExit – an exception that is generated by the sys.exit() function. Serves to terminate the program.
  - TypeError – data type mismatch error.
  - UnboundLocalError - subclass of NameError - access to a non-existent local variable.
  - ValueError - thrown when an object of the correct type is passed to a function or operation, but with an invalid value, and this situation cannot be described with a more precise exception, such as IndexError.
  - ZeroDivisionError - division by zero.

### In what cases can SyntaxError be handled

A syntax error occurs when the Python parser encounters a piece of code that does not conform to the language specification and cannot be interpreted.
Because, in the event of a syntax error in the main module, it occurs before program execution begins and cannot be caught, the primer in the Python documentation even separates syntax errors and exceptions. However, SyntaxError is also an exception that inherits from Exception, and there are situations where it can occur at runtime and be handled, namely:

- syntax error in the imported module;
- a syntax error in code that is represented as a string and passed to the eval or exec function.

### Is it possible to create custom exceptions

Can. They must be descendants of the Exception class. It is customary to name exceptions so that their class name ends with the word Error.

### What warnings are for and how to create your own

Warnings are usually displayed in situations where erroneous behavior is not guaranteed and the program can normally continue to run, but the user should be notified of something.
The base class for warnings is Warning, which inherits from Exception.
The Warning base class for user-defined warnings is UserWarning.

### What is the warning module for?

The warning module contains functions for working with warnings.
The main function is warn, which takes one mandatory message parameter, which can be either a message string or an instance of the Warning class or subclass (in which case the category parameter is set automatically) and two optional parameters: category (default is UserWarning) - the warning class and stacklevel (default - 1) - nesting level of functions, starting from which it is necessary to display the contents of the call stack (useful, for example, for wrapper functions for displaying warnings, where stacklevel=2 should be set so that the warning refers to the place where this function was called, not the function itself).

## Decorators

- [Understanding decorators in Python, step by step. Step 1(rus)](https://habr.com/en/post/141411/)
- [Understanding decorators in Python, step by step. Step 2(rus)](https://habr.com/en/post/141501/)

### What are decorators. Why do we need

A decorator in a broad sense is a design pattern when one object changes the behavior of another. In Python, a decorator is usually a function A that takes a function B and returns a function C. In this case, the C function uses the B function in itself.

To decorate a function means to replace it with the result of the decorator.

### What can be a decorator. What decorator can be applied to

A decorator can be any callable object: a function, a lambda, a class, an instance of a class. In the latter case, define a `__call__` method.

You can apply a decorator to any object. Most often to functions, methods and classes. Decorating is so common that a special `@` operator is dedicated to it.

```python
def auth_only(view):
     ...

@auth_only
def dashboard(request):
     ...
```

If the decor operator didn't exist, we would write the code above like this:

```python
def auth_only(view):
     ...

def dashboard(request):
     ...

dashboard = auth_only(dashboard)
```

### What is the difference between \@foobar and \@foobar()

The first is the usual decoration with the foobar function.

The second case is decorating with the function that foobar will return. In another way, this is called a parametric decorator or decorator factory. See next question.

### What is a decorator factory

This is a function that returns a decorator. For example, you need a decorator to check permissions. The validation logic is the same, but there can be many rights. In order not to produce copy-paste, we will write a factory of decorators.

```python
from functools import wraps

def has_perm(perm):
     def decorator(view):
         @wraps(view)
         def wrapper(request):
             if perm in request.user.permissions:
                 return view(request)
             else:
                 return HTTPRedirect('/login')
         return wrapper
     return decorator

@has_perm('view_user')
def users(request):
     ...
```

### Why do we need wraps

`wraps` - Python standard decorator, `functools` module. It assigns the same `__name__`, `__module__`, `__doc__` fields to the wrapper function as the original function you are decorating. This is necessary so that after decorating the wrapper function in stack traces looks like a decorated function.

## Metaclasses

- [Metaclasses in Python: what it is and what it is eaten with(rus)](https://proglib.io/p/metaclasses-in-python/)
- [Metaclasses in Python(rus)](https://habr.com/en/post/145835/)

### What are metaclasses

A metaclass is a "thing" that creates classes.

We create a class in order to create objects, right? And classes are objects. A metaclass is what creates these very objects.

### What is type. How metaclass lookup works when creating an object

`type` is a metaclass that Python uses internally to create all classes.

When you write:

```python
class Foo(Bar):
   pass
```

Python does the following:

- Does class Foo have a `__metaclass__` attribute?
- If so, creates a class object in memory named Foo using what is specified in `__metaclass__`.
- If Python doesn't find `__metaclass__`, it looks for `__metaclass__` in the parent class Bar and tries to do the same.
- If `__metaclass__` is not in any parent, Python will look for `__metaclass__` at the module level.
- And if it can't find any `__metaclass__` at all, it uses `type` to create a class object.

### How metaclasses work

- intercept class creation
- change class
- return modified

### Why use metaclasses at all

The main use of metaclasses is to create APIs. A typical example is Django ORM.

It allows you to write something like this:

```python
classPerson(models.Model):
   name = models.CharField(max_length=30)
   age = models.IntegerField()
```

However, if you run the following code:

```python
guy = Person(name='bob', age='35')
print guy.age

```

you will get not `IntegerField`, but `int`, and the value can be obtained directly from the database.

This is possible because `models.Model` defines `__metaclass__` which will do some magic and turn the `Person` class we just defined with a simple expression into a complex database binding.

Django makes something complicated look simple by exposing a simple API and using metaclasses that recreate the code from the API and do all the work behind the scenes.

## Input Output

### What is a file object

A file object is an object that provides a file-oriented API (methods `read()`, `write()`, etc.) for accessing a resource. Depending on how it was created, a file object can provide access to a real file on disk or another kind of storage or data transfer device (standard input/output streams, memory buffers, sockets, etc.).

More:

In Python, a file object represents a file on disk or another source of data, such as a network connection or memory, that can be accessed as a sequence or stream of bytes.

Python uses the built-in open() function to create a file object. This function opens a disk file or other data source and returns the associated file object. The file object provides methods for reading, writing, and manipulating the position in the file.

A file object can be opened in different modes: for reading, writing, or appending data. It can also be binary or text, depending on the type of data that is stored in the file.

Usage example:

```python
# Open file for reading
file = open("example.txt", "r")

# Read the contents of a file
content = file.read()

# Closing the file
file.close()
```

This creates a file object that opens example.txt for reading. The read() method is used to read the contents of the file, and then the file is closed using the close() method.

### What are the types of file objects

At the level of data types in Python 2, there is no difference between text and binary files. When opening, you can specify text or binary mode, but this is a random match only with the output of lines when executed under Windows, and under Unix systems, where line prediction is not required, it is not calculated for anything.

In Python 3, there are several types of file objects, depending on the source of the data:

- Text file objects: These represent files that contain human-readable text. They can be opened for reading, writing, or appending using the open() function with the appropriate mode ("r", "w", or "a"). Text file objects support methods like read(), readline(), write(), and writelines().

- Binary file objects: These represent files that contain non-textual data, such as images, audio, or video. They can be opened in binary mode ("rb", "wb", or "ab") using the open() function. Binary file objects support methods like read(), readline(), write(), and writelines(), but the data they read or write is represented as bytes rather than characters.

- Buffered file objects: These are file objects that have an internal buffer, which allows them to read or write data more efficiently. They can be created using the io module's BufferedReader and BufferedWriter classes, which wrap around a file object and provide buffering functionality.

- Raw file objects: These represent low-level file objects that provide access to the underlying operating system's file system. They can be created using the os module's open() function with the os.O_RDONLY, os.O_WRONLY, or os.O_RDWR flags. Raw file objects support methods like read(), write(), and seek(), but they do not perform any buffering or text encoding/decoding.

Different kinds of streams are represented by the corresponding classes of the io module.

The io module has been backported to the latest versions of Python 2, so Python 2 can also use an I/O system similar to Python 3 if desired.

### What is the difference between text and binary files

The main difference between text and binary files in Python is the way the data is stored and processed.

Text files are stored as a sequence of characters encoded in a specific format (such as ASCII or UTF-8). When a text file is read, the data is automatically decoded into Unicode strings, which can be processed and manipulated using Python's string methods.

Binary files, on the other hand, can contain any type of data, including non-textual data like images, audio, or video. When a binary file is read, the data is returned as a sequence of bytes, which can be processed using Python's bytes and bytearray types.

Another difference is the way that the data is written to the file. Text files are written one character at a time, while binary files are written one byte at a time. This means that binary files are generally more efficient for storing large amounts of non-textual data, while text files are better suited for storing human-readable text.

It's also important to note that different platforms may use different newline characters in text files (for example, Windows uses "\r\n" while Unix/Linux uses "\n"). Python's built-in file objects automatically handle these platform-specific differences when reading and writing text files.

### How to use the open function

Function signature in Python 2: `open(file, mode='r', buffering=-1)`.

Function signature in Python 3 (and in Python 2 when using the io.open function):
`open(file, mode='r', buffering=-1, encoding=None, errors=None, newline=None, closefd=True, opener=None)`.

Main parameters:

- file – file name or file descriptor;
- mode – file opening mode;
- encoding - file encoding;
- buffering - whether to use buffering: a negative number (by default, you do not need to specify explicitly) - the standard value for this type of file object, 0 - disable buffering, 1 - line buffering (for text files), another value - enable buffering and set the appropriate buffer size.

Only the first one is required. Most often, the `open()` function is used with two parameters.

mode can start with characters "r" (read), "w" (write, clear file if already exists), "x" (exceptional creation, fail if file already exists), "a" (append, write to end file).
Also, the mode parameter can have a second letter to define the file type: "t" for text (default) and "b" for binary.
You can also add a "+" symbol to open in read and write mode at the same time. The order of the last two characters does not matter: "rb+" and "r+b" specify the same mode.

### Why you need to close files

When finished working with a file, be sure to close it using the `close()` method, especially if it was opened for writing. When using buffered output, the data that is written to the file does not go to it immediately, but is written to the buffer.
The contents of the buffer are written to the file when it is full or when the `flush()` or `close()` methods are called. Also, if a file is open for writing, it will be blocked from being opened for writing by other processes until it is closed. All open files are automatically closed when the corresponding file objects are removed from memory by the Python interpreter's garbage collector and when the interpreter itself exits, but files should be kept open for the minimum amount of time required.

### What methods do tell and seek

The `tell()` method returns the current read/write probability of the file. Method `search(offset, from)` to create it. The offset parameter specifies the indent, and from where is the point from which this indent counts: `io.SEEK_SET(0)` is the beginning of the file, `io.SEEK_CUR(1)` is the current position, `io.SEEK_END(2)` is the end file.

More:

In Python, the tell() and seek() methods are used to read and manipulate the current position of a file object's cursor.

The tell() method returns the current position of the cursor in the file, as an integer representing the number of bytes from the beginning of the file. This method can be useful for keeping track of your position within a file while reading or writing data.

The seek() method is used to move the cursor to a specific position within the file. It takes two arguments: the first is the offset from the reference point (which can be the beginning of the file, the current position of the cursor, or the end of the file), and the second is an optional parameter that specifies the reference point. The offset argument can be a positive or negative integer, and the whence argument can be one of the following constants defined in the io module:

0 (default): the offset is relative to the beginning of the file
1: the offset is relative to the current position of the cursor
2: the offset is relative to the end of the file
For example, to move the cursor to the beginning of a file, you could use file.seek(0). To move the cursor to the end of a file, you could use file.seek(0, 2).

Together, the tell() and seek() methods allow you to read and manipulate the contents of a file in a flexible and efficient manner.

### What StringIO and BytesIO do

The `io.StringIO` and `io.BytesIO` classes are streams for reading from and writing to strings or byte strings in memory. They can be used to use strings and byte strings as text and binary files.

More:

`StringIO` and `BytesIO` are both classes in the Python io module that provide in-memory file-like objects that can be used for reading and writing data as if it were a file on disk.

`StringIO` is used for working with string data. It creates a file-like object that behaves like a regular text file, allowing you to write strings to it, read strings from it, and move the cursor around using the `tell()` and `seek()` methods.

For example, the following code creates a `StringIO` object, writes a string to it, moves the cursor to the beginning of the file, and then reads the contents of the file:

```python
from io import StringIO

buffer = StringIO()
buffer.write("Hello, world!")
buffer.seek(0)
print(buffer.read())  # prints "Hello, world!"
```

`BytesIO`, on the other hand, is used for working with binary data. It creates a file-like object that behaves like a regular binary file, allowing you to write bytes to it, read bytes from it, and move the cursor around using the `tell()` and `seek()` methods.

For example, the following code creates a `BytesIO` object, writes some binary data to it, moves the cursor to the beginning of the file, and then reads the contents of the file:

```python
from io import BytesIO

buffer = BytesIO()
buffer.write(b"\x48\x65\x6c\x6c\x6f\x2c\x20\x77\x6f\x72\x6c\x64\x21")
buffer.seek(0)
print(buffer.read())  # prints b'Hello, world!'
```

Both `StringIO` and `BytesIO` are useful when you need to work with data in memory instead of on disk. They can be particularly useful in situations where you want to avoid the overhead of creating temporary files, or where you need to manipulate data as if it were a file but you don't want to write the changes to disk.

### Whether file objects are context managers

Yes, file objects in Python are context managers. This means that they support the context manager protocol, which allows you to automatically control the opening and closing of files in the `with` block. For example, to read the contents of a file, you can use the following code:

```python
with open('file.txt', 'r') as f:
    contents = f.read()
    print(contents)
```

In this example, the file object f is automatically closed when the `with` block exits.

### What is serialization

Serialization is the process of converting an object into a sequence of bytes or other data structure that can be stored in a file or transmitted over a network. Serialization allows you to save and restore the state of objects in a program, which can be useful in many cases, for example, for saving data to a database, transferring data over a network, or saving intermediate results of program execution.

In Python, you can use the pickle module to serialize objects. It allows you to convert Python objects to and from a byte sequence. In addition, there are many other serialization modules and formats in Python, such as JSON, XML, YAML, Protocol Buffers, and more.
Synonymous terms for marshaling/unmarshaling.

### json.dumps / json.dump , json.loads / json.load

The dumps function of the json module saves the JSON representation of an object to a string. The dump function is to a text file.
The loads function of the json module loads an object from a string. The load function is from a text file.

### What to do if you need to serialize data that is not supported by the standard json module

You can use pickle or extend the JSONEncoder and JSONDecoder classes.

### pickle.dumps / pickle.dump, pickle.loads / pickle.load

The dump, dumps, load, and loads functions of the pickle module are similar in purpose to the corresponding functions of the JSON module, but operate on byte strings and binary files.

The optional protocol parameter of these functions specifies the protocol version. The latest protocol version can be obtained as the pickle.HIGHEST_PROTOCOL constant, the current default version is pickle.DEFAULT_PROTOCOL.

At the time of this writing, there are five versions of the protocol:

- 0 and 1 are obsolete versions used in Python 2.2 and below;
- 2 is the major version of the protocol for Python 2;
- 3 - version of the protocol that appeared in Python 3, the standard protocol in Python 3 at the moment, cannot be deserialized in Python 2;
- 4 - version of the protocol, introduced in Python 3.4, supports very large memory objects, supports more types of objects, some optimizations have been added.
- 5 is the protocol version introduced in Python 3.8. It adds out-of-band data support and in-band data acceleration. PEP 574 describes the changes in more detail.

## Testing

### Testing Pyramid

```
More Integration                      Faster
    ˆ                                   ˆ
    |                /\                 |
    |               /  \                |
    |              /    \               |
    |             /      \              |
    |            /E2 Tests\             |
    |           /          \            |
    |          /(UI Testing)\           |
    |         /==============\          |
    |        /                \         |
    |       /   Integration    \        |
    |      /       Tests        \       |
    |     /======================\      |
    |    /                        \     |
    |   /        Unit Tests        \    |
    |   =============================   |
  More                               Slower
Isolation
```

### What is mocking

- [Mock module: Dummy mockups in testing(rus)](https://habr.com/ru/post/141209/)

Mock in English means "imitation", "fake". The principle of its operation is simple: if you need to test a function, then everything that does not belong to it (for example, reading from a disk or from a network) can be replaced with dummy layouts. At the same time, the tested functions do not need to be adapted for tests: Mock replaces objects in other modules, even if the code does not accept them as parameters. That is, you can test without adapting to tests at all.

### What to do if the function under test uses a remote connection to external services, which sometimes sees a timeout error, 404 and the like

If we are talking about unit tests, then they should not call external resources, that is, make http requests and so on. Therefore, either lock the http client that uses the function to call the service, or, which is usually the best solution, pass what calls that service to the function as a dependency (unless, of course, we are testing the client itself to call the service).

### What to do if the function under test takes a long time to perform repetitive operations inside it

For example, inside a loop from 1 to 1000000, where something is read, written, calculated.

Suppose this function has no problems with decomposition - this is a function that performs one action and breaking it into several others does not make any sense. In that case I would:

- would make it possible to replace the upper bound of the loop from the test (via a parameter or a mock constant, setting, etc.)
- if the function calls for calculations another resource-intensive function, third-party or from its codebase, then it would probably be locked up and checked that it is called with the necessary parameters
- if possible, would prepare for the test such an incoming data set, in which it was performed quickly

If the function does not meet the conditions described in the first sentence, you should first deal with its decomposition.

### What types of tests do you know

- [Pyramid of tests in practice(rus)](https://habr.com/en/post/358950/)
- [Tests that a developer should write(rus)](https://medium.com/front-end-in-regions-grodno/%D1%82%D0%B5%D1%81%D1%82%D1%8B-%D0%BA%D0%BE%D1%82%D0%BE%D1%80%D1%8B%D0%B5-%D0%B4%D0%BE%D0%BB%D0%B6%D0%B5%D0%BD-%D0%BF%D0%B8%D1%81%D0%B0%D1%82%D1%8C-%D1%80%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D1%87%D0%B8%D0%BA-a04cab35f45b)
- [Different types of testing and their features(rus)](https://techrocks.ru/2018/12/08/different-types-of-testing/)

More:

There are several types of testing in Python, the most common of which are:

- Unit Testing - testing each individual "unit" of code (function, method, class) in isolation from the rest of the code. For unit testing in Python, the unittest standard library is used.

- Integration Testing - testing the interaction between different components of the system, for example, between several modules or between a client and a server. For integration testing, you can use the pytest or unittest library.

- Functional Testing - testing the functionality of the system as a whole. For functional testing, you can use the Selenium library, which allows you to automate testing of web applications.

- Load Testing - testing the system at maximum load to evaluate its performance and stability. For load testing, you can use the Locust library.

- Automated Testing - testing that is performed automatically, without human intervention. Automated testing can be applied to any of the above types of testing.

- Security Testing - Testing a system for vulnerabilities and bugs that could lead to security breaches. For security testing in Python, you can use the Pytest Security library.

#### Unit tests

_What is checked?_
Unit tests check whether each individual module (unit) of your code works correctly. Ideally, when planning and writing unit tests, you want to isolate functionality that can't be broken down into smaller pieces and test it.

Unit tests should not test external dependencies or interactions. You definitely need to mock out api calls. Unit test purists will also insist on mocking database calls to make sure your code behaves correctly when given valid input from external sources. Unit tests need to be fast, otherwise they slow down development significantly.

_When will they be launched?_
You must write and run unit tests in parallel with your code.

#### Integration tests

This term is used more often for tests that directly cover the public API of the service. The focus is on checking the interaction of different systems according to the “service-client” principle.

_What is checked?_
Integration tests check the interaction between two (or more than two) separate units of your code.

Your application is made up of individual modules that perform certain small functions. Each of them can work well in isolation, but break down in conjunction with others.

Integration tests also verify that your code integrates with external dependencies, such as database connections or third-party APIs.

_When will they be launched?_
Integration tests are the next step after unit tests.

_What if the tests fail?_
Failing integration tests means that two (or more) features of your application don't work together. It could be two modules you wrote that clash because of some complex business logic. Also, the failure can happen due to the fact that the structure of the response of the third-party API has changed. Failing tests can be a warning about poor error handling in case of a database connection failure.

#### Functional testing

- Functional testing can be defined as testing individual functions of modules.
- It refers to testing a software product on an individual level to verify its functionality.
- It is very different from unit or integration testing; you can't write countless test cases for functional testing because it's more complex than unit testing.
- Functional testing tools seek to test the functionality (operability) of software. Test cases are used to test the expected and unexpected results of software testing.
- This type of testing is done more from the user's point of view. That is, it considers the user's expectation of the selected input type.
- Selenium is one of the most common tools used for functional testing.

#### System test, Service test

Automated tests that verify the operation of the entire integrated system. In fact, they represent an extreme case of integration tests. System tests do not directly test business rules. Instead, they check that the components of the system are correctly connected to each other, and the interaction between them goes according to the original plan. Performance and throughput tests usually fall into this category.

System testing is testing the program as a whole. For small projects, this is usually manual testing - launched, clicked, made sure that (does not) work. Can be automated. There are two approaches to automation.

These tests are written by system architects and leading experts from the technical side. Typically, they are written in the same language and in the same environment as UI integration tests. System tests are run relatively infrequently (depending on how long they run), but the more often, the better.

System tests cover 10% of the system. This is because they are designed to check the correctness of not the behavior of the system, but its design. The correct behavior of the underlying code and components has already been verified at the lower levels of the pyramid.

#### Health check (Smoke test, Sanity check)

This is a special case of an integration test. Usually these are very small tests that are run before the system is launched to make sure that third-party software is working, which is necessary for the correct functioning of our system. If such tests fail, we can notify the user about the problem or even stop the system from starting.

Smoke testing - came from the field of equipment testing, if, after applying power, smoke and a burning smell appear, then the equipment is faulty.

Also, smoke tests can accompany legacy code refactoring, because writing full-fledged unit tests can be very time-consuming.

### Security testing

Security testing in Python is an essential part of the software development process to ensure that the application is secure from vulnerabilities and attacks. Here are some common techniques and tools used for security testing in Python:

1. Static code analysis: This technique involves analyzing the source code of an application for potential vulnerabilities before it is compiled or executed. There are many Python tools available for this, such as Bandit, Pylint, and PyCodeStyle.

2. Dynamic code analysis: This technique involves analyzing the running code of an application to identify security flaws. This can be done by using Python testing frameworks, such as PyTest and Unittest, and security-specific tools, such as OWASP ZAP, Nmap, and Nessus.

#### Regression testing

It can be any kind of test described above, which is written after a problem has been discovered. The test must emulate exactly the steps to reproduce the problem. The presence of such a test after fixing the problem guarantees that exactly the same bug will not appear in the system again.

_What is checked?_
Regression tests test a set of scenarios that used to work and should be relatively stable.

3. Penetration testing: This technique involves simulating attacks on the application to identify and exploit vulnerabilities. There are many Python-based penetration testing tools, such as Metasploit, The Social-Engineer Toolkit (SET), and Recon-ng.

4. Fuzz testing: This technique involves generating random inputs to an application to identify vulnerabilities caused by unexpected input. Python tools, such as AFL and Radamsa, can be used for fuzz testing.

5. Secure coding practices: Finally, it's important to adopt secure coding practices when writing Python code, such as input validation, secure storage of sensitive data, and secure authentication and authorization mechanisms.

Overall, security testing is an important aspect of the software development process, and Python provides a range of tools and techniques to help ensure the security of your applications.

### How integration testing differs from functional testing

- [Comparison of integration and functional testing(rus)](http://juice-health.ru/program/software-testing/497-integration-and-functional-testing)

Integration and functional testing are two phases in the software testing process. The former is done after unit testing and the latter is a black box testing method.

_Functional testing is also referred to as E2E testing for browser testing._

## Functional programming

### What is functional programming

- [Functional Programming with Examples(rus)](https://medium.com/@kiky.tokamuro/%D1%84%D1%83%D0%BD%D0%BA%D1%86%D0%B8%D0%BE%D0%BD%D0%B0%D0%BB%D1%8C%D0%BD%D0%BE%D0%B5-%D0%BF%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5-%D0%B2-%D0%BF%D1%80%D0%B8%D0%BC%D0%B5%D1%80%D0%B0%D1%85-be5ebe4a6053)

Functional programming is a section of discrete mathematics and a programming paradigm in which the process of calculation is interpreted as the calculation of the values of functions in the mathematical sense of the latter (as opposed to functions as subroutines in procedural programming).

Functional programming is a programming paradigm that emphasizes the use of functions to solve problems. In functional programming, functions are treated as first-class citizens, which means that they can be passed as arguments to other functions, returned as values from functions, and assigned to variables. Functional programming is often contrasted with imperative programming, which emphasizes explicit changes in state and the use of control structures like loops and conditionals.

Functional programming languages typically provide a set of higher-order functions that can be used to manipulate collections of data, such as maps, filters, and folds. These functions operate on immutable data structures, which means that the original data is not modified. Instead, new data structures are created that reflect the desired changes.

Functional programming has several advantages over imperative programming, including the ability to write more concise and expressive code, the avoidance of mutable state, which can lead to fewer bugs, and the ability to take advantage of parallelism and concurrency, which can improve performance on modern hardware. However, functional programming can also be more difficult to learn and can require a different way of thinking about programming problems.

### Features of functional programming

Features of functional programming:

- Pure functions are functions that have no side effects and are also deterministic.

- Anonymous functions / Lambda functions are functions that are declared at the place of use and do not receive a unique identifier to access them. The most common way to define anonymous functions is to use lambda expressions.

- Higher-order functions are functions that can take other functions as arguments, or return other functions as a result.

- Function composition is the application of one function to the result of another function.
  Currying is the transformation of a function with many arguments, to a set of functions from one argument.

- A closure is a combination of a function and the environment in which it was defined. That is, it is a function that is defined in the body of another function, and is created every time it is executed, and it also has references to local variables of the external function.

- Immutable data is data whose state cannot be changed after it has been created.

- Pattern matching is a method of data analysis and processing based on matching the value under study with one or another pattern, which can be a number, string, or other construct supported by the language.

- Recursion is a function call from itself, or through other functions.

### Like Python with functional programming support

Python partially supports the functional programming paradigm and allows you to write code in a functional style. In addition, it contains certain features that are specific to functional languages or first appeared in functional languages (list inclusions, lambda functions, higher-order functions, etc.).

### What is a first class object

A first-class object in programming is an object that can be passed to a function as an argument, returned from the function as a result, and assigned to a variable. In Python, all objects are first class objects, which means that functions are also first class objects and can be passed as arguments to other functions, returned from functions, and assigned to variables. This approach to programming allows you to use functions as data, which in turn allows you to create more flexible and scalable programs.

An object is called a "first class object" if it:

- can be stored in a variable or data structures;
- can be passed to a function as an argument;
- can be returned from a function as a result;
- can be created during program execution;
- internally self-identifying (independent of naming).

The term "object" is used here in a general sense, and is not limited to programming language objects.
In Python, as in functional languages, functions are first-class objects.

### What is a higher order function

A higher-order function is a function that takes one or more functions as arguments or returns a function as its result. In other words, a higher-order function treats functions as first-class citizens, allowing them to be used and manipulated in the same ways as other values. This is a fundamental concept in functional programming and enables powerful abstractions and techniques, such as function composition and currying.

The basic idea is that functions have the same status as other data objects.

### What is currying

_Curring_ is the transformation of a function of many arguments into a set of functions, each of which is a function of one argument. We can pass part of the arguments to a function and get back a function that expects the rest of the arguments. This transformation was introduced by M. Sheinfinkel and G. Frege and got its name in honor of H. Curry.

Currying is a technique in functional programming that allows you to turn a function with multiple arguments into a sequence of functions with one argument. Each subsequent function uses the previous result as the first argument.

Let's create a simple greet function that takes a greeting and a name as arguments:

```python
def greet(greeting, name):
     print(greeting + ', ' + name)

greet('Hello', 'German')
```

A small improvement will allow us to create a new function for any type of greeting and pass a name to this new function:

```python
def greet_curried(greeting):
     def greet(name):
         print(greeting + ', ' + name)
     return greet

greet_hello = greet_curried('Hello')

greet_hello('German')
greet_hello('Ivan')
```

Or directly `greet_curried`

```python
greet_curried('Hi')('Roma')

And then you can do it with any number of arguments:

def greet_deeply_curried(greeting):
     def w_separator(separator):
         def w_emphasis(emphasis):
             def w_name(name):
                 print(greeting + separator + name + emphasis)
             return w_name
         return w_emphasis
     return w_separator

greet = greet_deeply_curried("Hello")("...")(".")
greet('German')
welcome('Ivan')
```

In Python, currying can be implemented using higher order functions and closures. For example, you can define a function that takes the first argument and returns an inner function that takes the next argument, and so on. When all arguments have been passed, the original function will be called with the full set of arguments. Example:

```python
def add(x):
    def inner(y):
        return x + y
    return inner

add5 = add(5)
print(add5(3)) # Output: 8
```

In this example, the add function takes the first argument x and returns an internal inner function that takes an argument y and returns the sum of x + y. We then call add(5) to get a new add5 function that will add 5 to whatever value is passed to it. Calling add5(3) will return the result 8.

### Describe the map, reduce, filter functions of the functools module

The `functools` module in Python provides some functions that can be useful when working with functional programming.

1. `map(function, iterable)`:
   This function takes a function and a sequence as arguments and returns an iterator that applies that function to each element of the sequence.
   The `map` function applies a function to each element of a sequence. Returns a list in Python 2, an iterator object in Python 3.

Example:

```python
# Example: square each number in a list
numbers = [1, 2, 3, 4, 5]
squared_numbers = list(map(lambda x: x**2, numbers))
print(squared_numbers)
# Output: [1, 4, 9, 16, 25]
```

2. `filter(function, iterable)`:
   This function takes a function and a sequence as arguments and returns an iterator that returns only those elements of the sequence for which the function returns True.
   Returns a list in Python 2, an iterator object in Python 3.

Example:

```python
# Example: filter out odd numbers from a list
numbers = [1, 2, 3, 4, 5]
odd_numbers = list(filter(lambda x: x % 2 != 0, numbers))
print(odd_numbers)
# Output: [1, 3, 5]
```

3. `reduce(function, iterable[, initializer])`:
   This function takes a function and a sequence as arguments and returns a single value, which is the result of applying this function to a sequence. It is used to collapse a sequence into a single value. For Python 3+, the `reduce()` function has been moved from the `functools` module to the `functools.reduce()` module.
   More:
   Takes a function of two arguments, a sequence and an optional initial value, and computes a fold of the sequence as the result of applying the given function sequentially to the current value (called the accumulator) and the next element of the sequence.

Example:

```python
# Example: find the product of numbers from a list
from functools import reduce
numbers = [1, 2, 3, 4, 5]
product = reduce(lambda x, y: x*y, numbers)
print(product)
# Output: 120
```

### What other functions do you know from the functools module

In addition to the `map`, `reduce`, and `filter` functions, the `functools` module also contains a number of other higher-order functions. Below are some of them:

1. `partial(func, *args, **keywords)`: creates a new function with partially defined arguments. Returns a new function that calls the original function with the arguments passed in and the additional arguments passed when the new function was called. For example:

```python
from functools import partial

def multiply(x, y):
    return x * y

double = partial(multiply, 2)
triple = partial(multiply, 3)

print(double(4)) # 8
print(triple(4)) # 12
```

2. `wraps(wrapped, assigned=WRAPPER_ASSIGNMENTS, updated=WRAPPER_UPDATES)`: This is a decorator that is used to preserve the metadata (such as documentation and function name) of the original function after it has been decorated. This is useful when you create your own decorators that can change function metadata. For example:

```python
from functools import wraps

def my_decorator(func):
    @wraps(func)
    def wrapper(*args, **kwargs):
        print("Before the function is called.")
        result = func(*args, **kwargs)
        print("After the function is called.")
        return result
    return wrapper

@my_decorator
def say_hello(name):
    """A function that says hello."""
    print(f"Hello, {name}!")

say_hello("Alice")
print(say_hello.__name__)  # "say_hello"
print(say_hello.__doc__)   # "A function that says hello."
```

3. `lru_cache(maxsize=128, typed=False)`: This is a decorator that is used to memoize functions. Memoization is an optimization technique in which the results of executing a function are cached to avoid re-evaluation with the same arguments. `lru_cache` saves the most recently used results and removes rarely used results to conserve memory space. For example:

```python
from functools import lru_cache

@lru_cache(maxsize=128)
def fibonacci(n):
    if n <= 1:
        return n
    else:
        return fibonacci(n-1) + fibonacci(n-2)

print([fibonacci(n) for n in range(10)])  # [0, 1, 1, 2, 3, 5, 8, 13, 21, 34]
```

### What functions do you know from the itertools module

The `itertools` module is part of the Python standard library and provides a set of tools for working with iterables such as lists, tuples, sets, and more.

The `itertools` module implements various functions such as:

- `product` – Cartesian product of iterators (to avoid nested for loops);
- `permutations` - generation of permutations;
- `combinations` – generation of combinations;
- `combinations_with_replacement` - generation of placements;
- `takewhile` - getting sequence values while the value of the predicate function for its elements is true;
- `dropwhile` - getting the values of the sequence starting from the element for which the value of the predicate function will no longer be true.
- `count(start=0, step=1)` - an infinite iterator that returns numbers starting at `start` with `step`.
- `cycle(iterable)` - an infinite iterator that repeats the values from the `iterable`.
- `repeat(elem, n=None)` - An iterator that returns the value of `elem` `n` times, or an infinite number of times if `n` is not specified.
- `chain(*iterables)` - A function that chains multiple iterables into a single iterator.
- `islice(iterable, start, stop[, step])` - a function that returns a slice of the elements from an `iterable` object iterable from index `start` to index `stop` in increments of `step`.
- `groupby(iterable, key=None)` - A function that groups the elements of an `iterable` by the given `key`, which is a function applied to each element to determine the grouping.

In addition, the `itertools` module also provides functions for working with permutations, combinations, and combinations of elements from iterables.

Examples of using:

```python
import itertools

# count
for i in itertools.count(1, 2):
    print(i)
    if i > 10:
        break

# cycle
for i, c in zip(range(10), itertools.cycle('abc')):
    print(i, c)

# repeat
for i in itertools.repeat(3, 4):
    print(i)

# chain
for i in itertools.chain([1, 2, 3], [4, 5, 6]):
    print(i)

# islice
for i in itertools.islice(range(10), 1, 9, 2):
    print(i)

# groupby
data = [('A', 1), ('B', 2), ('A', 3), ('C', 4)]
groups = itertools.groupby(data, key=lambda x: x[0])
for key, group in groups:
    print(key, list(group))
```

### What is the operator module for?

The `operator` module in Python provides functions that correspond to standard language operators such as addition, multiplication, comparison, and so on. The functions in this module are typically used to perform operations on elements in a list, dictionary, or other iterable without having to explicitly call the operator.

For example, the function `operator.add(x, y)` is equivalent to the expression `x + y`. The `operator` module also provides functions for sorting a list by a given key (`operator.itemgetter()`, `operator.attrgetter()`), finding the minimum and maximum elements in a sequence (`operator.min()`, `operator.max()`), etc.

The advantage of using functions from the `operator` module is that they can be used in conjunction with higher-order functions such as `map()`, `filter()`, `reduce()`, etc., which simplifies and speeds up some operations.

## GIL, threads, processes

### What is GIL. What problems does he have

- [GlobalInterpreterLock](https://wiki.python.org/moin/GlobalInterpreterLock)
- [How the GIL works in Python(rus)](https://habr.com/ru/post/84629/)
- [How the GIL works in Python(eng)](http://www.dabeaz.com/python/GIL.pdf)

Only one Python thread can be running at any given time. The global interpreter lock - GIL - carefully controls the execution of threads. The GIL guarantees each thread exclusive access to interpreter variables (and the corresponding C extension calls work correctly).

The principle of operation is simple. Threads hold the GIL while they are executing. However, they release it when it locks for I/O operations. Each time a thread is forced to wait, other threads that are ready to run take their chance to run.

When a thread starts running, it performs a GIL capture. After some time, the process scheduler decides that the current thread has done enough work and passes control to the next thread. Thread #2 sees that the GIL is captured, so it doesn't continue, but puts itself to sleep, yielding the processor to thread #1.

But a thread cannot hold the GIL indefinitely. Prior to Python 3.3, the GIL switched every 100 machine code instructions. In later versions, the GIL can only be held by a thread for a maximum of 5ms. The GIL is also freed if the thread makes a system call, disk or network access.

The problem is that due to the GIL, not all tasks can be solved in threads. On the contrary, their use most often reduces the performance of the program (for CPU-bound tasks). Using threads, you need to monitor access to shared resources: dictionaries, files, database connections.

- The GIL makes it easy to integrate non-thread safe C libraries. Thanks to the GIL, we have so many fast modules and bindings for just about everything.
- C libraries have access to the GIL control mechanism. So for example NumPy releases it on long operations.

Essentially, the GIL in python renders useless the idea of using threads for parallelism in computational tasks. They will run consistently even on a multiprocessor system. On CPU Bound tasks, the program will not speed up, but only slow down, since now the threads will have to divide the processor time in half. At the same time, the I / O operation of the GIL will not slow down, since the thread releases the GIL before the system call.

### Have you worked with asyncio. What is its feature

Asynchronous programming in Python is a way of organizing parallel computing, in which one thread can perform several tasks at the same time without blocking. Unlike synchronous programming, where tasks are performed sequentially using blocking I/O operations, asynchronous programming allows you to efficiently use I/O wait time while executing other tasks.

The main idea behind asynchronous programming in Python is the use of the event model. In this model, code is organized into event handlers that are called when certain events occur, such as the completion of an I/O operation or the arrival of a message.

To implement asynchronous programming in Python, the asyncio mechanism, which appeared in Python 3.4, is used. It provides asynchronous versions of the standard I/O functions and allows you to organize event handlers using coroutines (`async/await`) that run within the event loop (event loop).

The main advantages of asynchronous programming in Python are:

- Efficient use of I/O wait time.
- Ability to handle a large number of connections at the same time.
- Reducing resource consumption by not creating a large number of threads.
- Reducing the overhead of thread context switching.

Flaws:

- The complexity of debugging and writing code in an asynchronous paradigm can be higher than in a synchronous one.
- Due to the asynchronous nature, some standard functions and libraries may not work correctly.

Let's imagine that we are writing an HTTP or WebSocket server that handles each connection in a separate thread.

Here, you can create 100, maybe even 500 threads to handle the required number of concurrent connections. For short requests, this will even work and allow you to handle a load of 5000 RPS on the cheapest DO instance for five bucks - not bad at all. If you have less, you may not need any AsyncIO/Tornado/Twisted here.

But what if their number tends to infinity? Say, this is a big chat with lots of channels, where the number of concurrent participants is unlimited. In this situation, I would not risk creating so many threads to satisfy each user. And here's why:

As mentioned above, while the GIL is held by one thread, the others will not work. The operating system scheduler doesn't know anything about GIL and will still give the processor to the threads that are blocked. Such a thread will, of course, see that the GIL is held and immediately fall asleep, but valuable time will be spent switching the processor context.

Context switching is generally an expensive operation for the processor, requiring the resetting of registers, cache, and memory page mapping table. The more threads are running, the more the processor performs idle switches to the threads blocked by GIL before reaching the one that holds this GIL. Not very efficient.

There are good old coroutines - what AsyncIO and Tornado now offer. They are also called coroutines or just user-level threads. A trendy thing now, but far from new, was used in the days when multitasking-unsupported OS was popular.

Unlike threads, coroutines only perform useful work, and switching between them occurs only at the moment when the coroutine is waiting for the completion of some external operation.

As with threads, async programming is useless for computations. The situation is even worse here because a thread stuck in calculations will eventually release the GIL, but blocking code in a coroutine will block the entire thread until it executes entirely. Unlike native threads, coroutines do not have a timer interrupt. Control transfer to the next coroutine occurs manually when the await (or yield, if generator-based coroutines are used) construction is explicitly called. Therefore, it is essential to ensure that there is no blocking code in async programs and only async calls are used, and all calculations occur in separate processes.

Threads will be easier if you have a typical web application that does not depend on external services and has a relatively finite number of clients for whom response time will be predictably short.

AsyncIO is suitable if the application spends most of its time reading / writing data, and not processing it. For example, you have a lot of slow requests - web sockets, long polling, or slow external synchronous backends, requests to which you don’t know when to complete.

### What is async/await, what are they for and how to use them

The `async` keyword comes before `def` to indicate that the method is asynchronous. The `await` keyword indicates that you are waiting for the coroutine to complete.

```python
import asyncio
import aiohttp

urls = ['http://www.google.com', 'http://www.yandex.ru', 'http://www.python.org']

async def call_url(url):
     print('Starting {}'.format(url))
     response = await aiohttp.get(url)
     data = await response.text()
     print('{}: {} bytes: {}'.format(url, len(data), data))
     return data

futures = [call_url(url) for url in urls]

loop = asyncio.get_event_loop()
loop.run_until_complete(asyncio.wait(futures))
```

The program consists of an async method. During execution, it returns a coroutine, which is then pending.

`async/await` is needed in order not to block the execution thread while waiting for some asynchronous event. The `async/await` construct essentially turns the procedure into a coroutine (coroutine): it stops its execution for the `await` time, waits for an asynchronous event, and resumes work.

In the non-async version, the wait turns out to be blocking, or you need to manually do tricks: start the operation and subscribe to its end. Async makes code simpler and more linear.

### How python implements multithreading. What modules

In Python, `multithreading` can be implemented using the `threading` module or the `multiprocessing` module.

The `threading` module allows you to create threads within a single process. These are native `Posix` threads. Such threads are executed by the operating system, not by the virtual machine. To create a thread, you need to define a class that inherits from the threading.Thread class and override the `run()` method, which will contain the code that will be executed in the thread. The class is then instantiated and the `start()` method is called, which starts the thread.

Sample code for creating a thread using the threading module:

```python
import threading

class MyThread(threading.Thread):
    def run(self):
        # Code running on the thread
        print("Hello from thread")

# Create a thread
thread = MyThread()

# Start a thread
thread.start()

# Wait for the thread to finish
thread.join()
```

The `multiprocessing` module allows you to create processes in Python. To create a process, you need to define a function that will be executed in the process, and create an instance of the `multiprocessing.Process` class with this function as an argument. The `start()` method is then called, which starts the process.

Sample code for creating a process using the `multiprocessing` module:

```python
import multiprocessing

def worker():
    # Code running on the process
    print("Hello from process")

# Create a process
process = multiprocessing.Process(target=worker)

# Start a process
process.start()

# Wait for the process to finish
process.join()
```

Both modules allow you to create multiple threads/processes and execute them in parallel. At the same time, it is necessary to monitor the synchronization of access to shared resources, since changing them from different threads/processes can lead to errors and unexpected results. To solve this problem, you can use mutexes, locks, and other synchronization facilities that are provided by the threading and multiprocessing modules.

### What is the difference between threading and multiprocessing

Threads and multiprocessing are two approaches to achieve concurrency in a program. While they share some similarities, they have fundamental differences in how they work and what kind of problems they are best suited to solve.

Threads are lightweight units of execution within a single process. Each thread shares the same memory space as the other threads in the same process, which allows them to share data and communicate with each other very easily. Threads are managed by the operating system's scheduler, which assigns a certain amount of CPU time to each thread, allowing them to run concurrently.

One of the key advantages of threads is that they are fast and efficient, since they do not require the overhead of creating a new process. They are also very useful for tasks that involve a lot of I/O, such as network or disk operations, since threads can be blocked while waiting for I/O to complete, allowing other threads to run in the meantime.

However, threads are not well-suited to problems that involve heavy CPU usage, since they are limited by the number of available CPU cores. This means that if a program with many threads is run on a machine with only a few cores, the threads will have to take turns using the CPU, resulting in slower overall performance.

Multiprocessing, on the other hand, is the use of multiple processes to achieve concurrency. Each process has its own memory space and runs independently of the other processes, communicating with them through various inter-process communication mechanisms (e.g. pipes, sockets, shared memory). Since each process has its own memory space, they are not subject to the same data sharing issues as threads, making it easier to write correct and safe concurrent programs.

Multiprocessing is well-suited to problems that involve heavy CPU usage, since each process can be assigned to a separate CPU core, allowing them to run truly concurrently. However, creating a new process incurs a significant overhead, both in terms of memory usage and startup time. This makes multiprocessing less efficient for tasks that involve a lot of I/O or small computations, where the overhead of creating new processes may outweigh the benefits of true concurrency.

In summary, threads are best suited for tasks that involve a lot of I/O and benefit from lightweight concurrency, while multiprocessing is best suited for tasks that involve heavy CPU usage and benefit from true concurrency.

### Which tasks are well parallelized, which ones are bad

Tasks that generate long IO are well parallelized. When a thread hits a socket or disk wait, the interpreter abandons that thread and starts the next one. This means there will be no downtime due to waiting. On the contrary, if you go to the network in one thread (in a cycle), then each time you have to wait for a response.

However, if the thread then processes the received data, then only it will be executed. This will not only not give an increase in speed, but also slow down the program due to switching to other threads.

The short answer is that networking tasks fit well with threads. For example, download a hundred urls. Process the received data outside of threads.

### You need to calculate 100 equations. Do it in threads or not

- No, because there is no I/O in this task. The interpreter will only spend extra time switching threads. It is better to move complex mathematical problems into separate processes, or use the Celery framework for distributed tasks, or connect them as C-libraries.

- Other answer:
  If these equations are independent of each other and run independently, then it makes sense to use multithreading to calculate them. In this case, each equation can be calculated in a separate thread, which will speed up the overall calculation time.
  However, if these equations have any dependencies or require shared resources (for example, access to the same file), then using multithreading can lead to errors and inefficiencies. In this case, it is better to perform calculations sequentially in the main thread.
  In addition, it is worth considering the characteristics of the computer on which the calculations are performed. If your computer has multiple processors or cores, then multithreading may be more efficient. If the processor is single-threaded, then the use of multithreading may not give a significant increase in the speed of program execution.

### Threads in Python are native threads or not

Yes, in Python, threads are native, they are implemented in the standard library of the language. Specifically, the threading module provides classes and functions for working with threads in Python.

Threads in Python are implemented using the pthread_create (POSIX Threads) system call, which creates a new thread of execution within a process. Thus, threads in Python are fully integrated into the operating system and use its task scheduling mechanisms.

However, it's worth noting that Python also provides alternative approaches to parallel code execution, such as the multiprocessing module, which uses processes instead of threads. Depending on the specific task and its characteristics, the use of threads or processes may be more efficient or convenient.

### What are greenlets. General concept. Implementation examples

Greenlets are a lightweight concurrency library for Python that allows for cooperative multitasking of microthreads within a single thread of execution. A greenlet is a small independent execution context that can be switched between other greenlets in a cooperative manner.

Greenlets are useful in situations where the overhead of creating and managing multiple threads is too high, but you still need to perform concurrent operations in your code. Greenlets can be used to perform I/O-bound tasks, such as network requests, without blocking the main thread of execution.

One popular implementation of greenlets in Python is the gevent library, which provides a high-level interface for working with greenlets and includes support for network and I/O operations. Another implementation is the greenlet library, which provides a lower-level interface for creating and managing greenlets.

Greenlet == Green thread == Green threads == lightweight threads inside a virtual machine. They can be called coroutines, coprocesses, actors, etc. platform dependent. The operating system does not see them. From the point of view of the OS, one process of the virtual machine is running, and what is inside it is unknown. Such threads are managed by the virtual machine itself: it generates, executes, and coordinates access to resources.

Examples: coroutines in Go and Lua, lightweight processes in Erlang, the greenlet module for Python. The gevent module uses greenlets

Here's an example of how you might use greenlets in Python:

```python
import gevent

def worker(name):
    for i in range(5):
        print(f"{name} working on task {i}")
        gevent.sleep(1)

gevent.joinall([
    gevent.spawn(worker, "Worker 1"),
    gevent.spawn(worker, "Worker 2")
])
```

In this example, we define a `worker` function that simulates doing some work by printing a message every second. We then use the `gevent.spawn` function to create two greenlets that will execute the `worker` function. Finally, we use `gevent.joinall` to wait for both greenlets to complete. The output of this program might look something like this:

```python
Worker 1 working on task 0
Worker 2 working on task 0
Worker 1 working on task 1
Worker 2 working on task 1
Worker 1 working on task 2
Worker 2 working on task 2
Worker 1 working on task 3
Worker 2 working on task 3
Worker 1 working on task 4
Worker 2 working on task 4
```

## What are the options for implementing the Singleton pattern in python

- [Creating a singleton in Python](https://stackoverflow.com/questions/6760685/creating-a-singleton-in-python)

**Decorator:**

```python
def singleton(class_):
     instances = {}
     def getinstance(*args, **kwargs):
         if class_not in instances:
             instances[class_] = class_(*args, **kwargs)
         return instances[class_]
     return getinstance

@singleton
class MyClass(BaseClass):
     pass
```

_Pros:_

- Decorators are often more intuitive than multiple inheritance.

_Flaws:_

- Although objects created using `MyClass()` will be true singleton objects, `MyClass` itself is a function, not a class, so you cannot call class methods from it.
- Increases testing difficulty

**Base class:**

```python
class Singleton(object):
     _instance = None
     def __new__(class_, *args, **kwargs):
         if not isinstance(class_._instance, class_):
             class_._instance = object.__new__(class_, *args, **kwargs)
         return class_._instance

class MyClass(Singleton, BaseClass):
     pass
```

_Pros:_

- It's real class.

_Flaws:_

- Multiple inheritance complicates the code. `__new__` can be overwritten during inheritance from the second base class?

**Metaclasses:**

```python
class Singleton(type):
     _instances = {}
     def __call__(cls, *args, **kwargs):
         if cls not in cls._instances:
             cls._instances[cls] = super(Singleton, cls).__call__(*args, **kwargs)
         return cls._instances[cls]

#Python2
class MyClass(BaseClass):
     __metaclass__ = Singleton

#Python3
class MyClass(BaseClass, metaclass=Singleton):
     pass
```

_Pros:_

- This is real class.
- Automatically covers inheritance
- We use metaclasses for their intended purpose

_Flaws:_

- Do they exist?

**Module:**

_Pros:_

- Simplicity

_Flaws:_

- Not lazy-initialized

## What tools do you know for checking codestyle

- [Tools for analyzing Python code. Part 1(rus)](https://proglib.io/p/python-code-analysis/)
- [Tools for analyzing Python code. Part 2(rus)](https://proglib.io/p/python-code-analysis-tools/)

**Pycodestyle** is a simple console tool for analyzing Python code, specifically for checking code against PEP8. One of the oldest code analyzers, until 2016 was called pep8, but was renamed at the request of the creator of the Python language, Guido van Rossum.

**Pydocstyle** checks if modules, classes, functions have docstring and if they conform to the official PEP257 convention.

**Pylint** combined both the search for logical and stylistic errors. This powerful, highly customizable tool for analyzing Python code features a large number of checks and a variety of reports.

**Vulture** is a small utility for finding "dead" code in Python programs. It uses the ast module of the standard library and creates abstract syntax trees for all source code files in a project. Next, a search is performed for all objects that have been defined but are not used. Vulture is useful for cleaning up and finding bugs in large base codes.

**Flake8** - binding to the utilities included in it - pyflakes, pycodestyle, mccabe. Flake8 has the same core functionality as pylint. However, it has a number of differences and features:

- The possibilities of statistical reports are limited to counting the number of each of the errors (--statistics) and their total number (--count).
- To run in multiple threads (`-jobs=<num>`) the multiprocessing module is used, for this reason multi-threading will not work on Windows systems.
- No ability to generate reports in json format; when called with the --bug-report key, only the header for the report is created, indicating the platform and versions of the incoming utilities.
- Comments in code blocking output. Adding the comment # noqa to the line with the error will remove it from the report.
- During editing, to suppress individual errors on the fly, you can list excluded errors in the key `--extend-ignore=<errors>`
- Syntax check in doctest lines (-doctests).
- Presence of Version Control Hooks. Integration with version control systems takes place literally with the help of two commands (git and mercurial are supported).
- Extensibility. Flake8 for Python code analysis allows you to create and use plugins. Using plugins in Flake8, you can: add additional checks, use other report formats, or automatically fix errors found. PyPi has a large number of open-source plugins.

**Prospector** is a tool for analyzing Python code. Combines the functionality of other Python analysis tools like pylint, pep8, mccabe, Pyflakes, Dodgy, pydocstyle (experimental, bugs are possible). Additionally, you can connect mypy, pyroma, vulture. The main feature of prospector is the presence of pre-installed profiles, which contain the settings of the utilities included in it, designed to suppress the most captious warnings and leave only important messages.

**Pylama** is a code audit tool for Python and JavaScript. Serves as a wrapper for such utilities as: pydocstyle, pycodestyle, pyflakes, mccabe, pylint, radon (a tool for collecting and calculating various metrics from source code). gjslint is used to work with JavaScript code.

**autopep8** modifies non-PEP8 compliant code. Checking for compliance with conventions is done using the pycodestyle utility. autopep8 has support for multithreading, recursive directory traversal, the ability to save settings in a file, set the range of lines to correct, error filtering, and directly modify the file being checked.

**yapf** is similar to autopep8 but uses a different approach which is based on the "clang-format" developed by Daniel Jasper. The yapf-formatted code will not only respect the accepted conventions, but also look like it was written by a good programmer. The second important difference is the ability to set styles. To do this, use the --style key and pass the settings file or one of the predefined values (pep8, google, chromium, facebook) as an argument.

**black** is a no-compromise formatter that works fast and saves programmers time and mental energy for more important things.

## What is a list/dict/set comprehension

In Python, comprehension is a concise way of creating lists, dictionaries, and sets. It is a syntax construct that allows for creating new collections by iterating over existing sequences.

1. List comprehension: It is a way of creating a new list by performing some operations on each item of an existing list. The syntax of list comprehension is enclosed in square brackets and contains an expression followed by a `for` loop or multiple `for` loops and an optional `if` clause.

Example:

```python
# Creating a new list of even numbers from an existing list
old_list = [1, 2, 3, 4, 5, 6, 7, 8, 9]
new_list = [x for x in old_list if x % 2 == 0]
print(new_list) # Output: [2, 4, 6, 8]
```

2. Dictionary comprehension: It is a way of creating a new dictionary by iterating over an existing sequence. The syntax of dictionary comprehension is enclosed in curly braces and contains a `key-value` pair expression followed by a `for` loop or multiple `for` loops and an optional `if` clause.

Example:

```python
# Creating a dictionary from two lists
keys = ['a', 'b', 'c']
values = [1, 2, 3]
new_dict = {k:v for k, v in zip(keys, values)}
print(new_dict) # Output: {'a': 1, 'b': 2, 'c': 3}
```

3. Set comprehension: It is a way of creating a new set by performing some operations on each item of an existing set. The syntax of set comprehension is enclosed in curly braces and contains an expression followed by a `for` loop or multiple `for` loops and an optional `if` clause.

Example:

```python
# Creating a new set of even numbers from an existing set
old_set = {1, 2, 3, 4, 5, 6, 7, 8, 9}
new_set = {x for x in old_set if x % 2 == 0}
print(new_set) # Output: {2, 4, 6, 8}
```

_Energetic_ - an iterable that builds all of its elements at once. In Python, inclusions are energetic operations. The opposite is _lazy_.

## What's the difference between single and double underscore

- [Understanding the underscore of Python](https://hackernoon.com/understanding-the-underscore-of-python-309d1a029edc)

There are 5 use cases for underlining in Python:

1. To store the value of the last expression in the REPL
2. Ignoring value
3. To define a special value for a function or variable
   - single at the beginning or end of the name
   - double at the beginning
   - double at the beginning and end
4. For use as a localization function
5. To separate the characters of a number (`1_00 == 100`)

More:

`private` and `protected` methods:

In Python, single underscore and double underscore have different purposes.

- A single underscore before a method or attribute name indicates that it is not intended to be used outside of the class or module in which it is defined. This is not a limitation, but rather an agreement between programmers. For example:

```python
class MyClass:
    def __init__(self):
        self._my_attr = 42

    def _my_method(self):
        print("Hello from _my_method")

obj = MyClass()
print(obj._my_attr)     # Attribute access using single underscore
obj._my_method()        # Method call using single underscore
```

A double underscore at the beginning of a method or attribute name makes it "private" in the sense that it cannot be directly accessed from outside the class. The double underscore also performs the "name mangling" mechanism, which changes the name of a method or attribute by prefixing it with two underscores and the class name. This is done to prevent name conflicts between classes. For example:

```python
class MyClass:
    def __init__(self):
        self.__my_attr = 42

    def __my_method(self):
        print("Hello from __my_method")

obj = MyClass()
print(obj.__my_attr)     # Error: Attribute not accessible from outside the class
obj.__my_method()        # Error: Method not accessible from outside the class
```

However, a double-underscored attribute or method name can still be accessed from outside the class using the name mangling mechanism. For example:

```python
class MyClass:
    def __init__(self):
        self.__my_attr = 42

    def __my_method(self):
        print("Hello from __my_method")

obj = MyClass()
print(obj._MyClass__my_attr)     # Accessing an attribute with a mangling name
obj._MyClass__my_method()        # Calling a method with a mangling name
```

Despite this, the use of names with double underscores should be avoided if necessary for backward compatibility with other versions of the code. Instead, it's better to use a single underscore to denote "internal

## Difference between copy() and deepcopy()

- [Deep vs Shallow Copies in Python](https://stackabuse.com/deep-vs-shallow-copies-in-python/)

The `deepcopy()` deep copy creates a new and separate copy of the entire object or list with its own unique memory address. This means that any changes you make to the new copy of the object or list will not be reflected in the original. This process goes like this: first, a new list or object is created, and then all elements are recursively copied from the original to the new one.

The `copy()` shallow copy also creates a separate new object or list, but instead of copying the child elements into a new object, it simply copies the references to their memory addresses. Therefore, if you make a change to the original object, it will be reflected in the copied object, and vice versa. In short, both copies depend on each other.

## What is a garbage collector. What are its pros and cons

- [All you need to know about the garbage collector in Python(rus)](https://habr.com/ru/post/417215/)

GC (generational garbage collector) is a garbage collector, it was created primarily to detect and remove cyclic references.
`gc` is a built-in module in python and can be turned off and started manually (or not started) if necessary. To understand why the GC was created, you need to understand how the memory manager works in Python and how this memory is released.

Unlike other popular languages, Python does not free all memory back to the operating system as soon as it deletes an object. Instead, it uses an additional memory manager designed for small objects (less than 512 bytes). To work with such objects, it allocates large blocks of memory, in which many small objects will be stored in the future.

As soon as one of the small objects is deleted - the memory from under it does not pass to the operating system, Python leaves it for new objects with the same size. If there are no objects left in one of the allocated memory blocks, then Python can release it to the operating system. Typically, block release happens when a script creates a lot of temporary objects.

Thus, if a long-lived Python process starts consuming more memory over time, this does not mean that there is a memory leak problem in your code.

The standard python interpreter (CPython) uses two garbage collection algorithms at once, reference counting and a generational garbage collector (hereinafter referred to as GC), better known as the standard gc module from Python.

The reference counting algorithm is very simple and efficient, but it has one big drawback. It doesn't know how to define circular references. It is because of this that Python has an additional collector called the generational GC that keeps track of objects with potential circular references.

In Python, the reference counting algorithm is fundamental and cannot be disabled, while GC is optional and can be disabled.

Unlike the reference counting algorithm, circular GC does not run in real time and runs periodically. Each run of the collector creates micro-pauses in the code, so CPython (the standard interpreter) uses various heuristics to determine how often the garbage collector is run.

The cyclic garbage collector divides all objects into 3 generations (generations). New objects fall into the first generation. If the new object survives the garbage collection process, then it is moved to the next generation. The higher the generation, the less often it is scanned for garbage. Since new objects often have a very short lifetime (are temporary), it makes sense to poll them more often than those that have already gone through several stages of garbage collection.

Each generation has a special counter and trigger threshold, upon reaching which the garbage collection process is triggered. Each counter stores the number of allocations minus the number of deallocations in a given generation. As soon as any container object is created in Python, it checks these counters. If the conditions are met, then the garbage collection process begins.

If several or more generations crossed the threshold at once, then the oldest generation is selected. This is due to the fact that older generations also scan all previous ones. To reduce garbage collection pauses for long-lived objects, the oldest generation has an additional set of conditions.

The default trigger thresholds for generations are set to 700, 10, and 10 respectively, but you can always change them with the gc.get_threshold and gc.set_threshold functions.

## What is introspection

- [Introspection in Python](http://zetcode.com/lang/python/introspection/)

_Introspection_ is the ability of a program to inspect the type or properties of an object while the program is running. You may wonder what type of object is it, is it an instance of a class. Some languages even let you know the inheritance hierarchy of an object. The possibility of introspection exists in languages such as Ruby, Java, PHP, Python, C++ and others. All in all, introspection is a very simple and very powerful phenomenon. Here are some examples of using introspection:

```java
// Java

if(obj instanceof Person){
    Person p = (Person)obj;
    p.walk();
}
```

```php
//PHP

if ($obj instanceof Person) {
    // do whatever
}
```

In Python, the most common form of introspection is to use the dir method to list an object's attributes:

```python
#Python

class foo(object):
   def __init__(self, val):
     self.x = val
   def bar(self):
     return self.x

...

dir(foo(5))
=> ['__class__', '__delattr__', '__dict__', '__doc__', '__getattribute__', '__hash__', '__init__', '__module__',
'__new__', '__reduce__', '__reduce_ex__', '__repr__', '__setattr__', '__str__', '__weakref__', 'bar', 'x']
```

## What is reflection

Introspection allows you to examine the attributes of an object at runtime, while reflection allows you to manipulate them. _Reflection_ is the ability of a computer program to learn and modify its structure and behavior (values, metadata, properties, and functions) at run time. In simple terms: it allows you to call methods of objects, create new objects, modify them without even knowing the names of interfaces, fields, methods at compile time. This nature of reflection makes it more difficult to implement in statically typed languages, since type errors occur at compile time rather than runtime (more on that here). However, it is possible because languages such as Java, C#, and others allow both introspection and reflection (but not C++, which only allows introspection).

For the same reason, reflection is easier to implement in interpreted languages, because when functions, objects, and other data structures are created and called at runtime, some kind of memory allocation system is used. Interpreted languages usually provide such a system by default, while compiled languages will require an additional compiler and interpreter to ensure that reflection is correct.

_Example_:

```python
# No reflection
Foo().hello()

# With reflection
getattr(globals()['Foo'](), 'hello')()
```

# Django

## What is Middleware, why, how it is implemented

Middleware in Django is a component that can process HTTP requests and responses in an intermediate way. It allows you to modify the requests that are sent to your Django application, as well as the responses that are returned to the client. Middleware can perform various tasks such as authentication, caching, logging, changing request and response headers, and more.

Middleware in Django works like a chain. Each middleware receives the request and can modify it, pass it to the next middleware, or pass it to the view handler. Then, each middleware can modify the response returned by the view, pass it to the previous middleware, or send it to the client.

Django comes with a lot of built-in middleware that can be used for a variety of tasks. It is also possible to create your own middleware to solve specific problems.

At the language level, this is an object with methods `process_request` and `process_response`. Methods must return the received object (request or response) for further processing, or throw an exception if something is wrong. In this case, further processing stops.

To enable Middleware, just add the path to it to the `MIDDLEWARE` list.

## Name the main middleware. What are they needed for

Basic middleware in Django:

1. `Authentication Middleware`: Checks if the user is authenticated. If not, it redirects it to the login page.
2. `CSRF Middleware`: Protects against cross-site request forgery (CSRF) attacks.
3. `Common Middleware`: Handles various HTTP requests, including handling static files, handling 404 and 500 errors, and setting security headers.
4. `Session Middleware`: Handles user sessions.
5. `Message Middleware`: Handles the messages to be passed to the user on the next request.

## Describe how the CSRF middleware works

For each request, the system generates a unique token and sets it in cookies. Each form has a hidden `csrf-token` field with the same token. When submitting a form using the `POST` method, Django checks that the form field and the value in the cookie match. If not, it means that the request is forged or sent from another domain.

To free some view from checking (if it is an API, for example), it is enough to wrap it with the `csrf_except` decorator.

The CSRF middleware and template tag provide easy-to-use protection against Cross-Site Request Forgery. This type of attack occurs when a malicious Web site contains a link, a form button, or some javascript that is designed to perform some action on your Web site using the credentials of an authorized user who visited the malicious site in their browser. It also includes a related type of attack, `login CSRF`, where the attacked site tricks the user's browser into logging into the site with someone else's credentials.

The first defense against CSRF attacks is to ensure that GET requests (and other 'safe' methods defined in 9.1.1 Safe Methods, HTTP 1.1, [RFC 2616#section-9.1.1](https://tools.ietf.org/html/rfc2616.html#section-9.1.1)) are free from side effects. Requests via 'unsafe' methods such as `POST`, `PUT` and `DELETE` can be secured using the steps below.

_How it works:_

CSRF is based on the following things:

1. A CSRF cookie that is set as a random number (Session Independent Random Word, as it's sometimes called) that other sites won't have access to. This cookie is set using `CsrfViewMiddleware`. It should be permanent, but since there is no way to set cookies that never expire, it is sent with every response that called django.middleware.csrf.get_token() (the function used internally to get the CSRF token).

2. All POST forms contain a hidden `csrfmiddlewaretoken` field. The field value is equal to the CSRF cookie. This part is done by the template tag.

3. All HTTP requests that are not `GET`, `HEAD`, `OPTIONS` or `TRACE` must contain a CSRF cookie and a 'csrfmiddlewaretoken' field with the correct value. Otherwise, the user will receive a 403 error. This check is done in `CsrfViewMiddleware`.

4. In addition, for HTTPS requests, the “referer” (request source) is checked in CsrfViewMiddleware. This is necessary to prevent a MITM attack (Man-In-The-Middle), which is possible when using HTTPS and a token not tied to the session, because clients accept (unfortunately) the 'Set-Cookie' HTTP header, even though communication with the server is via HTTPS. (This check is not performed for HTTP requests because the "Referer" header is easily spoofed when using HTTP.) If the CSRF_COOKIE_DOMAIN setting is specified, the "referer" value will be compared against this value. The value supports sub-domains. For example, CSRF_COOKIE_DOMAIN = '.example.com' will allow POST requests from www.example.com and api.example.com. If the setting is not specified, "referer" must be equal to the Host HTTP header. To expand the list of available domains beyond the current host and cookie domain, use CSRF_TRUSTED_ORIGINS.

This approach ensures that only forms submitted from trusted domains can submit POST data.

GETs are deliberately ignored (and all other requests that are considered “safe” according to RFC 2616). These requests should never perform any potentially harmful actions, and CSRF attacks via a GET request should be harmless. RFC 2616 defines `POST`, `PUT` and `DELETE` as "unsafe".

## What are signals? Why are they needed? What are the main

Signals in Django are a way for certain senders to notify a set of receivers that some action has taken place. This can be useful for decoupling applications, allowing them to interact without necessarily having any direct dependencies.

Signals are essentially a kind of event framework, where senders emit signals when something happens, and receivers handle those signals by executing some code in response.

Some of the main built-in signals in Django include:

- `pre_save` and `post_save`: These signals are sent before and after an object is saved to the database, respectively.
- `pre_delete` and `post_delete`: These signals are sent before and after an object is deleted from the database, respectively.
- `m2m_changed`: This signal is sent when a ManyToManyField on a model is changed.
- `request_started` and request_finished: These signals are sent at the beginning and end of each HTTP request, respectively.
  Signals are useful because they provide a way to decouple the code that sends a signal from the code that handles the signal. This can make it easier to write reusable code, since you can write a signal handler that can be used by multiple senders without those senders having to know about each other.

In addition to the built-in signals, you can also create your own custom signals to use in your applications.

Signals propagate synchronously. This means that by subscribing a hundred handlers to one signal, we will increase the time required to return a response.

The main signals are the beginning of the request and its end, before saving the model and after, accessing the database.

**Important:** model signals work individually, that is, for one model. Batch processing such as `queryset.all().delete()` or `queryset.all().update({'foo'=42})` will not fire delete or update events.

## How m2m communication is implemented at the database level

In Django, many-to-many (m2m) relationships are implemented using an intermediary table. This table is created automatically when you define a many-to-many field in your models. The table stores the relationships between the two tables as a pair of foreign keys.

For example, let's say you have two models, Author and Book, and you want to create a many-to-many relationship between them. You can define the relationship in the following way:

```python
class Author(models.Model):
    name = models.CharField(max_length=100)
    books = models.ManyToManyField('Book')

class Book(models.Model):
    title = models.CharField(max_length=100)
```

Django will create a third table to store the relationship between `Author` and `Book`. This table will have two foreign keys, one for `Author` and one for `Book`. The names of the foreign keys are generated automatically by Django.

When you add an `Author` instance to a `Book` instance's `authors` attribute, Django creates a new row in the intermediary table with the foreign keys pointing to the `Author` and `Book` instances.

When you query the `books` attribute of an `Author` instance, Django will automatically perform a `JOIN` operation between the `Author`, intermediary, and `Book` tables to retrieve the related `Book` instances.

In summary, m2m communication in Django is implemented using an intermediary table with foreign keys pointing to the two tables involved in the relationship.

## Is it better to submit a form - GET or POST

It depends on the specific use case and what you want to achieve. In general, you should use GET requests when you want to retrieve data from the server, and use POST requests when you want to submit data to the server for processing.

In Django, GET requests are typically used for retrieving data, such as displaying a list of items, filtering data based on user input, or performing a search. POST requests are typically used for creating or updating data, such as submitting a form or uploading a file.

However, it's important to note that using GET requests to submit sensitive data, such as passwords or personal information, is not recommended. This is because GET requests can be cached by the browser or logged by intermediaries, potentially exposing the sensitive data.

In summary, the choice of whether to use GET or POST requests in Django depends on the specific use case and the type of data being transmitted. It's important to carefully consider the potential security and performance implications of each option.

The form can be submitted both ways. In the first case, the variables are attached to the query string after the question mark. In the second, they are transmitted in the request body.

The technical limitation of the GET method is that they cannot transfer a file, unlike POST.

It is desirable to submit the form using the POST method for the following reasons:

- GET requests can be cached, especially in IE family browsers
- GET requests end up in provider, server, browser history logs. The password and login in this case can light up in many places.
- some viruses monitor the contents of the address bar and send them to third parties.

## How Serializer works in Django REST Framework

In Django REST Framework (DRF), `Serializer` is a key component for handling data serialization and deserialization. It provides a way to convert complex data types, such as querysets and model instances, to Python native data types that can be easily rendered into JSON, XML, or other content types.

When a request is made to a DRF view, the framework automatically checks the request method (e.g., `GET`, `POST`, `PUT`, `DELETE`) to determine whether to serialize or deserialize data. If the request method is GET, the framework will serialize the data to send it to the client. If the request method is POST or PUT, the framework will deserialize the data received from the client into a Python object.

To use the Serializer in DRF, you need to create a new serializer class that inherits from `serializers.Serializer` or `serializers.ModelSerializer`. You can define the fields that you want to serialize or deserialize using `SerializerMethodField`, `CharField`, `IntegerField`, `BooleanField`, and other similar fields. You can also define custom validation and data manipulation methods using the `validate()` and `to_representation()` methods.

In addition, the Serializer class provides many built-in validation methods and fields that allow you to validate the incoming data against specific criteria. This ensures that the data is consistent with the model structure and other predefined business rules.

Overall, Serializer in Django REST Framework is a powerful tool for handling data serialization and deserialization. It allows you to quickly and easily convert complex data types to native Python data types that can be easily rendered into JSON, XML, or other content types.

Serializer converts information stored in the database and defined using Django models into a format that is easily and efficiently passed through the API.

Django models intuitively represent the data stored in the database, but the API should convey the information in a less complex structure. Although the data will be represented as instances of the Model classes, it must be converted to JSON format in order to be passed through the API.

The DRF serializer does this conversion. When the user submits information (such as creating a new instance) via the API, the serializer takes the data, validates it, and converts it into something that Django can fold into a model instance. Similarly, when the user accesses information via the API, the corresponding instances are passed to the serializer, which converts them into a format that can be easily passed to the user as JSON.

The most common form a DRF serializer takes is one that is bound directly to a Django model:

```python
class ThingSerializer(serializers.ModelSerializer):
  class Meta:
    model = Thing
    fields = (‘name’, )
```

The fields settings allow you to specify exactly which fields are available to this serializer. Alternatively, exclude can be set instead of fields, which will include all fields in the model except those specified in exclude.

Serializers are an incredibly flexible and powerful component of DRF. Although connecting a serializer to a model is the most common, serializers can be used to create any Python data structure via an API, according to certain parameters.

## What is Meta in Django classes and what is it for

In Django, `Meta` is a class that is defined inside the model or form class to provide metadata about the class itself. It allows you to specify various options and settings that are not directly related to the model or form fields, but rather to the model or form as a whole.

Some common use cases for `Meta` include:

- Specifying the database table name for the model class
- Defining model permissions and ordering
- Configuring the default ordering of querysets returned by the model
- Defining unique constraints and indexes for the model
- Setting up custom validation rules and error messages for the form

`Meta` options can be defined as class variables within the `Meta` class. Here's an example of how it can be used in a Django model:

```python
class MyModel(models.Model):
    name = models.CharField(max_length=50)
    created_at = models.DateTimeField(auto_now_add=True)

    class Meta:
        ordering = ['-created_at']
        verbose_name_plural = 'My Models'
```

In this example, the `Meta` class is used to specify the default ordering for querysets returned by the `MyModel` class, as well as to set a custom plural name for the model. The `ordering` option specifies that querysets should be ordered by the `created_at` field in descending order. The `verbose_name_plural` option sets the plural name for the model to "My Models" instead of the default "My Models".

Django does a lot of its work through metaclasses.

In short, metaclasses are classes that construct other classes. They are declared through the class attribute `__metaclass__` (in jung, through the compatibility layer with python 3 through the six module up to version 2).

So when Django constructs your class, it does so with its metaclass. In order for her to know some parameters of your class when constructing, well, for example, a model or fields in your case, she looks for a class called Meta in your class.

In general, all this magic with metaclasses is very important in jang and therefore it is better not to redefine the very logic of the formation of a class.

## What Meta is responsible for in the serializer

In Django REST Framework, the `Meta` class inside a serializer is used to provide additional metadata about the serializer.

The `Meta` class can be used to define:

- The model that the serializer is based on
- The fields that should be included or excluded from the serialized output
- The ordering of the fields in the serialized output
- Custom validation or processing of the serialized data

Here's an example of using Meta in a serializer:

```python
from rest_framework import serializers
from myapp.models import MyModel

class MySerializer(serializers.ModelSerializer):
    class Meta:
        model = MyModel
        fields = ['id', 'name', 'email']
```

In the above example, the `Meta` class is used to define that the `MySerializer` serializer should be based on the
`MyModel` model. It also specifies that the `id`, `name`, and `email` fields should be included in the serialized output.

## What is the difference between django and flask

Django and Flask are two of the most popular frameworks for developing web applications in Python. Here are some of the main differences between them:

1. Architecture: Django is a complete MVC framework where M is the model, V is the view, and C is the controller, which in Django is called a URL router. Flask, on the other hand, does not impose hard restrictions on the architecture, allowing the developer to define the structure of the application himself.

2. Size and Complexity: Django is a large-sized framework that includes many built-in features and tools for a variety of tasks such as authentication, URL routing, database manipulation, and more. Flask, on the other hand, is a lightweight framework that provides only the bare essentials and everything else can be implemented using third-party packages.

3. Databases: Django comes with an ORM (Object-Relational Mapping) that makes it easy to work with databases and allows you to work with them through an object-oriented interface. Flask does not have its own ORM and can work with any database package of the developer's choice.

4. Administrative interface: Django comes with a built-in administrative interface that allows administrators to manage the data stored in the database, such as adding, deleting, or modifying entries in the database. Flask does not have such a built-in administrative interface.

5. RESTful API: Django has built-in support for creating RESTful APIs through the Django REST framework. Flask also allows you to create RESTful APIs using third party libraries such as Flask-RESTful.

6. Speed and Performance: Flask is faster and more lightweight than Django because Flask doesn't have built-in components that can slow down performance.

The choice between Django and Flask depends on what task needs to be solved and what are the requirements for the application.

You need to take your own tool for each task, Django is well suited for news sites, blogs, etc., due to the fact that it already has a lot out of the box (including the admin panel), and it was created specifically for this type of site. Flask, on the other hand, out of the box, has almost nothing and is better suited for any microservices or applications for which the technology stack that comes with Django is not suitable.

## How Django's authentication system works

Django's authentication system provides a secure way to manage user authentication in web applications. Here is a brief overview of how it works:

1. User authentication begins when the user enters their login credentials (e.g. username and password) into a login form.
2. When the login form is submitted, Django's authentication system verifies the user's credentials by checking them against the user model in the database.
3. If the user's credentials are valid, Django creates a session for the user and stores the session key in a cookie on the user's browser.
4. On subsequent requests, the user's browser sends the session cookie to the server, allowing Django to identify the user and retrieve their session data (e.g. user ID).
5. Django's authentication system provides a variety of built-in views and utilities for handling common authentication tasks, such as logging in, logging out, and resetting passwords.
   A6. dditionally, Django allows developers to customize the authentication system by creating their own authentication backends, which can provide custom authentication methods (e.g. social login, two-factor authentication) or integrate with external authentication systems (e.g. OAuth, LDAP).

Overall, Django's authentication system provides a convenient and secure way to manage user authentication in web applications, with many built-in features and options for customization.

Django comes with a user authentication system. It provides user accounts, groups, permissions and sessions based on cookies.

The Django authentication system is responsible for both aspects: authentication and authorization. In short, authentication verifies the user, while authorization determines what the authenticated user can do. In what follows, the term “authentication” will be used to refer to both aspects ([User authentication in Django](https://docs.djangoproject.com/en/2.2/topics/auth/)).

The authentication system consists of:

- Users
- Permissions: Binary (yes/no) flags that determine whether the user has the right to perform certain actions.
- Groups: A general way to assign labels and rights to multiple users.
- Customizable password hashing system
- Tools for forms and views to authenticate users or restrict access to content
- Plugin systems

The Django authentication system tries to be very simple and does not provide some of the features common in other web authentication systems. Such features are implemented in third-party packages:

- Password complexity check
- Limit login attempts
- Authentication through third-party services (OAuth, for example)

## What are views and viewsets in django? what are their features and differences

In Django, views are Python functions or classes that define how web pages or other content should be displayed to the user. Views are responsible for processing incoming requests, handling any errors, and returning an HTTP response.

Django REST framework introduces ViewSets, which are classes that provide CRUD (Create, Read, Update, Delete) operations for APIs. ViewSets are similar to views in that they define how data should be displayed or handled, but they have several key differences:

1. Functionality: ViewSets provide additional functionality beyond basic views, such as the ability to handle multiple HTTP methods on the same endpoint (e.g. GET and POST).
2. Routing: ViewSets are used in conjunction with routers, which automatically generate URLs and link them to appropriate ViewSet methods.
3. Code organization: ViewSets are organized by resource, making it easier to manage related code in a single place.
4. Default methods: ViewSets provide default implementations for standard API actions, such as list(), retrieve(), create(), update(), and destroy().

Overall, ViewSets provide a more structured and flexible approach to building APIs than traditional views. However, they may be more complex to work with and require additional configuration. The choice between using a View or a ViewSet largely depends on the specific requirements of the application.

## What mechanism in django is responsible for working with templates and how it is implemented

In Django, the template system is responsible for working with templates. It is implemented using the Django template language, which is a simple, yet powerful, syntax for rendering dynamic content in HTML files.

The Django template language allows you to define placeholders, called template tags, which are replaced with actual content when the template is rendered. These tags can be used to include variables, perform logic operations, iterate over lists, and much more.

To use the template system in Django, you need to define your templates in HTML files and then create a view that renders the template with the context data. The context data is a dictionary that contains the data you want to pass to the template.

Views are Python functions that define the logic for rendering a template. They take a request object as input and return an HttpResponse object that contains the rendered HTML. Views can be written in two different ways: function-based views or class-based views.

Function-based views are simple Python functions that take a request object as input and return an HttpResponse object. They are easy to write and understand, but can become complex as your application grows.

Class-based views are more powerful and flexible than function-based views. They allow you to reuse common functionality across different views, and provide a consistent interface for handling different HTTP methods (GET, POST, PUT, DELETE, etc.). Class-based views are defined as Python classes that inherit from one of the built-in view classes provided by Django.

In addition to views, Django also provides a set of built-in viewsets that make it easy to build APIs using Django REST framework. Viewsets are classes that define the CRUD (Create, Read, Update, Delete) operations for a specific model or set of models. They provide a consistent interface for handling HTTP requests and responses, and can be customized to handle different authentication and permission requirements.
