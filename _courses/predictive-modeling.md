---
title: "Predictive Modeling"
layout: single
permalink: /courses/predictive-modeling/
classes: wide
order: 1

videos:
  - title: "Lecture 1"
    url: "https://www.youtube.com/watch?v=nQQ--PTt8IE&list=PL7nhsj3rJk8MvHnuMNUcAaE0xGpmsCMhO&index=1"

  - title: "Lecture 2"
    url: "https://www.youtube.com/watch?v=iuYGn7C4NjE&list=PL7nhsj3rJk8MvHnuMNUcAaE0xGpmsCMhO&index=2"

  - title: "Lecture 3"
    url: "https://www.youtube.com/watch?v=fI2CYAE22Ag&list=PL7nhsj3rJk8MvHnuMNUcAaE0xGpmsCMhO&index=3"
---

## Videos in this course

<div class="course-grid">
  {% for video in page.videos %}
    {% assign vid = video.url | split: 'v=' | last | split: '&' | first %}
    <div class="course-card">
      <a href="{{ video.url }}" target="_blank" rel="noopener noreferrer">
        <img src="https://i.ytimg.com/vi/{{ vid }}/hqdefault.jpg" alt="{{ video.title }}">
      </a>
      <p class="course-title">
        <a href="{{ video.url }}" target="_blank" rel="noopener noreferrer">{{ video.title }}</a>
      </p>
    </div>
  {% endfor %}
</div>
