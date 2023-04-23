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
