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
**The Midterm Exam is on Tuesday, February 25th, from 7-9PM. Read [this post on Ed](https://edstem.org/us/courses/69737/discussion/6233420) for logistical information, including your seat assignment, and come to our review sessions on Sunday from 5-7PM and Monday from 3-4:30PM!**


[Jump to Week 8: Midterm Exam](#week-8-midterm-exam){: .btn .btn-green } [Announcements 📣](https://edstem.org/us/courses/69737/discussion/5943734){: .btn .btn-purple }

{% for module in site.modules %}
{{ module }}
{% endfor %}