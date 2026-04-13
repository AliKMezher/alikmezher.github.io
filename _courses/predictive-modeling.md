---
title: "Predictive Modeling"
layout: single
permalink: /courses/predictive-modeling/
classes: wide
order: 1
header:
  teaser: /images/predictive-modeling-thumb.jpg

videos:
  - title: "Lecture 1: Orthonormal basis, inner, outer, and tensor product"
    url: "https://www.youtube.com/watch?v=VIDEO_ID_1"

  - title: "Lecture 2: Hilbert spaces, orthonormal basis, and linear compact operators"
    url: "https://www.youtube.com/watch?v=VIDEO_ID_2"

  - title: "Lecture 3: Markov Monte Carlo series and Metropolis–Hastings algorithm"
    url: "https://www.youtube.com/watch?v=VIDEO_ID_3"
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

<ul>
  {% for video in page.videos %}
    <li><a href="{{ video.url }}" target="_blank">{{ video.title }}</a></li>
  {% endfor %}
</ul>
