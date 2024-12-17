---
layout: page
title: 👩‍🏫 Staff
description: A listing of all the course staff members.
nav_order: 6
---

# 👩‍🏫 Staff

{: .green }
Welcome to Practical Data Science in Winter 2025! This site is currently under construction. Until this disclaimer is removed, all information here is subject to change. See you on January 8th!

## Instructor

{% assign instructors = site.staffers | where: 'role', 'Instructor' %}
{% for staffer in instructors %}
{{ staffer }}
{% endfor %}
