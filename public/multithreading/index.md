# Multithreading



### **Multithreading on a Single Processor**

- The execution of **multiple threads** on a **single CPU**
- Multithreading on a single processor gives the **illusion** of running in parallel. In reality, the processor is switching by using a scheduling algorithm. Or, it’s switching based on a combination of external inputs (interrupts) and how the threads have been prioritized.
- These threads run concurrently and they share resources

> For example, this is a bit like chatting with different people through various IM windows; although you’re actually switching back and forth, the net result is that you’re having multiple conversations at the same time.

### **Multithreading on Multiple Processors**

Multiprocessing is the use of two or more central processing units within a single computer system

- The execution of **multiple threads** on multiple **CPU cores**
- Multithreading on multiple processor cores is truly parallel. Individual microprocessors work together to achieve the result more efficiently. There are multiple parallel, concurrent tasks happening at once.

> For example, in a browser, multiple tabs can be different threads. MS Word uses multiple threads: one thread to format the text, another thread to process inputs

## **Issues Involved with Multiple Threads**

### **Deadlock**

Deadlocks happen when two or more threads aren’t able to make any progress because the resource required by the first thread is held by the second and the resource required by the second thread is held by the first.

### **Race conditions**

https://stackoverflow.com/questions/34510/what-is-a-race-condition



Race conditions happen when threads run through critical sections without thread synchronization. The **threads** “race” through the critical section to write or read **shared resources** and depending on the order in which threads finish the “race”, the program output changes.
- Critical section is any piece of code that has the possibility of being executed concurrently by more than one thread of the application and exposes any shared data or resources used by the application for access.

In short: 

Threads **access shared resources** at the **same time** -> program output is **inconsistent**

Detailed race condition with example:

    
> A race condition occurs when two or more threads can access shared data and they try to change it at the same time. Because the thread scheduling algorithm can swap between threads at any time, you don't know the order in which the threads will attempt to access the shared data. Therefore, the result of the change in data is dependent on the thread scheduling algorithm, i.e. both threads are "racing" to access/change the data.

> Problems often occur when one thread does a "check-then-act" (e.g. "check" if the value is X, then "act" to do something that depends on the value being X) and another thread does something to the value in between the "check" and the "act". E.g:

    if (x == 5) // The "Check"
    {
        y = x * 2; // The "Act"
    
        // If another thread changed x in between "if (x == 5)" and "y = x * 2" above,
        // y will not be equal to 10.
    }
    

>The point being, y could be 10, or it could be anything, depending on whether another thread changed x in between the check and act. You have no real way of knowing.

>In order to prevent race conditions from occurring, you would typically put a lock around the shared data to ensure only one thread can access the data at a time. This would mean something like this:


    // Obtain lock for x
    if (x == 5)
    {
        y = x * 2; // Now, nothing can change x until the lock is released.
                    // Therefore y = 10
    }
    // release lock for x



### **Starvation**

Other than a deadlock, an application thread can also experience starvation, where it **never gets CPU time or access to shared resources** because other “greedy” threads hog the resources.

### **Livelock**

A livelock happens when two threads keep taking actions in response to the other thread instead of making any progress. The best analogy is to think of two persons trying to cross each other in a hallway. John moves to the left to let Arun pass, and Arun moves to his right to let John pass.

Both block each other now. John sees he’s now blocking Arun and moves to his right and Arun moves to his left seeing he’s blocking John. They never cross each other and keep blocking each other. This scenario is an example of a livelock.

## **How to avoid issues with multiple threads**

### **How to avoid deadlocks?**

- **Avoid Nested Locks:** This is the main reason for deadlock. Deadlock mainly happens when we give locks to multiple threads. Avoid giving locks to multiple threads if you already have given to one.
- **Avoid Unnecessary Locks:** You should lock only those members which are required. Having unnecessary locks can lead to a deadlock. As a best practice, try to reduce the need to lock things as much as you can.

### **How to avoid race conditions?**

Race conditions occur within the critical section of your code. These can be avoided with proper **thread [synchronization**](https://www.geeksforgeeks.org/synchronization-in-java/?ref=lbp) within critical sections by using techniques like locks, atomic variables, and message passing.

A synchronized block in Java is synchronized on some object. All synchronized blocks synchronize on the same object and ***can only have one thread executed*** inside them at a time.

### **How to avoid starvation?**

The best way to avoid starvation is to use a lock such as ReentrantLock or a mutex. This introduces a “fair” lock which favors granting access to the thread that has been waiting longest. If you wanted to have multiple threads run at once while preventing starvation, you can use a semaphore.

### **How to avoid livelocks?**

Livelocks can be avoided by making use of ReentrantLock as a way to determine which thread has been waiting longer so that you can assign it a lock. As a best practice, don’t block locks; if a thread can’t acquire a lock, it should release previously acquired locks to try again later.
