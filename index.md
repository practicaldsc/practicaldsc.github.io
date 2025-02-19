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


<!-- {: .green }
**Welcome to Practical Data Science in Winter 2025 <span class="wave">👋</span>!** Make sure to read the [**Syllabus**](syllabus), follow the steps in [**Environment Setup**](env-setup), and fill out the [**Welcome Survey**](https://docs.google.com/forms/d/e/1FAIpQLSfwn5kPDKgrHlyypVlp0hl2WyTVifBnQ1OO_g9U56FlrFE6aQ/viewform). -->


[Jump to Week 7: Introduction to Machine Learning](#week-7-introduction-to-machine-learning){: .btn .btn-green } [Announcements 📣](https://edstem.org/us/courses/69737/discussion/5943734){: .btn .btn-purple }

{% for module in site.modules %}
{{ module }}
{% endfor %}