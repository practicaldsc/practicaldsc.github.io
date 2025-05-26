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
EECS 398, Spring 2025 🌸 at the <b><span style="background-color: #FFCB05; color: #00274C">University of Michigan</span></b>
{: .no_toc }
{: .fs-6 .fw-300 .mb-2 }

<!-- 4 credits • Open to all majors • ULCS for Computer Science majors, Advanced Technical Elective or Application Elective for Data Science majors, Flexible Technical Elective for Electrical Engineering majors -->

{% for staffer in site.staffersnobio %}
{{ staffer }}
{% endfor %}

{: .green }
> If you've signed up for a Technical Interview, see [**this post**](https://edstem.org/us/courses/78535/discussion/6722090) for practice problems and a walkthrough video.
>
> The Midterm Exam is **this Wednesday, May 28th from 2-4PM in 1670 BBB**. Read [**this post**](https://edstem.org/us/courses/78535/discussion/6727704) for tips on how to study.
>
> The deadlines for Homeworks 5 and 6 have been pushed back; see the calendar below.

[Jump to Week 3: Text Data, Introduction to Machine Learning](#week-3-text-data-introduction-to-machine-learning){: .btn .btn-green } [Announcements 📣](https://edstem.org/us/courses/78535/discussion/6647877){: .btn .btn-purple }

{% for module in site.modules %}
{{ module }}
{% endfor %}
