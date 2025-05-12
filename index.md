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
> In-person lecture on Tuesday, May 13th is cancelled. Lecture videos from last semester have been posted below. We'll see you back in lecture on Thursday!

[Jump to Week 2: More Pandas, EDA, and Web Scraping](#week-2-more-pandas-eda-and-web-scraping-br-small-in-person-lecture-on-tuesday-may-13th-is-cancelled-lecture-videos-from-last-semester-have-been-posted-below-make-sure-to-read-the-dataframe-internals-guide-small){: .btn .btn-green } [Announcements 📣](https://edstem.org/us/courses/78535/discussion/6647877){: .btn .btn-purple }

{% for module in site.modules %}
{{ module }}
{% endfor %}
