# Unit 8: Multithreading in Java

### 1. **Difference Between Multithreading and Multitasking**

- **Multitasking** refers to the ability of an operating system to execute multiple tasks or processes concurrently. These tasks can be independent of each other, and the operating system manages the allocation of CPU time to each task.
  - **Types of Multitasking**:
    - **Process-based multitasking**: Multiple processes running simultaneously, each with its own memory space.
    - **Thread-based multitasking**: Multiple threads within the same process run simultaneously, sharing the same memory space.

- **Multithreading** is a specific type of multitasking where a process is divided into smaller threads that can be executed concurrently. These threads run within the same process and share the same memory space. Java supports multithreading as a way to improve performance by executing multiple threads in parallel.

  **Key Difference**:
  - **Multitasking** involves multiple processes, while **multithreading** involves multiple threads within a single process.

### 2. **Thread Life Cycle**

In Java, the **life cycle of a thread** is governed by the `Thread` class. A thread goes through several states during its execution. The thread life cycle consists of the following stages:

1. **New (Born)**: 
   - A thread is in the **new** state when it is created but not yet started. In this state, the thread is not yet eligible for CPU execution.
   ```java
   Thread t = new Thread();
   ```

2. **Runnable**:
   - A thread enters the **runnable** state when the `start()` method is invoked. It is ready to be executed by the CPU, but the actual execution depends on the system's scheduler.
   ```java
   t.start();
   ```

3. **Blocked/Waiting**:
   - A thread enters the **blocked** or **waiting** state when it cannot proceed due to some external condition, such as waiting for a resource, I/O operation, or waiting for a lock. It will remain in this state until the condition is satisfied.
   ```java
   synchronized(t) {
       // Thread waits for lock
   }
   ```

4. **Timed Waiting**:
   - A thread can enter the **timed waiting** state when it is waiting for a specified amount of time. This is done using methods like `sleep()` or `join()`.
   ```java
   t.sleep(1000);  // Thread sleeps for 1 second
   ```

5. **Terminated (Dead)**:
   - A thread enters the **terminated** state when it has completed its execution. A thread can also be manually stopped by the `stop()` method, though this is deprecated in modern Java versions.

### 3. **Creating Threads in Java**

There are two main ways to create threads in Java:

1. **By Extending the `Thread` Class**:
   - You can create a new thread by creating a subclass of `Thread` and overriding the `run()` method. Then, create an instance of the subclass and call the `start()` method to begin execution.
   ```java
   class MyThread extends Thread {
       public void run() {
           System.out.println("Thread is running");
       }
   }

   public class Main {
       public static void main(String[] args) {
           MyThread t1 = new MyThread();
           t1.start();  // Start the thread
       }
   }
   ```

2. **By Implementing the `Runnable` Interface**:
   - Instead of extending the `Thread` class, you can implement the `Runnable` interface, which requires the implementation of the `run()` method. The `Runnable` object is passed to the `Thread` constructor, and then the `start()` method is called to begin execution.
   ```java
   class MyRunnable implements Runnable {
       public void run() {
           System.out.println("Thread is running");
       }
   }

   public class Main {
       public static void main(String[] args) {
           MyRunnable myRunnable = new MyRunnable();
           Thread t1 = new Thread(myRunnable);
           t1.start();
       }
   }
   ```

### 4. **Thread Priorities**

Java provides the ability to assign priorities to threads to influence the order in which they are scheduled for execution by the thread scheduler. Thread priority is an integer value between `Thread.MIN_PRIORITY (1)` and `Thread.MAX_PRIORITY (10)`.

- By default, all threads have the same priority, which is `Thread.NORM_PRIORITY (5)`.
- You can set a thread's priority using the `setPriority()` method.

**Example**:
```java
Thread t1 = new Thread();
Thread t2 = new Thread();

t1.setPriority(Thread.MAX_PRIORITY);  // Highest priority
t2.setPriority(Thread.MIN_PRIORITY);  // Lowest priority

t1.start();
t2.start();
```

**Note**: Thread priority does not guarantee a particular execution order, as thread scheduling is ultimately controlled by the underlying operating system, which may or may not respect the specified priorities.

### 5. **Synchronizing Threads**

**Thread synchronization** is used to prevent thread interference and memory consistency errors when multiple threads access shared resources concurrently.

- **Why Synchronization is Needed**: When two or more threads access a shared resource simultaneously, there may be conflicts if one thread modifies the resource while another is reading it.

To ensure that only one thread can access a shared resource at a time, Java provides the `synchronized` keyword.

1. **Synchronized Methods**:
   - A method can be declared `synchronized`, ensuring that only one thread at a time can execute it for a given object.
   ```java
   class Counter {
       private int count = 0;

       public synchronized void increment() {
           count++;
       }
   }
   ```

2. **Synchronized Blocks**:
   - Instead of synchronizing the entire method, you can use synchronized blocks to lock only the critical section of the code. This allows other parts of the method to run concurrently.

   ```java
   class Counter {
       private int count = 0;

       public void increment() {
           synchronized (this) {
               count++;
           }
       }
   }
   ```

3. **Locking Shared Resources**:
   - In multithreading, it is important to avoid situations where two threads are trying to access or modify shared resources simultaneously. By synchronizing the critical sections, you ensure that only one thread can access the shared resource at a time.

**Example of Synchronization**:
```java
class SharedCounter {
    private int count = 0;

    // Synchronized method to ensure only one thread updates the count at a time
    public synchronized void increment() {
        count++;
    }

    public int getCount() {
        return count;
    }
}

public class Main {
    public static void main(String[] args) {
        SharedCounter counter = new SharedCounter();

        // Creating two threads
        Thread t1 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) {
                counter.increment();
            }
        });

        Thread t2 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) {
                counter.increment();
            }
        });

        t1.start();
        t2.start();

        try {
            t1.join();  // Ensure main thread waits for t1 to finish
            t2.join();  // Ensure main thread waits for t2 to finish
        } catch (InterruptedException e) {
            e.printStackTrace();
        }

        System.out.println("Final count: " + counter.getCount());
    }
}
```

### Summary of Key Concepts:

1. **Multithreading vs. Multitasking**: 
   - Multithreading refers to multiple threads running in a single process, while multitasking refers to multiple processes running concurrently.
   
2. **Thread Life Cycle**:
   - Threads go through several states: **New**, **Runnable**, **Blocked**, **Timed Waiting**, and **Terminated**.

3. **Creating Threads**:
   - Threads can be created by extending the `Thread` class or by implementing the `Runnable` interface.

4. **Thread Priorities**:
   - Thread priorities help influence the order in which threads are executed, but the actual scheduling depends on the operating system.

5. **Synchronizing Threads**:
   - Synchronization is used to prevent thread interference and ensure safe access to shared resources. This can be done using the `synchronized` keyword in methods or blocks.

By understanding these key points, you can effectively manage multithreading in Java and create programs that run efficiently in a concurrent environment.