---
layout: default
title: Quizzes
---

<table id="customers">
  <tr>
    <th> # </th>
    <th>Topic</th>
    <th>Date</th>
    <th>Questions</th>
    <th>Solutions</th>
  </tr>
  {% for iteml in site.data.quiz %}  
    {% assign item = iteml[1] %}
    <tr>
        <td>{{ item.num }}</td>
        <td> {{ item.topic }} </td>
        <td> {{ item.date | date: "%b %d" }} </td>
        <td> 
            {% if item.questions-link %}
            <a href="{{ site.base }}{{ item.questions-link }}"
                style="text-decoration: none">
                <img class="homework-icon"
                    alt="Homework {{ item.num }} Questions"
                    title="Homework {{ item.num }} Questions"
                    src="{{ site.base }}/img/icons/lab_questions.png" />
            </a>
            {% endif %}
        </td>
        <td> 
            {% if item.solutions-link %}
            <a href="{{ site.base }}{{ item.solutions-link }}"
                style="text-decoration: none">
                <img class="homework-icon"
                    alt="Homework {{ item.num }} Questions"
                    title="Homework {{ item.num }} Questions"
                    src="{{ site.base }}/img/icons/lab_solutions.png" />
            </a>
            {% endif %}
        </td>
    </tr>        


  {% endfor %}

</table>

&nbsp;

Couple things to note about quizzes:
- Quizzes will be conducted in-person during your assigned discussion section. 
- Quizzes will consist of **one problem** related to the previous lecture/lab. The questions will be of varying forms  
- The quizzes consists 25% of your final course grade. Each quiz will contribute up to 2 points to your final question average (up to 25 points). 
- It's a bad idea to skip quizzes. Even if you've maxed out your quiz points for the semester, I'd still recommend going to lab and taking the quizzes to stay up to date with the material. 
- Yes there are 8 discussion sections and 8 versions of every quiz. I will monitor the averages of each section closely to ensure the quiz average of every section is roughly equal. 

### Quiz Grading Policies: 

- **Quizzes** are graded by the entire course staff, within Gradescope. All quizzes are graded on a scale 0-2 points.  
- The quiz part of the final grade is worth 25%. Each quiz is worth two points toward that total. That means you only need to get 12.5 out of the 20 quizzes correct in order to achieve full credit for the quiz portion of your grade!
- Under normal circumstances, all quizzes should be graded within two weeks of submission. However, your graders also have significant responsibilities and may take longer to grade. **Let's all be kind and give eachother some grace.** After the due date the quiz questions and solutions are immediately posted. I would suggest against immediately  
- Partial credit is given for work that is very close to being correct. 
- **We will give zero points for long and tedious solutions** (i.e., solutions that are longer than the official solutions by a significant amount). We reserve the right of not even reading your solution if it exceedingly and unnecessarily long. In this course (and in life), **conciseness matters**.
>If I had more time, I would have written a shorter letter. 
><cite> - [Unknown](https://www.lb7.uscourts.gov/documents/314-cv-921.pdf) <cite>
- Along a similar theme, submissions with multiple solutions will be marked incorrect.  


### Missing a Quiz

If you are unable to attend a lab for any reason, you can simply drop that quiz. Again, you only need to get 12.5 quizzes correct to get full credit toward your final grade. You have a buffer of 7.5 quizzes to drop before it impacts you! For this reason, **there are no make-up quizzes**. 
- If I was to give make-up quizzes, I might as well not offer any drops and just take the quiz average for the final grade. I think we can all agree that dropping 7.5 misses is a far more generous policy. 

### Low quiz average

In general I am not a fan of assigning more work to force knowledge. Like in theory if I assigned 20 homeworks, 20 quizzes, and 5 exams people would learn more ... but is it worth it? Balance is important but the difficult thing for me is that for some students, they have already mastered the material and hence, extra homeworks/quizzes ends up being nothing more than a penalty. And I don't want to force people to work unnecessarily. 

So here's the deal. If you believe that the quizzes are nonsense and you are able to master the material without them, then I believe you. You don't have to do the quizzes but I will take the average *unweighted (no curve)* exam score and use that as your quiz average. If you can master the material without the quizzes, great, that means your exams should have high averages and you don't lose anything by skipping the quizzes and labs. 

The deal extends to even if you've taken the quizzes but performed poorly. Again, I am going to take the average of your un-curved exams and your quiz total and use whatever is more. 

So in addition to drops, you have an out this way too. As long as you master the material, there is no reason not to do well in this course. 

### Regrades

Regrades requests would be open for a week once grades are released (except for final exam because of registrar grade submission deadlines). Regrade requests are not intended for arguing about point allocation, or whether the grading scale is fair.

Unfortunately, certain students think that they can tire us into giving them point that they did not earn, by keep asking for unjustified regrade requests. As such, superfluous, argumentative and repetitive regrade requests, after an appropriate warning, would result in a zero on the relevant questions - please do not waste our time. Again if you are the type of student that is hesitating on whether to submit a regrade request this abolsutely does not apply to you. This policy is for the 1-2 students (out of 300) who just submit a two word regrade request for every question in their exam (I wish I was exaggerating). Please do not let this policy scare you from submitting a regrade request. 

### How to study
For every lecture and lab, ask yourself "If I saw the problem without the aid of the solution, would I be able to perform it correctly?" If the answer is yes, you're probably in good shape for the quizzes. If the answer is no, you got some trouble ahead of you. The best thing you can do for yourself is go to every single lecture and lab, and if you have any doubts about any questions, try to work through them **without the solutions!** Everything makes sense when you read the solution. Coming up with the solution on your own is the difficult part that requires practice.   

### DRES
- If you have a DRES accommodation, please email the course staff directly (not sure if sending documents over Piazza is compliant with EHR policies or not, but why risk it). Make sure I respond that I've recorded your accommodation! If I don't respond email again.
- Because of the quiz structure (10 minutes at the beginning of discussion), DRES accommadations for the quizzes will be limited. There will be a 10 minute quiz at the beginning of discussion followed by a 5 minute cool down period and this extra time is potentially available to DRES students that require extra time. However, not much else is feasible. If you require extra accommadations please email the course staff. Remember that the quizzes are made to be brief and only require five minutes so extra time will likely not be even necessary.