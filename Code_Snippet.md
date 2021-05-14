* Main
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

* [Python 3 print](http://www.python-course.eu/python3_print.php)
```python
print(value1, ..., sep=' ', end='\n', file=sys.stdout, flush=False)
```

* [Python 3 formatted print](http://www.python-course.eu/python3_print.php)
  ![formatted print](http://www.python-course.eu/images/format_string_value_set.png) 


* Import
```python
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
```

* Named Tuple
```python
import collections

Employee = collections.namedtuple("Employee", ["id", "title", "salary"])
e = Employee(1, "engineer", 10000) # Employee(id=1,title="engineer", salary= 10000)
print(e)
print("Title is", e.title)
```
*  *args **kwargs
* Anonymous (lambda) Function
* Iterator
  * enumerate, zip, map, filter

```python
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
```

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

