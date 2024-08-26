---
title: Lecture 21 - NP-complete problems and reductions II
placeholder: false
back-color: fffaff
card-link: LecLink21
# subtitle: And a subtitle
description: We'll discuss more NP-complete problems/reductions and specifically focus on reductions requiring gadgets. 
people:
layout: lecture
# no-link: true  # stops link to page 
deliverydate: 2023-11-09
link-slides: /materials/lecture_slides/lec22.pdf
link-scribbles: /materials/lecture_slides/lec22_scribbles_sp23.pdf
link-recording: https://mediaspace.illinois.edu/media/t/1_2iaj8d73
pre-recording: https://youtube.com/playlist?list=PLmCFrqjQFNr2JxxkGoKPOvw07jhp4nyle&si=tQLAb4UP5_Hu6bwb
---


<h4> Jigsaw Problem Reduction </h4>

I'm a huge fan of the youtube channel [StuffMadeHere](https://www.youtube.com/c/StuffMadeHere?app=desktop) where a professional machinist named Shane Wighton makes fun little objects/robots to perform complex tasks. Four months ago he dropped a video about making a robot that can solve a large jigsaw puzzle.

Super cool but not the point of this post. As many of you know (or will soon learn), building the robot is only half the battle! You need to give the robot a (hopefully fast) brain. In the [original video](https://www.youtube.com/watch?v=Gu_1S77XkiM), Mt. Wighton promised to post a follow-up video where he discusses all the algorithms he used to enable his robot to solve a multi-thousand piece video. That's the video he posted today:

[https://www.youtube.com/watch?v=WsPHBD5NsS0](https://www.youtube.com/watch?v=WsPHBD5NsS0)

My favorite part of this video is that it presents quite a few algorithmic concepts and how they relate to this cool fun application of building a jigsaw solving robot. Most of the stuff he presented are well-known heuristic and approximate algorithms which are a class of algorithms devoted to improving the average compute time (amortized analysis) of known NP problems (even if the worst-case running time is still exponential). Heuristic/approximate algorithms are why there are SAT solvers that can solve SAT formulas with tens of thousands of literals and clauses in minutes!

One of your CAs, Mr. Sumedh Vemuganti decided that it might be fun to [prove if the JigSaw puzzle problem is NP-Complete](/materials/extra_content/Jigsaw_Sumedh.pdf) (spoiler: depends on how we define the problem)

<h4>Additional Resources</h4>

* Textbooks 
  * Erickson, Jeff. *Algorithms* 
    * [Chapter 12 - NP-Hardness](https://jeffe.cs.illinois.edu/teaching/algorithms/book/12-nphard.pdf)
  * Sipser, Michael. *Introduction to the Theory of Computation*
    * Chapter 7 - Time Complexity
  * Skiena, Steven. *The Algorithms Design Manual*
    * Chapter 11 - NP-completeness
  * Sedgewick, Robert and Wayne, Kevin. *Algorithms (Forth Edition)*
    * Chapter 6 - Context.Intractability
  * Cormen, Thomas, et al. *Algorithms (Forth Edition)*
    * Chapter 32 - NP-Completeness 
    
* [Sariel's Lecture 23](https://www.youtube.com/watch?v=jXH40tp_RcI&list=PLaEwgrahG-Lq0llcS-fcyCDTQdFm3peLZ&pp=iAQB)






