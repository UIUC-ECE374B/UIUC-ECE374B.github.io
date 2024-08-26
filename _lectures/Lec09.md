---
title: Lecture 9 - Recursion and reductions
placeholder: false
back-color: fffffa
card-link: LecLink09
# subtitle: And a subtitle
description: "We'll begin the algorithms portion of our course with a quick recap of the most fundamental algorithmic technique: recursion. We'll also briefly go over solving recurrences. "
people:
  - nicholas
layout: lecture
# no-link: true  # stops link to page 
deliverydate: 2023-09-26
link-slides: /materials/lecture_slides/lec10.pdf
link-scribbles: /materials/lecture_slides/lec10_scribbles_sp23.pdf
link-recording: https://mediaspace.illinois.edu/media/t/1_9t2dnipk
pre-recording: https://www.youtube.com/playlist?list=PLmCFrqjQFNr1WA3qnzZU7viSjYaoOR1Ro
---

### Algorithms
#### **Algorithmic Problem**:
An algorithmic problem is to compute $f: \Sigma^\ast \rightarrow \Sigma^\ast$, a functions over the strings of a finite alphabet. We say an algorithm solves $f$ if for every input sting $\omega$ the algorithm outputs $f(\omega)$

#### **Types of Algorithmic Problems**:
- Decision Problems: Is the input a YES or a NO

    example: Given a graph $G$, for nodes $s,t$ is there a path from $s$ to $t$ in $G$.
- Search Problems: Find a solution if the input is a YES

    example: Given a graph $G$, for nodes $s,t$ find a path from $s$ to $t$ in $G$.
- Optimization Problem: Find the best solution if the input is a YES

    example: Given a graph $G$, for nodes $s,t$ find the shortest path from $s$ to $t$ in $G$.

#### **Analysis of Algorithmic Problems**:
- Does the algorithm correctly solve the problem.
- What is the asymptotic worst-case running time of the algorithm.
- What is the asymptotic worst-case space used by the algorithm.

An algorthim has an asymptotic running time of $O(f(n))$ if for every input of size $n$ the algorithm terminates after $$O(f(n))$$ steps.

### Reductions
A reduction from problem $A$ to problem $B$ is formatting problem $A$ in terms of problem $B$. The algorithm for $A$ uses the algorithm for $B$ as a black box.

example: Given an array $A$ of n integers, are there any duplicates in $A$.

Solving directly by comparing every element to every other element takes $O(n^2)$ running time. If we sort the array first then elements only need to be compared to adjacent elements which takes total $O(n log(n))$ running time. This is a reduction of the duplicate elements problem into the sorting problem when we use the sorting algorithm as a black box.

#### **Types of Reductions**:
Given 2 problems $C$ and $D$ where problem $C$ reduces to problem $D$
- Positive Direction: Constructing an algorithm for $C$ implies a construction of an  algorithm for $D$. 
- Negative Direction: If the reduction from problem $C$ to problem $D$ **is** "efficient". Assuming there **is no** "efficient" algorithm for $C$ implies there **is no** "efficient" algorithm for $D$


### Recursions
A recursion is a special case of reduction where the problem is reduced to a "smaller" instance of itself.

example: Tower of Hanoi, moving a tower of size $n$ from peg $0$ to peg $2$.

The problem can be generalized to move a tower of size $m$ from peg $x$ to peg $y$. Then the problem of moving a tower of size $n$ from peg 0 to peg 2 can be viewed as moving a tower of size $n-1$ from peg 0 to peg 1, then moving the bottom disk to peg 2, and finally moving the tower of size $n-1$ from peg 1 to peg 2. Therefore a general algorithm that moves a tower of size $m$ from peg $x$ to peg $y$ can be recursively implemented as the ordering/ labeling of the pegs does not impact the problem.

#### **Running Time Analysis**:
- Recursion Tree: A recurrence relation can be viewed as tree which splits at a node based on the integer constant that multiplies the recurrent function. Then the running time can be computed by looking at the running time contributed by each layer in the tree.

example: $T(n) = 2T(n/2)+cn$ split into 2 after each node but the running time contributed by each split is $cn/2$. This results in a constant amount of work done at each level. The total running time is the sum of the running times for each level. Because $n$ divides by 2 each time, there are $log(n)$ levels. This results in a total running time of $O(nlog(n))$.

<img src="/img/lectures/Lec10/lec10_fig1.PNG" alt="Example3" style="height: 150px;">

- Expanding the Recurrence: Expanding the recurrence is done by replacing the recurrent function on the right side of the equation the right hand side of the equation for the smaller case.

example: $T(n) = 2T(n/2) + cn$ can be rewritten as $T(n) = 2(2T(n/4)+cn/2)+cn = 4T(n/4)+cn+cn$. This replacement can occur $log(n)$ times because $n$ divides by 2 each time. Every time the replacement occurs an extra $cn$ is added. This means the eventual expansion will be $T(n) = cn+...cn = cnlog(n)$ which has a running time of $O(nlog(n))$.

<h4>Additional Resources</h4>

* Textbooks 
  * Erickson, Jeff. *Algorithms* 
	* [Chapter 1 - Recursion](https://jeffe.cs.illinois.edu/teaching/algorithms/book/03-dynprog.pdf)
  * Skiena, Steven. *The Algorithms Design Manual*
    * Chapter 1.5 - Modeling the Problem
    * Chapter 2.1 - The RAM Model of Computation
    * Chapter 2.2 - The Big Oh Notation
    * Chapter 2.5 - Reasoning about Efficiency
  * Sedgewick, Robert and Wayne, Kevin. *Algorithms (Forth Edition)*
    * Chapter 1.1 - Basic Programming Model
  * Cormen, Thomas, et al. *Algorithms (Forth Edition)*
    * Chapter 2.3 - Designing Algorithms
    * Chapter 4 - Divide and Conquer 
    * Chapter 4.4 - The recursion tree method for solving recurrences
    * Chapter 4.5 - The master method for solving recurrences

- [Sariel's Lecture 10](https://courses.engr.illinois.edu/cs374/fa2020/lec_prerec/) 
- [Great Reducible video on Towers of Hanoi](https://www.youtube.com/watch?v=rf6uf3jNjbo)
* [Sariel's Lecture 10](https://www.youtube.com/watch?v=vBl8JSdKrvw&list=PLaEwgrahG-LpCO04ip9-KfGIYSr1YGbwE&pp=iAQB)













