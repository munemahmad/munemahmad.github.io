---
layout: archive
title: "Op-Eds"
permalink: /opeds/
author_profile: true
---

{% include base_path %}

{% for post in site.opeds reversed %}
  <div class="archive-item">
    <h3><a href="{{ post.url | default: post.permalink }}">{{ post.title }}</a></h3>
    <p><em>{{ post.newspaper }}</em> | <a href="{{ post.url }}">Read Online</a></p>
    <p>{{ post.excerpt }}</p>
  </div>
{% endfor %}
