Create 3 Column Question,Answer, Tag
Tag Column 
	Heap
Answer Column 
	Surround Answer Content with <pre> </pre> Tag
	Apply line break So that each Content will be in new line 
Share me xlsx Files


Java Priority Queue
https://www.scaler.com/topics/java-priority-queue/



PriorityQueue Syntax 
PriorityQueue<E> minPQ = new PriorityQueue<E>();
PriorityQueue<E> maxPQ = new PriorityQueue<E>(Collections.reverseOrder());

General Thought About Heap
For Minimium -> Declare maxPQ
For Maximium -> Declare minPQ

PriorityQueue Operation Names 
Insert ->  add(),Offer()
Delete ->  poll (), peek(), remove()
Clear ->  clear()
Size ->  size()


Methods	Time complexity
poll ->  O(logn)
peek ->  O(1)
remove ->  O(logn)
add ->  O(logn)
offer ->  O(logn)
clear ->  O(1)
size ->  O(1)
contains ->  O(n)
toArray() ->  O(n)


- What is the Difference b/w poll (), peek() ?
	poll() - removes the element
	peek() - return the top of element of priority-queue
	
- What is Complete Binary Tree ?
	A Complete Binary Tree is a binary tree where:		 
		1. Every level is fully filled except possibly for the last level.
		2. All nodes are as far left as possible

- What is Heap Order Property ?
- Is it possible to Visualise Array/ArrayList as BinaryTree (Heap)  ?
	Parent -> (i-1)/2
	Left -> 2*i-1
	Right -> 2*i+2

Last Non-Leaf Node
heap.size() = n 
(n-1)-1)/2
(n-2)/2
n/2-1

