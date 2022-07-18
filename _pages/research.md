---
permalink: /research/
title: "Research"
layout: single
modified: 2022-07-16
---

Placeholder descriptions. Figures to be added soon. 
{% assign projects = site.projects | sort: 'start_year' | reverse %}
{% for project in projects %}
<div class="jumbotron">
  <h2>{{ project.name }}</h2>
  <p>{{ project.content | markdownify }}</p>
</div>
{% endfor %}

{% comment %}
<h2>Active Projects</h2>
{% assign projects = site.projects | sort: "start_year" | reverse %}
{% for project in projects %}
<div class='row'>
    {% if project.image %}
        <div class="column">
            <img width="20%" src="/assets/images/projects/{{ project.image }}" alt="{{ project.name }}">
        </div>
        <div class="column">
            <h4 class="media-heading">{{ project.name }}</h4>
            <p>{{ project.summary }}</p>
            <p>{{ project.content | markdownify }}</p>
        </div>
    {% else %}
        <div class="column">
            <h4 class="media-heading">{{ project.title }}</h4>
            <p>{{ project.summary }}</p>
            <p>{{ project.content | markdownify }}</p>
        </div>
    {% endif %}
</div>
{% endfor %}
{% endcomment %}


