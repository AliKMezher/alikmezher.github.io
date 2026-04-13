---
title: "Predictive Modeling"
layout: single
permalink: /courses/predictive-modeling/
classes: wide
order: 1

videos:
  - title: "Orthonormal basis, inner, outer, and tensor product"
    url: "https://www.youtube.com/watch?v=nQQ--PTt8IE&list=PL7nhsj3rJk8MvHnuMNUcAaE0xGpmsCMhO&index=1"

  - title: "Hilbert spaces, orthonormal basis, and linear compact operators"
    url: "https://www.youtube.com/watch?v=iuYGn7C4NjE&list=PL7nhsj3rJk8MvHnuMNUcAaE0xGpmsCMhO&index=2"

  - title: "Markov Monte Carlo series and Metropolis–Hastings algorithm"
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
