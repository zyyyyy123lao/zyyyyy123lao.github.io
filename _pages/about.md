---
permalink: /
title: "Yi Zhang"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

<div id="homepage"></div>
<section id="about-me" class="home-section">

Hi, I am **Yi Zhang**, an undergraduate student at [Southwest University](https://en.swu.edu.cn/) (2023-2027), in Chongqing, China.

My research interests focus on **World Models**, **MLLM** (Multimodal Large Language Models), and **AI Agent**. I am interested in how multimodal models, world models, and agentic systems can be built and applied to real-world tasks.

Feel free to reach out via [email](mailto:zyyyyy123@email.swu.edu.cn) or explore my publications for more.

</section>

<style>
  html {
    scroll-behavior: smooth;
  }

  .home-section {
    scroll-margin-top: 5rem;
  }

  .home-news-title {
    display: inline-block;
    border-bottom: 2px solid #f0d800;
    margin-bottom: 0.25em;
  }

  .home-news-list .highlight {
    color: #f0b400;
  }
</style>

<section id="news" class="home-section">

## <span class="home-news-title">News</span>

<ul class="home-news-list">
  <li>[2026/05] Our paper <span class="highlight">Code2Worlds</span> has been accepted to ICML 2026!</li>
  <li>[2026/04] Our paper <span class="highlight">PETR</span> has been accepted to ICMR 2026!</li>
</ul>

</section>

<section id="publications" class="home-section">

## Publications

{% if site.author.googlescholar %}
  <div class="wordwrap">You can also find my articles on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</div>
{% endif %}

{% include base_path %}

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

</section>

<section id="service" class="home-section">

## Service

- Reviewer, AAAI 2026
- Reviewer, TMLR

</section>

<section id="educations" class="home-section">

## Educations

- B.S. student, Southwest University, 2023-2027

</section>
