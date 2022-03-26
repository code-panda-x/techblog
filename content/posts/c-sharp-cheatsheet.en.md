---
title: "C# CheatSheet"
date: 2021-08-25T13:39:38-05:00
draft: false
tags: ["C#","Programming", "ASP.NET"]
categories: ["Programming Language"]
slug: "c-sharp-cheatsheet"
subtitle: "Questions regarding C# & ASP.NET"
description: "Questions regarding C# & ASP.NET"
keywords: 
- C#
- Programming
---

### Difference between C# and .Net
C# is a programming language

.Net is a framework that can run C# application
1. It is a collections of library
2. It has a CLR

### .Net framwork4.X vs .Net Core3.X vs .Net 5.0
```
            .Net framework      .Net Core           
Platform    Windows             Cross-platform      
Performance Slow                Better
CLI         IDE based           Full CLI command supported (Run CMD)
Packaging   One big framework   Delivered via modularly using Nuget

.Net5.0 is a unified platform
```

### What is IL code && What is the use of JIT?
IL: Intermediate language code (partial compiled code)
JIT: Just in time compiler

    Source Code --> IL --(JIT)--> Machine code

Benefit: For different runtime and dev environment, JIT compiles the best optimized code for that environment


### What is CLR
CLR: common language runtime
1. CLR invokes JIT to convert IL code to machine language
2. Cleans unused objects by using garbage collector

### Garbage collector
Background process which cleans Unused Managed resources
Cannot clean unmanaged recources

### CTS
Common types system ensures that data types defined in two different languages gets compiled to a common data type

### CLS
Common language specifications
A set of guidelines that make any language following .NET specifications (Case sensitive)

### Stack vs Heap
Stack stores primitive data types (int ,boolean, double)
Heap stores objects

**Stack handles function calls**

### Value type vs Reference type
Value types (contains actual data like int a = 0) are stores on stack 
Reference types (contains pointers and the pointers point to the actual data)are stored on heap

### Casting
Explicit casting:(lower to higher type)
    int y = (int)d;
Implicit casting:(lower to higher type)
    int i = 1;
    double d = i;

### Generic collections
Strongly typed and flexible
    List<int> geneint = new List<int>();
    geneit.Add(1);


---

### Advantages of using C#
1. Simple & fast
2. High scalability 
3. No buffering
4. Cross plaforms

### Code compilation in C#
1. Compliation of Source code
2. Clubbing newly created code (Test code and funtion code)
3. Executing assembly
4. CLR (Common language runtime)

### Access modifers in C
1. Public: it can be accessed by every part of the code
2. Private: it only can be accessed within the class
3. Protected: it only can be accessed within the class and the inheriting class (parent and child class)
4. Internal: it can be accessed in the class at the current assembly position

### Passing parameters to a method
1. Value parameters (not affect original value)
2. Reference parameters (affect original value)
3. Output parameters (returns more than one value)

### Difference between finally and finalize block
1. Final block is called after try catch blocks (not dependent on the exception handling)
2. Finalize method is called just before garbage collection (cleanup operation for unmanaged code)

### Managed code vs Unmanaged code
Managed code:
1. Executed by CLR
2. ALl the application code is dependent on .Net platform

Unmanaged code:
1. Executed by runtime application of some other structure
2. The runtime application deals with memory, security and other execution activities


### Define Sealed class
Created when you want to restrict the class being inherited

### Define a partial class
1. Make use of suplit function
2. Splits the definition of the class into multiple classes in same file or multiple files
3. One can create a class definition in multiple files but it is compiled as one class at run-time
4. User can create object of partial class and access all the methods from every source file


### StreamReader/StreamWrite class
    StreamReader sr = new StreamReader("C: Readme.txt")
    StreamWriter sr = new StreamWriter("C: Readme.txt")


### Class vs Struct
![class-vs-struct.png](/images/class-vs-struct.png)

### Virtual vs Abstract method
![virtual-vs-abstract.png](/images/virtual-vs-abstract.png)

### Namespaces
Used for organizing large code projects

### Boxing and Unboxing
Converting a value type to reference type is called boxing
    int value = 10
    // Boxing:
    Object boxedvalue = value1;

    // Unboxing:
    int Unboxing = int(boxedvalue)


### Jagged Array
Array of arrays

    Int[][] Jagarr = new[5][5];

### Array vs ArrayList
int [] arr = {1,2};
ArrayList list = new ArrayList();

![array-vs-arraylist.png](/images/array-vs-arraylist.png)

### Collections
A collection works like a container for instances of other classes, every class implements collection interface

### Serialization
Process that involves converting some code into its binary format
1. Binay Serialization
2. XML Serialization
3. SOAP

### Parsing
    String text = "200"
    int.num = int.Parse(text)

### Delegate
A delegate is a variable that holds the reference to a method
Useful to communicate between threads
It's a function pointer of the reference type

    public Delegate int myDel(int number)
    public int SubstractNum(int a) // Substract a by 10, return an int
    // In public void start()
    myDel DelegateExample = SubstractNum; // Holds the reference to a method

### System.String vs System.Text.StringBuilder
![string-vs-builder.png](/images/string-vs-builder.png)

### System.Array.CopyTo() vs System.Array.Clone()
Clone(): A new array obj is created with all elements

CopyTo(): All the elements get copied into another existing array


### Try...Catch...
    try
    {
        int y = 0;
        int z = 1 / y;
    }
    catch(Exception ex) // parameter type is system.Exception
    {
        // do something
    }


### Generics in C#.Net
1. Used to make reusable code classes that decrease code redundancy
2. Increase type safety, performance and optimization
3. Generics create collection

### Finalize vs dispose()
Dispose releases unmanaged resources

Finalize doesn't assure garbage collection (it releases unmanaged resources too)


### Thread
Thread: is a set of instructions that when executed enables the program to perform concurrent processing. Thread terminates immediately after execution

Multithreading: Execute more than one process/task at a time

Parallel execution:
```
Thread t = new Thread(Method1);
t.Start();
Thread t1 = new Thread(Method2);
t1.Start();
```

### Task
TPL: Task parallel Library
1. Parallel processing
2. Pooling threads
3. Perform actions with a task



### Events
Encapsulated delegate
    public Delegate void TestEvent();
    public TestEvent TestEvent1

### Synchronous and Asynchronous Operations
S: only a single thread will access in a given time
S call waits for completion of method and then continuous the program flow

A: the method call immediately returns allowing the program to perform other operations

### Async and Await (For creating Asynchronous methods)
///

### Deadlock
///

---

