---
layout: default
title: "[archive]"
permalink: /archive/
---

<div class="archive-content"><p><strong>~$</strong> ls -l .archive/</p></div>

{% assign archived_posts = site.posts | where: "archived", true %}
{% include post_list.html posts=archived_posts show_size=true empty_text="no archived posts yet." %}