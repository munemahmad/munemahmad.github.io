---
title: "Research Projects"
layout: archive
permalink: /projects/
collection: projects
entries_layout: list
author_profile: true
---


<ul>
{% assign sorted_projects = site.projects | sort: 'date' | reverse %}
{% for project in sorted_projects %}
  <li>
    <a href="{{ project.url }}">{{ project.title }}</a>  
    <br><strong>Duration:</strong> {{ project.duration }}  
    <br><strong>Client:</strong> {{ project.client }}  
    <br><strong>Sample Size:</strong> {{ project.sample_size }}  
    <br><strong>Responsibilities:</strong> {{ project.responsibilities }}  
    <br>{{ project.excerpt }}
  </li>
  <br>
{% endfor %}
</ul>

