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
> Technical Interview (and practice interview) signups are now open; check [**this post on Ed**](https://edstem.org/us/courses/78535/discussion/6710256) for details, and see [**this post**](https://edstem.org/us/courses/78535/discussion/6722090) for practice problems and a walkthrough video.

[Jump to Week 3: Text Data, Introduction to Machine Learning](#week-3-text-data-introduction-to-machine-learning){: .btn .btn-green } [Announcements 📣](https://edstem.org/us/courses/78535/discussion/6647877){: .btn .btn-purple }

{% for module in site.modules %}
{{ module }}
{% endfor %}
