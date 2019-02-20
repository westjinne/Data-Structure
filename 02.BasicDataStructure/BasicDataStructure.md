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
* stack_empty() : *top ≥ MAX_SIZE-1, stack_overflow() : *top == -1  
* void push(int *top, char x): *top++, char pop(int *top) : *top--  

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
* queue_empty(): front == rear, queue_overflow() : front == (*rear+1)%MAX_QSIZE  
* void enqueue(int front, int *rear, char x) : *rear = (*rear + 1)%MAX_QSIZE,  
&nbsp;char dequeue(int *front, int rear) : *front = (*front+1)%MAX_QSIZE  
* If rear == MAX_QSIZE => **rear = 0**  

