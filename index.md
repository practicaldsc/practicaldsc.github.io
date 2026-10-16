---
layout: minimal
title: Practical Data Science
description: A self-guided archive of Practical Data Science.
---

# Practical Data Science 🛠️
{: .no_toc .mb-2 }

EECS 398 at the <b><span style="background-color: #ffcb05; color: #00274c">University of Michigan</span></b>
{: .no_toc .fs-6 .fw-300 .mb-4 }

{: .green }
> This is an archive of Practical Data Science, taught as EECS 398 at the University of Michigan in 2024-2025. On this page you will find links to lecture slides, recordings, and assignments from the course. You can also find links to the "frozen course websites" from actual offerings of the course. If you have any questions about these materials, feel free to contact Suraj Rampure at [rampure@umich.edu](mailto:rampure@umich.edu).

> Skills and tools for building practical data science projects, along with their theoretical underpinnings, including `pandas`, NumPy, scikit-learn, BeautifulSoup, and Jupyter Notebooks. It also covers the mathematics behind loss functions, gradient descent, regression, and other machine-learning ideas.

**Frozen course websites:** [Spring 2025](/sp25/) · [Winter 2025](/wn25/) · [Fall 2024](/fa24/)

**Other links:** [Video playlist](https://www.youtube.com/playlist?list=PLRjECWtq5kTk) · [Exams and theory worksheets](https://study.practicaldsc.org/) · [Environment setup](https://practicaldsc.org/wn25/env-setup/) · [Winter 2025 syllabus](https://practicaldsc.org/wn25/syllabus/) · [Topic guides](https://practicaldsc.org/guides/)

<br>

<div class="archive-table-wrap">
<table class="archive-table">
  <thead>
    <tr>
      <th class="lecture-column" style="letter-spacing: normal; text-transform: none;">Lectures</th>
      <th class="homework-column" style="letter-spacing: normal; text-transform: none;">Assignments</th>
    </tr>
  </thead>
  <tbody>
  {% for block in site.data.archive %}
    {% for lecture in block.lectures %}
    <tr>
      <td>
        <div class="lecture-entry">
          <span class="lecture-number">LEC {{ lecture.number | plus: 0 }}</span>
          <div>
            <p class="lecture-title">{{ lecture.title }}</p>
            <div class="lecture-links">
              {% if lecture.html %}<a href="{{ lecture.html }}" class="btn btn-info btn-sm">📝 Filled HTML</a>{% endif %}
              {% if lecture.slides %}<a href="{{ lecture.slides }}" class="btn btn-info btn-sm">📝 Filled slides</a>{% endif %}
              {% if lecture.github %}<a href="{{ lecture.github }}" class="btn btn-info btn-sm">{% include icon-github.html %} GitHub</a>{% endif %}
              {% if lecture.recording %}<a href="{{ lecture.recording }}" class="btn btn-info btn-sm">📺 Recording</a>{% endif %}
            </div>
          </div>
        </div>
      </td>
      {% if forloop.first %}
      <td class="homework-cell" rowspan="{{ block.lectures.size }}">
        <span class="homework-label">{{ block.homework.label | replace: "Homework ", "HW " }}</span>
        <p class="homework-title">{{ block.homework.title }}</p>
        <a class="btn btn-info btn-sm" href="{{ block.homework.url }}">{% if block.homework.link_text %}{{ block.homework.link_text }}{% else %}{% include icon-github.html %} GitHub{% endif %}</a>
      </td>
      {% endif %}
    </tr>
    {% endfor %}
  {% endfor %}
  </tbody>
</table>
</div>
