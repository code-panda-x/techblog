# Python CheatSheet


## Where the program starts
```
if __name__ == '__main__':
    # statements
```

## Array types: 
List: 
```
letters = ['a', 'b', 'c', 'd', 'e', 'f', 'g']
len(letters) # Returns length of array
```

Tuple: is **immutable!**
```
dimensions = (200, 50) 
```

Dict:
```
student1 = {'gender': 'male', 'age': 18}
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

---

# To be reviewd 

## Class 
[Encapsulation/Inheritance/Polymorphism](https://turingplanet.org/2019/09/21/%e7%b1%bb-class/)

## Unit Testing
[Unit Testing](https://turingplanet.org/2019/10/04/python-testing/)
