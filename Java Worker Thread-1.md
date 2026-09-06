Thread Types
Worker Thread
Daemon Thread

Task 
Sequential
Parallel
Concurrent


Task Type
Synchronus Task
Asynchrnous Task

CPU Bound Task : Synchronus Task
IO Bound Task : Asynchrnous Task

ThreadPool
	Is it a collection of Worker Thread
	
	
ExecutorService 
Utility
Framework

Is it synchrnous or Asynchrnous ??


----





ExecutorService execute = Executors.newFixedThreadPool(5); nonDaemonThread
ExecutorService execute = Executors.newCachedThreadPool(); nonDaemonThread
ExecutorService execute = new ForkJoinPool();  ForkJoinWorkerThread , nonDaemonThread
ExecutorService execute = ForkJoinPool.commonPool();  ForkJoinWorkerThread , DaemonThread


ThreadPoolExecutor
ForkJoinWorkerThread  