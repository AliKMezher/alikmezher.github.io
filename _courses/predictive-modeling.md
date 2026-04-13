---
title: "Predictive Modeling"
layout: single
permalink: /courses/predictive-modeling/
classes: wide
order: 1

videos:
  - "https://www.youtube.com/watch?v=nQQ--PTt8IE&list=PL7nhsj3rJk8MvHnuMNUcAaE0xGpmsCMhO&index=1"
  - "https://www.youtube.com/watch?v=iuYGn7C4NjE&list=PL7nhsj3rJk8MvHnuMNUcAaE0xGpmsCMhO&index=2"
  - "https://www.youtube.com/watch?v=fI2CYAE22Ag&list=PL7nhsj3rJk8MvHnuMNUcAaE0xGpmsCMhO&index=3"
---

## Videos in this course

<div id="video-grid" class="course-grid"></div>

<script>
document.addEventListener("DOMContentLoaded", async function () {
  const apiKey = "PUT_YOUR_YOUTUBE_API_KEY_HERE";
  const links = {{ page.videos | jsonify }};

  function getVideoId(url) {
    try {
      const u = new URL(url);
      if (u.hostname.includes("youtu.be")) {
        return u.pathname.replace("/", "");
      }
      return u.searchParams.get("v");
    } catch (e) {
      return null;
    }
  }

  const ids = links.map(getVideoId).filter(Boolean);
  if (!ids.length) return;

  const endpoint =
    "https://www.googleapis.com/youtube/v3/videos" +
    "?part=snippet" +
    "&id=" + ids.join(",") +
    "&key=" + apiKey;

  const res = await fetch(endpoint);
  const data = await res.json();

  const byId = {};
  (data.items || []).forEach(item => {
    byId[item.id] = item;
  });

  const grid = document.getElementById("video-grid");

  links.forEach(link => {
    const id = getVideoId(link);
    const item = byId[id];
    if (!item) return;

    const title = item.snippet.title;
    const thumb =
      (item.snippet.thumbnails.high && item.snippet.thumbnails.high.url) ||
      (item.snippet.thumbnails.medium && item.snippet.thumbnails.medium.url) ||
      item.snippet.thumbnails.default.url;

    const card = document.createElement("div");
    card.className = "course-card";
    card.innerHTML = `
      <a href="${link}" target="_blank" rel="noopener noreferrer">
        <img src="${thumb}" alt="${title}">
      </a>
      <p class="course-title">
        <a href="${link}" target="_blank" rel="noopener noreferrer">${title}</a>
      </p>
    `;
    grid.appendChild(card);
  });
});
</script>
