---
title: "Opeds"
layout: default
permalink: /opeds/
---

<div class="container">
  <h1>My Opeds</h1>

  <ul class="opeds-list">
  {% for oped in site.opeds %}
    <li>
      <a href="{{ oped.url }}">{{ oped.title }}</a> - <em>{{ oped.newspaper }}</em>, {{ oped.date | date: "%B %d, %Y" }}</br>
      {{ oped.excerpt }}<br>
      <a href="{{ oped.read_online }}" target="_blank">Read Online</a>
    </li>
  {% endfor %}
  </ul>
</div>
