LinkedList 1->2->3->4->5


ListNode curr = head;    // 1
ListNode prev = null;    //
ListNode next;

while(curr!=null){
	next  = curr.next; // Preserve        || 2->3  
	curr.next = prev; // Reverse The Link    null<-1 || 1<-2
	prev = curr;  // Shift   prev= null => prev = 1   || prev = 2
	curr = next;   // Move Forward   1 => 2   => 
}

return prev;

