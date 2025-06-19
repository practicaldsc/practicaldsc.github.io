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

[Jump to Week 7: Clustering, Conclusion](#week-7-clustering-conclusion){: .btn .btn-green } [Announcements 📣](https://edstem.org/us/courses/78535/discussion/6647877){: .btn .btn-purple }

{: .green }
> We're in the final stretch of the semester! A few reminders:
> - Office hours for the remainder of the semester are on Zoom by appointment only. Sign up for as many slots as you'd like [**here**](https://calendar.app.google/qrKNHCLQzmU5JYCm6); make sure to sign up at least 2 hours in advance.
> - The Final Project is due on **Friday, June 20th**, and **slip days are not allowed**!
> - The Final Exam is on **Tuesday, June 24th from 1:30-3:30PM in CHRYS 133**. Practice using the worksheets [**here**](https://study.practicaldsc.org), including the review worksheets and the [**Winter 2025 Final Exam Solutions**](https://study.practicaldsc.org/wn25-final/index.html) (newly released!).
> - If at least 22/25 students complete both the internal <b><a href="https://forms.gle/KYgxU1RrdeX5QYQNA">End-of-Semester Survey</a></b> and the <b><a href="https://umich.bluera.com/umich/">Official Evaluations</a></b> by Sunday, we'll add an extra 1% to everyone's overall grade in the course.


{% for module in site.modules %}
{{ module }}
{% endfor %}
