2.1 Linear List
================================
(1) Linear list, ordered list, or just list (cuz "order" is important in here.)  
(2) Element. (if there's no element, => empty list. A = {})  
(3) A = (a𝟶, a𝟷, ..., a𝑛-𝟷) ≠ A = {a𝟶, a𝟷, ..., a𝑛-𝟷}  

2.1.1 Implementation of linear list
--------------------------------
* One-dimensional arrays, listed lists  

2.1.3 Features of **array**  
--------------------------
(1) Sequential mapping - by its logical address  
(2) Random access is possible  
(3) Insertion or elimination is inefficient (the other elements have to move)  
(4) Array : rigid ⟷ Linked List : flexible  
(5) When implementing  
- suppose there's a maximum length and declare it MAX_LENGTH (0 ≤ index ≤ MAX-1)  
- use structure (-> in Java, use an Object & Class -> OOP!)  
- element &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; address  
&nbsp;&nbsp;&nbsp;list[0]  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; B   
&nbsp;&nbsp;&nbsp;list[1]  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; B + sizeof(int)  
&nbsp;&nbsp;&nbsp;list[2]  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; B + 2*sizeof(int)  
&nbsp;&nbsp;&nbsp; ...  
&nbsp;&nbsp;&nbsp;list[n-1]  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; B + (n-1)*sizeof(int)  

2.1.5 Application of Array : Polynomials  
--------
(1) Implement in Linear List =>  
(2) Can contain several polynomials in one array  
&nbsp;&nbsp;&nbsp; if p(x) = 3x^1000 + 4x - 1  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;q(x) = x^3 + 20x^2 - 5x + 10  
**while (sp ≤ fp && sq ≤ fq)  

2.2 Stack & Queue  
====
(1) Special linear list, that position of insertion and elimination is limited.  
(2) Used in System SW, such as OS compiler.  
&nbsp;&nbsp;&nbsp;ex) return address in function : save at Stack, CPU scheduling : Queue)  

2.2.1 Stack 
----
(1) Insertion & elimination => only **top**  
(2) Bottom is fixed, top = -1  
(3) LIFO(Last In First Out)  
(4) Push(insert opr), pop(read & delete opr), craete, delete  
(5) When implement it, check its condition with "Stack_empty()" and "Stack_overflow".  
(6) Implementation of queue  
* stack_empty(): *top ≥ MAX_SIZE-1, stack_overflow(): *top == -1  
* void push(int *top, char x): *top++, char pop(int *top): *top--  

2.2.2 Queue 
---
(1) Insertion : rear, Elimintaion : Front  
(2) FIFO(First In First Out)  
(3) Enqueue(insert opr), dequeue(read & delete opr), create, destroy  
(4) Application of queue :  
* level-order search of tree, binary tree  
* breadth-first search of graph  
* scheduling(CPU, Disc), buffer  

(5) Implementation of queue => **Circular Queue**  
* Number of data is "MAX_SIZE-1" (limited)  
* Suppose as if the front and the rear of array are interlocked  
* Insertion and elimination is handled in index's operation  
* front: -1, rear: -1  
* queue_empty(): front == rear, queue_overflow(): front == (*rear+1)%MAX_QSIZE  
* void enqueue(int front, int *rear, char x): *rear = (*rear + 1)%MAX_QSIZE,  
&nbsp;char dequeue(int *front, int rear): *front = (*front+1)%MAX_QSIZE  
* If rear == MAX_QSIZE => **rear = 0**  

2.2.3 Multiple Stack 
---
(1) Several arrays in one pool  
(2) Generally, to implement n-stack in one array, divide array into n pieces and set the top and the bottom  
(3) Initialize multiple stack -> set stack's size equally  
<pre><code>top[0] = bottom[0] = -1;  
for(i = 1; i < n; i++) {
    top[i] = bottom[i] = (MAX_SIZE/n)*i;
}
bottom[n] = MAX_SIZE-1;
</code></pre>
* stack_empty(): top[k] == bottom[k], stack_overflow(): top[k] == bottom[k+1] 
* void push(int k, char x): multiple_stack[++top[k]] = x; char pop(int k): return multiple_stack[top[k]--]  


2.2.4 Application of Stack 
---
2.2.4.1 System Stack  
(1) Call up the sub program/function -> control goes over there => Have to remember the place to return  
(2) Frame ptr saves the stack frame's addr when push opr happens - when pop opr happens  
(3) Return addr saves the addr that returned after sub program executed (실행된 뒤에)  
(4) System stack is necessary when implement the **recrusion function**  

2.3 Linked List
====
2.3.1 Concepts of Linked List 
----
(1)   
(2) Node = Data field + Link field (Last node is NULL)  
(3) insertion :  
&nbsp;elimination :  
&nbsp;concatenation :   

2.3.2 Implementation of Linked Lists
----
2.3.2.1 Static approach (by using **array**, memory waste ↑)  
(1) Declares the record and record array of the node structure (Node 구조의 record and record array)    
(2) Record's link field saves its next node's array index   
(3) NULL's link field value is -1  
(4) List variable saves the index of the first node's array  
(5) Keep the non-using reords to avail list   
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ex) xlist = (a, b, d), ylist = (e, f, g), size = 10   

2.3.2.2 Dynamic approach (by using **Pointer & Dynamic Memory Allocation**)  
(1) Static variable => allocated in complie, fixed til the end   
- global variable, static local variable (data segment)  
- most of the memory allocated to static variable are not used (even it is fixed!) 

(2) Dymanic Varlable => while program is running -> allocate, return  
- use the space in the **heap** segment -> unrelocated to "Heap" that taught in Binary Tree  
- C: use pointer, set the ptr variable(for the addr) and use it  
- although the ptr itself might get addr value, the dynamic variable that ptr assign might be already has its own data type  
&nbsp;&nbsp;&nbsp;char *p  

2.3.3 Implementation of Stack and Queue using Linked List  
---
(1) push(), enqueue() => check if there's any Dynamic Memory left  
(2) pop(), dequueue() => free unneeded Memory  
(3) easier than circular queue  

2.3.4 Circularly Linked Lists  
---
(1) Make the last node point the first node  
(2) Set the list's addr = last node <- know last & first addr easily  
(3) Stack => top: clist -> link  
(4) Queue => rear: clist (when inserting, clist points new node)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;front: clist->link (eliminate the node that pointed by clist->link, make it point next node)  
(5) Concat => possible in O(1)  

2.3.5 Doubly Linked List  
---
(1) Two link (prev, next) => can find previous node easily  
(2) llink(left), rlink(right)  
(3) ptr = ptr->llink->rlink = ptr->rlink->llink  

2.3.5.1 Doubly Circularly Linked List  
(1) Connect the front node and the last node with Ptr  
(2) **Head Node** (to clarify empty list)  
(3) Insertion: dinsert(nodePtr x, nodePtr temp) {  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;temp->llink = x; temp->rlink = x->rlink;  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;x->rlink->llink = temp; x->rlink = temp; }   
(4) EliminatioL ddelete(nodePtr d_list, nodePtr x) {  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;if(d_list == x) -> HeadNode. Can't delete it  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;else {  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;x->llink->rlink = x->rlink;  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;x->rlink->llink = x->llink;  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;free(x);  }  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}  
