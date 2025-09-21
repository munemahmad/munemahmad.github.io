---
layout: archive
title: "Op-Eds"
permalink: /opeds/
author_profile: true
---
*(Clicking on a op-ed title will direct you to the unedited version.)*


<ul class="opeds-list">
{% assign sorted_opeds = site.opeds | sort: 'date' | reverse %}
{% for oped in sorted_opeds %}
  <li class="opeds-item">
    <strong>{{ oped.title }}</strong><br>
    <em>{{ oped.newspaper }}</em>, {{ oped.date | date: "%B %d, %Y" }}
    <a href="{{ oped.read_online }}" target="_blank" class="btn-read">Read Online</a><br>

    {% assign words = oped.content | number_of_words %}
    {% assign minutes = words | divided_by:200 | ceil %}
    <span class="reading-time">~{{ minutes }} min read</span>
  </li>
{% endfor %}
</ul>

