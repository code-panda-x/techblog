# Thread Process


# Thread vs Process

## What is a Thread, really?

* Short answer: 

    * Thread is **a subset of a process**

* Longer answer:

    * Thread is an independent **set of values** for CPU registers

* Detailed answer: 

    * A thread is an **execution context for CPU**, which is all the information CPU needs to execute instructions. Essentially: 

[More about thread](https://stackoverflow.com/questions/5201852/what-is-a-thread-really)


### Thread components:

- Program counter: keeps track of which instruc­tion to execute next
- Stack: which contains the execution history
- Registers: which hold its current working variables


### Example:
> A single thread could be displaying the current tab you’re in, and a different thread could be another tab.

## What is a Process, really?

* Short answer: 

    * Process is **a running program**

* Long answer:

    * The process model is based on two independent concepts: **resource grouping** and **execution (thread)** 
    
[More about process](https://byjus.com/gate/process-in-operating-system-notes/#:~:text=A%20process%20is%20a%20running,is%20an%20'active'%20entity)
    
### Process components:

- stack: stores functional calls, local variables
- heap: memory that is dynamically allocated to a process during its execution
- text/code: code instructions
- data: static variables
    
### Example:
> When you double click on the Google Chrome icon on your computer, you start a process which will run the Google Chrome program

## Thread vs Process

Essentially: Processes are used to **group resources together**; threads are the entities **scheduled for execution** on the CPU.

### Comparsion Table

| Process  | Thread |
| ------------- |:-------------:|
| Process is a running program | Thread is a subset of a process   |
| Process  is heavyweight | Thread is lightweight   |
| The process is independent  | Threads share memory |

### Resource Sharing Difference

- Processes have separate address spaces (indepedent)

- For multiple threads in the same process
    - Threads share same address space and code, data, heap segments
    - Threads **DO NOT SHARE STACK**
    



