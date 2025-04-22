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
> We have two review sessions this week, both in 1670 BBB: Wednesday 3-5PM and Saturday 1-3PM. Attempt their associated worksheets (linked below) **before** coming.
>
> If at least 85% of the class fills out both the <b><a href="https://docs.google.com/forms/d/1M5bqqDJB96b2KbXPJFe9iOTTqk6mPnKkyPzGiLbVBNQ/preview">End-of-Semester Survey</a></b> and <b><a href="https://umich.bluera.com/umich/">Official Evals</a></b> by 4/23 at 11:59PM, we'll add 1% of extra credit to everyone's overall grade.

[Jump to Week 16: Conclusion, Review](#week-16-conclusion-review){: .btn .btn-green } [Announcements 📣](https://edstem.org/us/courses/69737/discussion/5943734){: .btn .btn-purple }

{% for module in site.modules %}
{{ module }}
{% endfor %}
