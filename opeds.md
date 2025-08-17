---
layout: archive
title: "Opeds"
permalink: /opeds/
author_profile: true
---


<ul>
{% for oped in site.opeds %}
  <li>
    <a href="{{ oped.url }}">{{ oped.title }}</a> - <em>{{ oped.newspaper }}</em>, {{ oped.date | date: "%B %d, %Y" }}<br>
    {{ oped.excerpt }}<br>
    <a href="{{ oped.read_online }}" target="_blank">Read Online</a>
  </li>
{% endfor %}
</ul>
