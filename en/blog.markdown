---
layout: page
lang: en
title: Posts
permalink: /en/blog/
---

<p class="page-lede">Every note, in order of time.</p>

<div class="archive">
  {% assign posts_by_year = site.posts | where: "lang", "en" | group_by_exp: "post", "post.date | date: '%Y'" %}
  {% if posts_by_year.size == 0 %}<p class="empty">No posts yet. Check back soon.</p>{% endif %}
  {% for year in posts_by_year %}
  <section class="archive-year">
    <h2 class="archive-year-title">{{ year.name }}</h2>
    <ol class="notebook-list">
      {% for post in year.items %}
      <li class="notebook-item">
        <a href="{{ post.url | relative_url }}">
          <time class="notebook-date" datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%d/%m/%Y" }}</time>
          <span class="notebook-title">{{ post.title }}</span>
        </a>
      </li>
      {% endfor %}
    </ol>
  </section>
  {% endfor %}
</div>
