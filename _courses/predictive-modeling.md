---
title: "Predictive Modeling"
layout: single
permalink: /courses/predictive-modeling/
classes: wide
order: 1
thumb: "https://i.ytimg.com/vi/VIDEO_ID_1/hqdefault.jpg"

videos:
  - title: "Lecture 1: Orthonormal basis, inner, outer, and tensor product"
    url: "https://www.youtube.com/watch?v=VIDEO_ID_1"
    thumb: "https://i.ytimg.com/vi/VIDEO_ID_1/hqdefault.jpg"

  - title: "Lecture 2: Hilbert spaces, orthonormal basis, and linear compact operators"
    url: "https://www.youtube.com/watch?v=VIDEO_ID_2"
    thumb: "https://i.ytimg.com/vi/VIDEO_ID_2/hqdefault.jpg"

  - title: "Lecture 3: Markov Monte Carlo series and Metropolis–Hastings algorithm"
    url: "https://www.youtube.com/watch?v=VIDEO_ID_3"
    thumb: "https://i.ytimg.com/vi/VIDEO_ID_3/hqdefault.jpg"
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
      <a href="{{ video.url }}" target="_blank">
        <img src="{{ video.thumb }}" alt="{{ video.title }}">
      </a>
      <p class="course-title">
        <a href="{{ video.url }}" target="_blank">{{ video.title }}</a>
      </p>
    </div>
  {% endfor %}
</div>
