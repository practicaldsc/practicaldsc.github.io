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
> Welcome to the Spring 2025 offering of EECS 398! 👋 <br>Make sure to read the [**Syllabus**](/syllabus) and complete the action items in the [**Getting Started**](/syllabus#getting-started) section ASAP. In particular, fill out the [**Welcome Survey**](https://forms.gle/eZFdhpwn156CQuk29) and follow the steps in the [**⚙️ Environment Setup**](../env-setup) page of the course website.

[Jump to Week 1: Python, NumPy, and Pandas](#week-1-python-numpy-and-pandas){: .btn .btn-green } [Announcements 📣](https://edstem.org/us/courses/78535/discussion/6647877){: .btn .btn-purple }

{% for module in site.modules %}
{{ module }}
{% endfor %}
