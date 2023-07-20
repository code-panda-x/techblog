---
title: "Python CheatSheet"
date: 2021-07-22T16:33:33-05:00
draft: false
tags: ["Python","Programming"]
categories: ["Programming Language"]
slug: "python-cheatsheet"
subtitle: "Common used Python code"
description: "Common used Python code"
keywords: 
- Python
- Programming
- Gramma
---

## Where the program starts
```
if __name__ == '__main__':
    # statements
```

## Self
Use self to pass values between def's
```
self.arr = nums

```
## Array types: 
List: 
```
letters = ['a', 'b', 'c', 'd', 'e', 'f', 'g']
len(letters) # Returns length of array

## Common use
list = []
list.append((a,b))
list.sort() # nlogn
```

Tuple: is **immutable!**
```
dimensions = (200, 50) 
```

Dict: Basically HashMap
```
student1 = {'gender': 'male', 'age': 18}
d = {} # d = dict()
d[0] = 1 # or d = {0:1}
d = defaultdict(int) # init with 0

# Update dict
if s in d:
    d[s] += 1 
else:
    d[s] = 1

## Java-like version
count += d.get(s-k,0)
d[s] = d.get(s,0) + 1

```

Set:
```
new_set = {value1, value2, value2, ...}
new_set2 = set(value)
```

## Range function
```
# range(start, stop)
for i in range(1, 10): 
    print(i)

# range(stop) start from 0
for i in range(10):
    print(i)

# range(start, stop, step)
for i in range(0, 13, 5):
    print(i)

# travse backwards: https://www.tutorialspoint.com/backward-iteration-in-python
for i in range(len(nums)-1, -1, -1):
```

## If else 
```
if condition_1:
    statement_block_1 # Execute if condition_1 is True
elif condition_2:
    statement_block_2 # Execute if condition_1 is False & condition_2 is True
elif condition_3:
    statement_block 3 # Execute if condition_3 is True and 1 & 2 are False
else:
    statement_block_3 # Execute if previous conditions are all Falser 

```
## Heap

Min heap
    h =[]
    heapq.heappush(h,i[1])
    heapq.heapreplace(h,i[1])
## Loop
```
# While loop
num = 0
while num < 10:
    print(num)

# For loop
list = [1, 2, 3, 4, 5, 6]
for i in list:
    print(i)

for a, b, c in list:
    ## [[a,b,c],[1,2,3]]

for index, num in enumerate(nums)

for i in range(len(nums)):
```

## Functions 
```
def function_name(parameters):
    expressions
```


## Catch Exceptions
```
try:
    print(x)
except:
    print("Something went wrong")
finally: # finally will always be executed
    print("The 'try except' is finished")
```

## Math
```

max(num1, num2)
sum(nums)
i**2 # i^2
```

## Init
```
sum, num = 0,0
newlist = [0]
newlist = nums + [0]
newlist = [1] + [0] * k # [0:1, 0:0, 0:0]
newlist = list(rage(8))  # [0,1,..7]
```

## Slice notation
https://stackoverflow.com/questions/509211/understanding-slicing
---

## Sort Lambda
```
intervals = sorted(intervals, key = lambda x : x[0])
list.sort() # nlogn
```

# To be reviewd 

## Class 
[Encapsulation/Inheritance/Polymorphism](https://turingplanet.org/2019/09/21/%e7%b1%bb-class/)

## Unit Testing
[Unit Testing](https://turingplanet.org/2019/10/04/python-testing/)