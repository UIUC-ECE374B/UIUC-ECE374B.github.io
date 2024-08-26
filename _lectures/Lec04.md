---
title: Lecture 4 - DFA/NFA/RegEx equivalence and grammars
placeholder: false
back-color: faffff
card-link: LecLink04
# subtitle: And a subtitle
description: DFA/NFA/RegEx's can be converted from one form to another using the simple methods discussed in this lecture. 
people:
  - sandhya
layout: lecture
# no-link: true  # stops link to page 
deliverydate: 2023-09-05
link-slides: /materials/lecture_slides/lec4.pdf
link-scribbles: /materials/lecture_slides/lec4_scribbles_fa23.pdf
link-recording: https://mediaspace.illinois.edu/media/t/1_lpb396cl
pre-recording: 
---

<style>
  table{
    border-collapse:separate;
    border-spacing: 40px 0px;
  }
</style>

<p style="text-align:center;"><img src="/img/lectures/Lec5/Eq_diag.png" alt="Equivalence diagram" style="height: 300px;" class="center"> </p>

<h4> 1. DFA → NFA </h4>

All DFAs can represent any languages that are represented by NFAs. All DFAs by definition are NFAs.

<h4> 2. NFA → DFA </h4>

Consider any non-deterministic finite automata **(NFA) N = $(Q, \Sigma, \delta, s, A)$** where :<br><br>
• Q is a finite set whose elements are called states,<br>
• $\Sigma$ is a finite set called the input alphabet,<br>
• $\delta$ : Q × $\Sigma$ $\cup$ {$\epsilon$} → P(Q) is the transition function (here
P(Q) is the power set of Q),<br>
• s ∈ Q is the start state,<br>
• A ⊆ Q is the set of accepting/final states.<br>

$\delta$(q, a) for a $\in$ $\Sigma$ $\cup$ {$\epsilon$} is a subset of Q — a set of states.

An equivalent **DFA D = $(Q', \Sigma, \delta', s', A')$** can be constructed using the **Subset State Construction** such that:

• $Q' = P(Q)$<br>
• $$s' = \epsilon  reach(s) = \delta^{*}(s,\epsilon)$$<br>
• $A' = \{ X \subseteq Q | X \cap A \neq \emptyset\}$<br>
• $\delta'(X, a) = \bigcup\limits_{q \in X} \delta^{*} (q,a) for each X \subseteq Q , a \in \Sigma$<br>

<h4> 3. Regular Expressions → NFA </h4>

Any regular expression can be converted to an NFA using the Thompson’s Algorithm as follows:

<table border='0'> 
  <tr>
    <td>
      <img src="/img/lectures/Lec5/tp_union.png" alt="Union" style="width: 320px;">
    </td>
    <td>
      <img src="/img/lectures/Lec5/tp_concat.png" alt="Concatenation" style="width: 350px;">
    </td>  
    <td>
      <img src="/img/lectures/Lec5/tp_star.png" alt="Kleene star" style="width: 300px;">
    </td>  
  </tr>
</table>
<br>
Example: Construct a NFA for (101 + 010) <br>
<img src="/img/lectures/Lec5/tp_eg.png" alt="Example" style="width:1000px;" >
<h4> 4. DFA → Regular Expressions </h4>

A Regular expression can be obtained from a DFA using two methods.

<b> A. State Removal Method </b>

If q1 = $\delta$(q0, x) and q2 = $\delta$(q1, y), then q2 = $\delta$(q1, y) = $\delta$($\delta$(q0, x), y) = $\delta$(q0, xy). This way, we can eliminate state q1.

<img src="/img/lectures/Lec5/strem.png" alt="State removal method illustration" style="width: 850px;">

Example: 

<img src="/img/lectures/Lec5/state_eg.png" alt="State removal method example" style="width: 1000px;">

Therefore, the resulting regular expression for the given DFA is $(01 + (1 + 00)(10)^{∗}(0 + 11))^{∗}$

<b> B. Algebraic Method </b>

This method involves treating transition functions as algebraic expressions. That is,  $q_1 = \delta(q_0, x)$ can be written as $q_1 = q_0x$ and the resulting expressions can be solved for the accepting state.

Example: Convert the following DFA to regular expression using Algebraic Method.

<img src="/img/lectures/Lec5/agdfa.png" alt="Algebraic method example" style = "width: 400px;">

Writing down transitions as algebraic functions :<br>
• $q_{0} = \epsilon + q_{1}1 + q_{2}0$<br>
• $q_{1} = q_{0}0$<br>
• $q_{2} = q_{0}1$<br>
• $q_{3} = q_{1}0 + q_{2}1 + q_{3}(0 + 1)$<br>

Now we simple solve the system of equations for $q_{0}$:<br>
•  $q_{0} = \epsilon + q_{1}1 + q_{2}0$<br>
=> $q_{0} = \epsilon + q_{0}01 + q_{0}10$<br>
=> $q_{0} = \epsilon + q_{0}(01 + 10)$<br>

Make use of Theorem (Arden’s Theorem) that states $R = Q + RP = QP^{∗}$<br>

=> $q_{0} = \epsilon(01 + 10)^{∗} = (01 + 10)^{∗}$<br>

<h4> 5. NFA → Regular Expressions </h4>

Any NFA can be converted to regular expressions using the same two methods as listed above :

• Algebraic Method - Treat transition functions as algebraic functions and solve for accepting state.

• State Removal Method - Normalize the NFA to have an isolated starting and ending state and then follow the same process as listed above.

Example:

<img src="/img/lectures/Lec5/part1.png" alt="State removal method illustration- NFA pt1" style="width: 1000px;">
<img src="/img/lectures/Lec5/part2.png" alt="State removal method illustration- NFA pt2" style="width: 1000px;">

<h4> 6. Regular Expressions → DFA </h4>

To convert Regular Expressions to DFA we can make use of the Brzozowski derivative, where ($u^{−1}$ S) of a set S of strings and a string u is the set of strings obtainable from a string in S by cutting of the prefix u.

Example: To construct language $R = (ab + c)^{*}$
<br><br>
<div class="row">
    <div class="col-md-3">
        <b> R </b>
    </div>
    <div class="col-md-3">
        <b> $a^{-1}R$ </b>
    </div>
    <div class="col-md-3">
        <b> $b^{-1}R$ </b>
    </div>
    <div class="col-md-3">
        <b> $c^{-1}R$ </b>
    </div>
 </div>
 <hr>
 <div class="row">
    <div class="col-md-3">
        $q_0 = \epsilon^{-1}R = (ab+c)^{*}$
    </div>
    <div class="col-md-3">
        $b(ab + c)^{*}$
    </div>
    <div class="col-md-3">
        $\emptyset$ 
    </div>
    <div class="col-md-3">
        $(ab + c)^{*}$ 
    </div>
 </div>
 <div class="row">
    <div class="col-md-3">
        $q_1 = b(ab + c)^{*}$
    </div>
    <div class="col-md-3">
        $\emptyset$ 
    </div>
    <div class="col-md-3">
        $(ab + c)^{*}$
    </div>
    <div class="col-md-3">
        $\emptyset$ 
    </div>
 </div>
 <div class="row">
    <div class="col-md-3">
        $q_2 = \emptyset$
    </div>
    <div class="col-md-3">
        $\emptyset$ 
    </div>
    <div class="col-md-3">
        $\emptyset$ 
    </div>
    <div class="col-md-3">
        $\emptyset$ 
    </div>
 </div>
<br>

<h4>Additional Resources</h4>

* Textbooks 
  * Erickson, Jeff. *Algorithms* 
    * [Jeff's - Notes on non-deterministic automata](https://jeffe.cs.illinois.edu/teaching/algorithms/models/04-nfa.pdf)
  * Sipser, Michael. **Introduction to the Theory of Computation*
    * Chapter 1 - Regular Languages
* [Sariel's Lecture 5](https://www.youtube.com/watch?v=jyIgH1T2Npk&list=PLaEwgrahG-Lo_6PDz_2UrsK9bkPtbd8y0&pp=iAQB)
* Check out Mike Montano's [NFA-to-DFA subset construction](/resources/SubsetConstruction) tool to visualize how to convert a NFA to a DFA!
* Rust has a pretty robust RegEx library and a former 374-er spent some time investigating Rust's procedural macros and how to convert a RegEx to a NFA. It's a super interesting analysis requiring knowledge of grammars and programming paradigms. [Check it out](https://github.com/djohn49/fastregex)






