---
layout: default
title: "[archive]"
permalink: /archive/
---

**~$** ls -l .archive/

{% assign archived_posts = site.posts | where: "archived", true %}

total {{ archived_posts.size }}

{% if archived_posts.size > 0 %}
<ul>
  {% for post in archived_posts %}
  <li>
    {% assign date_format = "%b  %d %H:%M" %}
    {{post.size}} {{ post.date | date: date_format }} <a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
  </li>
  {% endfor %}
</ul>
{% else %}
no archived posts yet.
{% endif %}
