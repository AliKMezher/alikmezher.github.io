---
layout: archive
permalink: /courses/
title: "Courses"
author_profile: true
entries_layout: grid
---

{% include base_path %}

{% assign sorted_courses = site.courses | sort: "order" %}
{% for post in sorted_courses %}
  {% include archive-single.html type="grid" %}
{% endfor %}
