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
    {% assign first_video = course.videos | first %}
    {% assign vid = first_video.url | split: 'v=' | last | split: '&' | first %}
    <div class="course-card">
      <a href="{{ course.url | relative_url }}">
        <img src="https://i.ytimg.com/vi/{{ vid }}/hqdefault.jpg" alt="{{ course.title }}">
      </a>
      <p class="course-title">
        <a href="{{ course.url | relative_url }}">{{ course.title }}</a>
      </p>
    </div>
  {% endfor %}
</div>
