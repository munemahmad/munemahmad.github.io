---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

You can download my latest CV from here:  [📄 Download CV (PDF)](/files/CV.pdf)

You can download my latest resume from here:  [📄 Download Resume (PDF)](/files/Resume.pdf)

{% include base_path %}

Education
======
* MSS in Economics, Comilla University, 2020 
* BSS in Economics, Comilla University, 2019 

Work experience
======
* January 2025- Present: Research Fellow
  * Bangladesh Institute of Social Research Trust

* July 2024 – January 2025: Quantitative Researcher 
  * Impact Research Team, Work on Climate  
 
* June 2023- December 2024: Research Associate
  * Bangladesh Institute of Social Research Trust

* May 2022- June 2023: Research Assistant
  * Change Initiative 

* June 2020- April 2022: Graduate Research Assistant
  * Department of Economics, Comilla University 

  
Skills
======
* Eviews
* SPSS
* STATA
* R (Basic)
* Kobo Toolbox
* Survey CTO
* ODK (XLS)
* ArcGIS (Basic)
* Github


Publications
======
{% assign categories = "articles,working-papers,work-in-progress" | split: "," %}

{% for cat in categories %}
  {% assign pubs = site.publications | where: "category", cat | where_exp: "post", "post.is_abstract != true" %}
  {% if pubs.size > 0 %}
    <h3>
      {% if cat == "articles" %}
        Articles
      {% elsif cat == "working-papers" %}
        Working Papers
      {% elsif cat == "work-in-progress" %}
        Work in Progress
      {% endif %}
    </h3>

    <ul>
    {% for post in pubs reversed %}
      <li>
        {% if cat == "work-in-progress" %}
          <em>{{ post.authors }}</em>: {{ post.title }}
        {% else %}
          {{ post.citation }}
        {% endif %}
      </li>
    {% endfor %}
    </ul>
  {% endif %}
{% endfor %}
  
  
Teaching
======
  <ul>{% for post in site.teaching reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  

