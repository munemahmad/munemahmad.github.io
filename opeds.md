---
layout: archive
title: "Op-Eds"
permalink: /opeds/
author_profile: true
---


<ul>
{% for oped in site.opeds %}
  <li>
    <a href="{{ oped.url }}">{{ oped.title }}</a>
  </li>
{% endfor %}
</ul>

