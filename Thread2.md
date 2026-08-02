# Thread


├── 1. Thread Fundamentals
│   ├── What is a Thread?
│   ├── Process vs Thread
│   ├── Concurrency vs Parallelism (Coffee Example)
│   ├── Multithreading
│   ├── Platform Thread
│   └── Virtual Thread (Project Loom)



│
├── 2. Thread Class Basics
│   ├── Thread Constructors
│   ├── Thread Methods
│   │   ├── Instance Methods
│   │   ├── Static Methods
│   │   └── yield()
│   ├── Thread Method Classification
│   ├── Deprecated Methods
│   │   └── stop(), suspend(), resume()
│   └── Methods Belonging to Object
│       ├── wait()
│       ├── notify()
│       └── notifyAll()




## 1. Thread Creation
- Extending Thread class
- Implementing Runnable interface (Preferred)
- Implementing Callable interface (returns result)
- Future & FutureTask
- Lambda Expressions

│
├── 3. Thread Creation
│   ├── Extending Thread Class
│   ├── Implementing Runnable
│   ├── Implementing Callable
│   ├── Runnable vs Callable
│   └── Thread vs Runnable
│     ├── Future & FutureTask
│     └── Lambda Expressions




## 2. Thread Management
- Thread Life Cycle
- start() vs run()
- sleep()
- join()
- yield()
- interrupt()
- Thread Priority
- Daemon Thread
- Thread States

├── 4. Thread Lifecycle
│   ├── NEW
│   ├── RUNNABLE
│   ├── RUNNING
│   ├── BLOCKED
│   ├── WAITING
│   ├── TIMED_WAITING
│   ├── TERMINATED
│   ├── start()
│   ├── run()
│   ├── join()
│   ├── sleep()
│   └── interrupt()


## 3. Thread Synchronization
- synchronized Method
- synchronized Block
- Object Monitor Lock
- volatile
- Atomic Classes
- ReentrantLock
- ReadWriteLock
- Condition
- Lock vs synchronized

├── 5. Synchronization
│   ├── synchronized Method
│   ├── synchronized Block
│   ├── synchronized Block vs Method
│   ├── Object Monitor Lock
│   ├── Intrinsic Lock
│   ├── volatile
│   ├── Thread Safety
│   └── Visibility vs Atomicity


## 4. Inter Thread Communication
- wait()
- notify()
- notifyAll()
- Producer Consumer Problem
- BlockingQueue

├── 5. Thread Communication
│   ├── wait()
│   ├── notify()
│   ├── notifyAll()
│   ├── wait() vs sleep()
│   ├── notify() vs notifyAll()
│   ├── Who releases the lock?
│   └── Inter Thread Communication



├── 6. Thread Scheduling
│   ├── Thread Priority
│   │   ├── MIN_PRIORITY
│   │   ├── NORM_PRIORITY
│   │   └── MAX_PRIORITY
│   ├── Thread Scheduler
│   │   ├── Priority Scheduling
│   │   └── Time Slicing
│   └── yield()




├── 7. Thread Types
│   ├── User Thread
│   ├── Daemon Thread
│   ├── What is Daemon Thread?
│   ├── User → Daemon Conversion
│   ├── Daemon → User (Tricky)
│   ├── ThreadGroup
│   └── DaemonGroup

   ├── Thread Types
│   │   ├── User Thread
│   │   ├── Daemon Thread
│   │   ├── Daemon Thread Scenarios
│   │   └── User vs Daemon Thread






│   ├── Thread Methods
│   │   ├── start() vs run()
│   │   ├── sleep()
│   │   ├── join()
│   │   ├── yield()
│   │   ├── interrupt()
│   │   ├── currentThread()
│   │   ├── getName()
│   │   ├── setName()
│   │   ├── getState()
│   │   └── isAlive()
│   │








## 5. Thread Problems
- Race Condition
- Deadlock
- Livelock
- Starvation
- Thread Safety

├── 10. Thread Problems
│   ├── Race Condition
│   ├── Data Inconsistency
│   ├── Deadlock
│   └── Livelock
│




## 6. Executor Framework
- Executor
- ExecutorService
- ThreadPoolExecutor
- Fixed Thread Pool
- Cached Thread Pool
- Single Thread Executor
- ScheduledExecutorService
- submit() vs execute()
- shutdown() vs shutdownNow()
- Future
- Callable
- CompletionService

│
├── 13. Executor Framework
│   ├── Executor
│   ├── ExecutorService
│   ├── ThreadPoolExecutor
│   ├── ForkJoinPool
│   ├── Runnable Support
│   ├── Callable Support
│   ├── execute() vs submit()
│   └── shutdown() vs shutdownNow()
│



├── Executor Framework
│   ├── Executor
│   ├── ExecutorService
│   ├── ScheduledExecutorService
│   └── ThreadPoolExecutor
│





## 7. Java Concurrency Framework
- ConcurrentHashMap
- CopyOnWriteArrayList
- ConcurrentLinkedQueue
- BlockingQueue
- Semaphore
- CountDownLatch
- CyclicBarrier
- Phaser
- Exchanger
- ForkJoinPool

## 8. CompletableFuture
- supplyAsync()
- runAsync()
- thenApply()
- thenCompose()
- thenCombine()
- exceptionally()
- handle()
- allOf()
- anyOf()

## 9. Interview Scenarios
- Thread Pool in Spring Boot
- @Async
- Async REST Calls
- Parallel Processing
- File Processing
- Kafka Consumers & Threads
- Database Connection Pool
- CPU Bound vs IO Bound Tasks
│
└── 17. Interview Scenarios
    ├── Producer Consumer
    ├── Thread Pool Tuning
    ├── Parallel File Processing
    ├── Spring Boot @Async
    ├── Kafka Consumer Concurrency
    ├── CompletableFuture in REST APIs
    ├── Connection Pool vs Thread Pool
    ├── CPU Bound vs IO Bound
    └── Virtual Threads vs Platform Threads





├── 8. Synchronization
│   ├── synchronized Method
│   ├── synchronized Block
│   ├── synchronized Block vs Method
│   ├── Object Lock
│   ├── Mutex Lock
│   ├── Intrinsic Lock
│   └── Extrinsic Lock


│
├── 9. Lock Framework
│   ├── Lock Interface
│   ├── ReentrantLock
│   ├── synchronized vs Lock
│   ├── Lock vs ReentrantLock
│   ├── Object Lock
│   ├── Semaphore
│   ├── Semaphore vs ReentrantLock
│   └── AtomicInteger
│
│
├── 6. Lock Framework
│   ├── Lock Interface
│   ├── ReentrantLock
│   ├── ReadWriteLock
│   ├── Condition
│   ├── synchronized vs Lock
│   ├── Lock vs ReentrantLock
│   └── Mutex Lock
│




├── 11. Synchronizers
│   ├── Semaphore
│   │   └── Permit Based Control
│   ├── CountDownLatch
│   ├── CyclicBarrier
│   └── Phaser



│
├── 12. Blocking Queues
│   ├── BlockingQueue
│   ├── Producer Consumer
│   └── Queue Implementations



│
├── 14. Thread Pools
│   ├── Fixed Thread Pool
│   ├── Cached Thread Pool
│   ├── Single Thread Executor
│   ├── Scheduled Thread Pool
│   └── Thread Pool Sizing
│       ├── CPU Bound
│       └── IO Bound



├── 15. Fork/Join Framework
│   ├── ForkJoinPool
│   ├── RecursiveTask
│   ├── RecursiveAction
│   └── Work Stealing Algorithm



│
├── 16. Future & CompletableFuture
│   ├── Task
│   │   ├── Synchronous
│   │   ├── Asynchronous
│   │   ├── Blocking
│   │   └── Non Blocking
│   ├── Future
│   │   ├── get()
│   │   ├── Blocking Call
│   │   ├── Limitations
│   │   └── Future vs CompletableFuture
│   └── CompletableFuture
│       ├── supplyAsync()
│       ├── runAsync()
│       ├── thenApply()
│       ├── thenAccept()
│       ├── thenCompose()
│       ├── thenCombine()
│       ├── get() vs join()
│       ├── allOf()
│       ├── anyOf()
│       ├── exceptionally()
│       ├── handle()
│       ├── whenComplete()
│       └── Exception Handling Comparison



│
└── Atomic Classes
    ├── AtomicInteger
    └── AtomicBoolean

       ├── Atomic Classes
│   │   ├── AtomicInteger
│   │   ├── AtomicLong
│   │   ├── AtomicBoolean
│   │   └── AtomicReference




│
├── Concurrent Collections
│   ├── ConcurrentHashMap
│   ├── CopyOnWriteArrayList
│   └── BlockingQueue



├── 4. Inter-Thread Communication
│   ├── wait()
│   ├── notify()
│   ├── notifyAll()
│   ├── wait() vs sleep()
│   ├── notify() vs notifyAll()
│   ├── Object Monitor
│   └── Producer Consumer Problem
