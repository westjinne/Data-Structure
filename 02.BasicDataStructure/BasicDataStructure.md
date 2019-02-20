2.1 Linear List
================================

* Linear list, ordered list, or just list (cuz "order" is important in here.)  
* Element. (if there's no element, => empty list. A = {})  
* A = (a𝟶, a𝟷, ..., a𝑛-𝟷) ≠ A = {a𝟶, a𝟷, ..., a𝑛-𝟷}  

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
