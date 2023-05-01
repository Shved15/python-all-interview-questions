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

### Where search will be faster, and where enumeration and why: dict, list, set, tuple

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

### Why exceptions can use the try finally construct without except

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

### How is support for functional programming implemented in Python

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

### What is GIL. What problems does it have

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

## Are you keeping up with the development of the language? What are the latest updates that you are aware of?

Of course, in the fall of 2021, version 3.10 was released, and in the fall of 2022, version 3.11 of the language was released.

Python 3.10, released in October 2021, contains a number of new features, including:

- `match` operator for pattern matching
- Support for parameter annotations in `functools.cache()` and `functools.lru_cache()` decorators
- Added `ctx` and `future_warning` options to `importlib.resources.open_binary()`, `importlib.resources.open_text()`, `importlib.resources.path()`, `importlib.resources.read_binary()`, `importlib.resources.read_text()`, and `importlib.resources.as_file()`
- Improvements in type hint syntax and variable typing, including support for `+` and `|` for a combination of types
- Multiple `with` blocks can now be combined into a single block using the `as` operator (e.g. `with a as x, b as y:`)
- Updated and expanded standard library, including new modules and methods such as `zoneinfo`, `pathlib.Path.replace()`, and `statistics.median_low()`
  These are just a few of the many changes introduced in Python 3.10. A complete list of changes can be found in the Python documentation.

One of the major innovations in Python 3.10 is the addition of the "match" construct (analogous to "switch" in other programming languages) to more easily handle multiple choices. Instead of using a long chain of "if-elif-else" conditional statements to compare a single value with multiple options, you can now use the "match" construct, which allows you to more clearly define all the possible values for a variable.

For example:

```python
def calculate(value1, operator, value2):
    match operator:
        case '+':
            return value1 + value2
        case '-':
            return value1 - value2
        case '*':
            return value1 * value2
        case '/':
            return value1 / value2
        case _:
            raise ValueError("Invalid operator")

result = calculate(10, '+', 5)
print(result)  # Output: 15

result = calculate(10, '%', 5)  # Invalid operator
```

In this example, the `calculate` function takes two numeric values, `value1` and `value2`, and an operator `operator`, which can be one of four valid values: `+`, `-`, `*`, `/`. The match construct tests the value of an operator and performs the corresponding action on two numbers. If the statement does not match any of the valid values, then a `ValueError` exception is thrown.

Calling the `calculate(10, '+', 5)` function will return the value `15`, while calling `calculate(10, '%', 5)` will throw a `ValueError` exception.

Main features of match in Python 3.10:

- Support for various data types. You can use strings, integers, enums, objects, lists, and many other data types in a match.

- Template support. Match can use wildcards to match values more precisely. For example, you can use a pattern to match all integers that are even.

- Condition support. A match can use conditions to match values more precisely. For example, you can use a condition to match only those strings that contain a specific substring.

- Range support. A match can use ranges to match values that are within a certain range. For example, you can use a range to match all integers from 1 to 10.

- Support for multiple mappings. A match can perform multiple matches that use different patterns, conditions, and ranges.

In addition, improvements have been made to the annotation type, new operators have been added, including an assignment operator with an operation ("walrus" operator), work has been improved with asynchronous programming, new methods and functions have been added for working with strings and bytes, work with decorators has been improved, etc. .d.

It is also worth noting that deprecated functions and methods have been removed in Python 3.10, which has reduced the size and simplification of the interpreter code.

At the time of the answer (April 2023), a stable version of Python 3.11 has not yet been released, so it is not possible to fully answer the question.

However, on the official Python website (https://www.python.org/downloads/release/python-3110a1/) you can find information about additions and changes in Python 3.11. Some of them:

- Added exception handling in asynchronous functions
- Added new features in pathlib and contextvars modules
- Improved work with virtual environments (venv)
- Changes have been made to the standard library (for example, new methods have been added to the math module)
- Changes have been made to the syntax of the language (for example, support for the match operator has been added)
  And much more.

Key differences between Python 3.9 and 3.10:

1. PEP 634 - Structural Pattern Matching: Specification - The major new feature in Python 3.10 is the introduction of structural pattern matching, which allows developers to match and destructure data structures such as tuples, lists, and dictionaries. This feature was proposed in PEP 634 and provides a more concise and expressive way of writing code that deals with complex data structures.

2. PEP 604 - Allow writing union types as X | Y - Another significant change in Python 3.10 is the ability to use the pipe operator (|) to create union types. This feature, proposed in PEP 604, provides a more concise and Pythonic way of expressing complex type annotations.

3. PEP 616 - String methods to remove prefixes and suffixes - Python 3.10 introduced two new string methods, str.removeprefix() and str.removesuffix(), which make it easier to remove prefixes and suffixes from strings. These methods are intended to replace the existing str.startswith() and str.endswith() methods when only the prefix or suffix needs to be removed.

4. PEP 613 - Explicit Type Aliases - Python 3.10 added support for explicit type aliases, which allow developers to create aliases for complex type annotations. This feature, proposed in PEP 613, makes it easier to write and read complex type annotations by providing a way to give a name to a type.

5. PEP 635 - Structural Pattern Matching: Motivation and Rationale - Python 3.10 also introduced PEP 635, which explains the motivation and rationale behind the new structural pattern matching feature. This document provides an in-depth look at why the feature was added and how it can be used effectively.

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

# Web development

## What is CGI. Pros, cons

CGI stands for Common Gateway Interface, which is a standard protocol used to communicate between a web server and a web application. It allows web servers to interact with external applications or scripts and generate dynamic content based on user requests.

The pros of using CGI are:

1. Platform independence: CGI is supported by almost all web servers and can be used on any platform that supports HTTP.

2. Flexibility: CGI allows for the use of any programming language to create web applications, which provides a lot of flexibility to developers.

3. Security: CGI provides a certain level of security by ensuring that the script runs with limited privileges, preventing it from accessing sensitive system resources.

4. The program does not store state, which is convenient for debugging.

The cons of using CGI are:

1. Performance: Since CGI scripts are executed every time a request is made, it can have a negative impact on the performance of the web server, especially when handling high volumes of requests.

2. Scalability: Due to the performance limitations of CGI, it may not be suitable for large-scale web applications that require high performance and scalability.

3. Maintenance: CGI scripts can be difficult to maintain, especially when dealing with complex applications that require multiple scripts to work together.

4. Transferring data via `stdout` is slower than Unix sockets.

## How to protect cookies from theft and forgery

Cookies can be protected from theft and forgery in several ways:

1. Use the `Secure` flag: Setting the `Secure` flag on a cookie ensures that the cookie can only be transmitted over an encrypted HTTPS connection. This helps to prevent eavesdropping and man-in-the-middle attacks.

2. Use the `HttpOnly` flag: Setting the `HttpOnly` flag on a cookie prevents client-side scripts from accessing the cookie through the document.cookie API. This helps to prevent cross-site scripting (XSS) attacks.

3. Use the `SameSite` attribute: Setting the `SameSite` attribute on a cookie restricts the cookie to first-party usage, meaning it can only be sent in requests originating from the same site. This helps to prevent cross-site request forgery (CSRF) attacks.

4. Set an expiration date: Setting an expiration date on a cookie ensures that it will only be valid for a limited period of time, reducing the risk of theft and forgery.

5. Use session cookies: Session cookies are stored in memory and are deleted when the user closes their browser. This can help to prevent long-term cookie theft.

6. Add a `User-Agent` header to the session key. Then if you steal the cookie and install it on another machine, the session key will be different.

7. Same as above, but add the user's `IP`.

8. Sign cookies with a secret key. Add a `sig` field that is equal to `HMAC-SHA1(cookie-body, secret_key)`. Check on the server that the signature matches.

It's important to note that while these measures can help to protect cookies from theft and forgery, they are not foolproof. It's also important to follow other security best practices, such as keeping software up-to-date, using strong passwords, and monitoring logs for suspicious activity.

## What is the difference between authentication and authorization

**Identification** (from the Latin identifico - to identify): assigning an identifier to subjects and objects and / or comparing an identifier with a list of assigned identifiers. For example, the representation of a person by name and patronymic is identification.

**Authentication** (from Greek: αυθεντικός ; real or authentic): verification of the correspondence of the subject and the person he is trying to impersonate, using some unique information (fingerprints, iris color, voice, etc.), in the simplest case - using a login and password.

**Authorization** is a check and determination of the authority to perform certain actions (for example, read the /var/mail/eltsin file) in accordance with the previously performed authentication.

All three procedures are interconnected:

1. First determine the name (login or number) - identification
2. Then they check the password (key or fingerprint) - authentication
3. And at the end they provide access - authorization

## What is XSS. Examples. How to secure an app

XSS (Cross-Site Scripting) is a type of web security vulnerability that allows attackers to inject malicious scripts into web pages viewed by other users. These scripts can steal sensitive information such as login credentials, session tokens, and personal data, or even modify the content of the page in ways that are harmful to the user.

There are three types of XSS attacks:

1. Stored XSS: Attacker injects malicious script into the server and is served to all users that visit the page
2. Reflected XSS: Attacker sends a link that contains malicious script, victim clicks on the link and the script is executed in their browser
3. DOM-Based XSS: Malicious code is executed as a result of manipulating the DOM of the web page

To secure an app from XSS attacks, you can take the following measures:

1. Input validation and sanitization: All user input should be validated on both the client and server side to ensure that only expected values are received. Additionally, any input that is displayed on the page should be sanitized to remove any potentially harmful content.

2. Use a Content Security Policy (CSP): This is an HTTP header that specifies which sources of content are allowed to be loaded by the browser. It can prevent scripts from running from untrusted sources.

3. Use HTTP-only cookies: Cookies that are marked as HTTP-only cannot be accessed by client-side scripts, which can help prevent attacks that rely on stealing session tokens.

4. Escape special characters: Special characters such as <, >, and & should be properly escaped in order to prevent them from being interpreted as HTML or JavaScript.

5. Keep software up-to-date: Make sure that you are using the latest version of your web server software and all the libraries and frameworks your application depends on. Security vulnerabilities can be found in outdated software.

By following these best practices, you can help protect your web application from XSS attacks.

XSS stands for Cross Site Requests. The affected page forces the user to make a request to another page, or to run unwanted js code.

For example, a user posted a comment that contained the code:

```html
<script>
  alert("foo");
</script>
```

The site engine does not filter comment text, so the `<script>` tag becomes part of the page and is executed by the browser. Anyone who visits a page with a dangerous comment will see a pop-up window with the test `foo`.

Another example. The search page accepts the search term `q`. In the title, the phrase “Search result for the query” + parameter text. If the parameter is not escaped, `/search?q=<script>alert('foo');</script>` will produce the same result.

Knowing that the page is executing js code, a hacker can load contextual advertising, banners on the page, force browsers to go to any page, and steal cookies.

The vulnerability is eliminated by escaping unsafe characters, cleaning (sanitizing) HTML tags.

## REST & SOAP

### What is REST

- [REST Principles and Architectural Constraints](https://restfulapi.net/rest-architectural-constraints/)

REST (Representational state transfer) is an agreement on how to build services. REST is often referred to as the so-called HTTP REST API. As a rule, this is a web application with a set of urls - endpoints. Urls accept and return data in JSON format. The operation type is set by the HTTP request method, for example:

- `GET` - get an object or a list of objects
- `POST` - create an object
- `PUT` - update an existing object
- `PATCH` - partially update an existing object
- `DELETE` - delete an object
- `HEAD` - get object metadata

The REST architecture actively uses the capabilities of the HTTP protocol to avoid the so-called. "bicycles" - own solutions. For example, caching parameters are passed by standard headers `Cache`, `If-Modified-Since`, `ETag`. Authorization - header `Authentication`.

REST is an architectural style for designing loosely coupled HTTP applications, which is often used when developing web services. REST doesn't dictate how it should be implemented at the low level, it just provides high level guidelines and leaves you free to implement your own implementation.

For web services built with REST in mind (that is, not violating the restrictions imposed by it), the term "RESTful" is used.

Unlike web services (web services) based on SOAP, there is no "official" standard for RESTful web API. The point is that REST is an architectural style while SOAP is a protocol.

REST defines 6 architectural constraints that will allow you to create a true RESTful API:

1. Interface uniformity
2. Client-server
3. Lack of state
4. Caching
5. Layers
6. Code on demand (optional limitation)

**Uniform interface**
You must come up with an API interface for system resources that is available to users of the system and follow it at all costs. A resource in the system should have only one logical URI, which should provide a way to get related or additional data. It is always better to associate (synonymize) a resource with a web page.

Any resource should not be too large and contain everything and everything in its representation. When appropriate, the resource should contain links (HATEOAS: Hypermedia as the Engine of Application State) pointing to relative URIs to retrieve related information.

Also, resource representations in the system must follow certain guidelines, such as naming conventions, link formats, or data format (xml or/and json).

> Once a developer is familiar with one of your APIs, they can follow a similar approach for other APIs.

**Client-Server**
Essentially, this means that the client application and the server application MUST be able to develop separately without any dependency on each other. The client only needs to know the URI of the resource and nothing else. This is a normal practice in web development today, so nothing special is required on your part. Be more simple.

> Servers and clients can also be replaced and developed independently as long as the interface between them does not change.

**No state**
Roy Fielding took inspiration from HTTP and this is reflected in this limitation. Make all client-server interaction stateless. The server will not store information about the client's latest HTTP requests. It will treat each request as a new one. No session, no history.

If the client application is to be a stateful application for the end user, where the user logs in once and then performs other authorized operations, then each request from the client must contain all the information necessary to service the request, including authentication and authorization details.

> Client context should not be stored on the server between requests. The client is responsible for managing the state of the application.

**Caching**
In today's world, data and response caching is paramount wherever applicable/possible. Caching improves performance on the client side and increases the scalability for the server as the load is reduced.

In REST, caching must be applied to resources when applicable, and then those resources MUST be declared cacheable. Caching can be implemented on the server or client side.

> Well-tuned caching partially or completely eliminates some client-server interactions, further improving scalability and performance.

**Layers**
REST allows you to use a layered system architecture where you deploy APIs on server A, store data on server B, and authenticate requests against server C, for example. intermediary.

**Code on demand (optional limitation)**
This is an optional restriction. Most of the time, you will be sending static representations of resources in the form of XML or JSON. But when you need to, you can return executable code to support part of your application, for example, clients can call your API to get the rendering code for a user interface widget. It is allowed

All of the above restrictions help you create a truly RESTful API and you should follow them. However, sometimes you may encounter a violation of one or two restrictions. Don't worry, you're still building RESTful APIs, but not "true RESTful".

### What is SOAP

SOAP (Simple Object Access Protocol) is a messaging protocol used for exchanging structured information between distributed applications over the internet. It relies on XML as its message format and typically uses HTTP or HTTPS as its transport protocol.

SOAP was designed to facilitate communication between applications running on different platforms and programming languages. It defines a set of rules for exchanging messages, which includes a message envelope, a set of encoding rules, and a convention for representing remote procedure calls and responses.

SOAP messages typically consist of a header and a body, where the header contains metadata about the message and the body contains the actual data being transmitted. The header can include information such as authentication details, routing information, and other optional parameters.

One of the primary advantages of SOAP is that it supports a wide range of platforms and programming languages, making it ideal for distributed systems. However, it is often criticized for being too complex and difficult to use compared to more lightweight protocols such as REST.

Initially, SOAP was intended mainly for implementing remote procedure call (RPC). Now the protocol is used to exchange arbitrary messages in XML format, and not just to call procedures. The official specification of the latest version 1.2 of the protocol does not decipher the name SOAP in any way. SOAP is an extension of the XML-RPC protocol.
SOAP can be used with any application layer protocol: SMTP, FTP, HTTP, HTTPS, etc. However, its interaction with each of these protocols

### What is the difference between REST and SOAP web services

The main difference between REST and SOAP web services is in their architectural styles, message formats, and communication protocols.

REST (Representational State Transfer) is an architectural style for designing distributed systems that allows clients to interact with web services using HTTP methods such as GET, POST, PUT, and DELETE. REST is based on the principle of using a unique URL (Uniform Resource Locator) to represent each resource, and each URL responds to a particular action. RESTful web services use simple text formats such as XML, JSON or YAML for message exchange, and they do not require the use of a separate messaging protocol.

SOAP (Simple Object Access Protocol) is a messaging protocol that defines how XML messages can be exchanged between two different endpoints. SOAP uses the XML format for messages, and it requires a separate messaging protocol such as HTTP, TCP, or SMTP to transport the messages. SOAP web services use WSDL (Web Services Description Language) for defining the interface of the web service.

- REST supports various formats: text, JSON, XML; SOAP - XML only,
- REST works only over HTTP(S), while SOAP can work with various protocols,
- REST can work with resources. Each URL is a representation of some resource. SOAP works with operations that implement some kind of business logic using several interfaces,
- Read-based SOAP cannot be cached, while REST can be cached in this case,
- SOAP supports SSL and WS-security while REST only supports SSL, SOAP supports ACID (Atomicity, Consistency, Isolation, Durability). REST supports transactions, but none of the ACIDs are compatible with a two-phase commit.

In summary, REST is a simpler and more lightweight protocol compared to SOAP. It uses HTTP methods to access and manipulate resources, and it uses simple text formats for message exchange. SOAP, on the other hand, is a more complex protocol that uses a separate messaging protocol and XML for message exchange.

### Can we send SOAP messages with an attachment

Yes, it is possible to send SOAP messages with attachments. The SOAP with Attachments specification (SWA) defines a mechanism for attaching binary data, such as images or documents, to SOAP messages. This is accomplished by encoding the binary data as a MIME attachment and including it in the SOAP message using the "cid" URI scheme. The receiving SOAP node can then extract the attachment and process it as needed.

You can send attachments in various formats: PDF, images, or other binary data. SOAP messages work in conjunction with the MIME extension, which provides for multipart/related.

### How would you decide which REST or SOAP web service to use

Choosing between REST and SOAP web services depends on the specific requirements and constraints of the project. Here are some factors to consider when deciding which type of web service to use:

Complexity: SOAP is typically more complex than REST, due to its adherence to a strict messaging protocol and the use of XML for message exchange. REST, on the other hand, is simpler and more flexible, and allows for easier integration with other systems.

Security: SOAP includes built-in security features, such as encryption and digital signatures, while REST relies on HTTPS for security. If you need strong security features, SOAP may be the better choice.

Performance: REST is generally faster and more lightweight than SOAP, due to its simpler messaging format and lack of additional protocol layers. SOAP, however, is more reliable and offers more advanced error handling.

Interoperability: SOAP is designed to work across different platforms and programming languages, while REST is more limited in this regard. If you need to integrate with a variety of systems, SOAP may be the better choice.

API Design: REST APIs follow a resource-oriented design, while SOAP APIs are based on a service-oriented architecture. The choice between the two depends on the nature of the application and the type of data being exchanged.

Ultimately, the choice between REST and SOAP web services depends on the specific needs of the project, as well as the resources and expertise available to the development team.

REST vs. SOAP can be rephrased as "Simplicity vs. Standard". In the case of REST (simplicity), you will have speed, extensibility and support for many formats. In the case of SOAP, you will have more options for security (WS-security) and transactional security (ACID).

## What methods for monitoring web applications in production have you used or know

- [51 tools for APM and server monitoring(rus)](https://habr.com/ru/company/pc-administrator/blog/304356/)

There are various methods for monitoring web applications in production, including:

1. Log monitoring: Monitoring the application logs to track errors, performance issues, and security breaches.

2. Performance monitoring: Monitoring system metrics such as CPU usage, memory usage, network usage, and disk I/O to ensure the application is performing well.

3. User monitoring: Tracking user behavior and usage patterns to understand how the application is being used and identify areas for improvement.

4. Synthetic monitoring: Simulating user interactions with the application to monitor its availability and performance.

5. Real user monitoring (RUM): Collecting data from actual user interactions with the application to track performance and identify issues.

6. Error monitoring: Tracking errors and exceptions in the application code to identify bugs and performance issues.

7. Security monitoring: Monitoring the application for security threats and vulnerabilities, such as unauthorized access attempts or malicious activity.

The choice of monitoring method will depend on the specific needs of the application and the resources available for monitoring. It is often best to use a combination of methods to get a comprehensive view of the application's performance and health in production.

# HTTP

## How the HTTP protocol works

HTTP (Hypertext Transfer Protocol) is an application-layer protocol used to transmit data over the internet. It is the foundation of the World Wide Web and is used by web browsers and servers to communicate with each other. The HTTP protocol is based on a client-server architecture, where the client sends a request to the server and the server responds with the requested data.

When a user types a URL into their browser, a request is sent to the server hosting the website. This request contains a request method, which can be one of the following:

- GET: Retrieves information from the server.
- POST: Sends information to the server for processing.
- PUT: Updates an existing resource on the server.
- DELETE: Deletes a resource from the server.

After the server receives the request, it sends a response back to the client. This response contains the requested data and also includes a status code that indicates whether the request was successful or not. Some of the most common status codes include:

- 200 OK: The request was successful.
- 404 Not Found: The requested resource was not found on the server.
- 500 Internal Server Error: An error occurred on the server while processing the request.

HTTP also supports other features such as caching, authentication, and encryption, which are used to improve the performance and security of web applications.

HTTP is a text protocol that runs on top of TCP/IP. HTTP consists of a request and a response. Their structures are similar: start line, headers, response body.

The start query string consists of the method, path, and protocol version:

```plaintext
GET /index.html HTTP/1.1
```

The start line of the response consists of the protocol version, the response code, and the textual transcript of the response.

```plaintext
HTTP/1.1 200 OK
```

Headers are a set of key-value pairs, eg `User-Agent`, `Content-Type`. The headers contain request metadata: user language, authorization, redirection. The `Host` header must always be present in the request.

The response body can be empty, or it can transfer pairs of variables, files, binary data. The body is separated from the headers by a blank line.

## Write a raw request to google home page

An example of a raw request to the Google homepage using the HTTP/1.1 protocol:

```plaintext
GET / HTTP/1.1
Host: www.google.com
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:92.0) Gecko/20100101 Firefox/92.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,*/*;q=0.8
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Upgrade-Insecure-Requests: 1
```

This specifies the `GET` method to get the main page, as well as the request headers such as `User-Agent`, `Accept`, `Accept-Language`, and so on. In response to this request, the server will return the corresponding page with HTML code.

## How to tell the client if the request was successful or not

Check response status. Answers are divided by senior category. We have five groups with the following semantics:

- `1xx`: rarely used. This group has only one status `100 Continue`.
- `2xx`: request was successful (data received or created)
- `3xx`: redirect to another resource
- `4xx`: error caused by the user (no such page, no access rights)
- `5xx`: error caused by the server (error in code, network, configuration)

## What needs to be sent to the browser to redirect to another page

To redirect a user to another page, the server needs to send an HTTP response with a status code of 3xx(`301` or `302`), indicating a redirection. Specifically, the server needs to include a `Location` header in the response, which specifies the URL to redirect to. Here is an example of what an HTTP response to redirect to `https://example.com` might look like:

```plaintext
HTTP/1.1 302 Found
Location: https://example.com
```

When the browser receives this response, it will automatically send a new request to the URL specified in the `Location` header. This will cause the browser to navigate to the new page.

You can place `HTML` in the body of the response with a link to the new resource. Then users of older browsers will be able to navigate manually.

## How to manage caching in HTTP

HTTP caching is an important feature that allows clients and servers to efficiently store and retrieve resources, such as web pages, images, and other files. There are several ways to manage caching in HTTP:

1. `Cache-Control` header: This header is used to specify caching directives that control how and for how long the content should be cached. The `Cache-Control` header can include several directives, such as `max-age`, `no-cache`, `no-store`, `must-revalidate`, and `private`.

2. `ETag` header: This header is used to identify a specific version of a resource. The server generates an `ETag` for each version of a resource, and the client includes the `ETag` in subsequent requests to indicate which version it has cached.

3. `Last-Modified` header: This header is used to indicate the last time a resource was modified. The server includes this header in its response, and the client includes the value of this header in subsequent requests to check if the resource has been modified since the last time it was cached.

4. `Conditional` requests: HTTP also supports conditional requests, which allow the client to check if a resource has been modified since the last time it was cached without actually downloading the entire resource. This can be achieved using the If-Modified-Since or If-None-Match headers.

By properly managing caching in HTTP, we can improve the performance and reduce the load on both the server and the network.

## How files are cached at the protocol level

When `Nginx` serves up a static file, it adds an `Etag` header - the `MD5` hash of the file. The client remembers this hash. The next time the file is requested, the client sends the hash. The server checks the client's hash for this file. If the hash does not match (the file has been updated), the server responds with a `200` code and uploads the current file with the new hash. If the hashes are equal, the server responds with a `304 Not Modified` code with an empty body. In this case, the browser substitutes a local copy of the file.

## What is HTTP

- [In plain language about HTTP(rus)](https://habr.com/en/post/215117/)
- [HTTP Protocol Overview - HTTP(rus)](https://developer.mozilla.org/ru/docs/Web/HTTP/Overview)

HTTP is a widely used data transfer protocol, originally intended for the transfer of hypertext documents (that is, documents that may contain links that allow you to navigate to other documents).

The abbreviation HTTP stands for HyperText Transfer Protocol. According to the OSI specification, HTTP is an application (upper, 7th) layer protocol. The current version of the protocol, HTTP 1.1, is described in the RFC 2616 specification.

The HTTP protocol assumes the use of a client-server data transfer structure. The client application forms a request and sends it to the server, after which the server software processes this request, generates a response and sends it back to the client. After that, the client application can continue to send other requests, which will be processed in the same way.

The task that is traditionally solved using the HTTP protocol is the exchange of data between a user application that accesses web resources (usually a web browser) and a web server. At the moment, it is thanks to the HTTP protocol that the work of the World Wide Web is ensured.

HTTP is also often used as the communication protocol for other application layer protocols such as SOAP, XML-RPC, and WebDAV. In such a case, the HTTP protocol is said to be used as a "transport".

## What is the difference between HTTP and HTTPS

HTTP (HyperText Transfer Protocol) and HTTPS (HyperText Transfer Protocol Secure) are both protocols used for transmitting data over the internet, but there are some significant differences between the two.

1. Security: HTTPS is a more secure version of HTTP as it uses SSL/TLS (Secure Sockets Layer/Transport Layer Security) encryption to encrypt all data between the web server and the client browser. This provides end-to-end encryption, ensuring that data transmitted between the server and client is secure and cannot be intercepted or tampered with.

2. Port: HTTP uses port 80, while HTTPS uses port 443. This is why a URL for an HTTPS website will have "https://" and a URL for an HTTP website will have "http://".

3. Authentication: HTTPS also provides authentication, meaning that the client can verify that they are communicating with the correct server. This is done through SSL/TLS certificates, which are issued by trusted Certificate Authorities.

4. Speed: HTTPS can be slower than HTTP because the encryption and decryption of data requires additional processing power and time. However, advancements in SSL/TLS technology have reduced the performance gap between HTTP and HTTPS.

5. SEO: HTTPS is becoming increasingly important for search engine optimization (SEO), as search engines like Google give priority to secure websites in search results. This means that websites using HTTPS are more likely to rank higher in search results.

In summary, HTTPS is a more secure and reliable version of HTTP, providing end-to-end encryption, authentication, and better SEO. However, it can be slower than HTTP due to the additional processing required for encryption and decryption of data.

# General

## OOP

### Encapsulation

_Encapsulation_ is a language mechanism that allows you to combine data and methods that work with this data into a single object and hide implementation details from the user.

The true purpose of encapsulation is to collect in one place the knowledge related to the device of a certain entity, the rules for handling and operations with it. Encapsulation appeared much earlier than is commonly thought. Modules in C programs are encapsulation. Assembly subroutines are encapsulation. The opposite of encapsulation is spreading knowledge about how something works throughout the program.

_Example_: Working with monetary values. It's no secret that in many e-commerce systems monetary values are implemented as floating point numbers. I think all of us are aware that simply adding two "integer" numbers represented as floating point variables can result in a "slightly non-integer" number. Therefore, with such an implementation, it is necessary to insert a call to the rounding function here and there. This is the smearing of knowledge about the structure of the entity throughout the program. Encapsulation in this case is to collect (hide) in one place the knowledge that money is represented as a floating point value, and that it constantly has to be rounded off during the most innocent operations. Hide so that when using the “money” entity, rounding is not even mentioned. With encapsulation, there will be no problem to change the implementation of "money" from a floating point number to a fixed point number.

We can say that hiding is one of the tasks of encapsulation. But data hiding is not encapsulation in and of itself. It would also be wrong to say that encapsulation is hiding data. Because its tasks go beyond concealment.

If we say that a given method encapsulates a certain algorithm, then we mean that a certain calculation takes place in this method, the details of which we do not need to know, but the results of which we can trust and use. We can also say that the object in which the data is encapsulated can hide it - that is, protect it from unauthorized access. Thus, it is still necessary and important to distinguish between the concept of encapsulation and data hiding, and it is important to see the line between them. Encapsulation is a technology for combining the actual data and methods for processing it. As a result, both the data itself and the algorithms for working with them become logically inseparable. A typical example from C++ is the fields and methods of a class.

So, if encapsulation provides a kind of integrity to the object, then hiding - hides details about the process. To "customize" access to data in the class and to the class directly, so-called access modifiers are used. So the use of these access modifiers is hiding.

In python:

Encapsulation in Python refers to the concept of wrapping data and methods into a single unit, such as a class. This is done to control the access to the data and methods, and to prevent them from being accessed or modified accidentally from outside the class.

In Python, encapsulation can be achieved by using access modifiers such as public, protected, and private. By default, all attributes and methods in a class are public, which means they can be accessed from anywhere in the program. However, you can use access modifiers to specify that certain attributes or methods should only be accessed from within the class or its subclasses.

The private access modifier is achieved by prefixing the attribute or method name with two underscores (e.g. \_\_attribute). This makes it so that the attribute or method can only be accessed from within the class itself, and not from outside the class. Protected access is achieved by prefixing the attribute or method name with a single underscore (e.g. \_attribute), which indicates that it should only be accessed from within the class and its subclasses.

### Inheritance

_Inheritance_ is a language mechanism that allows you to describe a new class based on an existing one. In "true" OOP, it is necessary to ensure the implementation of polymorphism as an independent unit, it is not necessary and even harmful, because it is the cause of strong coupling. It is better to prefer composition to inheritance.
In Python, inheritance is a mechanism that allows you to define a new class based on an existing class, which is called the parent or base class. The new class, called the child or derived class, inherits all the attributes and methods of the parent class and can also have additional attributes and methods of its own.

To create a child class in Python, you use the keyword `class` followed by the name of the child class and the name of the parent class in parentheses. For example, if you have a parent class called `Animal`, you can create a child class called `Dog` as follows:

```python
class Animal:
    def __init__(self, name):
        self.name = name

class Dog(Animal):
    def bark(self):
        print("Woof!")
```

In this example, the `Dog` class is defined as a child of the Animal class using the syntax `class Dog(Animal):`. This means that the `Dog` class inherits all the attributes and methods of the `Animal` class, including the `__init__` method which sets the name attribute.

The `Dog` class also has an additional method called `bark` that is not present in the `Animal` class. This method can be used to make a dog `bark` by calling the bark method on an instance of the `Dog` class.

When you create an instance of the `Dog` class, you can set the name attribute by calling the `__init__` method of the parent class, like this:

```python
my_dog = Dog("Fido")
```

In this example, the `my_dog` object is created as an instance of the `Dog` class with the name "Fido". Because the `Dog` class inherits the `__init__` method from the `Animal` class, the `name` attribute is set to "Fido" automatically.

In summary, inheritance in Python allows you to create new classes that are based on existing classes, and inherit all their attributes and methods. This can help you write more efficient and reusable code by avoiding duplication and promoting code reuse.

### Polymorphism

Polymorphism in Python refers to the ability of objects of different classes to be used interchangeably, based on the fact that they share a common interface or base class. This allows you to write more flexible and reusable code, since you can write code that works with objects of a certain type, and then use it with objects of different types that share the same interface or base class.

There are two main types of polymorphism in Python: runtime polymorphism and compile-time polymorphism.

Runtime polymorphism, also known as dynamic polymorphism, is achieved through method overriding. Method overriding allows a subclass to provide its own implementation of a method that is already defined in its parent class. When a method is called on an object of the subclass, the subclass's implementation of the method is executed instead of the parent class's implementation.

For example:

```python
class Animal:
    def make_sound(self):
        print("The animal makes a sound")

class Dog(Animal):
    def make_sound(self):
        print("The dog barks")

class Cat(Animal):
    def make_sound(self):
        print("The cat meows")

# Create objects
animal = Animal()
dog = Dog()
cat = Cat()

# Call the make_sound method on each object
animal.make_sound()  # The animal makes a sound
dog.make_sound()     # The dog barks
cat.make_sound()     # The cat meows
```

In this example, the `Animal` class defines a `make_sound` method that prints "The animal makes a sound". The `Dog` and `Cat` classes inherit from the `Animal` class and override the `make_sound` method with their own implementations. When the make_sound method is called on an object of the `Dog` or `Cat` class, their respective implementations are executed instead of the implementation in the parent `Animal` class.

Compile-time polymorphism, also known as static polymorphism, is achieved through method overloading. Method overloading allows a class to define multiple methods with the same name, but with different parameter types. When a method is called, the appropriate version of the method is selected based on the types of the arguments that are passed in.

However, it's worth noting that Python does not support method overloading in the same way as some other languages like Java and C++. In Python, you can define multiple methods with the same name, but the method that gets called is determined by the number and types of the arguments that are passed in, rather than by the parameter types.

_Polymorphism_ has several forms:

- Special (Ad-Hoc) (in some languages it is represented by the method overloading mechanism)
- Parametric (in some languages represented by generics)
- Subtype polymorphism (achieved using inheritance and upcast mechanisms). When people talk about polymorphism, they most often mean it.

_Polymorphism_ - the ability for similar data types that are explicitly defined by the inheritance hierarchy to have different implementations (using method overriding and upcasting)

Also in programming languages and type theory, polymorphism is the ability of a function to handle data of different types.

### Abstraction

_Abstraction_ says that we should highlight the important characteristics of the object. The idea is that we can determine the minimum necessary set of these characteristics in order to be able to solve the problem.
Often confused with encapsulation, because both indirectly affect the formation of a type's public interface.
A rather trivial paradigm and therefore often not stated as such.

Abstraction in Python refers to the process of hiding the implementation details of a class or function and only exposing a simplified interface to the user. The purpose of abstraction is to make it easier for the user to work with the code by reducing complexity and providing a high-level view of the system.

In Python, abstraction can be achieved through the use of abstract classes and interfaces. An abstract class is a class that cannot be instantiated, but can be subclassed to provide concrete implementations. An interface is a collection of method signatures that a class can implement to provide a specific functionality.

The `abc` module in Python provides tools for working with abstract classes and interfaces. To create an abstract class, you can use the `abc.ABC` class as a base class, and then define abstract methods using the `@abstractmethod` decorator. Abstract methods are methods that are declared in the abstract class, but have no implementation. Instead, the implementation is provided by the concrete subclasses.

For example:

```python
import abc

class Animal(metaclass=abc.ABCMeta):
    @abc.abstractmethod
    def make_sound(self):
        pass

class Dog(Animal):
    def make_sound(self):
        print("The dog barks")

class Cat(Animal):
    def make_sound(self):
        print("The cat meows")

# Create objects
dog = Dog()
cat = Cat()

# Call the make_sound method on each object
dog.make_sound()  # The dog barks
cat.make_sound()  # The cat meows
```

In this example, the `Animal` class is defined as an abstract class with an abstract method called `make_sound`. The `Dog` and `Cat` classes inherit from the Animal class and provide their own implementations of the `make_sound` method. When the `make_sound` method is called on an object of the `Dog` or `Cat` class, their respective implementations are executed.

Abstraction can also be achieved through the use of interfaces, which are similar to abstract classes, but do not provide any implementation. Instead, they define a set of method signatures that a class must implement to provide a specific functionality. However, Python does not have built-in support for interfaces, so they are typically implemented using abstract classes or conventions.

## What programming principles do you know

### KISS

The KISS principle is a design principle in software engineering that stands for "Keep It Simple, Stupid." The principle states that systems should be kept as simple as possible, and unnecessary complexity should be avoided. The KISS principle is a common sense approach that emphasizes simplicity over complexity.

In programming, the KISS principle suggests that code should be written in a clear and concise manner, with a focus on readability and maintainability. This means avoiding unnecessary features, functions, and classes, and using simple and straightforward logic wherever possible. Code that follows the KISS principle is usually easier to understand, debug, and modify, and is less likely to contain bugs.

In Python, the KISS principle is implemented through the use of simple and intuitive syntax and a rich standard library that provides a wide range of functionality out of the box. Python's syntax is designed to be easy to read and write, with a focus on minimizing unnecessary syntax and boilerplate code.

Some specific examples of how the KISS principle is implemented in Python include:

1. Concise syntax for common operations: Python provides concise syntax for common operations, such as list comprehension, which allows for easy creation of lists based on existing lists.

2. Use of built-in functions: Python provides a large number of built-in functions that perform common operations, such as sorting and filtering, without the need for custom code.

3. Clear and concise documentation: Python's documentation is written in a clear and concise manner, making it easy for developers to quickly find the information they need.

4. Emphasis on readability: Python emphasizes readability by enforcing indentation and whitespace rules that make code easier to read and understand.

Overall, the KISS principle is an important design principle in software engineering that emphasizes simplicity and clarity over complexity. In Python, the KISS principle is implemented through the use of intuitive syntax, a rich standard library, and a focus on readability and maintainability.

Examples of violating this principle include writing a separate function just to perform the addition operation, or using the bitwise operator (right shift >> 1) to divide integers by 2. The latter is certainly more efficient than the usual (/2), but this greatly reduces the clarity of the code. Using this approach, you are doing clever coding (“abstruse coding”) and over-optimization (over-optimization). Both are not good for the health of your code in the long run.

### DRY

DRY stands for "Don't Repeat Yourself." The DRY concept is a principle of software engineering that states that code should be written in a way that avoids repetition and promotes reuse. The idea is to eliminate duplicate code and create a single source of truth for each piece of information or logic.

In Python, the DRY concept is implemented in several ways. Here are some examples:

1. Functions: Functions in Python are a key way to implement DRY. Instead of writing the same code multiple times, you can define a function that encapsulates the logic and call it whenever you need it.

2. Modules: Python modules are another way to implement DRY. Modules are files that contain functions, classes, and other objects that can be imported and reused in other programs.

3. Object-Oriented Programming: Object-oriented programming (OOP) is another approach that can help implement DRY. By defining classes and objects, you can encapsulate logic and data in a reusable way.

4. List Comprehensions: Python's list comprehensions provide a concise way to create new lists based on existing lists. By using list comprehensions, you can avoid writing repetitive code to create new lists.

5. Template Strings: Python's template strings provide a way to reuse common text strings with placeholders for dynamic content. By using templates, you can avoid duplicating the same text in multiple places.

Overall, the DRY concept is an important principle of software engineering that can help improve code quality and maintainability. In Python, the DRY concept is implemented through the use of functions, modules, object-oriented programming, list comprehensions, and template strings, among other techniques.

### YAGNI

The YAGNI principle is a design principle in software engineering that stands for "You Ain't Gonna Need It." The principle states that developers should avoid implementing functionality until it is actually needed. The idea is to avoid spending time and resources on features that may not be useful or necessary.

In programming, the YAGNI principle suggests that code should be written with a focus on solving the immediate problem at hand, without worrying about potential future requirements. This means avoiding premature optimization, over-engineering, and unnecessary complexity.

In Python, the YAGNI principle is implemented through a focus on simplicity and minimalism. Python's design philosophy emphasizes the importance of writing code that is easy to read, write, and maintain. The Python community values pragmatic solutions that get the job done without unnecessary complexity.

Here are some specific examples of how the YAGNI principle is implemented in Python:

1. Simple and concise syntax: Python's syntax is designed to be simple and concise, making it easy to read and write code. This simplicity helps ensure that code is focused on the task at hand and doesn't include unnecessary complexity.

2. Minimalist approach to modules and packages: Python's module and package system is designed to be minimalist and focused on solving specific problems. This helps ensure that modules and packages are focused on specific tasks and don't include unnecessary functionality.

3. Iterative development: Python's emphasis on iterative development and rapid prototyping encourages developers to focus on solving immediate problems rather than worrying about potential future requirements.

4. TDD (Test Driven Development): Python's support for TDD encourages developers to write tests that focus on immediate requirements, which helps ensure that code is focused on solving the current problem and avoids over-engineering for future requirements.

Overall, the YAGNI principle is an important design principle in software engineering that emphasizes the importance of focusing on solving immediate problems without worrying about potential future requirements. In Python, the YAGNI principle is implemented through a focus on simplicity and minimalism, iterative development, and a pragmatic approach to solving problems.

### SLAP

The Single Level of Abstraction Principle (SLAP) is a programming principle that suggests that a function or a module should have only one level of abstraction, meaning that it should either perform low-level operations or high-level operations, but not both. This principle helps to ensure that code is easier to read, understand, and maintain, by keeping code focused on one level of abstraction.

In Python, the SLAP principle can be implemented by breaking up complex functions into smaller, more focused functions that perform specific tasks at a single level of abstraction. By doing so, each function becomes more reusable, testable, and easier to understand. For example, a function that performs both high-level business logic and low-level file I/O can be refactored into two separate functions: one that handles the business logic and another that handles the file I/O at a lower level of abstraction.

Here is an example of how SLAP can be implemented in Python:

```python
def read_data(file_path):
    with open(file_path, 'r') as file:
        data = file.read()
    return data

def process_data(data):
    # process data here
    return processed_data

def save_data(processed_data, file_path):
    with open(file_path, 'w') as file:
        file.write(processed_data)

def main():
    data = read_data('input.txt')
    processed_data = process_data(data)
    save_data(processed_data, 'output.txt')
```

In this example, we have three separate functions: `read_data`, `process_data`, and `save_data`, each of which performs a single level of abstraction. The `main` function then orchestrates these functions to read data from a file, process it, and save it to another file. By separating the concerns in this way, the code is easier to understand, test, and modify, following the SLAP principle.

### SOLID

_SOLID_ is an acronym for 5 principles described by Robert Martin that contribute to good object-oriented code (and more).

#### S

**S**: Single Responsibility Principle.

> Each class should only do one task

The "S" in SOLID stands for the Single Responsibility Principle (SRP). The SRP is a design principle in software engineering that states that every module or class should have only one responsibility or reason to change. The idea behind the SRP is to create software components that are focused, modular, and easy to understand and maintain.

In practice, the SRP can be implemented by breaking down large classes or modules into smaller, more focused components. Each component should have a clear and well-defined responsibility or functionality, and should not be responsible for multiple unrelated tasks. By dividing the functionality of a system into smaller, more focused components, developers can improve the maintainability, testability, and flexibility of the software.

Here are some key principles of the SRP:

1. High Cohesion: Each module or class should have a high degree of cohesion, meaning that all of its functions or methods are related to a single responsibility.

2. Low Coupling: Modules or classes should have low coupling, meaning that they are loosely connected and do not rely on each other's internal details.

3. Single Responsibility: Each module or class should have a single responsibility, meaning that it is responsible for one and only one aspect of the system's functionality.

4. Separation of Concerns: Related functionality should be grouped together in a separate module or class, rather than being spread across multiple components.

In Python, the SRP can be implemented through the use of classes and modules that have a clear and well-defined responsibility. Python's support for modules, classes, and functions makes it easy to create focused, modular components that adhere to the SRP. By following the SRP, Python developers can create software that is easier to understand, maintain, and test, and that can evolve more easily over time.

Here's an example of implementing the SRP in Python:

Let's say we have a class called `User`, which represents a user in a web application. The `User` class has methods for authentication, registration, and password reset.

However, this violates the SRP because the `User` class has multiple responsibilities, which makes it harder to maintain and test.

To adhere to the SRP, we can create separate classes for each responsibility:

```python
class Authenticator:
    def authenticate(self, username, password):
        # authenticate user

class Registration:
    def register(self, username, password, email):
        # register user

class PasswordReset:
    def reset_password(self, username, email):
        # reset user password
```

Now, each of these classes has a single responsibility and can be tested and maintained independently. The User class can then be refactored to use these new classes:

```python
class User:
    def __init__(self, username, password, email):
        self.username = username
        self.password = password
        self.email = email
        self.authenticator = Authenticator()
        self.registration = Registration()
        self.password_reset = PasswordReset()

    def authenticate(self):
        self.authenticator.authenticate(self.username, self.password)

    def register(self):
        self.registration.register(self.username, self.password, self.email)

    def reset_password(self):
        self.password_reset.reset_password(self.username, self.email)
```

By separating responsibilities into their own classes, the User class is now focused on managing user data, and each of the new classes is responsible for a single task. This makes the code easier to read, maintain, and test.

#### O

**O**: Open-Closed Principle.

> Programming entities (classes, modules, functions) should be open for extension, but not for modification.

The "O" in SOLID stands for the Open-Closed Principle (OCP). The OCP is a design principle in software engineering that states that software entities (such as classes, modules, and functions) should be open for extension but closed for modification. This means that once a software entity has been created, it should not be modified directly, but rather extended or overridden to add new functionality.

The idea behind the OCP is to create software that is flexible and easily extensible without requiring changes to the existing codebase. By following the OCP, developers can add new functionality to a system without breaking existing code or introducing new bugs.

In practice, the OCP can be implemented through the use of inheritance, abstraction, and polymorphism. By creating abstract base classes that define the behavior of a system, and allowing concrete implementations to override or extend that behavior, developers can create software that is both flexible and maintainable.

Here are some key principles of the OCP:

1. Abstraction: Software entities should be abstracted to the highest possible level, so that they can be easily extended without modifying the existing code.

2. Inheritance: New functionality should be added through the use of inheritance, rather than modifying existing code directly.

3. Polymorphism: Concrete implementations should be able to override or extend the behavior of abstract base classes, allowing for flexible and extensible software.

4. Interfaces: Software entities should expose interfaces rather than implementation details, allowing for easy substitution of components.

In Python, the OCP can be implemented through the use of abstract base classes, interfaces, and the duck typing philosophy. Python's support for inheritance, polymorphism, and dynamic typing makes it easy to create software that adheres to the OCP. By following the OCP, Python developers can create software that is both flexible and maintainable, and that can be easily extended to meet changing requirements.

Here's an example of implementing the OCP in Python:

Let's say we have a system that manages shapes, and we want to be able to calculate the area of various shapes. We start with a basic `Shape` class:

```python
class Shape:
    pass
```

We can then create subclasses for each type of shape we want to support, and define a method for calculating the area of each shape:

```python
class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.14 * (self.radius ** 2)

class Square(Shape):
    def __init__(self, side):
        self.side = side

    def area(self):
        return self.side ** 2
```

Now, let's say we want to add support for calculating the area of a new shape, a rectangle. Instead of modifying the existing code, we can create a new class that extends the `Shape` class and implements its own `area` method:

```python
class Rectangle(Shape):
    def __init__(self, width, height):
        self.width = width
        self.height = height

    def area(self):
        return self.width * self.height
```

We've extended the functionality of our system without modifying any of the existing code. This follows the Open-Closed Principle, and makes our code more flexible and easier to maintain.

#### L

**L**: Liskov Substitution Principle.

> Subclasses need to be able to serve as replacements for their superclasses.

The "L" in SOLID stands for the Liskov Substitution Principle (LSP). The LSP is a design principle in software engineering that states that if a program is using a base class, it should be able to use any of its derived classes without knowing it. In other words, objects of derived classes should be substitutable for objects of their base classes without affecting the correctness of the program.

The LSP is important because it ensures that code is both correct and maintainable. If a derived class is not a proper substitution for its base class, it can lead to bugs and errors in the program, and make it difficult to modify and extend the code.

To adhere to the LSP, the following conditions should be met:

1. The preconditions of a base class method cannot be strengthened in a derived class method.

2. The postconditions of a base class method cannot be weakened in a derived class method.

3. Invariants of the base class must be preserved in a derived class.

In practical terms, the LSP means that if you have a function or method that takes an object of a certain class as a parameter, it should be able to take any object of a subclass of that class as well, without breaking the functionality of the function.

In Python, the LSP can be implemented through the use of inheritance and polymorphism. By creating a base class that defines the behavior of a system, and allowing derived classes to override or extend that behavior, developers can create software that is both flexible and maintainable. However, it's important to ensure that derived classes do not violate the contract established by the base class. This means that they should maintain the same preconditions, postconditions, and invariants as the base class, and not introduce any new assumptions or behaviors that could break the program.

Here's an example of implementing the LSP in Python:

Let's say we have a `Rectangle` class with a `set_width` and `set_height` method:

```python
class Rectangle:
    def __init__(self, width, height):
        self.width = width
        self.height = height

    def set_width(self, width):
        self.width = width

    def set_height(self, height):
        self.height = height
```

We can create a subclass of `Rectangle` called `Square`:

```python
class Square(Rectangle):
    def __init__(self, side):
        self.width = side
        self.height = side

    def set_width(self, width):
        self.width = width
        self.height = width

    def set_height(self, height):
        self.width = height
        self.height = height
```

Now, let's say we create a `resize` function that takes a `Rectangle` object and changes its dimensions:

```python
def resize(rectangle, width, height):
    rectangle.set_width(width)
    rectangle.set_height(height)
```

If we pass in a `Rectangle` object to `resize`, it will behave as expected:

```python
rectangle = Rectangle(2, 3)
resize(rectangle, 4, 5)
print(rectangle.width)  # Output: 4
print(rectangle.height)  # Output: 5
```

However, if we pass in a `Square` object, the behavior is unexpected:

```python
square = Square(2)
resize(square, 4, 5)
print(square.width)  # Output: 5
print(square.height)  # Output: 5
```

This violates the Liskov Substitution Principle, as the behavior of the `Square` object is unexpected when passed to the `resize` function. To fix this, we can change the implementation of `Square` to make it behave like a rectangle:

```python
class Square(Rectangle):
    def __init__(self, side):
        self.side = side
        super().__init__(side, side)

    def set_width(self, width):
        self.side = width
        super().set_width(width)
        super().set_height(width)

    def set_height(self, height):
        self.side = height
        super().set_width(height)
        super().set_height(height)
```

Now, the behavior of `Square` is consistent with the behavior of `Rectangle`, and we can pass `Square` objects to the resize function without unexpected behavior:

```python
square = Square(2)
resize(square, 4, 5)
print(square.width)  # Output: 4
print(square.height)  # Output: 4
```

By following the Liskov Substitution Principle, we've created a more robust and maintainable system.

#### I

**I**: Interface Segregation Principle.

> Create highly specialized interfaces designed for a specific client. Clients should not depend on interfaces they do not use.

The "I" in SOLID stands for the Interface Segregation Principle (ISP). The ISP is a design principle in software engineering that states that clients should not be forced to depend on interfaces that they do not use. In other words, it's better to have many small, specific interfaces than one large, general-purpose interface.

The ISP is important because it promotes modularity and flexibility in code. When interfaces are small and specific, it makes it easier to change and maintain the code, and reduces the risk of introducing bugs or errors. It also makes it easier to reuse code across different projects or systems.

To adhere to the ISP, the following guidelines should be followed:

1. Interfaces should be specific to the needs of clients.

2. Clients should not be forced to implement methods they don't need.

3. Interfaces should be cohesive and have a clear purpose.

4. Interfaces should be stable and not change frequently.

In practical terms, the ISP means that if you have a class that implements an interface, it should only include methods that are relevant to its purpose. This ensures that clients that use the class only depend on the methods they need, and don't have to worry about the implementation details of methods they don't use.

In Python, the ISP can be implemented through the use of abstract base classes (ABCs) and interfaces. By defining specific interfaces for different types of objects and operations, and using ABCs to enforce their implementation, developers can create code that is both flexible and maintainable. However, it's important to ensure that interfaces are stable and cohesive, and not changed frequently, as this can introduce additional complexity and risk into the system.

Here's an example of how the Interface Segregation Principle can be applied in Python:

Suppose we have an interface called `Bird`, which has methods for both flying and swimming:

```python
class Bird:
    def fly(self):
        pass

    def swim(self):
        pass
```

However, not all birds can swim. If we have a client that only needs to interact with birds that can fly, it shouldn't be forced to depend on the `swim()` method. We can solve this problem by splitting the `Bird` interface into two smaller interfaces: `FlyingBird` and `SwimmingBird`:

```python
class FlyingBird:
    def fly(self):
        pass

class SwimmingBird:
    def swim(self):
        pass
```

Now, any bird that can both fly and swim can implement both interfaces:

```python
class Duck(FlyingBird, SwimmingBird):
    def fly(self):
        print("Duck is flying")

    def swim(self):
        print("Duck is swimming")
```

And any client that only needs to interact with flying birds can depend on the FlyingBird interface:

```python
class BirdWatcher:
    def watch_bird(self, bird: FlyingBird):
        bird.fly()
```

This ensures that clients are not forced to depend on methods they do not need, making the code more modular and flexible.

#### D

**D**: Dependency Inversion Principle.

> The object of dependence should be an abstraction, not something specific.

The "D" in SOLID stands for the Dependency Inversion Principle (DIP). The DIP is a design principle in software engineering that states that high-level modules should not depend on low-level modules, but both should depend on abstractions. In addition, abstractions should not depend on details, but details should depend on abstractions.

The DIP is important because it promotes the decoupling of modules, making it easier to change and maintain the code. It also promotes the reuse of code, as modules can be swapped in and out without affecting the rest of the system.

To adhere to the DIP, the following guidelines should be followed:

1. High-level modules should not depend on low-level modules. Both should depend on abstractions.

2. Abstractions should not depend on details. Details should depend on abstractions.

3. The use of dependency injection can help to achieve the DIP.

In practical terms, the DIP means that instead of writing code that relies on specific implementations of modules or classes, developers should write code that relies on interfaces or abstract classes. This way, if the implementation of a module needs to be changed, the rest of the code doesn't need to be modified.

In Python, the DIP can be implemented through the use of dependency injection frameworks like Flask-Injector, which allow developers to inject dependencies into their code using interfaces or abstract classes. By using dependency injection, developers can create code that is both flexible and maintainable, and easily swap in and out different modules without affecting the rest of the system.

Here's an example of how the Dependency Inversion Principle can be applied in Python:

Suppose we have a high-level module called `PaymentProcessor` that needs to process payments, and it depends on a low-level module called `PaymentGateway`:

```python
class PaymentProcessor:
    def __init__(self):
        self.gateway = PaymentGateway()

    def process_payment(self, amount):
        self.gateway.charge(amount)
```

The `PaymentProcessor` class depends on the `PaymentGateway` class, which is a low-level detail. If we need to change the payment gateway, we would have to modify the `PaymentProcessor` class.

We can apply the Dependency Inversion Principle by introducing an abstraction that both the high-level and low-level modules can depend on:

```python
class PaymentGatewayInterface:
    def charge(self, amount):
        pass
```

Now, we can modify the `PaymentProcessor` class to depend on the `PaymentGatewayInterface` abstraction:

```python
class PaymentProcessor:
    def __init__(self, gateway: PaymentGatewayInterface):
        self.gateway = gateway

    def process_payment(self, amount):
        self.gateway.charge(amount)
```

And we can create a new `PaymentGateway` class that implements the `PaymentGatewayInterface`:

```python
class PaymentGateway(PaymentGatewayInterface):
    def charge(self, amount):
        print(f"Charging {amount} using PaymentGateway")
```

Now, both the `PaymentProcessor` and `PaymentGateway` classes depend on the `PaymentGatewayInterface` abstraction, rather than on each other. This makes the code more modular and flexible, and makes it easier to change the payment gateway implementation without affecting the `PaymentProcessor` class.

## What design patterns do you know

- [GitHub - pkolt/design_patterns: Design patterns](https://github.com/pkolt/design_patterns)
- [GitHub - faif/python-patterns: A collection of design patterns/idioms in Python](https://github.com/faif/python-patterns)
- [Python Design Patterns](https://python-patterns.guide/)

### Creational

Design patterns are general reusable solutions to commonly occurring problems in software design. Creational patterns, also known as "design patterns of object creation", are a subset of design patterns that deal with object creation mechanisms, trying to create objects in a manner suitable for the situation.

Creational design patterns describe how to create objects. Usually an object is created by calling a constructor, but sometimes you need a lot of flexibility, and that's where spawn patterns are useful.

#### Abstract factory

The Abstract Factory design pattern is a creational pattern that provides an interface for creating families of related or dependent objects without specifying their concrete classes. It allows a client to create objects without needing to know the specifics of their implementations, making it easier to switch between different implementations and making the code more flexible and maintainable.

In Python, the Abstract Factory pattern can be implemented using abstract classes or interfaces to define the factory interface and concrete classes to implement the specific products. Here's an example implementation:

```python
from abc import ABC, abstractmethod

# abstract factory interface
class AbstractFactory(ABC):
    @abstractmethod
    def create_product_a(self):
        pass

    @abstractmethod
    def create_product_b(self):
        pass

# concrete factory 1
class ConcreteFactory1(AbstractFactory):
    def create_product_a(self):
        return ConcreteProductA1()

    def create_product_b(self):
        return ConcreteProductB1()

# concrete factory 2
class ConcreteFactory2(AbstractFactory):
    def create_product_a(self):
        return ConcreteProductA2()

    def create_product_b(self):
        return ConcreteProductB2()

# abstract product A
class AbstractProductA(ABC):
    @abstractmethod
    def do_something(self):
        pass

# concrete product A1
class ConcreteProductA1(AbstractProductA):
    def do_something(self):
        return "Product A1"

# concrete product A2
class ConcreteProductA2(AbstractProductA):
    def do_something(self):
        return "Product A2"

# abstract product B
class AbstractProductB(ABC):
    @abstractmethod
    def do_something_else(self):
        pass

# concrete product B1
class ConcreteProductB1(AbstractProductB):
    def do_something_else(self):
        return "Product B1"

# concrete product B2
class ConcreteProductB2(AbstractProductB):
    def do_something_else(self):
        return "Product B2"

# client code
def client_code(factory):
    product_a = factory.create_product_a()
    product_b = factory.create_product_b()
    print(product_a.do_something())
    print(product_b.do_something_else())

# using concrete factory 1
client_code(ConcreteFactory1())

# using concrete factory 2
client_code(ConcreteFactory2())
```

In this example, the `AbstractFactory` interface defines the methods for creating abstract `ProductA` and `ProductB` objects. The concrete `ConcreteFactory1` and `ConcreteFactory2` classes implement this interface to create specific implementations of `ProductA` and `ProductB`.

The `AbstractProductA` and `AbstractProductB` abstract classes define the interface for the specific product objects, while the `ConcreteProductA1`, `ConcreteProductA2`, `ConcreteProductB1`, and `ConcreteProductB2` concrete classes implement those interfaces.

Finally, the client code uses the `AbstractFactory` interface to create and use specific `ProductA` and `ProductB` objects, without needing to know the details of their implementations.

For example, in a GUI system, there may be an abstract widget factory that is inherited by three concrete factories: MacWidgetFactory, XfceWidgetFactory, WindowsWidgetFactory, each of which provides methods for creating the same objects (make_button(), make_spinbox(), etc.), stylized, however, as is customary on a particular platform. This makes it possible to create a generic create_dialog() function that takes a factory instance as an argument and creates a dialog box that looks like OS X, Xfce, or Windows, depending on which factory we passed in.

Abstract factory classes are often implemented using factory methods, but can also be implemented using the prototype pattern.

```python
"""
*What is this pattern about?
In Java and other languages, the Abstract Factory Pattern serves to provide an interface for
creating related/dependent objects without need to specify their
actual class.
The idea is to abstract the creation of objects depending on business
logic, platform choice, etc.
In Python, the interface we use is simply a callable, which is "builtin" interface
in Python, and in normal circumstances we can simply use the class itself as
that callable, because classes are first class objects in Python.
*What does this example do?
This particular implementation abstracts the creation of a pet and
does so depending on the factory we chose (Dog or Cat, or random_animal)
This works because both Dog/Cat and random_animal respect a common
interface (callable for creation and .speak()).
Now my application can create pets abstractly and decide later,
based on my own criteria, dogs over cats.
*Where is the pattern used practically?
*References:
https://sourcemaking.com/design_patterns/abstract_factory
http://ginstrom.com/scribbles/2007/10/08/design-patterns-python-style/
*TL;DR
Provides a way to encapsulate a group of individual factories.
"""

import random


class PetShop:

    """A pet shop"""

    def __init__(self, animal_factory=None):
        """pet_factory is our abstract factory.  We can set it at will."""

        self.pet_factory = animal_factory

    def show_pet(self):
        """Creates and shows a pet using the abstract factory"""

        pet = self.pet_factory()
        print("We have a lovely {}".format(pet))
        print("It says {}".format(pet.speak()))


class Dog:
    def speak(self):
        return "woof"

    def __str__(self):
        return "Dog"


class Cat:
    def speak(self):
        return "meow"

    def __str__(self):
        return "Cat"


# Additional factories:

# Create a random animal
def random_animal():
    """Let's be dynamic!"""
    return random.choice([Dog, Cat])()


# Show pets with various factories
if __name__ == "__main__":

    # A Shop that sells only cats
    cat_shop = PetShop(Cat)
    cat_shop.show_pet()
    print("")

    # A shop that sells random animals
    shop = PetShop(random_animal)
    for i in range(3):
        shop.show_pet()
        print("=" * 20)

# OUTPUT #
# We have a lovely Cat
# It says meow
#
# We have a lovely Dog
# It says woof
# ====================
# We have a lovely Cat
# It says meow
# ====================
# We have a lovely Cat
# It says meow
# ====================
```

#### Builder

The Builder design pattern is a creational pattern that separates the construction of a complex object from its representation, allowing for different representations to be created using the same construction process. The pattern involves creating a builder class that defines a series of methods for creating parts of the complex object, and a director class that uses the builder to construct the final object.

In Python, the Builder pattern can be implemented using a builder class and a director class. The builder class defines the methods for creating parts of the complex object, and the director class uses the builder to construct the final object.

Here's an example implementation of the Builder pattern in Python:

```python
class Car:
    def __init__(self):
        self.engine = None
        self.tires = None
        self.seats = None

class Builder:
    def build_engine(self):
        pass

    def build_tires(self):
        pass

    def build_seats(self):
        pass

    def get_result(self):
        pass

class Director:
    def __init__(self, builder):
        self.builder = builder

    def construct_car(self):
        self.builder.build_engine()
        self.builder.build_tires()
        self.builder.build_seats()

    def get_car(self):
        return self.builder.get_result()

class CarBuilder(Builder):
    def __init__(self):
        self.car = Car()

    def build_engine(self):
        self.car.engine = "V8"

    def build_tires(self):
        self.car.tires = "Michelin"

    def build_seats(self):
        self.car.seats = "Leather"

    def get_result(self):
        return self.car
```

In this example, the `Car` class represents the complex object that we want to create, and the `Builder` class defines the methods for creating its parts. The `Director` class uses the `Builder` to construct the final `Car` object, while the `CarBuilder` class provides a concrete implementation of the `Builder` interface.

To use the `Builder` pattern, we first create an instance of the `CarBuilder` class, which implements the `Builder` interface. We then create an instance of the `Director` class, passing in the `CarBuilder` instance as a parameter. Finally, we call the `construct_car` method on the `Director` instance to build the `Car` object, and then call the `get_car` method to retrieve the finished `Car` object.

```python
car_builder = CarBuilder()
director = Director(car_builder)
director.construct_car()
car = director.get_car()
```

This implementation of the Builder pattern allows us to create different types of `Car` objects with different engine types, tire brands, and seat materials, while keeping the construction process the same for all types of `Car` objects.

---

The Builder is similar to the Abstract Factory pattern in that both are designed to create complex objects composed of other objects. But it differs in that it not only provides methods for constructing a complex object, but also stores its complete representation inside itself.

This pattern allows for the same compositional structure as the Abstract Factory (i.e. complex objects made up of several simpler ones) but is particularly useful in situations where the representation of a composite object must be separated from composition algorithms.

Separates the construction of a complex object from its representation, so that different representations can result from the same construction process. It differs from an abstract factory in that it focuses on the step-by-step construction of an object. A builder returns an object in the last step, while an abstract factory returns an object immediately. The builder is often used to create a builder pattern.

```python
"""
*What is this pattern about?
It decouples the creation of a complex object and its representation,
so that the same process can be reused to build objects from the same
family.
This is useful when you must separate the specification of an object
from its actual representation (generally for abstraction).
*What does this example do?
The first example achieves this by using an abstract base
class for a building, where the initializer (__init__ method) specifies the
steps needed, and the concrete subclasses implement these steps.
In other programming languages, a more complex arrangement is sometimes
necessary. In particular, you cannot have polymorphic behaviour in a constructor in C++ -
see https://stackoverflow.com/questions/1453131/how-can-i-get-polymorphic-behavior-in-a-c-constructor
- which means this Python technique will not work. The polymorphism
required has to be provided by an external, already constructed
instance of a different class.
In general, in Python this won't be necessary, but a second example showing
this kind of arrangement is also included.
*Where is the pattern used practically?
*References:
https://sourcemaking.com/design_patterns/builder
*TL;DR
Decouples the creation of a complex object and its representation.
"""


# Abstract Building
class Building:
    def __init__(self):
        self.build_floor()
        self.build_size()

    def build_floor(self):
        raise NotImplementedError

    def build_size(self):
        raise NotImplementedError

    def __repr__(self):
        return 'Floor: {0.floor} | Size: {0.size}'.format(self)


# Concrete Buildings
class House(Building):
    def build_floor(self):
        self.floor = 'One'

    def build_size(self):
        self.size = 'Big'


class Flat(Building):
    def build_floor(self):
        self.floor = 'More than One'

    def build_size(self):
        self.size = 'Small'


# In some very complex cases, it might be desirable to pull out the building
# logic into another function (or a method on another class), rather than being
# in the base class '__init__'. (This leaves you in the strange situation where
# a concrete class does not have a useful constructor)


class ComplexBuilding:
    def __repr__(self):
        return 'Floor: {0.floor} | Size: {0.size}'.format(self)


class ComplexHouse(ComplexBuilding):
    def build_floor(self):
        self.floor = 'One'

    def build_size(self):
        self.size = 'Big and fancy'


def construct_building(cls):
    building = cls()
    building.build_floor()
    building.build_size()
    return building


def main():
    """
    >>> house = House()
    >>> house
    Floor: One | Size: Big
    >>> flat = Flat()
    >>> flat
    Floor: More than One | Size: Small
    # Using an external constructor function:
    >>> complex_house = construct_building(ComplexHouse)
    >>> complex_house
    Floor: One | Size: Big and fancy
    """


if __name__ == "__main__":
    import doctest
    doctest.testmod()
```

#### Factory method

The Factory Method is a design pattern that provides an interface for creating objects but allows subclasses to alter the type of objects that will be created. It falls under the category of creational patterns in object-oriented programming.

In this pattern, we create an interface that defines a method for creating objects, but we let the subclasses decide which class to instantiate. This allows us to encapsulate the object creation logic and delegate the responsibility to the subclasses.

Here's an example implementation of the Factory Method pattern in Python:

```python
from abc import ABC, abstractmethod

class Animal(ABC):
    @abstractmethod
    def speak(self):
        pass

class Dog(Animal):
    def speak(self):
        return "Woof"

class Cat(Animal):
    def speak(self):
        return "Meow"

class AnimalFactory:
    def get_animal(self, animal_type):
        if animal_type == 'dog':
            return Dog()
        elif animal_type == 'cat':
            return Cat()
        else:
            return None
```

In the code above, we define an abstract class `Animal` with an abstract method `speak()`. We then define two concrete classes `Dog` and `Cat` that inherit from `Animal` and implement the `speak()` method in their own way.

Finally, we define the `AnimalFactory` class that has a `get_animal()` method. This method takes an `animal_type` parameter and returns an object of the appropriate type. If the `animal_type` is not recognized, the method returns `None`.

With this implementation, we can create a new `AnimalFactory` object and use it to create `Dog` and `Cat` objects:

```python
factory = AnimalFactory()
dog = factory.get_animal('dog')
cat = factory.get_animal('cat')
```

The `dog` and `cat` objects are created by the `AnimalFactory` object based on the `animal_type` parameter passed to the `get_animal()` method. This allows us to create objects without knowing the exact class of the object at compile time.

---

The Factory Method pattern is used when we want subclasses to choose which class to instantiate when an object is requested. This is useful on its own, but can be taken further and used when the class is not known in advance (for example, it depends on information read from a file or user input).

An abstract factory is often implemented using factory methods.
Factory methods are often called inside template methods.

```python
"""*What is this pattern about?
A Factory is an object for creating other objects.
*What does this example do?
The code shows a way to localize words in two languages: English and
Greek. "get_localizer" is the factory function that constructs a
localizer depending on the language chosen. The localizer object will
be an instance from a different class according to the language
localized. However, the main code does not have to worry about which
localizer will be instantiated, since the method "localize" will be called
in the same way independently of the language.
*Where can the pattern be used practically?
The Factory Method can be seen in the popular web framework Django:
http://django.wikispaces.asu.edu/*NEW*+Django+Design+Patterns For
example, in a contact form of a web page, the subject and the message
fields are created using the same form factory (CharField()), even
though they have different implementations according to their
purposes.
*References:
http://ginstrom.com/scribbles/2007/10/08/design-patterns-python-style/
*TL;DR
Creates objects without having to specify the exact class.
"""


class GreekLocalizer:
    """A simple localizer a la gettext"""

    def __init__(self):
        self.translations = {"dog": "σκύλος", "cat": "γάτα"}

    def localize(self, msg):
        """We'll punt if we don't have a translation"""
        return self.translations.get(msg, msg)


class EnglishLocalizer:
    """Simply echoes the message"""

    def localize(self, msg):
        return msg


def get_localizer(language="English"):
    """Factory"""
    localizers = {
        "English": EnglishLocalizer,
        "Greek": GreekLocalizer,
    }
    return localizers[language]()


def main():
    """
    # Create our localizers
    >>> e, g = get_localizer(language="English"), get_localizer(language="Greek")
    # Localize some text
    >>> for msg in "dog parrot cat bear".split():
    ...     print(e.localize(msg), g.localize(msg))
    dog σκύλος
    parrot parrot
    cat γάτα
    bear bear
    """


if __name__ == "__main__":
    import doctest
    doctest.testmod()
```

#### Prototype

The Prototype design pattern is a creational pattern that allows creating new objects by cloning existing ones, rather than creating new objects from scratch. This can be useful when creating new objects is expensive or when we need to create objects that are similar to existing ones.

In the Prototype pattern, we have a prototype object that serves as a blueprint for creating new objects. This prototype object is cloned to create new objects, rather than creating new objects from scratch. The cloning process can be shallow or deep, depending on the requirements.

To implement the Prototype pattern in Python, we can use the built-in `copy` module, which provides the `copy()` and `deepcopy()` functions for creating shallow and deep copies of objects, respectively. We can also define our own clone() method in the prototype object to customize the cloning process.

Here's an example implementation of the Prototype pattern in Python:

```python
import copy

class Prototype:
    def __init__(self):
        self._objects = {}

    def register_object(self, name, obj):
        self._objects[name] = obj

    def unregister_object(self, name):
        del self._objects[name]

    def clone(self, name, **kwargs):
        obj = copy.deepcopy(self._objects.get(name))
        obj.__dict__.update(kwargs)
        return obj

class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def __str__(self):
        return f"{self.name} ({self.age})"

p1 = Person("John", 30)

proto = Prototype()
proto.register_object("person", p1)

p2 = proto.clone("person")
print(p2)  # Output: John (30)

p3 = proto.clone("person", name="Jane")
print(p3)  # Output: Jane (30)
```

In this example, we define a `Person` class that represents an object that we want to clone. We then define a `Prototype` class that manages the prototype objects and provides a `clone()` method for creating new objects.

We register a prototype object of `Person` class with the `Prototype` class and then use it to create new objects using the `clone()` method. We can also pass keyword arguments to the `clone()` method to customize the cloned object. The resulting objects are clones of the original object, but with the updated attributes.

---

The Prototype pattern is used to create a new object by cloning the original one and then modifying the clone.

Ways to create a new object in Python:

```python
classPoint:
     __slots__ = ('x', 'y',)

     def __init__(self, x, y):
         self.x = x
         self.y = y

# With this classic definition of the Point class, there are seven ways to create a new point

def make_object(cls, *args, **kwargs):
     return cls(*args, **kwargs)

point1 = Point(1, 2)
point2 = eval('{}({}, {})'.format('Point', 2, 4)) # Dangerous
point3 = getattr(sys.modules[__name__], 'Point')(3, 6)
point4 = globals()['Point'](4, 8)
point5 = make_object(Point, 5, 10)
point6 = copy.deepcopy(point5)
point6.x = 6
point6.y = 12
point7 = point1.__class__(7, 14)
```

When creating point6, we use the classic prototype-based approach: we first clone an existing object, and then we initialize and configure it. To create point7, we take an object of the point1 class and pass other arguments to it.

In point6, we see that Python already has built-in support for prototypes in the form of the copy.deepcopy() function. However, the point7 example shows that Python has better features: instead of cloning an existing object and modifying the clone, Python provides access to an object of the existing object's class, so we can create a new object directly, which is much more efficient than cloning.

A prototype is a pattern that generates objects. Specifies the kinds of objects to create using a prototype instance, and creates new objects by copying this prototype.

```python
"""
*What is this pattern about?
This patterns aims to reduce the number of classes required by an
application. Instead of relying on subclasses it creates objects by
copying a prototypical instance at run-time.
This is useful as it makes it easier to derive new kinds of objects,
when instances of the class have only a few different combinations of
state, and when instantiation is expensive.
*What does this example do?
When the number of prototypes in an application can vary, it can be
useful to keep a Dispatcher (aka, Registry or Manager). This allows
clients to query the Dispatcher for a prototype before cloning a new
instance.
Below provides an example of such Dispatcher, which contains three
copies of the prototype: 'default', 'objecta' and 'objectb'.
*TL;DR
Creates new object instances by cloning prototype.
"""


class Prototype:

    value = 'default'

    def clone(self, **attrs):
        """Clone a prototype and update inner attributes dictionary"""
        # Python in Practice, Mark Summerfield
        obj = self.__class__()
        obj.__dict__.update(attrs)
        return obj


class PrototypeDispatcher:
    def __init__(self):
        self._objects = {}

    def get_objects(self):
        """Get all objects"""
        return self._objects

    def register_object(self, name, obj):
        """Register an object"""
        self._objects[name] = obj

    def unregister_object(self, name):
        """Unregister an object"""
        del self._objects[name]


def main():
    """
    >>> dispatcher = PrototypeDispatcher()
    >>> prototype = Prototype()
    >>> d = prototype.clone()
    >>> a = prototype.clone(value='a-value', category='a')
    >>> b = prototype.clone(value='b-value', is_checked=True)
    >>> dispatcher.register_object('objecta', a)
    >>> dispatcher.register_object('objectb', b)
    >>> dispatcher.register_object('default', d)
    >>> [{n: p.value} for n, p in dispatcher.get_objects().items()]
    [{'objecta': 'a-value'}, {'objectb': 'b-value'}, {'default': 'default'}]
    """


if __name__ == '__main__':
    import doctest
    doctest.testmod()
```

#### Singleton

The Singleton (Singleton) pattern is used when you need a class that must have a single instance in the entire program.

Many patterns (abstract factory, builder, prototype) can be implemented using singleton pattern.

The cookbook provides a simple Singleton class that any class can inherit to become a singleton.

```python
"""
Yet one singleton realization on Python without metaclass. Singleton may has __init__ method which will call only when first object create.
http://code.activestate.com/recipes/577208-singletonsubclass-with-once-initialization/
"""


class Singleton(object):

     def __new__(cls,*dt,**mp):
         if not hasattr(cls,'_inst'):
             cls._inst = super(Singleton, cls).__new__(cls,dt,mp)
         else:
             def init_pass(self,*dt,**mp):pass
             cls.__init__ = init_pass

         return cls._inst

if __name__ == '__main__':


     class A(Singleton):

         def __init__(self):
             """Super constructor
                 There is we can open file or create connection to the database
             """
             print "A init"


     a1 = A()
     a2 = A()
```

And the Borg class, which will give the same result in a very different way.

```python
"""
*What is this pattern about?
The Borg pattern (also known as the Monostate pattern) is a way to
implement singleton behavior, but instead of having only one instance
of a class, there are multiple instances that share the same state. In
other words, the focus is on sharing state instead of sharing instance
identity.
*What does this example do?
To understand the implementation of this pattern in Python, it is
important to know that, in Python, instance attributes are stored in a
attribute dictionary called __dict__. Usually, each instance will have
its own dictionary, but the Borg pattern modifies this so that all
instances have the same dictionary.
In this example, the __shared_state attribute will be the dictionary
shared between all instances, and this is ensured by assigining
__shared_state to the __dict__ variable when initializing a new
instance (i.e., in the __init__ method). Other attributes are usually
added to the instance's attribute dictionary, but, since the attribute
dictionary itself is shared (which is __shared_state), all other
attributes will also be shared.
*Where is the pattern used practically?
Sharing state is useful in applications like managing database connections:
https://github.com/onetwopunch/pythonDbTemplate/blob/master/database.py
*References:
https://fkromer.github.io/python-pattern-references/design/#singleton
*TL;DR
Provides singleton-like behavior sharing state between instances.
"""


class Borg:
    __shared_state = {}

    def __init__(self):
        self.__dict__ = self.__shared_state
        self.state = 'Init'

    def __str__(self):
        return self.state


class YourBorg(Borg):
    pass


def main():
    """
    >>> rm1 = Borg()
    >>> rm2 = Borg()
    >>> rm1.state = 'Idle'
    >>> rm2.state = 'Running'
    >>> print('rm1: {0}'.format(rm1))
    rm1: Running
    >>> print('rm2: {0}'.format(rm2))
    rm2: Running
    # When the `state` attribute is modified from instance `rm2`,
    # the value of `state` in instance `rm1` also changes
    >>> rm2.state = 'Zombie'
    >>> print('rm1: {0}'.format(rm1))
    rm1: Zombie
    >>> print('rm2: {0}'.format(rm2))
    rm2: Zombie
    # Even though `rm1` and `rm2` share attributes, the instances are not the same
    >>> rm1 is rm2
    False
    # Shared state is also modified from a subclass instance `rm3`
    >>> rm3 = YourBorg()
    >>> print('rm1: {0}'.format(rm1))
    rm1: Init
    >>> print('rm2: {0}'.format(rm2))
    rm2: Init
    >>> print('rm3: {0}'.format(rm3))
    rm3: Init
    """


if __name__ == "__main__":
    import doctest
    doctest.testmod()
```

However, the easiest way to get singleton functionality in Python is to create a module with global state stored in private variables and provide public functions to access it. For example, to get exchange rates, we need a function that will return a dictionary (the key is the name of the currency, the value is the exchange rate). You may need to call this function several times, but in most cases you need to retrieve rates from somewhere once. The Loner pattern will help to implement this.

```python
import re
import urllib.request


_URL = "http://www.bankofcanada.ca/stats/assets/csv/fx-seven-day.csv"


def get(refresh=False):
    if refresh:
        get.rates = {}
    if get.rates:
        return get.rates
    with urllib.request.urlopen(_URL) as file:
        for line in file:
            line = line.rstrip().decode("utf-8")
            if not line or line.startswith(("#", "Date")):
                continue
            name, currency, *rest = re.split(r"/s*,/s*", line)
            key = "{} ({})".format(name, currency)
            try:
                get.rates[key] = float(rest[-1])
            except ValueError as err:
                print("error {}: {}".format(err, line))
    return get.rates
get.rates = {}


if __name__ == "__main__":
    import sys
    if sys.stdout.isatty():
        print(get())
    else:
        print("Loaded OK")
```

Here we create the rates dictionary as an attribute of the Rates.get() function - this is our private value. When the public get() function is called for the first time (and also when called with the refresh=True parameter), we load the list of courses; otherwise, we simply return the last loaded courses.

#### Creational patterns. Outcome

All generative design patterns are implemented trivially in Python. The Singleton pattern can be implemented directly with a module, but the Prototype pattern is generally useless (although it can be implemented with the copy module), since Python provides dynamic access to class objects. Of the generative patterns, the Factory and Builder are the most useful, and there are several ways to implement them.

### Structural

Structural design patterns are design patterns that are concerned with object composition and class inheritance. These patterns are used to form large object structures and provide new functionality through the composition of objects and classes. Structural patterns also help to make a system more flexible by creating a stable interface between components, allowing the components to be modified or replaced without affecting the system as a whole.

Structural patterns describe how some objects are composed of other, larger ones. There are three main areas covered: customizing interfaces, adding functionality, and working with collections of objects.

#### Adapter

The Adapter pattern is a structural design pattern that allows incompatible interfaces of classes to work together by creating a wrapper around one of the existing classes. It converts the interface of a class into another interface that clients expect, without changing the original code. The Adapter pattern is useful when we have two classes with incompatible interfaces, and we need to use one class's functionality with the other class.

The main components of the Adapter pattern are:

1. Target: The interface that is used by the client code and needs to be adapted.
2. Adapter: The class that implements the Target interface and wraps the Adaptee object.
3. Adaptee: The class that has the functionality that needs to be adapted to work with the Target interface.

Here is an example implementation of the Adapter pattern in Python:

```python
class Target:
    """ The Target interface """
    def request(self) -> str:
        pass


class Adaptee:
    """ The Adaptee class """
    def specific_request(self) -> str:
        return "Adaptee request"


class Adapter(Target):
    """ The Adapter class """
    def __init__(self, adaptee: Adaptee):
        self.adaptee = adaptee

    def request(self) -> str:
        return f"Adapter: (TRANSLATED) {self.adaptee.specific_request()}"


def client_code(target: Target) -> None:
    """ Client code that uses the Target interface """
    print(target.request())


if __name__ == "__main__":
    adaptee = Adaptee()
    adapter = Adapter(adaptee)

    print("Adaptee interface is incompatible with the client.")
    print("But with adapter client can call it's method.")

    client_code(adapter)
```

In this example, the `Adaptee` class has a `specific_request()` method that is incompatible with the `Target` interface's `request()` method. We create an `Adapter` class that takes an instance of `Adaptee` and implements the `Target` interface by calling the `Adaptee`'s `specific_request()` method in its own `request()` method. Finally, we have a `client_code()` function that uses the `Target` interface and can call the `Adapter`'s `request()` method to get the desired output.

---

```python
"""
*What is this pattern about?
The Adapter pattern provides a different interface for a class. We can
think about it as a cable adapter that allows you to charge a phone
somewhere that has outlets in a different shape. Following this idea,
the Adapter pattern is useful to integrate classes that couldn't be
integrated due to their incompatible interfaces.
*What does this example do?
The example has classes that represent entities (Dog, Cat, Human, Car)
that make different noises. The Adapter class provides a different
interface to the original methods that make such noises. So the
original interfaces (e.g., bark and meow) are available under a
different name: make_noise.
*Where is the pattern used practically?
The Grok framework uses adapters to make objects work with a
particular API without modifying the objects themselves:
http://grok.zope.org/doc/current/grok_overview.html#adapters
*References:
http://ginstrom.com/scribbles/2008/11/06/generic-adapter-class-in-python/
https://sourcemaking.com/design_patterns/adapter
http://python-3-patterns-idioms-test.readthedocs.io/en/latest/ChangeInterface.html#adapter
*TL;DR
Allows the interface of an existing class to be used as another interface.
"""


class Dog:
    def __init__(self):
        self.name = "Dog"

    def bark(self):
        return "woof!"


class Cat:
    def __init__(self):
        self.name = "Cat"

    def meow(self):
        return "meow!"


class Human:
    def __init__(self):
        self.name = "Human"

    def speak(self):
        return "'hello'"


class Car:
    def __init__(self):
        self.name = "Car"

    def make_noise(self, octane_level):
        return "vroom{0}".format("!" * octane_level)


class Adapter:
    """
    Adapts an object by replacing methods.
    Usage:
    dog = Dog()
    dog = Adapter(dog, make_noise=dog.bark)
    """

    def __init__(self, obj, **adapted_methods):
        """We set the adapted methods in the object's dict"""
        self.obj = obj
        self.__dict__.update(adapted_methods)

    def __getattr__(self, attr):
        """All non-adapted calls are passed to the object"""
        return getattr(self.obj, attr)

    def original_dict(self):
        """Print original object dict"""
        return self.obj.__dict__


def main():
    """
    >>> objects = []
    >>> dog = Dog()
    >>> print(dog.__dict__)
    {'name': 'Dog'}
    >>> objects.append(Adapter(dog, make_noise=dog.bark))
    >>> objects[0].__dict__['obj'], objects[0].__dict__['make_noise']
    (<...Dog object at 0x...>, <bound method Dog.bark of <...Dog object at 0x...>>)
    >>> print(objects[0].original_dict())
    {'name': 'Dog'}
    >>> cat = Cat()
    >>> objects.append(Adapter(cat, make_noise=cat.meow))
    >>> human = Human()
    >>> objects.append(Adapter(human, make_noise=human.speak))
    >>> car = Car()
    >>> objects.append(Adapter(car, make_noise=lambda: car.make_noise(3)))
    >>> for obj in objects:
    ...    print("A {0} goes {1}".format(obj.name, obj.make_noise()))
    A Dog goes woof!
    A Cat goes meow!
    A Human goes 'hello'
    A Car goes vroom!!!
    """


if __name__ == "__main__":
    import doctest
    doctest.testmod(optionflags=doctest.ELLIPSIS)
```

#### Bridge

The Bridge pattern is a structural design pattern that decouples an abstraction from its implementation, allowing them to vary independently. It is useful when you want to avoid creating a massive number of subclasses to handle different variations of a component.

The pattern consists of two main components: the abstraction and the implementation. The abstraction defines the high-level interface for a client to interact with, while the implementation defines the low-level details that the abstraction relies on.

The key benefit of the Bridge pattern is that it allows for the separation of concerns between the abstraction and the implementation. This means that changes to one component will not affect the other, making it easier to maintain and extend the system over time.

Here is an example of the Bridge pattern in Python:

```python
# Implementor interface
class Renderer:
    def render_circle(self, radius):
        pass

# Concrete Implementor A
class VectorRenderer(Renderer):
    def render_circle(self, radius):
        print(f"Drawing a circle of radius {radius} using vector graphics")

# Concrete Implementor B
class RasterRenderer(Renderer):
    def render_circle(self, radius):
        print(f"Drawing a circle of radius {radius} using raster graphics")

# Abstraction
class Shape:
    def __init__(self, renderer):
        self.renderer = renderer

    def draw(self):
        pass

    def resize(self, factor):
        pass

# Refined Abstraction
class Circle(Shape):
    def __init__(self, x, y, radius, renderer):
        super().__init__(renderer)
        self.x = x
        self.y = y
        self.radius = radius

    def draw(self):
        self.renderer.render_circle(self.radius)

    def resize(self, factor):
        self.radius *= factor
```

In this example, we have two concrete implementors - `VectorRenderer` and `RasterRenderer` - that implement the `Renderer` interface. We also have an abstraction - `Shape` - that takes a `Renderer` object in its constructor.

The `Circle` class is a refined abstraction that inherits from `Shape` and adds additional properties for its coordinates and radius. When we call the draw method on a `Circle` object, it delegates the rendering of the circle to its `Renderer` object.

By using the `Bridge` pattern in this way, we can easily switch out different implementations of `Renderer` without affecting the `Shape` or `Circle` classes. For example, if we wanted to add a new `3DRenderer`, we could create a new concrete implementor that implements the `Renderer` interface and use it with our existing abstractions.

---

```python
"""
*References:
http://en.wikibooks.org/wiki/Computer_Science_Design_Patterns/Bridge_Pattern#Python
*TL;DR
Decouples an abstraction from its implementation.
"""


# ConcreteImplementor 1/2
class DrawingAPI1:
    def draw_circle(self, x, y, radius):
        print('API1.circle at {}:{} radius {}'.format(x, y, radius))


# ConcreteImplementor 2/2
class DrawingAPI2:
    def draw_circle(self, x, y, radius):
        print('API2.circle at {}:{} radius {}'.format(x, y, radius))


# Refined Abstraction
class CircleShape:
    def __init__(self, x, y, radius, drawing_api):
        self._x = x
        self._y = y
        self._radius = radius
        self._drawing_api = drawing_api

    # low-level i.e. Implementation specific
    def draw(self):
        self._drawing_api.draw_circle(self._x, self._y, self._radius)

    # high-level i.e. Abstraction specific
    def scale(self, pct):
        self._radius *= pct


def main():
    """
    >>> shapes = (CircleShape(1, 2, 3, DrawingAPI1()), CircleShape(5, 7, 11, DrawingAPI2()))
    >>> for shape in shapes:
    ...    shape.scale(2.5)
    ...    shape.draw()
    API1.circle at 1:2 radius 7.5
    API2.circle at 5:7 radius 27.5
    """


if __name__ == '__main__':
    import doctest
    doctest.testmod()
```

#### Composite

The Composite pattern is a structural design pattern that allows you to treat individual objects and compositions of objects uniformly, by creating a hierarchical tree-like structure of objects. It composes objects into tree structures to represent part-whole hierarchies. With the Composite pattern, you can work with complex object hierarchies in a simple and intuitive way, just like working with a single object.

The Composite pattern is based on two classes: the Component class, which is the base class for all the objects in the hierarchy, and the Composite class, which represents the internal nodes in the tree structure. The Component class defines the common interface for all objects in the tree, and the Composite class defines the interface for the objects that have children.

To implement the Composite pattern in Python, you can create a Component interface or an abstract base class that defines the common interface for all the objects in the hierarchy. Then, you can create two types of classes: Leaf classes and Composite classes. Leaf classes represent the individual objects in the tree, and Composite classes represent the internal nodes in the tree.

Here's an example of the Composite pattern implemented in Python:

```python
from abc import ABC, abstractmethod

class Component(ABC):
    """The base Component class"""

    @abstractmethod
    def operation(self) -> str:
        pass


class Leaf(Component):
    """A Leaf node class"""

    def operation(self) -> str:
        return "Leaf"


class Composite(Component):
    """A Composite node class"""

    def __init__(self) -> None:
        self._children = []

    def add(self, component: Component) -> None:
        self._children.append(component)

    def remove(self, component: Component) -> None:
        self._children.remove(component)

    def operation(self) -> str:
        results = []
        for child in self._children:
            results.append(child.operation())
        return f"Branch({'+'.join(results)})"
```

In this example, the Component class is defined as an abstract base class that has a single method, `operation()`. The Leaf class represents the individual objects in the tree, and the Composite class represents the internal nodes in the tree. The Composite class has a list of children, and it implements the `add()`, `remove()`, and `operation()` methods.

You can use the Composite pattern to create a tree-like structure of objects and treat them uniformly, without worrying about the difference between individual objects and collections of objects. The Composite pattern is useful when you need to work with complex object hierarchies that have a part-whole relationship.

#### Decorator

The Decorator pattern is a structural design pattern that allows objects to add new behaviors dynamically by wrapping them with decorator objects. It allows for adding new functionality to an existing object without altering its structure. This pattern follows the Open-Closed Principle, which states that classes should be open for extension but closed for modification.

The Decorator pattern involves creating a set of decorator classes that are used to wrap concrete components. The concrete components can be classes, objects, or data structures. Decorator objects have the same interface as the components they decorate, which allows them to be used interchangeably.

The Decorator pattern consists of four main components:

1. Component: An abstract class or interface that defines the methods to be implemented by the concrete components and decorators.
2. Concrete Component: A class that provides the basic implementation of the component interface.
3. Decorator: An abstract class or interface that defines the methods to be implemented by the concrete decorators. It holds a reference to a component object and has the same interface as the component it decorates.
4. Concrete Decorator: A class that implements the decorator interface and adds new functionality to the component it decorates.

Here's an example of how to implement the Decorator pattern in Python:

```python
# Define the base component class
class Component:
    def operation(self):
        pass

# Define the concrete component class
class ConcreteComponent(Component):
    def operation(self):
        return "ConcreteComponent"

# Define the base decorator class
class Decorator(Component):
    def __init__(self, component):
        self._component = component

    def operation(self):
        return self._component.operation()

# Define concrete decorator classes
class ConcreteDecoratorA(Decorator):
    def operation(self):
        return f"ConcreteDecoratorA({self._component.operation()})"

class ConcreteDecoratorB(Decorator):
    def operation(self):
        return f"ConcreteDecoratorB({self._component.operation()})"

# Create objects and call methods
component = ConcreteComponent()
decoratorA = ConcreteDecoratorA(component)
decoratorB = ConcreteDecoratorB(decoratorA)
print(decoratorB.operation())
```

In this example, we have a base component class called `Component`, which defines the interface for objects that can be decorated. We also have a concrete component class called `ConcreteComponent`, which implements the behavior of the base component.

We then define a base decorator class called `Decorator`, which holds a reference to a component object and implements the same interface as the component. We also define two concrete decorator classes called `ConcreteDecoratorA` and `ConcreteDecoratorB`, which add functionality to the component by calling its methods and doing some additional work.

Finally, we create a component object, wrap it with two decorators, and call the operation method on the outermost decorator.

#### Facade

The Facade pattern is a structural design pattern that provides a simplified interface to a complex system of classes, libraries, or frameworks. It hides the complexity of the underlying system and provides a higher-level interface to the client. This helps to decouple the client from the subsystems, making it easier to use and maintain.

The Facade pattern involves creating a Facade class that provides a simplified interface to a complex subsystem. The Facade class delegates client requests to the appropriate subsystem objects and returns the results to the client.

The Python standard library has several modules for working with compressed files - gzip, tar+gzip, zip. All of them have different interfaces. If we want to have one unified interface for working with archives, we can use the Facade pattern.

The Facade and Adapter patterns seem similar at first glance. The difference is that a Facade builds a simple interface on top of a complex one, while an Adapter builds a unified interface on top of some other (not necessarily complex) one. Both of these patterns can be used together. For example, define an interface for working with archive files, write an adapter for each format, and build a facade on top of them so that users don't have to worry about which particular file format is used.

Here's an example implementation of the Facade pattern in Python:

```python
"""
Example from https://en.wikipedia.org/wiki/Facade_pattern#Python
*What is this pattern about?
The Facade pattern is a way to provide a simpler unified interface to
a more complex system. It provides an easier way to access functions
of the underlying system by providing a single entry point.
This kind of abstraction is seen in many real life situations. For
example, we can turn on a computer by just pressing a button, but in
fact there are many procedures and operations done when that happens
(e.g., loading programs from disk to memory). In this case, the button
serves as an unified interface to all the underlying procedures to
turn on a computer.
*Where is the pattern used practically?
This pattern can be seen in the Python standard library when we use
the isdir function. Although a user simply uses this function to know
whether a path refers to a directory, the system makes a few
operations and calls other modules (e.g., os.stat) to give the result.
*References:
https://sourcemaking.com/design_patterns/facade
https://fkromer.github.io/python-pattern-references/design/#facade
http://python-3-patterns-idioms-test.readthedocs.io/en/latest/ChangeInterface.html#facade
*TL;DR
Provides a simpler unified interface to a complex system.
"""


# Complex computer parts
class CPU:
    """
    Simple CPU representation.
    """
    def freeze(self):
        print("Freezing processor.")

    def jump(self, position):
        print("Jumping to:", position)

    def execute(self):
        print("Executing.")


class Memory:
    """
    Simple memory representation.
    """
    def load(self, position, data):
        print("Loading from {0} data: '{1}'.".format(position, data))


class SolidStateDrive:
    """
    Simple solid state drive representation.
    """
    def read(self, lba, size):
        return "Some data from sector {0} with size {1}".format(lba, size)


class ComputerFacade:
    """
    Represents a facade for various computer parts.
    """
    def __init__(self):
        self.cpu = CPU()
        self.memory = Memory()
        self.ssd = SolidStateDrive()

    def start(self):
        self.cpu.freeze()
        self.memory.load("0x00", self.ssd.read("100", "1024"))
        self.cpu.jump("0x00")
        self.cpu.execute()


def main():
    """
    >>> computer_facade = ComputerFacade()
    >>> computer_facade.start()
    Freezing processor.
    Loading from 0x00 data: 'Some data from sector 100 with size 1024'.
    Jumping to: 0x00
    Executing.
    """


if __name__ == "__main__":
    import doctest
    doctest.testmod(optionflags=doctest.ELLIPSIS)
```

#### Flyweight

The Flyweight design pattern is a structural pattern that is used to reduce the memory usage of an application. It allows for sharing of common parts of objects between multiple objects, thereby reducing the overall memory usage of the application.

The pattern achieves this by separating the intrinsic state of an object, which is shared among multiple objects, from the extrinsic state of an object, which is unique to each object. The intrinsic state is stored in a separate Flyweight object, which is shared among multiple objects.

The flyweight is designed to handle a large number of relatively small objects, when many of these objects are duplicates. The implementation of the pattern assumes that each unique object is presented only once, and this instance is given to the request. In Python, it is easily implemented via a dictionary.

In Python, the approach to implementing flyweights is natural due to the presence of object references. For example, if we had a long list of strings with a lot of duplicates, then by storing references to objects (that is, variables) and not literal strings, we could significantly save memory

Here is an example implementation of the Flyweight pattern in Python:

```python
red, green, blue = 'red', 'green', 'blue'
x = (red, green, blue, red, green, blue, green)
```

```python
"""
*What is this pattern about?
This pattern aims to minimise the number of objects that are needed by
a program at run-time. A Flyweight is an object shared by multiple
contexts, and is indistinguishable from an object that is not shared.
The state of a Flyweight should not be affected by it's context, this
is known as its intrinsic state. The decoupling of the objects state
from the object's context, allows the Flyweight to be shared.
*What does this example do?
The example below sets-up an 'object pool' which stores initialised
objects. When a 'Card' is created it first checks to see if it already
exists instead of creating a new one. This aims to reduce the number of
objects initialised by the program.
*References:
http://codesnipers.com/?q=python-flyweights
https://python-patterns.guide/gang-of-four/flyweight/
*Examples in Python ecosystem:
https://docs.python.org/3/library/sys.html#sys.intern
*TL;DR
Minimizes memory usage by sharing data with other similar objects.
"""

import weakref


class Card:
    """The Flyweight"""

    # Could be a simple dict.
    # With WeakValueDictionary garbage collection can reclaim the object
    # when there are no other references to it.
    _pool = weakref.WeakValueDictionary()

    def __new__(cls, value, suit):
        # If the object exists in the pool - just return it
        obj = cls._pool.get(value + suit)
        # otherwise - create new one (and add it to the pool)
        if obj is None:
            obj = object.__new__(Card)
            cls._pool[value + suit] = obj
            # This row does the part we usually see in `__init__`
            obj.value, obj.suit = value, suit
        return obj

    # If you uncomment `__init__` and comment-out `__new__` -
    #   Card becomes normal (non-flyweight).
    # def __init__(self, value, suit):
    #     self.value, self.suit = value, suit

    def __repr__(self):
        return "<Card: {}{}>".format(self.value, self.suit)


def main():
    """
    >>> c1 = Card('9', 'h')
    >>> c2 = Card('9', 'h')
    >>> c1, c2
    (<Card: 9h>, <Card: 9h>)
    >>> c1 == c2
    True
    >>> c1 is c2
    True
    >>> c1.new_attr = 'temp'
    >>> c3 = Card('9', 'h')
    >>> hasattr(c3, 'new_attr')
    True
    >>> Card._pool.clear()
    >>> c4 = Card('9', 'h')
    >>> hasattr(c4, 'new_attr')
    False
    """


if __name__ == "__main__":
    import doctest
    doctest.testmod()
```

#### Proxy

The Proxy pattern is a design pattern that provides a surrogate or placeholder for another object to control access to it. It falls under the category of structural patterns.

In the Proxy pattern, a proxy object acts as an intermediary between the client and the real object, hiding the details of the real object and providing additional functionality such as lazy initialization, access control, and caching.

The Proxy pattern is useful when the real object is resource-intensive, or when there are multiple clients accessing the same object and the access needs to be controlled or coordinated. It is also useful when the real object is not available or needs to be replaced with a different implementation without affecting the client code.

The book "Design Patterns" describes 4 such cases:

1. remote proxy, when access to a remote object is proxied by a local object;
2. virtual proxy, which allows you to create lightweight objects instead of heavy ones, and create the latter only when necessary;
3. a security proxy that provides different levels of access, depending on the rights of the client;
4. a smart reference that performs "additional actions when accessing an object" (can also be implemented using the @property descriptor)

Here is an example of implementing the Proxy pattern in Python:

```python
"""
*TL;DR
Provides an interface to resource that is expensive to duplicate.
"""

import time


class SalesManager:
    def talk(self):
        print("Sales Manager ready to talk")


class Proxy:
    def __init__(self):
        self.busy = 'No'
        self.sales = None

    def talk(self):
        print("Proxy checking for Sales Manager availability")
        if self.busy == 'No':
            self.sales = SalesManager()
            time.sleep(0.1)
            self.sales.talk()
        else:
            time.sleep(0.1)
            print("Sales Manager is busy")


class NoTalkProxy(Proxy):
    def talk(self):
        print("Proxy checking for Sales Manager availability")
        time.sleep(0.1)
        print("This Sales Manager will not talk to you", "whether he/she is busy or not")


if __name__ == '__main__':
    p = Proxy()
    p.talk()
    p.busy = 'Yes'
    p.talk()
    p = NoTalkProxy()
    p.talk()
    p.busy = 'Yes'
    p.talk()

# OUTPUT #
# Proxy checking for Sales Manager availability
# Sales Manager ready to talk
# Proxy checking for Sales Manager availability
# Sales Manager is busy
# Proxy checking for Sales Manager availability
# This Sales Manager will not talk to you whether he/she is busy or not
# Proxy checking for Sales Manager availability
# This Sales Manager will not talk to you whether he/she is busy or not
```

#### Structural patterns. Outcome

The Adapter and Facade patterns make it easy to reuse classes in new contexts, while the Bridge pattern allows you to inject complex functionality from one class into another. The Composite makes it easy to create object hierarchies, although this is not particularly necessary in Python, since dictionaries are enough for this purpose. The decorator is so useful that Python has direct support for it, and the decorator idea is even extended to classes. The use of object references means that the language itself has a built-in variation on the Flyweight pattern. And the Proxy pattern in Python is especially easy to implement.

### Behavioral

Behavioral patterns in programming are design patterns that focus on communication between objects and how they collaborate to accomplish complex behaviors and responsibilities. These patterns primarily deal with algorithms and the assignment of responsibilities between objects. They aim to simplify communication between objects and reduce coupling, increasing flexibility and reusability in software design. Some of them have direct support in the Python syntax.

#### Chain of responsobility

The Chain of Responsibility is a behavioral design pattern that allows passing requests along a chain of objects to handle them. Each object in the chain can handle the request or pass it to the next object in the chain. This pattern provides loose coupling between the sender and the receiver of the request, allowing multiple objects to handle the request without knowing the chain structure and reducing the coupling between objects.

The Chain of Responsibility pattern consists of three main parts: the Handler interface, the ConcreteHandler classes, and the Client class.

The Handler interface defines the common interface for handling requests. It also contains a reference to the next object in the chain.

The ConcreteHandler classes implement the Handler interface and handle requests they are responsible for. They can also forward requests to the next object in the chain if they cannot handle them.

The Client class creates the chain of objects and sends requests to the first object in the chain.

The chain of responsibility pattern is designed to break the connection between the sender of a request and the recipient who processes this request. Instead of directly calling one function from another, the first function sends a request to a chain of recipients. The first recipient in the chain can either process the request and break the chain (without passing the request further), or pass the request on to the next recipient. The second recipient has the same choice, and so on, until the request reaches the last recipient (which may reject the request or throw an exception).

Imagine a user interface that receives events to process. Some events come from the user (such as mouse and keyboard events), others come from the system (such as timer events).

Here's an example implementation of the Chain of Responsibility pattern in Python:

```python
"""
*What is this pattern about?
The Chain of responsibility is an object oriented version of the
`if ... elif ... elif ... else ...` idiom, with the
benefit that the condition–action blocks can be dynamically rearranged
and reconfigured at runtime.
This pattern aims to decouple the senders of a request from its
receivers by allowing request to move through chained
receivers until it is handled.
Request receiver in simple form keeps a reference to a single successor.
As a variation some receivers may be capable of sending requests out
in several directions, forming a `tree of responsibility`.
*TL;DR
Allow a request to pass down a chain of receivers until it is handled.
"""

import abc


class Handler(metaclass=abc.ABCMeta):

    def __init__(self, successor=None):
        self.successor = successor

    def handle(self, request):
        """
        Handle request and stop.
        If can't - call next handler in chain.
        As an alternative you might even in case of success
        call the next handler.
        """
        res = self.check_range(request)
        if not res and self.successor:
            self.successor.handle(request)

    @abc.abstractmethod
    def check_range(self, request):
        """Compare passed value to predefined interval"""


class ConcreteHandler0(Handler):
    """Each handler can be different.
    Be simple and static...
    """

    @staticmethod
    def check_range(request):
        if 0 <= request < 10:
            print("request {} handled in handler 0".format(request))
            return True


class ConcreteHandler1(Handler):
    """... With it's own internal state"""

    start, end = 10, 20

    def check_range(self, request):
        if self.start <= request < self.end:
            print("request {} handled in handler 1".format(request))
            return True


class ConcreteHandler2(Handler):
    """... With helper methods."""

    def check_range(self, request):
        start, end = self.get_interval_from_db()
        if start <= request < end:
            print("request {} handled in handler 2".format(request))
            return True

    @staticmethod
    def get_interval_from_db():
        return (20, 30)


class FallbackHandler(Handler):
    @staticmethod
    def check_range(request):
        print("end of chain, no handler for {}".format(request))
        return False


def main():
    """
    >>> h0 = ConcreteHandler0()
    >>> h1 = ConcreteHandler1()
    >>> h2 = ConcreteHandler2(FallbackHandler())
    >>> h0.successor = h1
    >>> h1.successor = h2
    >>> requests = [2, 5, 14, 22, 18, 3, 35, 27, 20]
    >>> for request in requests:
    ...     h0.handle(request)
    request 2 handled in handler 0
    request 5 handled in handler 0
    request 14 handled in handler 1
    request 22 handled in handler 2
    request 18 handled in handler 1
    request 3 handled in handler 0
    end of chain, no handler for 35
    request 27 handled in handler 2
    request 20 handled in handler 2
    """


if __name__ == "__main__":
    import doctest
    doctest.testmod(optionflags=doctest.ELLIPSIS)
```

#### Command

The Command pattern is a behavioral design pattern that encapsulates a request as an object, thereby allowing you to parameterize clients with different requests, queue or log requests, and support undoable operations. In this pattern, a command object is used to represent a single action or a transaction. The command object contains all the information necessary for the action to be taken, including the method to be called, the arguments to be passed to the method, and any other relevant information.

The main participants in this pattern are the `Command`, `Invoker`, `Receiver`, and `Client`. The `Command` defines the interface for executing an operation. The `Invoker` asks the `Command` to carry out the request. The `Receiver` is the object that performs the action when the command is executed. The `Client` creates the `Command` and sets its `Receiver`.

Here is an example implementation of the Command pattern in Python:

```python
# Command interface
class Command:
    def execute(self):
        pass

# Concrete command classes
class LightOnCommand(Command):
    def __init__(self, light):
        self.light = light

    def execute(self):
        self.light.turn_on()

class LightOffCommand(Command):
    def __init__(self, light):
        self.light = light

    def execute(self):
        self.light.turn_off()

# Receiver class
class Light:
    def turn_on(self):
        print("Light turned on")

    def turn_off(self):
        print("Light turned off")

# Invoker class
class Switch:
    def __init__(self, on_command, off_command):
        self.on_command = on_command
        self.off_command = off_command

    def turn_on(self):
        self.on_command.execute()

    def turn_off(self):
        self.off_command.execute()

# Client code
light = Light()
on_command = LightOnCommand(light)
off_command = LightOffCommand(light)
switch = Switch(on_command, off_command)

switch.turn_on()
switch.turn_off()
```

In this example, we have a Command interface and two Concrete Command classes: `LightOnCommand` and `LightOffCommand`. The Receiver is the `Light` class, which has methods for turning the light on and off. The Invoker is the `Switch` class, which has methods for turning the light on and off by calling the execute method of the appropriate Command object. Finally, the Client creates the Command objects and sets their Receiver.

#### Interpreter

The Interpreter pattern is a behavioral design pattern that defines a language or syntax, and it uses an interpreter to evaluate and execute the instructions written in that language. This pattern is particularly useful when you have to interpret and execute specific language syntax, such as mathematical expressions or queries.

The Interpreter pattern consists of three main components: the Context, the Abstract Expression, and the Concrete Expression. The Context contains the information that the interpreter will use to evaluate the expressions. The Abstract Expression defines the interface for the expressions, and the Concrete Expression implements the interface and evaluates the expression.

Here's an example implementation of the Interpreter pattern in Python that evaluates a simple arithmetic expression:

```python
class Context:
    def __init__(self):
        self.variables = {}

    def get_value(self, variable):
        return self.variables.get(variable, 0)

    def set_value(self, variable, value):
        self.variables[variable] = value

class AbstractExpression:
    def interpret(self, context):
        pass

class NumberExpression(AbstractExpression):
    def __init__(self, number):
        self.number = number

    def interpret(self, context):
        return self.number

class PlusExpression(AbstractExpression):
    def __init__(self, left_expression, right_expression):
        self.left_expression = left_expression
        self.right_expression = right_expression

    def interpret(self, context):
        return self.left_expression.interpret(context) + self.right_expression.interpret(context)

class MinusExpression(AbstractExpression):
    def __init__(self, left_expression, right_expression):
        self.left_expression = left_expression
        self.right_expression = right_expression

    def interpret(self, context):
        return self.left_expression.interpret(context) - self.right_expression.interpret(context)

context = Context()
a = NumberExpression(5)
b = NumberExpression(10)
c = PlusExpression(a, b)
d = MinusExpression(c, a)

print(d.interpret(context)) # Output: 10
```

In this example, we have a Context class that contains a dictionary of variables and their values. We also have three types of expressions: NumberExpression, PlusExpression, and MinusExpression. NumberExpression represents a simple numeric value, while PlusExpression and MinusExpression represent binary arithmetic operations.

To evaluate an expression, we call its `interpret` method, passing in the context object as a parameter. The expression then recursively evaluates its sub-expressions until the final value is computed.

---

At its most primitive level, an application receives strings from the user, or from another program, that need to be interpreted (and possibly executed) in some way.

An example of a widespread implementation of such requirements is the creation of domain-specific languages (DSLs).

```python
"""
Interpreter - a pattern of class behavior.
For a given language, defines a representation of its grammar,
as well as an interpreter of the sentences of this language.
"""


class RomanNumeralInterpreter(object):
     """Roman numeral interpreter"""
     def __init__(self):
         self.grammar = {
             'I': 1,
             'V': 5
             'X': 10
             'L': 50
             'C': 100
             'D': 500
             'M': 1000
         }

     def interpret(self, text):
         numbers = map(self.grammar.get, text) # strings to values
         if None in numbers:
             raise ValueError('Invalid value: %s' % text)
         result = 0 # accumulate the result
         temp = None # remember the last value
         while numbers:
             num = numbers.pop(0)
             if temp is None or temp >= num:
                 result += number
             else:
                 result += (num - temp * 2)
             temp = num
         return result


interp = RomanNumeralInterpreter()
print interp.interpret('MMMCMXCIX') == 3999 # True
print interp.interpret('MCMLXXXVIII') == 1988 # True
```

#### Iterator

The iterator pattern is a design pattern that allows the sequential traversal of elements in a collection without exposing its underlying representation. It provides a way to access the elements of an aggregate object sequentially without exposing its underlying implementation.

In this pattern, an iterator is responsible for iterating over a collection of objects and returning them one at a time. The collection could be any type of data structure, such as an array, list, tree, or graph. The iterator provides a uniform interface for traversing the elements of the collection regardless of its implementation.

The iterator pattern has the following components:

1. Iterator: Defines the interface for the iterator. It includes methods such as next(), hasNext(), and remove().

2. ConcreteIterator: Implements the iterator interface and keeps track of the current position in the collection.

3. Aggregate: Defines the interface for the collection of objects.

4. ConcreteAggregate: Implements the collection interface and creates an iterator object.

It's so useful that Python has built-in support for it, and it also provides special methods that we can implement in our own classes to support iteration seamlessly.

Iteration can be supported in three ways: by following the sequence protocol, by using a variant of the iter() built-in function with two arguments, or by following the iterator protocol.

Here's an example implementation of the iterator pattern in Python:

```python
class MyList:
    def __init__(self):
        self.items = []

    def add(self, item):
        self.items.append(item)

    def __iter__(self):
        return MyListIterator(self)

class MyListIterator:
    def __init__(self, mylist):
        self.mylist = mylist
        self.index = 0

    def __next__(self):
        if self.index >= len(self.mylist.items):
            raise StopIteration
        item = self.mylist.items[self.index]
        self.index += 1
        return item

if __name__ == '__main__':
    mylist = MyList()
    mylist.add('apple')
    mylist.add('banana')
    mylist.add('orange')

    for item in mylist:
        print(item)
```

In this example, `MyList` is the aggregate and `MyListIterator` is the iterator. The `MyList` class has an `add()` method for adding items to the list and an `__iter__()` method that returns an instance of `MyListIterator`. The `MyListIterator` class keeps track of the current index and returns the next item in the list when the `__next__()` method is called.

When the code is executed, it prints out the items in the list: "apple", "banana", and "orange". The for loop iterates over the items in the list using the iterator.

#### Mediator

The Mediator design pattern is a behavioral pattern that promotes loose coupling between objects by introducing a mediator object that handles the communication between them. In other words, it allows objects to communicate with each other through a mediator instead of directly with each other. This helps to reduce the dependencies between objects, which in turn simplifies the design and makes it easier to maintain.

The Mediator pattern consists of several key components:

- Mediator: an interface or abstract class that defines the communication protocol between objects.
- Concrete Mediator: a class that implements the Mediator interface and manages the communication between the objects.
- Colleague: an interface or abstract class that defines the interface of the objects that will communicate with each other through the mediator.
- Concrete Colleague: a class that implements the Colleague interface and communicates with other objects through the mediator.

The mediator provides a loose coupling of the system, eliminating the need for objects to explicitly refer to each other and thereby allowing you to independently change the interactions between them.

Here is an example implementation of the Mediator pattern in Python:

```python
class Mediator:
    def send(self, message, colleague):
        pass

class ConcreteMediator(Mediator):
    def __init__(self, colleague1, colleague2):
        self._colleague1 = colleague1
        self._colleague2 = colleague2

    def send(self, message, colleague):
        if colleague == self._colleague1:
            self._colleague2.notify(message)
        else:
            self._colleague1.notify(message)

class Colleague:
    def __init__(self, mediator):
        self._mediator = mediator

    def send(self, message):
        self._mediator.send(message, self)

    def notify(self, message):
        pass

class ConcreteColleague1(Colleague):
    def notify(self, message):
        print("ConcreteColleague1 received message:", message)

class ConcreteColleague2(Colleague):
    def notify(self, message):
        print("ConcreteColleague2 received message:", message)

# Create objects and call methods
mediator = ConcreteMediator(ConcreteColleague1(mediator), ConcreteColleague2(mediator))
colleague1 = mediator._colleague1
colleague2 = mediator._colleague2
colleague1.send("Hello from ConcreteColleague1!")
colleague2.send("Hi from ConcreteColleague2!")
```

In this example, we have a Mediator interface and a ConcreteMediator class that manages the communication between two Colleague objects. The Colleague interface and the ConcreteColleague classes define the interface of the objects that will communicate with each other through the mediator. The ConcreteColleague1 and ConcreteColleague2 classes implement the Colleague interface and communicate with other objects through the mediator.

We create the objects, set up the mediator, and then send messages between the colleagues through the mediator. The mediator handles the communication between the colleagues and ensures that they do not have to interact with each other directly.

---

One more example:

```python
import collections


def main():
    form = Form()
    test_user_interaction_with(form)


class Form:

    def __init__(self):
        self.create_widgets()
        self.create_mediator()


    def create_widgets(self):
        self.nameText = Text()
        self.emailText = Text()
        self.okButton = Button("OK")
        self.cancelButton = Button("Cancel")


    def create_mediator(self):
        self.mediator = Mediator(((self.nameText, self.update_ui),
                (self.emailText, self.update_ui),
                (self.okButton, self.clicked),
                (self.cancelButton, self.clicked)))
        self.update_ui()


    def update_ui(self, widget=None):
        self.okButton.enabled = (bool(self.nameText.text) and
                                 bool(self.emailText.text))


    def clicked(self, widget):
        if widget == self.okButton:
            print("OK")
        elif widget == self.cancelButton:
            print("Cancel")


class Mediator:

    def __init__(self, widgetCallablePairs):
        self.callablesForWidget = collections.defaultdict(list)
        for widget, caller in widgetCallablePairs:
            self.callablesForWidget[widget].append(caller)
            widget.mediator = self


    def on_change(self, widget):
        callables = self.callablesForWidget.get(widget)
        if callables is not None:
            for caller in callables:
                caller(widget)
        else:
            raise AttributeError("No on_change() method registered for {}"
                    .format(widget))


class Mediated:

    def __init__(self):
        self.mediator = None


    def on_change(self):
        if self.mediator is not None:
            self.mediator.on_change(self)


class Button(Mediated):

    def __init__(self, text=""):
        super().__init__()
        self.enabled = True
        self.text = text


    def click(self):
        if self.enabled:
            self.on_change()


    def __str__(self):
        return "Button({!r}) {}".format(self.text,
                "enabled" if self.enabled else "disabled")


class Text(Mediated):

    def __init__(self, text=""):
        super().__init__()
        self.__text = text


    @property
    def text(self):
        return self.__text


    @text.setter
    def text(self, text):
        if self.text != text:
            self.__text = text
            self.on_change()


    def __str__(self):
        return "Text({!r})".format(self.text)


def test_user_interaction_with(form):
    form.okButton.click()           # Ignored because it is disabled
    print(form.okButton.enabled)    # False
    form.nameText.text = "Fred"
    print(form.okButton.enabled)    # False
    form.emailText.text = "fred@bloggers.com"
    print(form.okButton.enabled)    # True
    form.okButton.click()           # OK
    form.emailText.text = ""
    print(form.okButton.enabled)    # False
    form.cancelButton.click()       # Cancel


if __name__ == "__main__":
    main()
```

#### Memento

The Memento pattern is a behavioral design pattern that allows capturing and restoring the state of an object without violating its encapsulation. This pattern enables an object to save its state at a certain point in time and restore that state later if needed. The Memento pattern consists of three parts: the Originator, which is the object whose state needs to be saved and restored; the Memento, which is an object that stores the state of the Originator; and the Caretaker, which is an object that is responsible for the management of the Memento.

The Memento pattern is useful in situations where you need to save and restore the state of an object, such as when implementing undo-redo functionality in an application. It helps you to achieve separation of concerns by keeping the state management separate from the object's behavior.

Python has out-of-the-box support for this pattern; using the `pickle` module, we can serialize and deserialize arbitrary Python objects (with some restrictions, such as not being able to serialize a file object).

Even in those rare cases where we run into a serialization limitation, it is always possible to add our own support for this mechanism, for example by implementing the special methods `__getstate__()` and `__setstate__()` and possibly the `__getnewargs__()` method. Similarly, if we want to use the JSON format for our classes, we can extend the encoder and decoder by looking for the `json` module.

You could come up with your own format and protocols, but this makes little sense, since Python already provides advanced support for this pattern.

Here's an example implementation of the Memento pattern in Python:

```python
"""
http://code.activestate.com/recipes/413838-memento-closure/
*TL;DR
Provides the ability to restore an object to its previous state.
"""

from copy import copy
from copy import deepcopy


def memento(obj, deep=False):
    state = deepcopy(obj.__dict__) if deep else copy(obj.__dict__)

    def restore():
        obj.__dict__.clear()
        obj.__dict__.update(state)

    return restore


class Transaction:
    """A transaction guard.
    This is, in fact, just syntactic sugar around a memento closure.
    """

    deep = False
    states = []

    def __init__(self, deep, *targets):
        self.deep = deep
        self.targets = targets
        self.commit()

    def commit(self):
        self.states = [memento(target, self.deep) for target in self.targets]

    def rollback(self):
        for a_state in self.states:
            a_state()


class Transactional:
    """Adds transactional semantics to methods. Methods decorated  with
    @Transactional will rollback to entry-state upon exceptions.
    """

    def __init__(self, method):
        self.method = method

    def __get__(self, obj, T):
        def transaction(*args, **kwargs):
            state = memento(obj)
            try:
                return self.method(obj, *args, **kwargs)
            except Exception as e:
                state()
                raise e

        return transaction


class NumObj:
    def __init__(self, value):
        self.value = value

    def __repr__(self):
        return '<%s: %r>' % (self.__class__.__name__, self.value)

    def increment(self):
        self.value += 1

    @Transactional
    def do_stuff(self):
        self.value = '1111'  # <- invalid value
        self.increment()  # <- will fail and rollback


def main():
    """
    >>> num_obj = NumObj(-1)
    >>> print(num_obj)
    <NumObj: -1>
    >>> a_transaction = Transaction(True, num_obj)
    >>> try:
    ...    for i in range(3):
    ...        num_obj.increment()
    ...        print(num_obj)
    ...    a_transaction.commit()
    ...    print('-- committed')
    ...    for i in range(3):
    ...        num_obj.increment()
    ...        print(num_obj)
    ...    num_obj.value += 'x'  # will fail
    ...    print(num_obj)
    ... except Exception:
    ...    a_transaction.rollback()
    ...    print('-- rolled back')
    <NumObj: 0>
    <NumObj: 1>
    <NumObj: 2>
    -- committed
    <NumObj: 3>
    <NumObj: 4>
    <NumObj: 5>
    -- rolled back
    >>> print(num_obj)
    <NumObj: 2>
    >>> print('-- now doing stuff ...')
    -- now doing stuff ...
    >>> try:
    ...    num_obj.do_stuff()
    ... except Exception:
    ...    print('-> doing stuff failed!')
    ...    import sys
    ...    import traceback
    ...    traceback.print_exc(file=sys.stdout)
    -> doing stuff failed!
    Traceback (most recent call last):
    ...
    TypeError: ...str...int...
    >>> print(num_obj)
    <NumObj: 2>
    """


if __name__ == "__main__":
    import doctest
    doctest.testmod(optionflags=doctest.ELLIPSIS)
```

#### Observer

The Observer pattern is a design pattern in which an object, called the subject, maintains a list of its dependents, called observers, and notifies them automatically of any state changes, usually by calling one of their methods. This allows multiple objects to be notified and updated when there is a change in the state of the subject, without the subject having to know anything about the observers.

The Observer pattern consists of two main components:

1. Subject: The subject is the object that is being observed. It maintains a list of observers and provides methods for adding and removing observers.

2. Observer: The observer is the object that is notified when the subject changes. It provides a method that the subject calls to notify it of any changes.

The benefits of using the Observer pattern include:

1. Loose coupling between the subject and the observers.
2. The ability to add and remove observers dynamically.
3. A separation of concerns between the subject and the observers.

The Observer pattern maintains many-to-many dependency relationships between objects, for example, when the state of one object changes, all related objects are notified. Today, perhaps the most common example of this pattern and its variations is the model-view-controller (MVC) paradigm. In this paradigm, the model describes the data, one or more views render the data, and one or more controllers mediate between the input (eg, user interaction) and the model. And any changes in the model are automatically reflected in the views associated with it.

The MVC approach has one popular simplification - use only models and views, but leave the views to both render the data and pass the model as inputs; in other words, views are co-located with controllers. In terms of the Observer pattern, this means that the views are observers and the model is the observed object.

Examples include triggers in databases, Django's signaling system, the signals and slots mechanism in the QT library, and the many uses of WebSockets technology.

Here is an example of implementing the Observer pattern in Python

```python
class Subject:
    def __init__(self):
        self._observers = []

    def attach(self, observer):
        self._observers.append(observer)

    def detach(self, observer):
        self._observers.remove(observer)

    def notify(self):
        for observer in self._observers:
            observer.update(self)

class ConcreteSubject(Subject):
    def __init__(self):
        super().__init__()
        self._state = None

    @property
    def state(self):
        return self._state

    @state.setter
    def state(self, value):
        self._state = value
        self.notify()

class Observer:
    def update(self, subject):
        pass

class ConcreteObserverA(Observer):
    def update(self, subject):
        print(f"ConcreteObserverA: {subject.state}")

class ConcreteObserverB(Observer):
    def update(self, subject):
        print(f"ConcreteObserverB: {subject.state}")

subject = ConcreteSubject()
observerA = ConcreteObserverA()
observerB = ConcreteObserverB()

subject.attach(observerA)
subject.attach(observerB)

subject.state = 123

subject.detach(observerB)

subject.state = "hello"
```

In this example, we have a `Subject` class that maintains a list of observers and provides methods for adding and removing observers. We also have a `ConcreteSubject` class that inherits from `Subject` and defines a state variable. Whenever the state variable is changed, the `notify()` method is called, which in turn calls the `update()` method of each attached observer.

We also have an `Observer` class that defines the `update()` method, which is called by the subject whenever there is a change in state. Finally, we have two `ConcreteObserver` classes that inherit from `Observer` and define their own implementation of the `update()` method.

When we run this code, we get the following output:

```python
ConcreteObserverA: 123
ConcreteObserverB: 123
ConcreteObserverA: hello
```

This demonstrates how both observers are notified and updated when the state of the subject changes.

#### State

The State pattern is a behavioral design pattern that allows an object to change its behavior when its internal state changes. The pattern is used to define a state machine where an object's behavior is determined by its state. The State pattern is useful when an object has multiple possible states and transitions between states are complex.

In this pattern, the state of an object is encapsulated in a separate state object, and the object delegates the behavior to the state object. The state object, in turn, can change the object's behavior by changing its state.

The State pattern consists of several components:

Context: The object that has a state and delegates the behavior to the state object.
State: The interface that defines the behavior of the object.
ConcreteState: The implementation of the State interface that defines the behavior of the object for a specific state.

The State pattern is designed to create objects whose behavior changes when the state changes; this means that the object has modes of operation. From the outside, it seems that the class of the object has changed.

There are two main approaches to handling state stored within a class. The first is the use of state-sensitive methods. The second is the use of state-defined methods

Here is an example implementation of the State pattern in Python:

```python
class State:
    def write_name(self, name):
        pass

class LowerCaseState(State):
    def write_name(self, name):
        print(name.lower())

class UpperCaseState(State):
    def write_name(self, name):
        print(name.upper())

class Context:
    def __init__(self):
        self.state = None

    def set_state(self, state):
        self.state = state

    def write_name(self, name):
        self.state.write_name(name)

# Usage
context = Context()

lowercase_state = LowerCaseState()
context.set_state(lowercase_state)
context.write_name("John")

uppercase_state = UpperCaseState()
context.set_state(uppercase_state)
context.write_name("John")
```

In this example, the `State` interface defines the `write_name` method, which is implemented by `LowerCaseState` and `UpperCaseState`. The `Context` class delegates the behavior to the current state object, which can be changed by calling `set_state`. Finally, we create an instance of the `Context` class and set its state to `LowerCaseState` and `UpperCaseState` to print the name in lower and upper case, respectively.

Another example:

```python
"""
State (State) - a pattern of behavior of objects.
Allows an object to vary its behavior based on its internal state.
From the outside, it seems that the class of the object has changed.
"""


class LampStateBase(object):
     """Lamp status"""
     def get_color(self):
         raise NotImplementedError()


class GreenLampState(LampStateBase):
     def get_color(self):
         return 'Green'


class RedLampState(LampStateBase):
     def get_color(self):
         return 'Red'


class BlueLampState(LampStateBase):
     def get_color(self):
         return 'Blue'


class Lamp(object):
     def __init__(self):
         self._current_state = None
         self._states = self.get_states()

     def get_states(self):
         return [GreenLampState(), RedLampState(), BlueLampState()]

     def next_state(self):
         if self._current_state is None:
             self._current_state = self._states[0]
         else:
             index = self._states.index(self._current_state)
             if index < len(self._states) - 1:
                 index += 1
             else:
                 index = 0
             self._current_state = self._states[index]
         return self._current_state

     def light(self):
         state = self.next_state()
         print state.get_color()


lamp = Lamp()
[lamp.light() for i in range(3)]
#Green
#Red
# Blue
[lamp.light() for i in range(3)]
#Green
#Red
# Blue
```

#### Strategy

The Strategy pattern is a behavioral design pattern that allows you to define a family of algorithms, encapsulate each one as an object, and make them interchangeable at runtime. This pattern lets the algorithm vary independently from the clients that use it.

In other words, the Strategy pattern defines a set of interchangeable algorithms, encapsulates each one as an object, and makes them available for use by a client object. The client object can then choose the appropriate algorithm for its specific needs, without needing to know the details of the algorithm's implementation.

The key components of the Strategy pattern are:

1. The Strategy interface: This defines the interface for the algorithms that will be encapsulated by the strategy objects.

2. Concrete Strategy classes: These are the various implementations of the Strategy interface.

3. The Context class: This class maintains a reference to a Strategy object and delegates some work to it.

Here is an example implementation of the Strategy pattern in Python:

```python
# Define the Strategy interface
class Strategy:
    def do_algorithm(self, data):
        pass

# Define Concrete Strategy classes
class ConcreteStrategyA(Strategy):
    def do_algorithm(self, data):
        return sorted(data)

class ConcreteStrategyB(Strategy):
    def do_algorithm(self, data):
        return reversed(sorted(data))

# Define the Context class
class Context:
    def __init__(self, strategy):
        self._strategy = strategy

    def execute_strategy(self, data):
        result = self._strategy.do_algorithm(data)
        print(result)

# Use the Context class to execute different strategies
data = [1, 5, 3, 2, 4]

context = Context(ConcreteStrategyA())
context.execute_strategy(data)  # Output: [1, 2, 3, 4, 5]

context = Context(ConcreteStrategyB())
context.execute_strategy(data)  # Output: [5, 4, 3, 2, 1]
```

In this example, we first define the `Strategy` interface which defines the method `do_algorithm()`. Then, we create two concrete strategy classes, `ConcreteStrategyA` and `ConcreteStrategyB`, which implement the `do_algorithm()` method in different ways. Finally, we define the `Context` class which maintains a reference to a strategy object and uses it to execute a specific strategy.

In the main part of the code, we create a list of numbers and use the `Context` class to execute the `ConcreteStrategyA` strategy and then the `ConcreteStrategyB` strategy on this list. The output of each strategy is printed to the console.

#### Template method

The Template Method pattern is a behavioral design pattern that allows you to define the skeleton of an algorithm in a base class, while allowing subclasses to provide specific implementations of certain steps of the algorithm. In this pattern, the base class defines the overall structure of the algorithm, including the order of steps and the flow of control, while the subclasses provide concrete implementations for certain steps. This pattern promotes code reuse and enables you to change the implementation of the individual steps without changing the overall structure of the algorithm.

The Template Method pattern involves the following components:

- Abstract Class: This is the base class that defines the overall structure of the algorithm. It contains abstract methods that represent the steps of the algorithm that the subclasses are responsible for implementing. It also contains a template method that calls these abstract methods in a specific order to carry out the algorithm.

- Concrete Class: These are the subclasses that provide concrete implementations for the abstract methods defined in the abstract class.

Here is an example implementation of the Template Method pattern in Python:

```python
from abc import ABC, abstractmethod

class AbstractClass(ABC):

    def template_method(self):
        self._step_one()
        self._step_two()
        self._step_three()

    @abstractmethod
    def _step_one(self):
        pass

    @abstractmethod
    def _step_two(self):
        pass

    @abstractmethod
    def _step_three(self):
        pass

class ConcreteClassA(AbstractClass):

    def _step_one(self):
        print("ConcreteClassA: Step 1")

    def _step_two(self):
        print("ConcreteClassA: Step 2")

    def _step_three(self):
        print("ConcreteClassA: Step 3")

class ConcreteClassB(AbstractClass):

    def _step_one(self):
        print("ConcreteClassB: Step 1")

    def _step_two(self):
        print("ConcreteClassB: Step 2")

    def _step_three(self):
        print("ConcreteClassB: Step 3")

def client_code(abstract_class):
    abstract_class.template_method()

client_code(ConcreteClassA())
client_code(ConcreteClassB())
```

In this example, we define an abstract class `AbstractClass` that contains the `template_method()` which calls the abstract methods `_step_one()`, `_step_two()`, and `_step_three()`. The `ConcreteClassA` and `ConcreteClassB` are the concrete implementations of the abstract methods `_step_one()`, `_step_two()`, and `_step_three()`. The `client_code()` function takes an object of the `AbstractClass` as its argument and calls its `template_method()` method to execute the algorithm.

When we run this code, we get the following output:

```python
ConcreteClassA: Step 1
ConcreteClassA: Step 2
ConcreteClassA: Step 3
ConcreteClassB: Step 1
ConcreteClassB: Step 2
ConcreteClassB: Step 3
```

As we can see, the `template_method()` in the `AbstractClass` defines the overall structure of the algorithm, while the concrete implementations in `ConcreteClassA` and `ConcreteClassB` provide the specific steps for the algorithm. This allows us to reuse the code in `AbstractClass` for multiple implementations, and also makes it easy to modify the specific steps without changing the overall structure of the algorithm.

#### Visitor

The Visitor pattern is a behavioral design pattern that separates the algorithm from the object structure on which it operates. It defines a way to add new operations to existing object structures without modifying those structures. The pattern is useful when you have a complex object structure and you want to perform various operations on its elements without cluttering them with those operations.

In the Visitor pattern, you define a Visitor interface with a visit() method for each element of the object structure. Each ConcreteVisitor implements the visit() method for a specific type of element. The object structure is composed of elements that implement an accept() method that takes a Visitor as an argument. When the accept() method is called on an element, it calls the appropriate visit() method on the Visitor, passing itself as an argument.

The Visitor pattern is useful when you have a complex object structure that is difficult to change and you want to add new operations to it. The pattern makes it easy to add new operations to existing object structures without modifying those structures. However, the pattern can be complex and requires a lot of code, especially if you have many types of elements in your object structure.

The Visitor pattern is used when you need to apply some function to each element of a collection or aggregator object. This is not the same as the typical use of the Iterator pattern - where we iterate over a collection or aggregate and call some method on each element - because in the "visitor" case, the external function is called, not the method.

Python has built-in support for this pattern. For example, the construction `new_list = map(function, old_sequence)` means that `function()` is called for each element of `old_sequence`, resulting in a `new_list`

Here's an example implementation of the Visitor pattern in Python:

```python
class Element:
    def accept(self, visitor):
        visitor.visit(self)

class ConcreteElementA(Element):
    def operationA(self):
        pass

class ConcreteElementB(Element):
    def operationB(self):
        pass

class Visitor:
    def visitConcreteElementA(self, element):
        pass

    def visitConcreteElementB(self, element):
        pass

class ConcreteVisitorA(Visitor):
    def visitConcreteElementA(self, element):
        element.operationA()

    def visitConcreteElementB(self, element):
        pass

class ConcreteVisitorB(Visitor):
    def visitConcreteElementA(self, element):
        pass

    def visitConcreteElementB(self, element):
        element.operationB()

# Usage
elements = [ConcreteElementA(), ConcreteElementB()]

visitorA = ConcreteVisitorA()
for element in elements:
    element.accept(visitorA)

visitorB = ConcreteVisitorB()
for element in elements:
    element.accept(visitorB)
```

In this example, the Element interface defines the accept() method that takes a Visitor as an argument. The ConcreteElementA and ConcreteElementB classes implement the Element interface and provide their own operations.

The Visitor interface defines the visit() method for each type of ConcreteElement. The ConcreteVisitorA and ConcreteVisitorB classes implement the Visitor interface and provide their own implementations of the visit() method for each type of ConcreteElement.

Finally, we create a list of ConcreteElements and pass each one to a ConcreteVisitor. The accept() method is called on each ConcreteElement, passing in the appropriate ConcreteVisitor. The ConcreteVisitor's visit() method is called on each ConcreteElement, performing the appropriate operation.

Another example:

```python
"""
Visitor - a pattern of behavior of objects.
Describes an operation to be performed on each object in some structure.
The visitor pattern allows you to define a new operation without changing the classes of these objects.
"""


class FruitVisitor(object):
     """Visitor"""
     def draw(self, fruit):
         methods = {
             Apple: self.draw_apple,
             Pear: self.draw_pear,
         }
         draw = methods.get(type(fruit), self.draw_unknown)
         draw(fruit)

     def draw_apple(self, fruit):
         print 'Apple'

     def draw_pear(self, fruit):
         print 'Pear'

     def draw_unknown(self, fruit):
         print 'Fruit'


class Fruit(object):
     """Fruits"""
     def draw(self, visitor):
         visitor draw(self)


class Apple(Fruit):
     """Apple"""


class Pear(Fruit):
     """Pear"""


class Banana(Fruit):
     """Banana"""


visitor = FruitVisitor()

apple = apple()
apple.draw(visitor)
# Apple

pear = pear()
pear.draw(visitor)
# Pear

banana = banana()
banana draw(visitor)
# Fruit
```

#### Behavioral patterns. Outcome

Some behavioral patterns are directly supported in Python; the rest are easy to implement yourself. The Chain of Responsibility, Mediator, and Observer patterns can be implemented in the traditional way or with coroutines, and they are all variations on the theme of decoupling communication between cooperating objects. The Command pattern can be used for lazy evaluation and implementation of the execute-cancel mechanism. Since Python is an interpreted language (at the bytecode level), the Interpreter pattern can be implemented using Python itself, and even isolate the interpreted code in a separate process. Support for the Iterator pattern (and - implicitly - for the Visitor pattern) is built into Python. The Memento pattern is well supported in the Python standard library (for example, using the `pickle` and `json` modules). The State, Strategy, and Template Method patterns do not have direct support, but they are all easy to implement.

## LRU Cache. What is it

- [LRU, cache eviction method(rus)](https://habr.com/en/post/136758/)

LRU (Least Recently Used) Cache is a caching technique that stores a limited number of items in memory and removes the least recently used item when the cache reaches its limit. It is based on the assumption that if an item has not been accessed recently, it is less likely to be accessed again in the near future.

In an LRU cache, each item has a time stamp that is updated whenever it is accessed. When a new item is added to the cache, if the cache is already at its limit, the least recently used item is removed to make room for the new item. This ensures that the most recently used items are always available in the cache, while the least recently used items are removed.

Here's an example implementation of an LRU cache in Python using the `collections.OrderedDict` class:

```python
from collections import OrderedDict

class LRUCache:
    def __init__(self, capacity):
        self.capacity = capacity
        self.cache = OrderedDict()

    def get(self, key):
        if key not in self.cache:
            return -1
        value = self.cache.pop(key)
        self.cache[key] = value
        return value

    def put(self, key, value):
        if key in self.cache:
            self.cache.pop(key)
        elif len(self.cache) >= self.capacity:
            self.cache.popitem(last=False)
        self.cache[key] = value
```

In this implementation, `capacity` is the maximum number of items that can be stored in the cache. The `cache` is an ordered dictionary where the keys are the cache keys and the values are the cache values.

The `get` method returns the value associated with the given key if it exists in the cache, otherwise it returns -1. When the value is accessed, it is moved to the end of the ordered dictionary to mark it as the most recently used.

The `put` method adds a new key-value pair to the cache. If the key already exists, the existing value is updated and moved to the end of the ordered dictionary. If the cache is already at capacity, the least recently used item (i.e., the item at the beginning of the ordered dictionary) is removed to make room for the new item. Finally, the new key-value pair is added to the end of the ordered dictionary to mark it as the most recently used.

## MQ. What is it

MQ, or message queue, is a communication pattern that enables different parts of a software system to communicate with each other asynchronously. It works by sending messages between separate components of a system via a message broker, which acts as a middleman between senders and receivers.

In MQ, the sender and the receiver do not interact with each other directly; instead, they interact with the message broker, which is responsible for delivering the message to the appropriate receiver. The message broker ensures that messages are delivered in the order they were received, and it can also handle cases where the receiver is temporarily unavailable or busy.

MQ is particularly useful in distributed systems, where components are distributed across multiple machines or networks. It enables these components to communicate with each other in a reliable and scalable way, without requiring direct connections between all components.

Here's an example implementation of MQ using the Python library pika:

```python
import pika

# Connect to the message broker
connection = pika.BlockingConnection(pika.ConnectionParameters('localhost'))
channel = connection.channel()

# Create a message queue called "hello"
channel.queue_declare(queue='hello')

# Define a callback function to handle incoming messages
def callback(ch, method, properties, body):
    print("Received message:", body)

# Start consuming messages from the "hello" queue
channel.basic_consume(queue='hello', on_message_callback=callback, auto_ack=True)

print("Waiting for messages...")

# Start the event loop to receive messages
channel.start_consuming()
```

In this example, we first establish a connection to the message broker using pika. We then declare a message queue called "hello". We define a callback function to handle incoming messages, and start consuming messages from the "hello" queue using basic_consume. Finally, we start the event loop to receive messages.

To send a message to this queue, we can use the following code:

```python
# Connect to the message broker
connection = pika.BlockingConnection(pika.ConnectionParameters('localhost'))
channel = connection.channel()

# Send a message to the "hello" queue
channel.basic_publish(exchange='', routing_key='hello', body='Hello, world!')

print("Sent message: 'Hello, world!'")

# Close the connection
connection.close()
```

This code connects to the message broker, sends a message to the "hello" queue using basic_publish, and then closes the connection. When we run the consumer code, it will print out "Received message: Hello, world!" to the console.

Message queues are essentially the link between the various processes in your applications and provide a robust and scalable interface for interacting with other connected systems and devices.
A queue is a data structure with a first-in-first-out element access discipline. Adding an element is possible only to the end of the queue, selecting only from the beginning of the queue, while the selected element is removed from the queue.

Ten reasons why message queues are a vital component for any architecture or application:

- _Loose binding_ - message queues create implicit data exchange interfaces that allow processes to be independent of each other, i.e. you simply define the format of messages sent from one process to another.
- _Redundancy_ - Queues allow you to avoid cases of wasteful use of process resources (for example, memory) as a result of storing raw (redundant) information.
- _Scalability_ - message queues allow you to distribute information processing processes. Thus, they make it easy to scale up the speed at which messages are added to the queue and processed.
- _Elasticity and the ability to withstand peak loads_ - message queues can act as a kind of buffer for the accumulation of data in the event of a peak load, thereby mitigating the load on the information processing system and preventing its failure.
- _Fault Tolerance_ - Message queues allow you to separate processes from each other, so that if the process that processes messages from the queue crashes, then messages can be added to the queue for processing later, when the system recovers.
- _Guaranteed delivery_ - using the message queue guarantees that the message will be delivered and processed in any case (as long as there is at least one handler).
- _Guaranteed delivery order_ - most message queuing systems are able to provide guarantees that data will be processed in a certain order (most often in the order in which they arrived).
- _Buffering_ - message queues allow you to send and receive messages while working with maximum efficiency, offering a buffer layer - the process of writing to the queue can be as fast as the message queue is able to do, and not the message handler.
- - Understanding data flows \* - message queues allow you to identify bottlenecks in application data flows, you can easily determine which of the queues is clogged, which is idle and determine what needs to be done - add new message handlers or optimize the current architecture.
- _Asynchronous Communication_ - Message Queues provide an asynchronous data processing capability that allows you to put a message on a queue without processing, allowing the system to process the message later when it can.

## What ready-made MQ implementations do you know

- [RabbitMQ vs. Kafka: two different approaches to messaging(rus)](https://habr.com/ru/company/itsumma/blog/416629/)
- [Kafka VS RabbitMQ(rus)](https://medium.com/@vozerov/kafka-vs-rabbitmq-38e221cf511b)
- [Selecting MQ for a high-load project(rus)](https://habr.com/en/post/326880/)

There are many ready-made Message Queue (MQ) implementations available, both open-source and commercial. Some popular examples include:

1. RabbitMQ - an open-source message broker that implements the Advanced Message Queuing Protocol (AMQP) and supports multiple messaging protocols.
2. Apache ActiveMQ - an open-source message broker that supports a wide range of messaging protocols and integrates with other Apache projects such as Camel, CXF, and Karaf.
3. IBM MQ - a commercial message broker that supports a range of messaging protocols and provides high availability and scalability features.
4. Amazon Simple Queue Service (SQS) - a cloud-based message queue service provided by Amazon Web Services (AWS).
   Google Cloud Pub/Sub - a cloud-based message queue service provided by Google Cloud Platform (GCP).
5. Microsoft Azure Service Bus - a cloud-based messaging service provided by Microsoft Azure.

6. RedisQueue

7. Kafka

8. rocketMQ

9. zeroMQ

These are just a few examples of the many available options for implementing a message queue system. The choice of implementation will depend on the specific requirements of the project, such as the scale of the application, the desired level of availability and reliability, and the need for specific features and integrations.

## What is RPC

Remote procedure call, less commonly Remote Procedure Call (RPC) is a class of technologies that allow computer programs to call functions or procedures in a different address space (on remote computers or in an independent third-party system on the same device). Typically, the implementation of RPC technology includes two components: a network protocol for client-server communication and an object (or structure, for non-objective RPC) serialization language. At the transport layer, RPCs use mainly TCP and UDP protocols, however, some are built on top of HTTP (which violates the ISO / OSI architecture, since HTTP is not originally a transport protocol).

The salient features of a remote procedure call are:

- Asymmetry, that is, one of the interacting parties is the initiator;
- Synchronicity, that is, the execution of the calling procedure is suspended from the moment the request is issued and resumes only after the return from the called procedure.

In Python, there are several libraries that provide implementation of RPC protocols. One of the most popular is the Pyro4 library. Pyro4 allows developers to expose Python objects and methods as remote procedures that can be called from other processes, or even from other machines over a network.

## What is gRPC

- [Python Microservices With gRPC](https://realpython.com/python-microservices-grpc/)

gRPC is a high-performance, open-source, remote procedure call (RPC) framework that was originally developed by Google. It is designed to allow communication between microservices in a distributed system and is based on the Protocol Buffers data serialization format.

gRPC supports various programming languages, including Python, and offers features such as bi-directional streaming, flow control, and built-in authentication and load balancing. It uses HTTP/2 for transport and supports different types of communication patterns such as unary, server streaming, client streaming, and bidirectional streaming.

gRPC offers a simple and easy-to-use API for defining services and messages, which can be used to generate client and server code in various programming languages. It also offers features such as interceptors and middleware for extending and customizing the behavior of the framework.

Out of the box has:

- Protobuf as a tool for describing data types and serialization. Very cool and well-proven thing in practice. As a matter of fact, those who needed performance used to take Protobuf before, and then they bothered separately with transport. Now everything is included.
- HTTP/2 as transport. And this is an incredibly powerful move! All the charm of full data compression, traffic control, initiation of events from the server, reusing one socket for several parallel requests is beauty.
- Static paths - no more "service/collection/resource/request? parameter=value". Now only a "service", and what's inside - describe in terms of your model and its events.
- No binding of methods to HTTP methods, no binding of return values to HTTP statuses. Write what you want.
- SSL / TLS, OAuth 2.0, authentication through Google services, plus you can screw your own (for example, two-factor)
- Support for 9 languages: C, C++, Java, Go, Node.js, Python, Ruby, Objective-C, PHP, C# plus, of course, no one forbids you to take and implement your own version even for brainfuck.
- Support for gRPC in public APIs from Google. Already working for some services. No, REST versions, of course, will also remain. But judge for yourself, if you have a choice - use, say, a REST version from a mobile application that returns data in 1 second, or take a gRPC version that works 0.5 seconds with the same development costs - what will you choose? What will your competitor choose?

# Frontend

## What is html and css and their basic concepts

HTML (Hypertext Markup Language) and CSS (Cascading Style Sheets) are the two foundational technologies used for creating websites. HTML is used to structure content on a web page, while CSS is used to style and layout that content.

HTML is a markup language that uses a set of tags to define the structure and content of a web page. It provides a way to create headings, paragraphs, lists, images, and links on a web page. HTML tags are used to define the structure of a page, including headings, paragraphs, and lists, and can also be used to embed images and videos, create forms, and more.

CSS, on the other hand, is used to style and layout the content defined by HTML. It is a language that allows web developers to define colors, fonts, sizes, spacing, and more. CSS uses selectors to target specific HTML elements and apply styling rules to them. For example, a developer might use a CSS selector to target all of the headings on a web page and define their font size and color.

Both HTML and CSS are essential for creating modern web pages that are both visually appealing and easy to navigate. By separating the content and structure of a web page from its presentation, developers can create flexible, responsive designs that work well on a wide range of devices and screen sizes.

Some basic concepts of HTML include:

- Tags: HTML tags are used to define the structure and content of a web page. They are enclosed in angle brackets (<>) and typically come in pairs, with the opening tag defining the beginning of an element and the closing tag defining the end of that element.
- Attributes: HTML attributes provide additional information about an element, such as its ID, class, or style.
- Elements: HTML elements are composed of a pair of tags (opening and closing) that define a specific part of a web page's structure and content.
- Nesting: HTML elements can be nested inside one another to create a hierarchical structure for a web page.

Some basic concepts of CSS include:

- Selectors: CSS selectors are used to target specific HTML elements and apply styling rules to them. Selectors can be based on element type, class, ID, attribute, or relationship to other elements.
- Properties: CSS properties define the specific style rules to be applied to an HTML element. They include properties for color, font, size, margin, padding, and more.
- Values: CSS values define the specific settings for each property, such as a color value or a size value.
- Cascade: CSS styles can be inherited from parent elements and overridden by more specific selectors or inline styles. The order of precedence for CSS rules is known as the cascade.
  Overall, HTML and CSS are essential tools for any web developer, whether working on the frontend or the backend of a website. A solid understanding of these technologies is crucial for creating effective, responsive web designs that look great and function well for users.

## What is Javascript and what are its basic concepts. How does it interact with Python

JavaScript is a scripting language used primarily for creating dynamic web content and client-side scripting on web pages. It is a high-level, interpreted language that runs in a browser and is designed to be lightweight and easy to use. JavaScript has several important concepts, including variables, data types, functions, conditionals, loops, objects, and arrays.

Variables in JavaScript are used to store data values, and data types include strings, numbers, booleans, and objects. Functions are blocks of code that can be called upon to perform specific tasks, and conditionals and loops are used to control the flow of the program based on certain conditions or for repeating code.

Python and JavaScript can also communicate with each other through APIs or web services.

In summary, JavaScript is a programming language used for client-side scripting on web pages, and it has several important concepts including variables, data types, functions, conditionals, loops, objects, and arrays. CSS is a stylesheet language used to describe the presentation of HTML or XML documents, including layouts and visual effects. Python and JavaScript can interact with each other through various methods, including using a server-side language, libraries, or APIs.

## What is AJAX and how does it interact with python

Ajax stands for Asynchronous JavaScript and XML. It's a technique used in web development to make asynchronous requests to a web server using JavaScript and retrieve data without the need to reload the entire web page.

In an Ajax request, JavaScript code sends a request to the web server and receives a response in the background without requiring the user to manually refresh the page. This can greatly improve the user experience by making web applications more responsive and interactive.

Python can be used on the server-side to process Ajax requests and respond with the required data. For example, a Python web application may have a URL endpoint that responds to an Ajax request with a JSON object containing data requested by the user. Python web frameworks such as Flask and Django have built-in support for handling Ajax requests and returning responses in various formats such as JSON or XML.

Overall, Ajax is a powerful technique for building interactive and dynamic web applications, and it can be used effectively in combination with Python on the server-side to create high-performance web applications.

## What is api. In what format is the data exchanged between the Server and the Client

An API, or Application Programming Interface, is a set of protocols and tools that allow different software applications to communicate with each other. It specifies how software components should interact and what data should be exchanged between them. APIs are often used by web developers to allow third-party applications to access their web services or data.

The data exchanged between the server and the client through an API is typically in a standardized format such as JSON (JavaScript Object Notation) or XML (eXtensible Markup Language). JSON is a lightweight data format that is easy to read and write, and is often used by APIs built with JavaScript or Python. XML is a more verbose format that is used in some legacy systems.

When a client application makes a request to an API, it sends a request to the server with specific parameters or data. The server then processes the request and returns a response in the specified data format. The client application can then use the response data in its own application or display it to the user.

## What format is the data in json

Data in JSON (JavaScript Object Notation) format is in the form of a text string that contains structured data in the format of key-value pairs. They can be represented as arrays or objects, which can contain other arrays and nested objects.

An example of a JSON object representing information about a person:

```json
{
  "name": "John Smith",
  "age": 35,
  "address": {
    "street": "123 Main St",
    "city": "Anytown",
    "state": "CA",
    "zip": "12345"
  },
  "phoneNumbers": [
    {
      "type": "home",
      "number": "555-555-1234"
    },
    {
      "type": "work",
      "number": "555-555-5678"
    }
  ]
}
```

## What are media queries in CSS and what are they used for?

Media queries in CSS is a technique that allows you to change styles depending on the characteristics of the device on which the web page is displayed. This allows you to create responsive websites that can be optimized for different screens and different types of devices such as desktops, laptops, tablets and smartphones.

Media queries allow you to set different CSS properties for different types of devices. For example, you can change the size of the text, background, position of elements, and so on. depending on the screen size of the device on which the page is displayed.

```css
@media (max-width: 600px) {
  body {
    font-size: 14px;
    background-color: #f2f2f2;
  }
}
```

Python is used most often on the server side of web development and is not directly related to media queries. However, on the server side, it is possible to generate HTML code using media queries, depending on the type of device on which the page is displayed.

## What are cookies. Why they are, how to work with them and where they are stored

Cookies are small text files that are stored on a user's computer by a web browser when they visit a website. They are used to store information about the user's browsing behavior and preferences, such as login credentials, shopping cart contents, and language preferences.

Cookies work by being sent from the web server to the user's browser, where they are stored on the user's computer. When the user visits the same website again, the browser sends the cookies back to the server along with the user's request. This allows the server to remember information about the user and customize their experience.

There are two main types of cookies: session cookies and persistent cookies. Session cookies are temporary and are deleted when the user closes their browser, while persistent cookies are stored on the user's computer for a specified period of time.

To work with cookies in web development, developers use the document.cookie object in JavaScript to create, read, and delete cookies. Cookies can also be set and managed on the server-side using various programming languages such as Python.

Cookies are stored in a specific location on the user's computer depending on the browser and operating system being used. In general, they are stored in a browser's "cookie jar" which is a database of cookies. The location of this cookie jar varies by browser and operating system.

## Can the server change (add, remove) cookies

Yes, the server can change, add, or remove cookies. When the client makes a request to the server, it sends the cookies that are stored for that domain. The server can then read, modify, or delete the cookies and send back the updated cookies in the response headers.

To modify or delete a cookie, the server sends a new cookie with the same name as the existing cookie, but with updated or empty values, and with the same expiration and domain attributes as the original cookie. When the client receives the new cookie, it replaces the old cookie with the updated one or deletes it if the new cookie has an empty value.

It's worth noting that some browsers may restrict or block the modification of cookies through HTTP headers for security reasons, such as the HttpOnly flag. In that case, the server can still modify cookies through JavaScript using the document.cookie property.

## What is JWT (JSON Web Token)

A JSON Web Token, or JWT (pronounced "jot"), is a standardized, in some cases signed, and/or encrypted data packaging format that is used to securely transfer information between two parties.

JWT defines a specific structure of information that is sent over the network. It comes in two forms, serialized and deserialized. The first is used directly to transfer data with requests and responses. On the other hand, in order to read and write information to a token, it needs to be deserialized.

JWT stands for JSON Web Token. It’s one of the most used means of authentication in web applications but also helps with authorization and information exchanges.

According to RFC 7519, a JWT is a JSON object defined as a safe way of transmitting information between two parties. Information transmitted by JWT is digitally signed so it can be verified and trusted.

A JWT contains three parts—a header (x), a payload (y), and a signature (z)—that are separated by a dot:

> xxxxx.yyyyy.zzzzz

- Header
  The header of the JWT consists of two parts: the type of token and the signing algorithm being
  used. The signing algorithm is used to ensure that the message is authentic and not altered. Here’s an example of a header:

```json
{
  "alg": "RSA",
  "typ": "JWT"
}
```

Signing algorithms are algorithms used to sign tokens issued for your application or API.

- Payload
  The payload is the second part that contains the claims. According to the official JWT documentation (https://jwt.io/introduction), claims are statements about an entity (typically, the user) and additional data.
  Here’s an example of a payload:

```json
{
  "id": "d1397699-f37b-4de0-8e00-948fa8e9bf2c",
  "name": "John Doe",
  "admin": true
}
```

In the preceding example, we have three claims: the ID of the user, the name of the user, and also a Boolean for the type of user.

- Signature
  The signature of a JWT is the encoded header, the encoded payload plus a secret, and an
  algorithm specified in the header, all of them combined and signed.
  For example, it’s possible to create a signature the following way using the RSA algorithm:

```json
RSA(
  base64UrlEncode(header) + "." +
  base64UrlEncode(payload),
  secret)
```

The role of the signature is to track whether information has been changed.

Each time a user successfully logs in, a JWT is created and returned. The JWT will be represented as credentials used to access protected resources. The fact that it’s possible to store data in a JWT makes it vulnerable. That’s why you should specify an expiration time when creating a JWT.
To make it simple, two types of tokens:

- An access token: Used to access resources and handle authorization
- A refresh token: Used to retrieve a new access token
  But why use two tokens? As we stated earlier, a JWT is generated when users log in. Moreover, JWTs used to access resources should have a short lifespan. This means that after the JWT has expired, the user has to log in again and again – and no user wants the login page to appear every 5 minutes.
  That’s where a refresh token is useful. It’ll contain the essential information needed to verify the user and generate a new access token.

# SDLC

SDLC stands for Software Development Life Cycle, which is a process used by software development teams to design, develop, test, and deploy software. It is a structured approach to software development that helps teams to produce high-quality software that meets the requirements of stakeholders.

The SDLC process typically consists of several stages, each with its own set of activities and deliverables. The stages may vary depending on the methodology being used, but the most commonly used stages are:

1. Planning: In this stage, the project goals and objectives are defined, and the project team is assembled. The project scope is also defined, and the feasibility of the project is evaluated.

2. Requirements gathering: In this stage, the project team works with stakeholders to gather and document the requirements for the software.

3. Design: In this stage, the project team creates the architecture and design of the software, including the user interface, data structures, and algorithms.

4. Development: In this stage, the project team writes the code for the software, following the design specifications.

5. Testing: In this stage, the software is tested to ensure that it meets the requirements and is free of defects.

6. Deployment: In this stage, the software is released to the end-users, either in a production or test environment.

7. Maintenance: In this stage, the project team provides ongoing support and maintenance for the software, including bug fixes, updates, and enhancements.

Each stage of the SDLC process is important for producing high-quality software that meets the requirements of stakeholders. By following a structured approach to software development, teams can ensure that the software is developed efficiently, on time, and within budget.

## What is CI/CD. What is the difference between CI and CD

CI/CD stands for Continuous Integration and Continuous Delivery/Deployment. It is a set of practices used by software development teams to automate the process of building, testing, and deploying software.

Continuous Integration (CI) is the practice of regularly merging code changes from multiple developers into a central repository, where automated builds and tests are run to ensure that the code is functional and compatible with other parts of the system. The goal of CI is to catch and fix errors as early as possible in the development process, to reduce the risk of bugs and conflicts arising later on.

**Continuous integration (continuous integration)**
Continuous integration is as follows: all changes made to the code are merged in the central repository (the operation is called "merge"). The merge occurs several times a day, and after each merge in a particular project, an automatic build and test is triggered.

It happens that before building and testing the program needs to be compiled (this depends on the language in which it is written). Today, there is an increasing need to package an application in a Docker container. Automated tests then check specific code modules, UI performance, application performance, API robustness, and more. All of these steps collectively are commonly referred to as “builds.”

CI is a kind of safety net that allows developers to avoid a lot of problems before the project is delivered.

Continuous Delivery (CD) and Continuous Deployment (CD) are practices that build on top of CI. Continuous Delivery is the practice of automating the release of software to production, so that it is always in a deployable state. This means that the software can be released to production at any time, with a low risk of introducing bugs or causing downtime.

**Continuous delivery (continuous delivery)**
Continuous delivery is the practice of automating the entire software release process. The idea is to do CI, plus automatically prepare and push the release to production. In doing so, it is desirable to achieve the following: anyone with sufficient privileges to deploy a new release can deploy at any time, and this can be done in a few clicks. The programmer, getting rid of almost all manual work, works more productively.

Typically, the continuous delivery process requires at least one manual step: approve the deployment to production and run it. In complex systems with many dependencies, the continuous delivery pipeline may include additional manual or automated steps.

Continuous Deployment, on the other hand, is the practice of automatically deploying changes to production as soon as they pass the automated tests. This means that changes are released to production as soon as they are ready, without any manual intervention.

**Continuous deployment**
Continuous Deployment sits "a layer above" Continuous Delivery. In this case, all changes made to the source code are automatically deployed to production, without an explicit signal from the developer. As a rule, the task of the developer comes down to checking the pull request from a colleague and informing the team about the results of all important events.

Continuous deployment requires that the team has a well-functioning monitoring culture, everyone knows how to keep abreast and quickly restore the system.

Developers who practice CI and want to move to continuous deployment automate the deployment to a test environment to begin with, while deploying to production continues to be done manually - with one click.

The main difference between CI and CD is that CI focuses on ensuring that code changes are functional and compatible with the rest of the system, while CD focuses on automating the process of releasing changes to production. CD can be further divided into Continuous Delivery and Continuous Deployment, with the former focusing on automating the release process and the latter focusing on fully automating the deployment process.

Overall, CI/CD is a powerful set of practices that can help software development teams to improve their development process, reduce errors, and increase the speed and frequency of releases.
**Summary:**

- Continuous integration (CI): short-lived feature branches, the team merges them with the main development branch several times a day, build and test processes are fully automated, we have the result within 10 minutes; deployment is done manually.
- Continuous Delivery (CD): automates CI + the entire software release process. It may consist of several stages. Deployment to production is done manually.
- Continuous Deployment: CI + CD + fully automated production deployment.

## What is the difference between Scrum and Kanban

- [Scrum vs Kanban: what is the difference and what to choose?(rus)](https://habr.com/ru/company/hygger/blog/351048/)

Scrum and Kanban are representatives of the Agile family of methodologies. Both are considered flexible and iterative.

More than 17 years ago, IT development leaders formulated the Agile manifesto. The main points of the manifesto are:

People and interactions are more important than processes and tools.
Working software is more important than comprehensive documentation.
Collaboration with the customer is more important than contract negotiation.
Responding to change is more important than following a plan.
The basis of Scrum consists of short iterations or sprints, usually 2-3 weeks long. Before the start of the sprint, the team itself forms a list of features for the iteration, and then the sprint starts.

After the sprint is completed, completed features are uploaded to production, and unfinished features are transferred to another sprint. As a rule, the features that are being worked on during the sprint do not change: what was at the start of the sprint must be done at all costs by the end of the sprint.

Kanban provides more flexibility, if flexibility is understood as the frequency of changing priorities. Yesterday, you uploaded a new feature to production, and today you received data from the forefront and found out that this thing does not work as intended – people do not click the "buy" button. You "give a slap on the wrist" to the UX designer, he gives you new requirements. You move this task to the top of the queue, the programmer takes this task "from the top", completes it, and by the evening, the fix is already on production, and conversion rates have increased by 12%. This is a victory.

The main difference between Scrum and Kanban is in the length of the iterations. In Scrum, iterations are 2 weeks long, and in Kanban, you can "push" tasks to the programmer every day.

In Scrum, it is customary to evaluate tasks in Story points or hours. Without evaluation, it is impossible to form a sprint: we need to know if we can complete tasks within 2 weeks. After 2 weeks, we receive valuable statistics – how many hours or Story points the team was able to complete during the sprint. Velocity is the team's productivity for one sprint. This parameter allows the Scrum manager to predict where the team will be in 2 weeks.

In Kanban, evaluation is not customary. This is optional, the team decides for themselves. There is no concept of "team work velocity" here, only the average time for a task is considered. This time is calculated using a special report - Cycle Time.

So, in Scrum, our goal is to finish the sprint, and in Kanban, it is the task.

Scrum is like a bus that stops only at certain stops, where people get off in groups. And Kanban is like a minibus: if a passenger wants to get off, he asks the driver and gets off where he needs to.

## What is Code Debt and how to work with it

Code debt, also known as technical debt, refers to the accumulated cost of maintaining and updating software that was developed with inefficient or outdated code. It is a metaphorical term that compares it to financial debt. Just like financial debt, code debt accumulates interest over time, and the longer it remains unpaid, the more it costs to resolve.

Code debt can be the result of a variety of factors, such as using shortcuts during development, not keeping up with changes in technology, neglecting code refactoring, and so on. It is often the result of the need to deliver software quickly or the desire to add new features without considering the long-term consequences.

Dealing with code debt can be challenging, but it is an essential task to maintain the health and quality of software systems. There are several strategies to deal with code debt:

Refactor the code: Refactoring involves improving the design and structure of the code without changing its functionality. This can help simplify the code, remove redundant or duplicate code, and make it easier to maintain and update.

Prioritize code debt: Identify the parts of the codebase that are causing the most problems or are most critical to the business. Prioritizing code debt can help focus efforts and resources where they are most needed.

Establish coding standards: Consistent coding standards can help prevent code debt from accumulating in the first place. This includes using best practices, following coding conventions, and enforcing code reviews.

Plan for code maintenance: Building time into development schedules for regular maintenance and updates can help prevent code debt from becoming unmanageable.

Automate testing: Automated testing can help detect issues early and ensure that changes don't introduce new problems.

Educate the team: Educating the team on the importance of maintaining code quality and addressing code debt can help create a culture of continuous improvement.

In summary, code debt can be a significant problem for software systems, but it is possible to manage and reduce its impact. By prioritizing code debt, establishing coding standards, planning for maintenance, and educating the team, organizations can maintain the quality of their software systems and avoid the negative consequences of code debt accumulation.

In the classical sense, i.e. in the form in which this metaphor was described by Ward Cunningham, technical debt is understood as a conscious trade-off decision, when the customer and key developers clearly understand all the benefits of a quick, albeit not ideal, technical solution that will have to be paid for later. And while it may sound crazy to many developers, a bad decision can be a good one, but it is actually quite possible: if a short-term solution allows the company to gain visible advantages, release a product before competitors, satisfy a key customer, or some other way to gain advantages over competitors, then such a decision is completely justified. Sometimes this may be the only way for a long-term perspective to exist at all.

Technical debt in the classical sense is intentional and mainly concerns strategic decisions, therefore, the responsibility for it lies with customers, seasoned leads, architects and even PMs, but everything related to dirty code concerns mostly ordinary developers. In fact, the difference between messy code and a suboptimal policy decision isn't really all that big: when you add a new feature to a system, you have to pay the price of past shortsightedness.

Paying interest on technical debt is easier if you start thinking about it at the stage of creating a product.

- Make one-time MVP prototypes and include only confirmed hypotheses into work.
- Create an architecture that will be easy to change: microservices, versioned APIs.
- Refuse to organize your own server rooms in favor of cloud solutions. For example, Microsoft Azure, AWS Amazon Cloud, Yandex.Cloud, cloud from Mail.ru, and so on.
- Set a clear definition of done in the team, including quality metrics. It helps a lot to include a clause in the DOD that excludes the "acceptance" of a feature if there are bugs associated with it.
- It is good for MVP to design the system in such a way that the migration of users from prototypes to the stable part is imperceptible.

Companies deal with technical debt in different ways. There are three main strategies.

- Rewrite everything from scratch. This is the ultimate way to keep the system in a state where it is constantly ready for change if things have gone too far and the former flexibility is no longer there.
- Do gradual refactoring. Tasks for technical debt are sent to the backlog along with product tasks. This slows down the work on rolling out new features, but the business usually makes compromises.
- Reconcile with technical debt. If you don’t have a startup, but you need updates every six months, then you can simply put up with the fact that the code is not optimal, and act on the principle “it works, don’t touch it.” As soon as you realize that you made a mistake, you will somehow move to point 1.

# VCS

VCS, or Version Control System, is a software tool used in programming and software development to manage changes made to source code over time. It helps developers keep track of changes to the codebase, collaborate with other developers, and revert to earlier versions of the code when necessary.

VCS allows developers to create a history of changes made to the codebase, providing a complete record of every modification, who made it, and when it was made. This enables developers to easily track down and fix bugs, as well as to collaborate on larger coding projects without accidentally overwriting each other's work.

There are two main types of VCS: centralized and distributed. In a centralized VCS, there is a central server that stores the codebase, and developers check out and check in code changes to this central repository. Examples of centralized VCS include SVN (Subversion) and CVS (Concurrent Versions System).

In a distributed VCS, each developer has a complete copy of the codebase on their local machine, and changes can be synchronized between repositories. Examples of distributed VCS include Git and Mercurial.

One of the key benefits of using VCS is the ability to create branches. Branches are copies of the codebase that can be modified independently of the main codebase, allowing developers to work on new features or bug fixes without affecting the stability of the main codebase. When the new code is tested and stable, it can be merged back into the main codebase.

VCS also allows for easy collaboration among team members. Developers can work on their own branches, share code with other developers, and merge their changes back into the main codebase. VCS systems also provide tools for resolving conflicts when two developers have made changes to the same file.

Overall, VCS is a critical tool for software development and programming, allowing developers to keep track of changes to the codebase and collaborate effectively with other team members.

## What is Git Flow

Git flow is a branching model for Git that defines a strict branching and merging strategy designed to help manage large-scale software development projects. It was created by Vincent Driessen in 2010 and has become widely adopted in the industry.

The Git flow model defines a specific set of branches that are used for different purposes in the development lifecycle, each with a specific naming convention and function. The main branches in Git flow are:

- Master: This branch represents the stable production version of the code, and is where code that has been tested and is ready for release is merged.

- Develop: This branch is where ongoing development takes place. It represents the latest development version of the code, and is where feature branches are merged.

In addition to the main branches, Git flow defines several other branch types:

- Historical Branches:
  Instead of using only one master branch, this workflow uses two branches to record the project history. The master branch stores the official release history, while the development branch is used for active development. It is also important to tag commits in the master branch with version numbers.

- Feature branches:
  These branches are used for new features or functionality that are being developed. They are typically short-lived, and are merged into the Develop branch when the feature is complete.
  Each new feature should be developed separately - in its own branch, which should be pushed to the central repository for backup or collaboration with other developers. The development branch is used to create a feature branch. When the feature development is complete, it is merged into the development branch. Features should never be merged directly into the master branch.

- Release branches:
  These branches are used to prepare a new version of the code for release. They are created from the Develop branch, and are used to perform final testing and bug fixing before the code is merged into the Master branch.
  Once development has enough features for a release (or on a pre-determined date), a release branch is created from the development branch.
  Creating this branch starts a new release cycle, so no new features should be added to this branch - only bug fixes, documentation generation, and other tasks aimed at the release.
  Once the release branch is prepared, it is merged with master and tagged with a new version. It should also be merged with the development branch, which has likely moved ahead since the release was initiated.
  Using a separate branch for releases allows one team to prepare a release while another team continues to develop new features in development for future releases.

- Hotfix branches:
  These branches are used to fix critical bugs or issues in the code that require immediate attention. They are created from the Master branch, and are merged back into both the Master and Develop branches when the fix is complete.
  Hotfix branches are used for quick release patching. This is the only branch that is created from master. Once the fix is ready, it should be merged into both master and development (or a new release if there is one) and master should be tagged with a new version (incremented patch number, for example v.1.0.1).
  This allows errors to be fixed without interrupting the entire workflow or waiting for the next release to roll out the fixes.

The Git flow model provides a clear structure for managing code changes, and helps to ensure that changes are properly tested and reviewed before being merged into the main production codebase. It can be used in conjunction with other Git workflows and tools to provide a comprehensive approach to managing software development projects.

## What is Git Rebase

Git rebase is a command in Git that allows you to integrate changes from one branch into another branch by rewriting the history of the target branch. Unlike merge, which creates a new commit that combines the changes from both branches, rebase applies the changes of one branch onto another branch as if they were originally created on the target branch.

To perform a rebase, you typically start by checking out the branch that you want to apply the changes to. Then, you run the git rebase command followed by the name of the branch that you want to rebase onto the current branch. Git will then replay the changes made on the rebased branch onto the current branch, modifying the commit history to make it look as if the changes were always made on the current branch.

Rebasing can be useful for keeping your Git history cleaner and easier to follow, especially in cases where multiple developers are working on the same codebase and frequent merges can result in a cluttered commit history. However, it's important to use rebase carefully and only when it makes sense for the specific situation.

It's worth noting that rebasing changes the commit history of a branch, which can cause issues if other developers have already cloned the original branch and are also making changes to it. In this case, it's generally best to avoid rebasing and instead use merge to integrate changes.

Overall, Git rebase is a powerful tool for managing branches and integrating changes in Git, but it should be used with caution and only in situations where it makes sense for the specific project and workflow.

So, git works with commits. Each commit is a set of changes. Each commit has a unique hash. When branches are merged using the merge command:

`$ git merge "another_branch"`

All the commits are preserved - the commit comments, their hash, and usually, an additional artificial commit is added. At the same time, commits can alternate with each other. This is not always convenient. Suppose you decided to revert your commit - searching for your commit in the general list, along with others, is not very pleasant. In general, in the shared history, you want to see truly significant changes, not "oops, I forgot to put ;". To combine several commits into one, you can use rebase. Although in the GitHub interface, there is a button squash & commit - when you create a pull request (PR) from one branch to another (usually from your working branch to the main one), and after passing all the formalities, you can press squash & commit, update the comment, and your changes will appear in the main branch as one commit.

I want to write about two cases of using rebase:

1. When changes are incorporated from one branch to another, not through merge but through rebase:
   `$ git rebase "another*branch"`
   This allows you to place your local commits after all the commits that were made in the "another_branch". The hashes of your commits will change.
2. When you can manually edit several of your commits - for example, merge them, change the comment:
   `$ git rebase -i {HEAD~\_commit_count*|commit_hash}`
   So, you've done everything in your cozy branch and decided to share this commit with the world, but the world wants only one commit from you. `git rebase -i` will launch the editor and suggest editing commits (the order of the commits is from top to bottom, unlike git log). You can leave the commit as it is, change the comment, merge it with the previous one. Typically, you should leave your first commit as is, and change all the rest to `pick "commit_hash" "comment" → fixup "commit_hash" "comment"`.

At the same time, all comments that were in fixup commits will be lost, and the comment from the first commit will be used. If you cherish the comments, then it is worth using squash instead of fixup.

But if the development process was lengthy, then most likely, you had to merge the main branch. And all your commits will mix with the common ones, and merging yours with others will be a difficult task. Therefore, before doing `git rebase -i <>`, it is worth doing `git rebase`. `git rebase` will place all your commits at the end of the list of all commits (which can be verified by running `git log`) and then run `git rebase -i <HEAD~Number_of_your_commits>`, replace pick with {fixup|squash} in all lines except the first one, and voila - you have one commit.

If you messed up something while editing the commits with `git rebase -i <>`, then you should not press Control+C - the exit code of the git editor does not matter. It will just take the file and do everything according to it. Just delete or comment out all the lines in the file. Git will understand that you did not want to do anything, and it will not make any changes.

## What is Git Cherry pick

Git cherry-pick is a command that allows you to apply a specific commit from one branch to another. This means that you can pick a commit from a branch and apply it to another branch, even if they have diverged and have different commit histories.

When you use `git cherry-pick`, Git will apply the changes introduced by the specified commit to your current branch, creating a new commit with a new hash that incorporates the changes from the original commit. The new commit will have the same message as the original commit by default, but you can modify it if you want.

One common use case for `git cherry-pick` is when you want to apply a fix or feature from a different branch to the branch you are currently working on. Instead of merging the entire branch, which could bring in unwanted changes, you can cherry-pick just the commit that contains the changes you want.

To use `git cherry-pick`, you need to specify the commit you want to pick. You can do this by providing the commit hash or a branch name and a commit reference. For example:

```ruby
$ git cherry-pick <commit-hash>
$ git cherry-pick another-branch~2
```

Git will then apply the changes from that commit to your current branch, creating a new commit with the same changes. If there are any conflicts between the changes you're trying to apply and the changes in your current branch, Git will stop and ask you to resolve the conflicts before continuing.

It's important to note that when you cherry-pick a commit, you are essentially creating a new commit with the same changes as the original commit. This means that the new commit will have a different hash than the original commit, and any other changes that were made in the original branch will not be included in the new commit.

Overall, Git cherry-pick is a useful command for selectively applying changes from one branch to another. It can help you avoid merging unwanted changes and make it easier to manage your Git history.

## What is force push

In Git, a force push is a way to update a remote branch with your local changes, even if those changes conflict with the current state of the remote branch. It overwrites the remote branch with the local branch, discarding any changes made on the remote branch that are not on the local branch.

A regular push will only update the remote branch if the local branch is ahead of the remote branch. If the remote branch has changes that are not in your local branch, a regular push will fail, prompting you to pull the changes first.

However, there may be situations where you want to push your local changes to the remote branch, even if they conflict with the current state of the remote branch. This is where a force push comes in handy. A force push will update the remote branch with your local changes, regardless of whether the remote branch is ahead or behind your local branch.

It's important to note that force pushing can be dangerous and should be used with caution. It can potentially overwrite other developers' changes and cause conflicts. Therefore, it's important to communicate with your team before performing a force push and ensure that it won't cause any issues.

To perform a force push, you can use the `git push --force` or `git push -f` command, followed by the name of the remote branch and the local branch you want to push to the remote branch. For example, if you want to force push the changes in your local master branch to the `origin` remote's `master` branch, you would use the command `git push --force origin master`.

If you have corrected any old commits in git history, such as changing the author's name or email, or undoing the last commit, or using amend or revert, git will "complain" when attempting to push.

To push our changes anyway, we need to execute either:
`git push --force origin <branch_name>`

However, in this case, we risk overwriting someone else's changes if someone has pushed their commits since we pulled changes from the server. Therefore, it is better to use a safer command:
`git push --force-with-lease origin <branch_name>`.

This option is better because if someone has pushed their commits after we pulled changes from the server, they will not be overwritten, and we will receive an error message. We can then integrate other people's commits with our changes and try `push --force-with-lease` again.

## What is a pre-commit check

A pre-commit check is a software development practice that involves automatically verifying code changes for issues or errors before they are committed to the repository. This is done to ensure that the code is of high quality and meets the coding standards and guidelines of the project.

Pre-commit checks can be implemented using various tools such as linters, code analyzers, and testing frameworks. These tools can check for a variety of issues, including syntax errors, style violations, security vulnerabilities, and performance problems.

By running pre-commit checks, developers can catch and fix issues early in the development process, before they are introduced into the codebase. This can help prevent bugs and improve the overall quality and maintainability of the code.

Pre-commit checks can be integrated into the development workflow using various tools and plugins, such as Git hooks, IDE plugins, and CI/CD pipelines. When a developer makes changes to the code and attempts to commit them, the pre-commit checks are automatically run, and the commit is only allowed if there are no errors or issues detected.

Overall, pre-commit checks are an important practice for ensuring code quality and preventing issues from being introduced into the codebase. By catching and fixing issues early, developers can save time and effort in the long run and ensure that the code is of high quality and meets the requirements of the project.

As in many other version control systems, Git has the ability to run custom scripts at certain key moments. There are two groups of such interceptors, or hooks: client-side hooks and server-side hooks. Client-side hooks are intended for client operations, such as creating a commit and merging. Server-side hooks are needed for server operations, such as receiving sent commits. Hooks can be used to perform a wide variety of tasks, and we will talk about some of these tasks.

Pre-commit checks can be used, for example, to:

- perform code validation checks (such as compliance with PEP8 requirements, presence of documentation, etc.);
- perform comprehensive project checks (unit tests, etc.);
- abort the commit operation in case of errors and display a detailed log for troubleshooting.

# Dokcer

## What is docker and what features does it have

Docker can be used in CI/CD. Docker is a container management tool that allows you to run applications in isolated environments and package applications and all their dependencies into containers.

Using Docker can simplify the process of building and deploying applications to CI/CD. For example, instead of installing and configuring all the dependencies every time you build an application, you can create a Docker image that contains all the necessary dependencies and settings. This image can then be used in different stages of CI/CD such as build, test, and deployment.

In this way, Docker can speed up and automate the process of building, testing, and deploying applications on CI/CD, enabling teams to deliver high-quality software to production more quickly.

Docker is an open-source platform for building, shipping, and running applications in containers. Containers are a lightweight form of virtualization that allows applications to run in an isolated environment, with their own runtime, system libraries, and dependencies. Docker is widely used by software development teams to streamline the process of building, testing, and deploying applications.

Here are some key features of Docker:

1. Portability: Docker allows applications to be packaged in a container, along with all of their dependencies, making them highly portable. Containers can be easily moved between different environments, such as development, testing, and production, without the need to modify the application or its configuration.

2. Isolation: Docker containers provide a level of isolation between applications, which helps to ensure that they do not interfere with each other. Each container has its own file system, networking, and system resources, which are separate from the host operating system.

3. Scalability: Docker makes it easy to scale applications horizontally, by creating multiple instances of the same container. This can be done automatically, using tools like Docker Compose and Kubernetes, to ensure that the application can handle increasing amounts of traffic.

4. Consistency: Docker allows teams to create a consistent environment for building, testing, and deploying applications. This helps to reduce the risk of errors and conflicts, as all team members are working with the same tools and dependencies.

5 .Versioning: Docker allows teams to version their applications, by creating images of each container at different stages of the development process. This makes it easy to roll back to previous versions of the application, if needed.

6. Security: Docker provides built-in security features, such as namespace isolation, seccomp profiles, and AppArmor/SELinux profiles, which help to protect applications and data from external threats.

Overall, Docker is a powerful tool for software development teams, offering a range of features that can help to streamline the development process, improve the quality and consistency of applications, and make them more scalable and portable.

## Tell us what you know about docker components

DOCKER COMPONENTS:

1. CLIENT - Docker Client is a command-line interface (CLI) tool used to interact with the Docker daemon (server). It sends commands to the daemon, which then executes them. The client can be used to build, run, and manage containers, as well as manage images and networks. Example: `docker build`, `docker run`.

2. DAEMON - Docker daemon is the core component of Docker. It runs as a background service on the host operating system and manages the container lifecycle. It receives requests from the Docker client, and then builds, runs, and manages containers accordingly. Example: `dockerd`.

3. HOST - Docker host is the machine on which Docker is installed and runs. The host can be a physical machine, a virtual machine, or a cloud instance. It's the environment in which containers run. Example: A computer running Linux, macOS, or Windows.

4. CONTAINER - Docker container is an instance of an image. It's a lightweight, standalone, and executable package of software that contains everything needed to run an application, including code, runtime, system tools, libraries, and settings. Containers are isolated from each other and the host system, which makes them secure and portable. Example: 'docker container run'.

5. IMAGE - Docker image is a read-only template used to create Docker containers. It's a snapshot of the filesystem and configuration of an application. Images are built from a Dockerfile, which contains a list of instructions for building the image. Example: `docker image build`.

6. REPOSITORY - Docker repository is a collection of related Docker images. A repository contains one or more tagged images that share the same name but have different versions or tags. The repository can be hosted locally or remotely. Example: `docker push`, `docker pull`.

7. REGISTRY - Docker registry is a central place to store and distribute Docker images. It's a server-side application that stores and manages Docker repositories. The Docker Hub is the default public registry for Docker images, but you can also use private registries for security reasons. Example: `docker login`, `docker push`.

Other components of Docker include:

8. DOCKERFILE - Dockerfile is a text file that contains a list of commands for building a Docker image. It's used to automate the process of creating images, so you can easily reproduce the same environment in different locations. Example: `FROM`, `RUN`, `COPY`, `CMD`.

9. DOCKER COMPOSE - Docker Compose is a tool used to define and run multi-container Docker applications. It allows you to define your application's services, networks, and volumes in a YAML file and then start or stop them all with a single command. Example: `docker-compose up`.
