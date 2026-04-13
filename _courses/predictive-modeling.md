---
title: "Predictive Modeling"
layout: single
permalink: /courses/predictive-modeling/
classes: wide
order: 1

videos:
  - title: "Lecture 1"
    url: "https://www.youtube.com/watch?v=YOUR_FIRST_VIDEO_LINK_ID"

  - title: "Lecture 2"
    url: "https://www.youtube.com/watch?v=YOUR_SECOND_VIDEO_LINK_ID"

  - title: "Lecture 3"
    url: "https://www.youtube.com/watch?v=YOUR_THIRD_VIDEO_LINK_ID"
---

## Playlist

<iframe width="100%" height="600"
src="https://www.youtube.com/embed/videoseries?si=7tIbsjingaavJvcR&amp;list=PL7nhsj3rJk8MvHnuMNUcAaE0xGpmsCMhO"
title="Predictive Modeling Playlist"
frameborder="0"
allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
referrerpolicy="strict-origin-when-cross-origin"
allowfullscreen>
</iframe>

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
