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
        <img src="{{ course.thumb }}" alt="{{ course.title }}">
      </a>
      <p class="course-title">
        <a href="{{ course.url | relative_url }}">{{ course.title }}</a>
      </p>
    </div>
  {% endfor %}
</div>
