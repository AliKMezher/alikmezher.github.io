<div style="display: grid; grid-template-columns: repeat(auto-fill, minmax(300px, 1fr)); gap: 30px; margin-top: 20px;">

  {% for course in site.courses %}
  <div style="text-align: center; transition: transform 0.2s;" onmouseover="this.style.transform='scale(1.02)'" onmouseout="this.style.transform='scale(1)'">
    <a href="https://www.youtube.com/playlist?list={{ course.youtube_playlist }}" target="_blank" style="text-decoration: none; color: inherit;">
      <img src="https://img.youtube.com/vi/{{ course.youtube_thumbnail_id }}/maxresdefault.jpg" alt="{{ course.title }}" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
      <h3 style="margin-top: 12px; font-size: 1.25em;">{{ course.title }}</h3>
    </a>
  </div>
  {% endfor %}

</div>
