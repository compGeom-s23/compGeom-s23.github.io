---
layout: default 
title: Detailed schedule
nav_order: 6
---


### Detailed schedule (Fall 2022)

### Week 1: Introduction and warmup (bubble sort, insertion sort, selection sort). Asymptotic analysis basics.

_Aug 31, Sep 1_

We start by reviewing two fundamental problems---searching and sorting---and going over a couple of simple algorithms. We also review the basics of algorithms analysis using big-oh notation, as well as best-cases and worst-cases.  You are probably familiar with most of this content from Data Structures (if not, you'll need to budget more time this first week). 

__Objectives:__ 
  * Understand searching (linear search, binary search) and simple sorting (bubble sort, selection sort, insertion sort) and be able to compare them, analyze them and apply  them to various inputs
  * Understand the basics of algorithm analysis, big-Oh notation,  best-case and worst-case analysis

__Resources:__     
  * __Lecture:__ [LN-warmup.pdf](docs/week1-LN-warmup.pdf)     
  *  __Lab:__   [Lab 1](docs/lab1.pdf)
  * __Assignment:__ Week1 quiz in Canvas, [Assignment1](docs/hw1.pdf) in Gradescope
  
 ***
 
 
 
### Week 2: Asymptotic Notation and Summations

_Sep 5- 9_

Joke: An infinite number of computer scientists walk into a bar. The first one orders a beer. The second one, half a beer. The third one, a quarter. The barman pours two beers. The computer scientists complain: Is that all you're giving us? The barman says: "Come on guys, you should know your limits! "

The next two weeks introduce the tools for algorithms analysis.  Asymptotic analysis is expressed with O(), Ω() and Θ() notation. We give a formal definition of each one and discuss the differences between them and why big-oh is not sufficient.  We introduce the two summations that come up often: arithmetic and geometric summations. 

This part of the class is heavy on discrete math like logarithms, exponents, limits and recursive functions, which most of you have not seen in a long time.  The bright side is that there are formulas and rules for everything and it's just a matter of practice.  Give yourself time to practice and expect it will take time.   

__Objectives:__ 
* Understand the relevance of analysis in practice, as well as its assumptions and limitations
* Understand the definitions of O(), Ω(), Θ()
* Understand the rate of growth of common functions
* Find the rate of growth of a function
* Compare the order of growth of two arbitrary functions f(n), g(n)
* Analyze basic algorithm running times using O(), Ω(), Θ() 
* Understand arithmetic and geometric summations and their Θ() bound 
* Recognize arithmetic and geometric summations in different forms and give Θ() bounds


__Resources:__    
  * __Lecture:__ [LN-asymptoticNotation.pdf](docs/week2-LN-asymptoticNotation.pdf),  [LN-summations.pdf](docs/week2-LN-summations.pdf), [quiz2-practice.pdf](docs/week2-quiz-practice.pdf)
  * __Lab:__   [Lab2](docs/lab2.pdf) 
  * __Assignment:__   Week2 quiz in Canvas, [Assignment 2](docs/hw2.pdf) in Gradescope
  
***
   
   
   
   
   
### Week 3: Mergesort and Recurrences
_Sep 12-16_

We continue with analysis and introduce  the "recurrence" to express the running time of recursive algorithms. To motivate the first recurrence we introduce a new sorting algorithm called Mergesort.  Mergesort is the first algorithm we see in this class which beats the quadratic bound. 

__Objectives:__ 
* Understand Mergesort: how it works, why it works, and its running time analysis
* Understand how to express the running time of recursive algorithms using recurrences
* Solve recurrences by repeated iteration
* Recognize broadly classes of recurrences ( logarithmic, linear, Θ(n lg n), exponential)

__Resources:__    
  * __Lecture:__ [LN-recurrences.pdf](docs/week3-LN-recurrences.pdf), [quiz3-practice.pdf](docs/week3-quiz-practice.pdf)
   * __Lab:__   [Lab3](docs/lab3.pdf) 
  * __Assignment:__ Week3 quiz in Canvas, [Assignment 3](docs/hw3.pdf) in Gradescope
   
 ***



### Week 4: Heapsort and Quicksort
_Sep 19-23_

So far we discussed the tools necessary for analyzing algorithms (asymptotic notation, summations and recurrences) and we have seen a couple of sorting algorithms at work. This week we introduce new sorting algorithms: Heapsort, Quicksort, and it's randomized version, Randomized-Quicksort.  Randomized-Quicksort is considered the most efficient general-purpose sort in practice.

__Objectives:__ 
* Understand  how the binary heap is defined and the operations supported  (deleteMin, insert, heapify, buildheap) along with their analysis 
* Understand how Heapsort works in place 
* Be able to use the heap as a tool to solve new problems 
* Understand Quicksort, Randomized-Quicksort and analyzis


__Resources:__     
* __Lecture notes:__ [LN-heapsort.pdf](docs/week4-LN-heapsort.pdf), [LN-quicksort.pdf](docs/week4-LN-quicksort.pdf),  [slides-heaps.pdf](docs/week4-slides-heaps.pdf) ; [slides-quicksort.pdf](docs/week4-slides-quicksort.pdf)
* __Lab:__   [Lab4](docs/lab4.pdf)   
* __Assignment:__ Week4 quiz in Canvas, [Assignment 4](docs/hw4.pdf) in  Gradescope

 ***
  
  
  
### Week 5: Sorting lower bound. Faster sorting. Selection. 
_Sep 26-30_

We have seen the most important  sorting algorithms  and all of them have worst-case running times at least Ω(n lg n). The natural question is: Can a sorting algorithm do better than Θ(n lg n) in the worst-case? We introduce the concept of lower bound and show a lower bound for sorting in the comparison model of computation of Ω(n lg n). We describe a couple of different ways to sort (bucket sort and counting sort) which do not use the comparison model  and under certain assumptions run in linear time. 

The second topic this week is the __selection__ problem:  Given a set S of n elements, {x_1, x_2, ..., x_n} and an integer k (1 ≤ k ≤ n), find the kth smallest element in S. We describe several ideas for solving this problem, culminating with an elegant and ingenious algorithm that runs in O(n) worst-case.

__Objectives:__ 
* Understand the comparison-based sorting lower bound, when it applies and what assumptions it makes
* Understand BucketSort and CountingSort,  their analysis and assumptions
* Understand the selection problem and the algorithms for it (quick-select and smart-select)

__Resources:__     
  * __Lecture notes:__ [LN-linsort.pdf](docs/week5-LN-linsort.pdf), [LN-selection.pdf](docs/week5-LN-selection.pdf)
 * __Lab:__  [Lab5](docs/lab5.pdf),  [python-warmup.ipynb](docs/python-warmup.ipynb), [python-insertionSort.ipynb](docs/python-insertionSort.ipynb), [python-mergeSort.ipynb](docs/python-mergesort.ipynb), [python-quickSort.ipynb](docs/python-quicksort.ipynb)
 * __Assignment:__  Week5 quiz in Canvas, [Assignment 5](docs/hw5.pdf) in Gradescope
 *          
 ***



### Week 6: Problems and FLEX time 
_Oct 3-7_

At this point  in the class   (1) you have the tools to analyze algorithms and start to appreciate the interplay between analysis and design (what we mean by this is that analyzing your ideas gives you further ideas for how to improve on your  ideas) and (2) you have seen some fundamental algorithms and building blocks---sorting, priority queues and selection.   This week we'll work on new problems and start talking about techniques.   

__Objectives:__ This week's objective is algorithmic problem solving.  
* You work on  new problems that require using the algorithms learnt so far in new ways
* You understand that algorithmic problem solving is both a science and an art 
* You love this class

__Resources:__
  * __Lecture notes:__ (no new topics this week)
  * __Lab:__   [Lab6](docs/lab6.pdf) 
  *   Exam1 in class
  * __Assignment:__  none this week in view of Fall break 
  <!-- 
[Assignment 6](docs/hw6.pdf) in Gradescope
    -->
 
 ***
 
 
### Fall break!
 
 ***
 
### Week 7: Divide-and-conquer
_Oct  12-14_

What do you do when you want to solve a problem and you don't know where to start?  Coming up with new algorithms is both an art and a science, and although there are no recipes, there are some techniques that come up frequently.  We'll spend the next three weeks looking at more problems,  grouped by the technique used to solve them. 

The first technique is __divide-and-conquer__, which solves a problem by dividing the problem into  smaller subproblems and solving them recursively.  You already saw it  at work in Mergesort. This week you'll see more examples of problems that can be  solved via divide-and-conquer, including Karatsuba's integer multiplication and  Strassen's matrix multiplication algorithms. 

__Objectives:__ 
* Understand how  D&C works in general 
* Understand the D&C algorithms for integer multiplication and matrix multiplication (Karatsuba and Strassen) 
* Apply D&C to new problems

__Resources:__
  * __Lecture notes:__ [LN-divideAndConquer.pdf](docs/week7-LN-divideAndConquer.pdf)
   * __Lab:__   [Lab7](docs/lab7.pdf)
  * __Assignment:__ (no quiz this week);  [Assignment 7](docs/hw7.pdf) in Gradescope
         
 ***
 


### Week 8: Dynamic Programming 
_Oct 17-21_

We introduce the technique called _dynamic programming_ which can be used for optimization problems (problems where we have to find the best  way to do something) that have optimal sub-structure (an optimal solution to a problem contains within it optimal solutions to sub-problems). 

__Objectives:__ 
* Understand  how  dynamic programming  works
* Understand the  examples discussed in the lecture notes (including justification and analysis) 
* Apply DP to new problems 

__Resources:__
* __Lecture notes:__ [LN-dynprog.pdf](docs/week8-LN-dynprog.pdf), [LN-rod.pdf](docs/week8-LN-rod.pdf), [rod-summary.pdf](docs/summary-rod.pdf)
 * __Lab:__   [Lab8](docs/lab8.pdf) , [Fibonacci.ipynb](docs/python-Fibonacci.ipynb), [rodcutting.ipynb](docs/python-RodCutting.ipynb)
* __Assignment:__  (no quiz this week);   [Assignment 8](docs/hw8.pdf) in Gradescope
   
  
 ***
 
 
 
### Week 9: More DP examples and the Greedy technique 
_Oct 24-28_

We add more ddynamic programming examples, and we introduce the greedy technique via the _activity selection_ problem. 

__Objectives:__ 
* Understand the DP solution for the knapsack problem 
* Understand  how  the greedy technique works in general and contrast it with DP
* Understand the greedy solution for the example in the lecture  (activity selection), including the correctness justification 

__Resources:__
* __Lecture notes:__ [LN-knapsack.pdf](docs/week9-LN-knapsack.pdf), [knapsack-summary.pdf](docs/summary-knapsack.pdf), [LN-greedy.pdf](docs/week9-LN-greedy.pdf)
* __Lab:__   [Lab9](docs/lab9.pdf) 
* __Assignment:__ Quiz in Canvas, [Assignment 9](docs/hw9.pdf) in Canvas
   
 ***




### Week 10: More DP and FLEX time
_Oct 31-Nov 4_

We wrap up the module on algorithmic techniques ---divide and conquer, dynamic programming, and greedy---by seeing more examples. 

__Objectives:__ 

* Apply the greedy technique to new problems 
* Reflect on the problems you've seen so far and how the general technique was instantiated  for each problem. 


__Resources:__
* __Lecture notes:__ [LN-lcs.pdf](docs/week10-LN-lcs.pdf) ; [LN-review.pdf](docs/week10-LN-review.pdf) ; [lcs.ipynb](docs/python-LCS.ipynb) ; [summary-lcs.pdf](docs/summary-lcs.pdf)
* __Lab:__   [Lab10](docs/lab10.pdf) 
* __Assignment:__ [Assignment 10](docs/hw10.pdf) in Gradescope 

***



### Week 11: Graphs: Basics, BFS and DFS
_Nov 7-11_

Once you learn about graphs, you start to see their applications  everywhere. This week we start with basic terminology and the traversals, breadth-first and depth-first. These simple algorithms are the stepping stone to many other problems. 

__Objectives:__ 
* Compare and contrast the adjacency list and adjacency matrix representation of a graph 
* Compare and contrast different types of graph: sparse, complete, dense, trees
* Understand basic graph problems:  path, connectivity, connected components, reachability
* Understand breadth-first and depth-first traversals, their complexity,  and their properties 

__Resources:__
* __Lecture notes:__ [LN-graphBasics.pdf](docs/week11-LN-basics.pdf), [LN-bfsdfs.pdf](docs/week11-LN-bfsdfs.pdf)
* __Lab:__   [Lab11](docs/lab11.pdf) 
*  Exam 2 in class
* __Assignment:__  [Assignment 11](docs/hw11.pdf) in Gradescope

***
 
 
 
### Week 12 :  Application of BFS and DFS. Topological order. Shortest paths on DAGs.  
_Nov 14-18_

We introduce the problem of a computing topological order on a directed acyclic graph (DAG).  Then we look at how  topological order can be used to solve various other problems on DAGs, including a simple algorithm for  computing shortest paths on a DAG. 

__Objectives:__ 
* Understand  the concept of topological order and the two algorithms for computing a topological order 
* Use topological order to compute shortest paths on DAGs

__Resources:__
* __Lecture notes:__ [LN-topsort.pdf](docs/week12-LN-topsort.pdf)
* __Lab:__   [Lab12](docs/lab12.pdf)  
* __Assignment:__ Quiz in Canvas, [Assignment 12](docs/hw12.pdf) in Gradescope
  
 ***
 
 
 
 
### Week 13, 14: Shortest paths. 
_Nov 21-Dec 2_

We discuss shortest paths on graphs and see some of the nicest algorithms in computer science: Dijkstra's algorithm and Bellman-Ford's algorithm. While describing them we try to understand some common principles that guided their design.
We'll see that Bellman-Ford's algorithm uses dynamic programming and Dijkstra's  is a greedy algorithm, making these nice applications of the techniques we studied earlier in the semester. 

__Objectives:__ 
* Understand the algorithms for computing shortest paths explained in the notes:  how they work, why they work, and their complexity

__Resources:__
* __Lecture notes:__ [LN-shpaths.pdf](docs/week13-LN-shpaths.pdf)
*  __Lab:__   [Lab13](docs/lab13.pdf) 
* __Assignment:__ Quiz in Canvas, [Assignment 13](docs/hw13.pdf) in Gradescope
                   
 ***
 
 
 
### Week 15: Minimum spanning tree. 
_Dec 5-9_

We  introduce  another fundamental problem on graphs, the Minimum Spanning Tree (MST). We'll see a couple of properties of MSTs which will get us intuition for how to compute an MST efficiently. We'll glance at two well-known algorithms, Prim's and Kruskal's,  which are both greedy algorithms much in the spirit of Dijkstra.  Their correctness follows from a neat result called The Cut Theorem.   

This last week we'll also do a quick review and work on some extra fun problems!

__Objectives:__ 
* Understand the concept of MST (minimum spaninng tree) in a graph, and be able to answer basic questions about it sproperties
* Know the general idea of Kruskal's and Prim's algorithms, and the Cut Theorem which captures their correctness

__Resources:__
* __Lecture notes:__ [LN-mst.pdf](docs/week14-LN-mst.pdf), [LN-mst-summary.pdf](docs/week14-LN-mst-summary.pdf), [LN-review.pdf](docs/week14-LN-review.pdf)
* __Lab:__   [Lab14](docs/lab14.pdf) , [problem-trappingRain.pdf](docs/problem-trappingrain.pdf)

                      
***

Final exam: According to Polaris, we have two exam slots: 12/15 8:30-11:30am, and 12/19, 8:30-11:30am.  I have booked large rooms for both days (xact location will be announced on Slack). Choose  the slot that works best for you and just show up.  

***
