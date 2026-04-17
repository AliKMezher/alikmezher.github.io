---
permalink: /
title: "About Me"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

I am a Ph.D. student in the Department of Mathematics at The University of Texas at Austin, working with Professor [Thomas Chen](https://tc-math.github.io/web/index.html).

**My research interests:** Analysis of PDEs and Mathematical Physics.

**Currently,** I am working on some spectral and dynamical problems in quantum field theory. In particular,
* Scaling limits of quantum dynamical systems.
* Bose-Einstein Condensation (BEC) formation. 


Before joining UT Austin, I completed my M.Sc. in Applied Mathematics at Kyoto University, where I was affiliated with the Research Institute for Mathematical Sciences (RIMS), under the supervision of Professor [Kenji Nakanishi](https://www.kurims.kyoto-u.ac.jp/en/list/nakanishi.html).

*Feel free to browse my [publications](/publications/), view my [CV](/cv/), or contact me by [email](mailto:alimezher@utexas.edu).*


## Books and Lecture notes
<hr />

<ul>
{% assign books_lectures = site.publications | where: "category", "books_lectures" | sort: "date" | reverse %}
{% for item in books_lectures %}
  <li>
    <a href="{{ item.url }}">{{ item.title }}</a>
    {% if item.venue %}<br><em>{{ item.venue }}</em>{% endif %}
    {% if item.date %} ({{ item.date | date: "%Y" }}){% endif %}
  </li>
{% endfor %}
</ul>

## Recent Journal Publications
<hr />

{% assign recent_papers = site.publications | where: "category", "journals" | sort: "date" | reverse %}

<ul>
{% for paper in recent_papers limit: 3 %}
  <li>
    <a href="{{ paper.url }}">{{ paper.title }}</a>
    {% if paper.venue %}<br><em>{{ paper.venue }}</em>{% endif %}
    {% if paper.date %} ({{ paper.date | date: "%Y" }}){% endif %}
  </li>
{% endfor %}
</ul>
