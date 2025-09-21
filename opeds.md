---
layout: archive
title: "Opeds"
permalink: /opeds/
author_profile: true
---

<ul>
{% assign sorted_opeds = site.opeds | sort: 'date' | reverse %}
{% for oped in sorted_opeds %}
  <li>
    <a href="{{ oped.url }}">{{ oped.title }}</a> 
    - <em>{{ oped.newspaper }}</em>, {{ oped.date | date: "%B %d, %Y" }}<br>

    <!-- Reading Time -->
    {% assign words = oped.content | number_of_words %}
    {% assign minutes = words | divided_by:200 | ceil %}
    <span style="font-size:0.85em; color:#666;">~{{ minutes }} min read</span><br>

    <a href="{{ oped.read_online }}" target="_blank" class="btn-read">Read Online</a>
  </li>
{% endfor %}
</ul>
