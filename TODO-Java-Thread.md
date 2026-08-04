## 4. Inter Thread Communication
- BlockingQueue
│   ├── Object Monitor
│   └── Producer Consumer Problem






## 9. Interview Scenarios



│
├── 12. Blocking Queues
│   ├── BlockingQueue
│   ├── Producer Consumer
│   └── Queue Implementations



---

synchronized
Pro
Automatic lock release
Exception safe

cons
Limitations Cannot:
Try lock
Timeout
Interrupt waiting thread
Fairness

---
Reentrant Nature

1. Reentrant lock.lock(); lock.lock();
2. tryLock();
3. lock.tryLock(5,TimeUnit.SECONDS);
4. lock.lockInterruptibily();
5. new ReentrantLock(true); // Fairness FIFO

ReentrantLock vs synchronized

ReadWriteLock : Many readers but few writers.
ReadWriteLock Provides
readLock()
writeLock()

ReadWriteLock Use Cases
Cache
Configuration
Reference Data
Interview Favorite "When reads >> writes"


StampedLock
Instead of returning a lock object, it returns a stamp (long value).
It is advanced Version of ReadWriteLock
StampedLock Provides
readLock()
writeLock()
tryOptimisticRead() : "I'll read first. If nobody modified the data while I was reading, my data is valid."

Example : Peek From Window + Open Room Then Read Example 
Use Cases
Analytics
Cache
Read-heavy systems

ReadWriteLock vs StampedLock