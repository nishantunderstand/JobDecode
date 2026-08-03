JCF 

List 
Set 
Queue
Map 


---


List 

Duplicate 
Ordered 
Null Value
Dynamic Size
0-Based Indexing 

List Types
1. Vector (Legacy)
2. ArrayList
3. LinkedList
4. CopyOnWriteArrayList


ArrayList vs LinkedList vs CopyOnWriteArrayList
Cache Friendly 


How to make a List ThreadSafe ?
Collections.synchronizedList()

ReadHeavy  
WriteHeavy

List 
Mutable List
Immutable List


Can we prevent an ArrayList from growing?
1. Fixed-Size List using Arrays.asList()
2. Unmodifiable List
3. Custom Capacity Check

Does new ArrayList<>(10) create a fixed-size list?


Iterate
Enumeration
Iterator
ListIterator
SplitIterator
forEach

capacity and size?

---


Queue Types


---

Set 
Distinct
UnOrdered 
Is Null Allowed ? Depends


Set Types 
1. HashSet (1 Null)
2. LinkedHashSet   (1 Null )
3. CopyOnWriteArraySet  (1 Null )
4. TreeSet    (0 Null)

Collections.synchronizedSet()

HashSet vs LinkedHashSet vs TreeSet
Read Heavy vs Write Heavy

HashSet       -> Unordered       -> 1 Null
LinkedHashSet -> Insertion Order -> 1 Null
TreeSet       -> Sorted Order    -> 0 Null

Comparable vs Comparator (TreeSet)
Fail-Fast vs Fail-Safe 
ConcurrentModification


Internal Data Structure
HashSet       -> HashMap
LinkedHashSet -> LinkedHashMap
TreeSet       -> TreeMap (Red-Black Tree)

HashSet Internal Working
hashCode()
equals()
Buckets
Collision
How HashSet Identifies Duplicates
Why do duplicates still get inserted unless you override

HashSet vs ArrayList

---
Map Types
Key-Value
1 Null Allowed
Duplicate Key - Not Allowed
Duplicate Value - Allowed

Map 
1. HashMap 
2. LinkedHashMap
3. TreeMap 
4. ConcurrentHashMap

HashMap Internal Working

Data Structure
Array
Bucket
Node
Hashing
hashCode()
Index Calculation

Operations
put()
get()
remove()

Hash Collision
Collision
Chaining


When Threshold is 6,7,8

Java 7
Bucket → LinkedList

Java 8
Bucket → LinkedList
Treeification
Red Black Tree (Self Balancing Tree)

Thresholds
Initial Capacity = 16
Load Factor = 0.75
Treeify Threshold = 8
Untreeify Threshold = 6
Minimum Capacity for Treeification = 64

Rehashing
Resize
Capacity Doubling
Rehash Process


Contrat b/w hashCode and equals 
What happens if:
equals overridden but hashCode not overridden?
hashCode overridden but equals not overridden?
Both not overridden?

Working of Get ?
Working of Put ?
Working of Delete ?

Hashtable

HashMap vs HashTable vs ConcurrentHashMap

ConcurrentHashMap
Java-7 vs Java-8
Segementlevel vs BucketLevelBlocking 
Why Null Not Allowed?

forEach
Map.Entry
keySet()
entrySet()

How to make HashMap Thread Safe?