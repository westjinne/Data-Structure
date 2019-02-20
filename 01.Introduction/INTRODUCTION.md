1.1 Data structure and Algorithm
================================

1.1.1 Concept of Data Structure
--------------------------------
(1) Abstract data type : datas and models (of data's operation)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ex) Integer, Phonebook, Stack, Queue  
(2) Data type : dta object provided by programming language and valid operations.   
(3) Data structure : data organization, management and storage format that enables efficient access and modification.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ex) Stack, Queue, Binary tree, Graph

1.1.2 Relationship between Data structure and Algorithm
--------------------------------
(1) Program = Data Structure + Algorithm  
(2) If the program is a sentence, the data structure must be nouns and algorithm be verbs.  

1.4 Algorithm Analysis
================================
* Algorithm  =   
(1) input   
(2) output   
(3) definiteness   
(4) finiteness (it must be end after finite steps)  
(5) effectiveness   

1.4.1 Effectiveness of Algorithm and complexity function
--------------------------------
* Bacis operation  
ex) sort - compare its elements  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;search - compare keys and elements  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;multiply of matrix - addition and multiplication  
* Time Complexity (=> loop)  
(1) time complexity function : T(n), n is a size of problem (Generally, number of input)  
(2) worst-case time complexity function : T𝑤(n) = max{t(I)| I∈D𝑛}   
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(D𝑛 : set of all inputs(size n), I : element of D𝑛, t(I) : count number of algorithm's basic operation)
* Average analysis(expected-case analysis) : T𝑒(n) = ∑p(I)t(I) (p(I) : probability of input "I" happens)  
* Space complexity  
(1) Memory or space to save *input, temp result, final result*  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ex) Size of array, linked list  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Size of stack used in system  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Size of stack used in program  

1.4.2 Order notation : The Big O  
------------------------
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1 : constant  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;log n : log  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;log^2 n : square of log  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;n : linear  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;nlog n:  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;n^2 : quadratic  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;n^3 : cubric  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2^n : exponential  

1.5 Recursion Algorithm & Iteration Algorithm  
==========
* Recursion : function of procedure's recursive call  
- When problem or Data Structure is defined recrusively  
- Effectiveness if provlem solving, prooving accuracy of algorithm  
- Ineffect in time, space  
* Iteration : for, do, while loop  
(1) Factorial - Space complexity : S𝒓(n) = 𝜭(n)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;S𝒊(n) = 𝜭(1)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Time complexity :&nbsp;&nbsp;&nbsp;T𝒓(0) = 0  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;T𝒓(n) = n ∈ 𝜭(n)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;T𝒊(n) = n ∈ 𝜭(n)  
(2) Fibonacci - Space complexity : S𝒓(n) = n  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;S𝒊(n) = 𝜭(n)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Time complexity : T𝒓(n) = 0 (if n = 0 or 1)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;T𝒓(n) = O(c^n), c = (1+√5)/2, if n ≥ 2)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;T𝒊(n) = 𝜭(n)  
(3) Hanoi tower - Time complexity : T𝒓(1) = 1  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;T𝒓(n) = 2^n - 1 (n ≥ 2)   
** Recursion is one of the most basic concept in Computer Science. Usually, recrusion algorithm is designed by a divide - and - conquer algorithm. 
