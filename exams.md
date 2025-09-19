---
layout: default
title: Exams
---

<table id="customers">
  <tr>
    <th> # </th>
    <th>Topic</th>
    <th>Date</th>
    <th>Skillset</th>
    <th>Cheat Sheet</th>
    <th>Samples</th>
    <!-- <th>Sample 2</th> -->
    <th>Exam & Solutions</th>
  </tr>
  {% for iteml in site.data.exam %}  
    {% assign item = iteml[1] %}
    <tr>
        <td>{{ item.num }}</td>
        <td> {{ item.topic }} </td>
        <td> {{ item.date | date: "%b %d" }} </td>
        <td> 
        <!-- Skillset  -->
            {% if item.skillset %}
            <a href="{{ site.base }}{{ item.skillset }}"
                style="text-decoration: none">
                <img class="homework-icon"
                    alt="{{ iteml[0] }} skillset"
                    title="{{ iteml[0] }} skillset"
                    src="{{ site.base }}/img/icons/notes.png" />
            </a>
            {% endif %}
        </td>
        <td> 
        <!-- Cheatsheet  -->
            {% if item.cheat_sheet %}
            <a href="{{ site.base }}{{ item.cheat_sheet }}"
                style="text-decoration: none">
                <img class="homework-icon"
                    alt="{{ iteml[0] }} cheat sheet"
                    title="{{ iteml[0] }} cheat sheet"
                    src="{{ site.base }}/img/icons/cheat_sheet_icon.png" />
            </a>
            {% endif %}
        </td>
        <td> 
        <!-- Sample Exam 1 -->
            {% if item.samp_exam1 %}
            <a href="{{ site.base }}{{ item.samp_exam1 }}"
                style="text-decoration: none">
                <img class="homework-icon"
                    alt="{{ iteml[0] }} sample exam"
                    title="{{ iteml[0] }} sample exam"
                    src="{{ site.base }}/img/icons/lab_questions.png" />
            </a>
            {% endif %}
            {% if item.samp_exam2_sol %}
            <a href="{{ site.base }}{{ item.samp_exam1_sol }}"
                style="text-decoration: none">
                <img class="homework-icon"
                    alt="{{ iteml[0] }} exam solutions"
                    title="{{ iteml[0] }} exam solutions"
                    src="{{ site.base }}/img/icons/lab_solutions.png" />
            </a>
            {% endif %}              
        <!-- Sample Exam 2 -->
            {% if item.samp_exam2 %}
            <a href="{{ site.base }}{{ item.samp_exam2 }}"
                style="text-decoration: none">
                <img class="homework-icon"
                    alt="{{ iteml[0] }} sample exam"
                    title="{{ iteml[0] }} sample exam"
                    src="{{ site.base }}/img/icons/lab_questions.png" />
            </a>
            {% endif %}
            {% if item.samp_exam2_sol %}
            <a href="{{ site.base }}{{ item.samp_exam2_sol }}"
                style="text-decoration: none">
                <img class="homework-icon"
                    alt="{{ iteml[0] }} exam solutions"
                    title="{{ iteml[0] }} exam solutions"
                    src="{{ site.base }}/img/icons/lab_solutions.png" />
            </a>
            {% endif %}       
            <br>     
        <!-- Sample Exam 3 -->
            {% if item.samp_exam3 %}
            <a href="{{ site.base }}{{ item.samp_exam2 }}"
                style="text-decoration: none">
                <img class="homework-icon"
                    alt="{{ iteml[0] }} sample exam"
                    title="{{ iteml[0] }} sample exam"
                    src="{{ site.base }}/img/icons/lab_questions.png" />
            </a>
            {% endif %}
            {% if item.samp_exam3_sol %}
            <a href="{{ site.base }}{{ item.samp_exam2_sol }}"
                style="text-decoration: none">
                <img class="homework-icon"
                    alt="{{ iteml[0] }} exam solutions"
                    title="{{ iteml[0] }} exam solutions"
                    src="{{ site.base }}/img/icons/lab_solutions.png" />
            </a>
            {% endif %}            
        <!-- Sample Exam 4 -->
            {% if item.samp_exam4 %}
            <a href="{{ site.base }}{{ item.samp_exam2 }}"
                style="text-decoration: none">
                <img class="homework-icon"
                    alt="{{ iteml[0] }} sample exam"
                    title="{{ iteml[0] }} sample exam"
                    src="{{ site.base }}/img/icons/lab_questions.png" />
            </a>
            {% endif %}
            {% if item.samp_exam4_sol %}
            <a href="{{ site.base }}{{ item.samp_exam2_sol }}"
                style="text-decoration: none">
                <img class="homework-icon"
                    alt="{{ iteml[0] }} exam solutions"
                    title="{{ iteml[0] }} exam solutions"
                    src="{{ site.base }}/img/icons/lab_solutions.png" />
            </a>
            {% endif %}            
        </td>        
        <td> 
            {% if item.exam_questions %}
            <a href="{{ site.base }}{{ item.exam_questions }}"
                style="text-decoration: none">
                <img class="homework-icon"
                    alt="{{ iteml[0] }} exam questions"
                    title="{{ iteml[0] }} exam questions"
                    src="{{ site.base }}/img/icons/lab_questions.png" />
            </a>
            {% endif %}
            {% if item.exam_solutions %}
            <a href="{{ site.base }}{{ item.exam_solutions }}"
                style="text-decoration: none">
                <img class="homework-icon"
                    alt="{{ iteml[0] }} exam solutions"
                    title="{{ iteml[0] }} exam solutions"
                    src="{{ site.base }}/img/icons/lab_solutions.png" />
            </a>
            {% endif %}
        </td>
    </tr>        


  {% endfor %}

</table>



&nbsp;

Couple things to note about exams:
- All the midterms will be administered during lecture time in the usual lecture room. 
- The "final" period will be a block of time where you can redo up to two of the midterms (basically will be a second variation dealing with the same subject). The redo will

### Exam Policies

Besides the obvious "don't cheat" exam policies outlined in the [policies page](/policies/cheating) you should know about the following exam procedures: 

#### Exam Redo

**Exam redo replaces conflict exams.** As per the grading policy, we will allow up to retake up to two of the midterms during the final exam period. This exam redo has the same purpose as the quiz drop - to give students a buffer for those times when life gets in the way. Should you get sick or maybe have a moment of panic during one of the exams, you now have a redo so that one grade won't sink you.  

Because the final period is only 3 hours and each midterm will be 75 minutes, we will only be allowing you to redo up to two exams. I have taught this course more than 6+ times and I have yet to meet someone that missed two exams but had mastered the material. In the past three years that I have taught the course, every case of a student missing two or more exams is accompanied by the student performing in the bottom 10% of the exams they did take. This makes sense when you think about. Missing two exams is indicative of being absent for the majority of the semester which would in turn mean that the material was probably not mastered.

Still, maybe there's an exception. I would love to be surprised. Maybe there is someone out there that can basically take Midterm 3 and redo Midterms 1+2 in the final exam period (effectively speed running this course in a week). If you are that person, I sincerely wish you luck and am rooting for you. 

#### Cheatsheet

I've wrestled with the concept of cheatsheets a lot in past semesters. Ideally, what a cheatsheet is for is to help you memorize tedious equations or details that are easy to forget. However, I like to give exam questions that are very similar to the HWs/labs. In prior semesters, I noticed that cheat sheets didn't contain definitions/algorithms. Instead, they contained copied questions and solutions of HW/lab problems. Basically cheat sheets had become a "guess what Kani might put on the exam"-sheet. Worse, many, many people simply copied the cheatsheet solutions and were frustrated when they learned that those solutions didn't apply to the exam problems. This leaves me with two options: 

- Make sure that the exam problems are changed up so that copying from a HW/lab problem would hurt more than help. 
- Eliminate cheatsheets altogether. 

I think I've come up with a solution that'd help everyone. Over the course of four semesters, we've constructed a communal cheat sheet for each of the exams. These cheat sheets will be posted on the website well in advance of the exam and will be attached to the back of the exam. 

This lets me use problems that many of you have seen before but know that the people answering those problems are doing so because they actually mastered the material. 

#### Use pen

The exams will be scanned and uploaded to Gradescope where they will be graded by the TAs. Unfortunately, last semester we had a problem with a number of individuals that used a pencil with a light touch causing the exam to be illegible. Therefore, we're banning pencils. I'm not going to go around confiscating pencils like some weird pen nazi, but if we see an exam that is difficult to read, we will take off points. Just use pen, if you need to change something you can always cross out the previous answer and make a note for the grader to look at the scratch page.  

### Regrades

Regrades requests would be open for a week once grades are released (except for final exam). Regrade requests are not intended for arguing about point allocation, or whether the grading scale is fair.

Unfortunately, certain students think that they can tire us into giving them point that they did not earn, by keep asking for unjustified regrade requests. As such, superfluous, argumentative and repetitive regrade requests, after an appropriate warning, would result in a zero on the relevant questions - please do not waste our time.

### DRES
- If you have a DRES accommodation, please email the course staff directly (not sure if sending documents over Piazza is compliant with EHR policies or not, but why risk it). Make sure I respond that I've recorded your accommodation! If I don't respond email again.
- Because of the limited staff, DRES students will take the exams at the [TAC](https://www.disability.illinois.edu/academic-accommodations-and-supports/academic-accommodations/testing-accommodations) synchronously with the rest of the class. We'll hammer out the details closer to MT1. 
- Best thing you can do is to schedule the exams with TAC **now**. That way there is no chance on forgetting to schedule a slot and missing out on your accommodations.  