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

<!-- [Jump to Week 7: Clustering, Conclusion](#week-7-clustering-conclusion){: .btn .btn-green } [Announcements 📣](https://edstem.org/us/courses/78535/discussion/6647877){: .btn .btn-purple } -->

{: .green }
> **Welcome! 👋** This course has concluded, and will not be taught in AY 2025-26. Until it is offered again, you'll be able to find lecture slides, recordings, and assignments archived below.


{% for module in site.modules %}
{{ module }}
{% endfor %}
