---
layout: archive
title: "Blog"
permalink: /blog/
author_profile: true
---

Welcome to my blog — a space where I explore ideas at the intersection of **mathematics**, **machine learning**, and **real-world engineering**.

Every week, I share thoughts, insights, and deep-dives into topics ranging from **Bayesian inference** and **AI applications** to **compressor design** and **research life**. Whether you're an industry professional, a researcher, or just curious — I hope you find something here that inspires or informs you.

☕ Let’s think, question, and learn together. And if something sparks your interest, feel free to [connect](/contact/) — I’d love to hear your thoughts.

---

{% for post in site.posts %}
  {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
  {% if forloop.first %}
  <h2 id="{{ year }}">{{ year }}</h2>
  {% else %}
    {% capture prev_year %}{{ site.posts[forloop.index0].date | date: '%Y' }}{% endcapture %}
    {% if year != prev_year %}
      <h2 id="{{ year }}">{{ year }}</h2>
    {% endif %}
  {% endif %}

  {% include archive-single.html %}
{% endfor %}
