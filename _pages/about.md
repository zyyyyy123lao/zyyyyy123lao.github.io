---
permalink: /
title: "Yi Zhang"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

<style>
  html {
    scroll-behavior: smooth;
  }

  .home-anchor {
    display: block;
    position: relative;
    top: -5rem;
    visibility: hidden;
  }

  .page__content h2 {
    border-bottom: 1px solid #eeeeee;
    padding-bottom: 0.45em;
  }

  .home-news-list .highlight {
    color: #f0b400;
  }
</style>

<span id="homepage" class="home-anchor"></span>
<span id="about-me" class="home-anchor"></span>

Hi, I am Yi Zhang, an undergraduate student at [Southwest University](https://en.swu.edu.cn/), majoring in Software Engineering.

My research interests focus on **World Models**, **MLLM**, and **AI Agent**. I am interested in building physically grounded world models. Feel free to reach out via [email](mailto:zyyyyy123@email.swu.edu.cn) for collaboration.

<span id="news" class="home-anchor"></span>

## 🔥 News

<ul class="home-news-list">
  <li>[2026/05] 🎉 Our paper <span class="highlight">Code2Worlds</span> has been accepted to ICML 2026!</li>
  <li>[2026/04] 🎉 Our paper <span class="highlight">PETR</span> has been accepted to ICMR 2026!</li>
</ul>

<span id="publications" class="home-anchor"></span>

## 📝 Publications

{% if site.publication_category %}
  {% for category in site.publication_category %}
    {% assign title_shown = false %}
    {% for post in site.publications reversed %}
      {% if post.category != category[0] %}
        {% continue %}
      {% endif %}
      {% unless title_shown %}
        <h3>{{ category[1].title }}</h3>
        {% assign title_shown = true %}
      {% endunless %}
      {% include archive-single.html %}
    {% endfor %}
  {% endfor %}
{% else %}
  {% for post in site.publications reversed %}
    {% include archive-single.html %}
  {% endfor %}
{% endif %}

<span id="service" class="home-anchor"></span>

## 🤝 Service

- Reviewer, AAAI 2026
- Reviewer, TMLR

<span id="educations" class="home-anchor"></span>

## 📖 Educations

- B.S. student, Southwest University, 2023-2027
