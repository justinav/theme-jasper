---
layout: page
title: News & Opinions
permalink: /blog/
---

{% for post in site.posts %}
  <article class="{% if forloop.first %}first{% elsif forloop.last %}last{% else %}middle{% endif %}">
    <div class="post-header">
      <h2 class="title"><a href="/{{ post.url }}/" class="js-pjax">{{ post.title }}</a></h2>
      <p class="date">{{ post.date | date: "%b %d, %Y" }}</p>
    </div><!--/.article-head-->
  </article>
  {% if forloop.last %}{% else %}<div class="separater"></div>{% endif %}
{% endfor %}
