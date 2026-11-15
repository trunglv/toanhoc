---
layout: page
lang: vi
title: Chủ đề
permalink: /topics/
---

<p class="page-lede">Chọn một chủ đề để xem các bài viết liên quan.</p>

{% for topic in site.data.topics %}
{% assign tposts = site.posts | where: "lang", "vi" | where_exp: "p", "p.categories contains topic.slug" %}
<section class="topic-block" id="{{ topic.slug }}">
  <div class="topic-block-head">
    <span class="topic-block-symbol" aria-hidden="true">{{ topic.symbol }}</span>
    <h2 class="topic-block-title">{{ topic.name.vi }}</h2>
  </div>
  <p class="topic-block-desc">{{ topic.desc.vi }}</p>
  {% if tposts.size == 0 %}
  <p class="empty">Chưa có bài viết trong chủ đề này.</p>
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
