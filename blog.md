---
layout: default
title: Miscellaneous
permalink: /Miscellaneous
---

## Miscellaneous
---

<div class="posts">
  {% for post in site.posts %}
    <article class="post">

      <h2><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h2>

      <div class="entry">
        {% comment %} {{ post.excerpt }}  {% endcomment %}
        {% comment %} <p align="center"><img src="{{ post.teaser }}" width="60%"/></p> {% endcomment %}
        <a href="{{ site.baseurl }}{{ post.url }}"><img src="{{ post.teaser }}" alt="" width="60%"/></a>
      </div>

      {% comment %} <a href="{{ site.baseurl }}{{ post.url }}" class="read-more">Read More</a> {% endcomment %}
    </article>
  {% endfor %}
</div>
