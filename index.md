---
layout: page
title: 🏡 Home
description: >-
  Course homepage.
nav_order: 1
---

# Practical Data Science 🛠️
{: .no_toc }
{: .mb-2 }
EECS 398, Winter 2025 at the <b><span style="background-color: #FFCB05; color: #00274C">University of Michigan</span></b>
{: .no_toc }
{: .fs-6 .fw-300 .mb-2 }

<!-- 4 credits • Open to all majors • ULCS for Computer Science majors, Advanced Technical Elective or Application Elective for Data Science majors, Flexible Technical Elective for Electrical Engineering majors -->


{% for staffer in site.staffersnobio %}
{{ staffer }}
{% endfor %}


{: .green }
> **Welcome to Practical Data Science in Winter 2025 <span class="wave">👋</span>!** Make sure to:
> - Come to the first lecture on Wednesday 1/8 at 3PM, and meet us after in the BBB Atrium to socialize (and eat free donuts 🍩).
> - Attend a discussion section on Thursday 1/9 – we're taking attendance!
> - Read the [**Syllabus**](syllabus), follow the steps in [**Environment Setup**](env-setup), and fill out the [**Welcome Survey**](https://docs.google.com/forms/d/e/1FAIpQLSfwn5kPDKgrHlyypVlp0hl2WyTVifBnQ1OO_g9U56FlrFE6aQ/viewform).


[Jump to the current week](#week-1-introduction){: .btn } [Announcements 📣](https://edstem.org/us/courses/69737/discussion/5943734){: .btn .btn-purple }

{% for module in site.modules %}
{{ module }}
{% endfor %}

<!-- ---

1. TOC
{:toc}

---

### Fall 2024 Evaluations

Since this is a relatively new course, we've provided the complete set of course evaluations from Fall 2024 [**here**](../assets/marketing/fa24-evals.pdf) to help inform your decision on whether to enroll. The document contains dozens of written comments from students who took the course. 

Some useful summary statistics:

- This course advanced my understanding of the subject matter: **4.8 / 5**.
- Overall, this was an excellent course: **4.8 / 5**.
- Overall, Suraj Rampure was an excellent teacher: **4.9 / 5**.
- As compared with other courses of equal credit, the workload for this course was: **2.6 / 5** (lower values mean more work).

Regarding workload, we also ran our own internal survey:

<center><img src="../assets/marketing/workload.png" width=600></center>

---

### Content

> Skills and tools for building practical data science projects, along with their theoretical underpinnings. `pandas`, `numpy`, `scikit-learn`, `BeautifulSoup`, and Jupyter Notebooks, and also the math behind loss functions, gradient descent, linear and logistic regression, and other key ideas in machine learning.

<center>

<iframe width="600" height="320" src="https://www.youtube.com/embed/Z75-_YK5_XM?si=ilsVZvq51tBPyHG3" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

</center>

This course will train students to use industry-standard tools to solve real-world problems, while giving them an understanding of how these tools work under the hood. After taking this course, students will be prepared to build data science portfolios, participate in research across campus, succeed in data science internships, reason about abstract mathematical problems, and understand the foundations of machine learning models.

Students will be expected to complete **weekly homework assignments**, which will comprise of a mix of programming and theoretical questions distributed in Jupyter Notebooks, along with a longer "Portfolio Homework" that requires using topics from the entire semester to perform an end-to-end analysis.

The course will have **in-person, on-paper midterm and final exams that involve a mix of multiple choice, short answer, fill in the blank code, math, and English problems** (for context, see the Fall 2024 Midterm Exam and solutions [here](https://study.practicaldsc.org/fa24-midterm)).

The exams are scheduled for the following times:
- Midterm Exam: Tuesday, February 25th, 7-9PM (**tentative and subject to change**)
- Final Exam: Monday, April 28th, 10:30AM-12:30PM

Other materials from the Fall 2024 offering can be found at the [Fall 2024 website](https://practicaldsc.org/fa24).

---

### Prerequisites

The course is open to students from all majors.

The enforced prerequisites are discrete math (EECS 203), programming (EECS 280), calculus I, calculus II, and linear algebra. A probability and statistics course is an advisory prerequisite. Options include DATASCI 101, STATS 206, STATS 250, STATS 280, STATS 412, IOE 265, or ECON 451.

If you're interested in the class but don't meet one of the prerequisites, **email me and we can chat about your background and a potential override**. I encourage students of all backgrounds who are curious about data science to reach out!

{: .green }
**In particular, students without prior linear algebra experience will be directed to a linear algebra review website that we've created specifically for this course.**

---

### Enrollment Logistics

If you'd like to enroll in the course, sign up for these EECS 398 sections:
- lecture LEC 002 or LEC 003, **and**
- discussion DIS 021, 022, 023, or 024.

There is only one live, in-person lecture, **Monday and Wednesday 3-4:30PM in 1670 BBB** (as is listed for LEC 002), and lecture attendance is not required.
- All students, regardless of section, will have access to lecture recordings.
- All students, regardless of enrolled section, can also attend the in-person lectures, space permitting on the day of the attendance. Usually, enough students consume material remotely that we don't anticipate in-person space to be a bottleneck for anyone wishing to attend the class in-person.

In-person discussion attendance **will be required or incentivized**: make sure you can attend your enrolled discussion section.

Office hours will largely be in-person, but there will be some remote options as well.

<!-- ---

### Testimonials and Workload

The following quotes are by students who are currently in the course. They were submitted anonymously and have not been edited.

> I couldn't recommend this class enough! I'm a second year CS-LSA student and I'm taking this class as my first ULCS class with EECS 281. Despite not having the strongest foundation in linear algebra coming in, I’ve found the material very accessible with a bit of extra effort. The lectures, led by Suraj, are both engaging and informative; he has a talent in presenting complex ideas in a clear and interesting way that keeps you interested. The homework assignments are particularly cool—they push you to think creatively while applying what you’ve learned in class. The course is manageable with consistent effort, and I’ve found the resources provided by the staff to be helpful for filling in any gaps. If you're interested in diving deeper into data science and machine learning concepts, I’d definitely recommend taking this course.

> As a third year data science major, this has been my favorite course I've taken throughout my time in college. It's the first course that's felt tailored to my major and relevant to the industry. I've loved the combination of learning core Python skills and ML techniques, and have gained a breadth of understanding in just a semester. While the homework can be time-consuming and challenging, it's so worth it to gain a better understanding of class content. Not only that, but the concepts taught have helped me excel while interviewing for data science roles, and even land multiple offers. Also, the course staff are amazing -- they're incredibly intelligent and friendly, I've always had a great experience in office hours. Would highly recommend this course to anyone interested in data science!

> This is one of my favorite classes I've taken at umich. I have enjoyed the content of almost every lecture, and I wish I had taken this class before my past internship because it would've helped a ton. I really appreciate the structure of this course, with weekly homeworks and a good amount of late days, but not enough to fall behind. I actually don't have a single complaint about how this class is run. The professor gives out a grade report after the midterm, so we can see how many points we have in the class so far, what our current grade is, and how many late days we have remaining. I took linear algebra at a community college and learned pretty much nothing, but I still felt as though I could keep up because of the provided linear algebra review. I would recommend this course to anyone!

> As a CS senior, this is one of the best courses I've taken at Michigan! The course is incredibly well organized: each week's homework and discussion worksheet aligns well with the content covered in lecture, staff is very open to feedback, and the workload is very reasonable with consistent effort and doable alongside other difficult courses. Suraj is also such an engaging lecturer, and his notes/presentations are a really great mix of content, interactive demos, and practice problems. I would definitely recommend this course!

> Coming into this class, I hadn't had too much experience with Python and Data Science in general, so I was a bit unsure of how it would go. However, the result was completely unexpected: I now find myself really enjoying the course content not only because it is taught in an engaging way but also because I can see the value in the practical applications that come out of these concepts. Every week, even if I was unsure about a certain topic, I knew I could either come to office hours and get the help I needed, or reinforce those concepts through the homework problems, which really helped me build confidence in my understanding of the material. Most importantly, the course can really help you realize an interest for this content that you may have never known to have, as it did with me: I now am pursuing future courses like Machine Learning because the content in this class was taught so well and gave me a good foundation for future ULCS classes. Overall, the course is meant to challenge you, but it is quite rewarding in the end, and it is an enjoyable experience!

> I think this course should be required for any DS (or frankly even CS major). There's a lot to learn in the class. Although we spend a rather brief amount of time covering some of the topics, this class gives a great idea of lot's of things out there. It may be called practical data science, but the second half goes more into depth for a decent mathematical understanding of basic, but crucial, ML components. There's lot's of skills you pick up through it (SQL, Pandas, Latex, Numpy, SciKit Learn, Plotly, Regex, etc.). I also believe that the course is what you make of it. Suraj, and the staff, put in a lot of time to  gather resources to you can dwell deeper into areas of interest. 
> 
> My main cons of the course are that it's not were related to depth, regarding some APIs such as Pandas. If you're more into lower level programming (computer architecture, systems, DSA in C/C++), then this may not be the course for you. Although if you want a chill class which teaches you a thing or two, I'd say check it out. Bare through the initial few weeks and the content get's pretty sweet! Believe me, I went through it myself.
> 
> Make sure you know your linear algebra if you really want to appreciate the content in the second half of the course!
> 
> I think the ideal time to take the course is right after 203 and 280, probably alongside 281. Not only are you locking yourself into some internship experience (especially in today's ML heavy workforce) but also get to branch into some other areas.

While official evaluations for Fall 2024 aren't yet available, we administered an anonymous survey at the end of Fall 2024 that asked students about the course's workload. The results are shown below.
 -->
