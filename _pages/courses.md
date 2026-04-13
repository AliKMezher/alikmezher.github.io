---
layout: single
permalink: /courses/
title: "Courses"
author_profile: true
classes: wide
---

<div class="course-grid">
  {% assign sorted_courses = site.courses | sort: "order" %}
  {% for course in sorted_courses %}
    <div class="course-card">
      <a href="{{ course.url | relative_url }}">
        <p class="course-title">{{ course.title }}</p>
      </a>
    </div>
  {% endfor %}
</div>
