---
title: "Predictive Modeling"
layout: single
permalink: /courses/predictive-modeling/
classes: wide
order: 1
first_video_id: "VIDEO_ID_1"

videos:
  - title: "Introduction, orthonormal basis, inner, outer, and tensor product"
    id: "VIDEO_ID_1"

  - title: "Hilbert spaces, orthonormal basis, and linear compact operators"
    id: "VIDEO_ID_2"

  - title: "Markov Monte Carlo series and Metropolis–Hastings algorithm"
    id: "VIDEO_ID_3"

  - title: "Polynomial chaos expectation, stochastic process, Karhunen–Loève theorem"
    id: "VIDEO_ID_4"

  - title: "Kolmogorov’s Two-Series theorem and Sazanov’s theorem"
    id: "VIDEO_ID_5"
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
    <div class="course-card">
      <a href="https://www.youtube.com/watch?v={{ nQQ--PTt8IE&list=PL7nhsj3rJk8MvHnuMNUcAaE0xGpmsCMhO }}" target="_blank" rel="noopener noreferrer">
        <img src="https://i.ytimg.com/vi/{{ video.id }}/hqdefault.jpg" alt="{{ video.title }}">
      </a>
      <p class="course-title">
        <a href="https://www.youtube.com/watch?v={{ video.id }}" target="_blank" rel="noopener noreferrer">{{ video.title }}</a>
      </p>
    </div>
  {% endfor %}
</div>
