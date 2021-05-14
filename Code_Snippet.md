## Main
```python
class UsefulClass:
    '''This class might be useful to other module'''

def main():
    '''creates a useful class and does something with it for our module'''
    useful = UsefulClass()
    print(useful)
    
if __name__ == "__main__":
    main()
```

## Links
* [http://www.python-course.eu/python3_print.php Python 3 print]

[[code]]
print(value1, ..., sep=' ', end='\n', file=sys.stdout, flush=False)
[[/code]]

* [http://www.python-course.eu/python3_print.php Python 3 formatted print]
[[<image http://www.python-course.eu/images/format_string_value_set.png]]

* Import
[[code]]
#Explicit Module Import
import math
math.cos(math.pi)

#Explicit Module Import by Alias
import numpy as np
np.cos(np.pi)

# Explicit import of module contents
from math import cos,pi
cos(pi)

#Implicit import of module contents
from math import *
sin(pi)**2 + cos(pi)**2
[[/code]]

* Named Tuple
[[code type="Python"]]
import collections

Employee = collections.namedtuple("Employee", ["id", "title", "salary"])
e = Employee(1, "engineer", 10000) # Employee(id=1,title="engineer", salary= 10000)
print(e)
print("Title is", e.title)
[[/code]]

*  *args **kwargs
* Anonymous (lambda) Function
* Iterator
 * enumerate, zip, map, filter
[[code]]
L = [2,4,6,8,10]
for i,val in enumerate(L):
    print(i,val)

L = [2,4,6,8,10]
R = [3,6,9,12,15]
for lval,rval in zip(L,R):
    print(lval,rval)

square = lambda x: x**2
for val in map(square,range(10)):
    print (val,end=' ')

is_even = lambda x: x%2 == 0
for val in filter(is_even,range(10)):
    print (val,end=' ')
[[/code]]

* itertools
```python
print (*range(10))  # 0 1 2 3 4 5 6 7 8 9
print(*map(lambda x:x**2,range(5))) # 0 1 4 9 16
```

```python
from itertools import permutations
p = permutations(range(3))
print(*p) # (0, 1, 2) (0, 2, 1) (1, 0, 2) (1, 2, 0) (2, 0, 1) (2, 1, 0)

from itertools import combinations
c = combinations(range(4),2)
print(*c) # (0, 1) (0, 2) (0, 3) (1, 2) (1, 3) (2, 3)

from itertools import product
p = product('abc',range(3))
print(*p) # ('a', 0) ('a', 1) ('a', 2) ('b', 0) ('b', 1) ('b', 2) ('c', 0) ('c', 1) ('c', 2)
```


* [https://stackoverflow.com/questions/2573135/python-progression-path-from-apprentice-to-guru Python progression path - From apprentice to Guru]
 * [https://docs.python.org/3/tutorial/datastructures.html#list-comprehensions Discover list comprehensions]
  * [https://www.smallsurething.com/list-dict-and-set-comprehensions-by-example/ List, Dict And Set Comprehensions]
 * [https://stackoverflow.com/questions/102535/what-can-you-use-python-generator-functions-for Discover generators]
 * Incorporate map, reduce, filter, iter, range, xrange often into your code
  * [http://book.pythontips.com/en/latest/map_filter.html Map, Reduce, and Filter] 
 * [http://book.pythontips.com/en/latest/map_filter.html Discover Decorators]
 * Write recursive functions, a lot
 * Discover itertools and functools
  * itertools
   * [https://www.novixys.com/blog/python-itertools-count-cycle-chain/ count, cycle and chain]
   * [https://www.novixys.com/blog/python-itertools-compress-dropwhile-takewhile-groupby/ compress, dropwhile, takewhile, groupby] 
   * [https://www.novixys.com/blog/python-itertools-ifilter-islice-imap-izip/ ifilter, islice, imap, izip] 
 * Read Real World Haskell (read free online)
 * Rewrite all your old Python code with tons of higher order functions, recursion, and whatnot.
 * Annoy your cubicle mates every time they present you with a Python class. Claim it could be "better" implemented as a dictionary plus some functions. Embrace functional programming.
 * Rediscover the Strategy pattern and then all those things from imperative code you tried so hard to forget after Haskell.
 * Find a balance.
