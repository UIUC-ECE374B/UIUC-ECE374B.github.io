---
title: Lecture 0 - Course introduction and languages
placeholder: false
back-color: faffff
card-link: LecLink00
# subtitle: And a subtitle
description: This is the first lecture of the course. We'll discuss the course policies and why we model problems as languages.  
people:
  - kani
layout: lecture
# no-link: true  # stops link to page 
deliverydate: 2023-08-22 #last updated date
link-slides: /materials/lecture_slides/lec0.pdf
link-scribbles: /materials/lecture_slides/lec0_scribbles_fa23.pdf
link-recording: https://mediaspace.illinois.edu/media/t/1_eqr6mwfe
pre-recording: 
---

Course policies can be found on the website [ecealgo.com](https://ecealgo.com).

#### Big Questions

This course is focused on answering three big questions: 

- Given infinite time, how can we group problems by their "complexity" (Computability-theory)
- Given finite time, but a problem we know is computable, how fast can we solve the problem (Algorithmic design)
- Given a problem which is difficult to solve, can we infer how slow/fast we can solve it by comparing it to other known problems (Reductions)

&nbsp;
#### Two types of complexity
&nbsp;

| Computational Complexity      | Algorithmic Complexity |
| -----------                   | -----------            |
| <img src="/img/lectures/Lec1/Chomsky_Hierarchy-REfilled.png" alt="Chomsky Hierachy" style="height: 300px;">  | <img src="/img/lectures/Lec1/Algorithmic_complexity.png" alt="Algorithmic Complexity" style="height: 300px;">       |


&nbsp;
#### Why Languages? 
Problems need to be represented as languages to be comparable. A language is a set of strings and each string represents and *instance* of the problem (a specific set of inputs and their corresponding output). For example, the problem of adding two numbers together can be represented by the language: 

**Problem:** Multiplying two integers together               

**Language:** 
$$L_{MULT2} = 
\begin{bmatrix}
  1 \times 1|1, & 1 \times 2|2, & 1 \times 3|3, \ldots\\
  2 \times 1|2, & 2 \times 2|4, & 2 \times 3|6, \ldots \\
  \vdots & \vdots & \vdots \\
  n \times 1|n, & n \times 2|2n, & n \times 3|3n, \ldots \\
\end{bmatrix}$$


&nbsp;
<h4>Additional Resources</h4>

* Textbooks 
  * Erickson, Jeff. *Algorithms* 
    * [Jeff's Textbook - Introduction and History](https://jeffe.cs.illinois.edu/teaching/algorithms/book/00-intro.pdf)
    * [Jeff's - Notes on strings](https://jeffe.cs.illinois.edu/teaching/algorithms/models/01-strings.pdf)
  * Sipser, Michael. *Introduction to the Theory of Computation*
    * Chapter 0 - Introduction - Mathematical Notation and Terminology  
* [Sariel's Lecture 1](https://www.youtube.com/watch?v=Szd-pWE2Ztc)
* [Very cool use of induction with hydra problem](https://www.youtube.com/watch?v=prURA1i8Qj4)
