---
layout: page
lang: en
title: Topics
permalink: /en/topics/
---

<p class="page-lede">Pick a topic to see related posts.</p>

{% for topic in site.data.topics %}
{% assign tposts = site.posts | where: "lang", "en" | where_exp: "p", "p.categories contains topic.slug" %}
<section class="topic-block" id="{{ topic.slug }}">
  <div class="topic-block-head">
    <span class="topic-block-symbol" aria-hidden="true">{{ topic.symbol }}</span>
    <h2 class="topic-block-title">{{ topic.name.en }}</h2>
  </div>
  <p class="topic-block-desc">{{ topic.desc.en }}</p>
  {% if tposts.size == 0 %}
  <p class="empty">No posts in this topic yet.</p>
  {% else %}
  <ol class="notebook-list">
    {% for post in tposts %}
    <li class="notebook-item">
      <a href="{{ post.url | relative_url }}">
        <time class="notebook-date" datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%d/%m/%Y" }}</time>
        <span class="notebook-title">{{ post.title }}</span>
      </a>
    </li>
    {% endfor %}
  </ol>
  {% endif %}
</section>
{% endfor %}
