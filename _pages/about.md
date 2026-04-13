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

**Current focus:**
* Spectral and dynamical problems in quantum field theory.
* Scaling limits of quantum dynamical systems.
* Analysis of nonlinear dispersive PDEs.


Before joining UT Austin, I completed my M.Sc. in Applied Mathematics at Kyoto University, where I was affiliated with the Research Institute for Mathematical Sciences (RIMS), under the supervision of Professor [Kenji Nakanishi](https://www.kurims.kyoto-u.ac.jp/en/list/nakanishi.html).

*Feel free to browse my [publications](/publications/), view my [CV](/cv/), or contact me by [email](mailto:alimezher@utexas.edu).*


## Recent Papers

{% assign recent_papers = site.publications | sort: "date" | reverse %}

<ul>
{% for paper in recent_papers limit: 3 %}
  <li>
    <a href="{{ paper.paperurl }}">{{ paper.title }}</a>
    {% if paper.venue %}<br><em>{{ paper.venue }}</em>{% endif %}
    {% if paper.date %} ({{ paper.date | date: "%Y" }}){% endif %}
  </li>
{% endfor %}
</ul>
