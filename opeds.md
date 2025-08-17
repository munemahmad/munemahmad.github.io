---
layout: default
title: "Op-Eds"
permalink: /opeds/
author_profile: true
---


<h1>Op-eds</h1>
<ul>
{% for oped in site.opeds %}
  <li>
    <a href="{{ oped.url }}">{{ oped.title }}</a>
  </li>
{% endfor %}
</ul>

