---
title: "Predictive Modeling"
layout: single
permalink: /courses/predictive-modeling/
classes: wide
order: 1
playlist_url: "https://www.youtube.com/playlist?list=PL7nhsj3rJk8MvHnuMNUcAaE0xGpmsCMhO"
---

## Videos in this course

<div id="video-grid" class="course-grid"></div>

<script>
document.addEventListener("DOMContentLoaded", async function () {
  const apiKey = "PUT_YOUR_YOUTUBE_API_KEY_HERE";
  const playlistUrl = {{ page.playlist_url | jsonify }};

  function getPlaylistId(url) {
    try {
      const u = new URL(url);
      return u.searchParams.get("list");
    } catch (e) {
      return null;
    }
  }

  const playlistId = getPlaylistId(playlistUrl);
  if (!playlistId) return;

  async function fetchAllPlaylistItems(pid) {
    let items = [];
    let nextPageToken = "";
    do {
      const endpoint =
        "https://www.googleapis.com/youtube/v3/playlistItems" +
        "?part=snippet" +
        "&maxResults=50" +
        "&playlistId=" + encodeURIComponent(pid) +
        "&key=" + encodeURIComponent(apiKey) +
        (nextPageToken ? "&pageToken=" + encodeURIComponent(nextPageToken) : "");

      const res = await fetch(endpoint);
      const data = await res.json();

      if (data.items) items = items.concat(data.items);
      nextPageToken = data.nextPageToken || "";
    } while (nextPageToken);

    return items;
  }

  const items = await fetchAllPlaylistItems(playlistId);
  const grid = document.getElementById("video-grid");

  items.forEach(item => {
    const sn = item.snippet;
    if (!sn || !sn.resourceId || !sn.resourceId.videoId) return;

    const videoId = sn.resourceId.videoId;
    const title = sn.title || "Video";
    const thumb =
      (sn.thumbnails?.high?.url) ||
      (sn.thumbnails?.medium?.url) ||
      (sn.thumbnails?.default?.url) ||
      ("https://i.ytimg.com/vi/" + videoId + "/hqdefault.jpg");

    const videoUrl = "https://www.youtube.com/watch?v=" + videoId + "&list=" + playlistId;

    const card = document.createElement("div");
    card.className = "course-card";
    card.innerHTML = `
      <a href="${videoUrl}" target="_blank" rel="noopener noreferrer">
        <img src="${thumb}" alt="${title}">
      </a>
      <p class="course-title">
        <a href="${videoUrl}" target="_blank" rel="noopener noreferrer">${title}</a>
      </p>
    `;
    grid.appendChild(card);
  });
});
</script>
