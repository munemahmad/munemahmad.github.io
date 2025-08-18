---
title: "Research Projects"
layout: page
permalink: /projects/
---

## My Research Projects

<ul>
{% assign sorted_projects = site.projects | sort: 'date' | reverse %}
{% for project in sorted_projects %}
  <li>
    <a href="{{ project.url }}">{{ project.title }}</a>  
    <br><strong>Duration:</strong> {{ project.duration }}  
    <br><strong>Client:</strong> {{ project.client }}  
    <br><strong>Sample Size:</strong> {{ project.sample_size }}  
    <br><strong>My Role:</strong> {{ project.role }}  
    <br>{{ project.excerpt }}
  </li>
  <br>
{% endfor %}
</ul>

