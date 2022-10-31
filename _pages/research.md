---
permalink: /research/
title: "Research"
layout: single
modified: 2022-07-16
---

Placeholder descriptions. Figures to be added soon. 

<!--- {% assign projects = site.projects | sort: 'start_year' | reverse %}
{% for project in projects %}

<div class="jumbotron">
  <h2>{{ project.name }}</h2>
  <p>{{ project.content | markdownify }}</p>
</div>
{% endfor %} --->
NOW TESTING OUT NEWEST STUFF

{% assign projects = site.projects | sort: 'start_year' | reverse %}
{% for project in projects %}

<h2>{{ project.name }}</h2>
{% if project.image %}
<table>
<tr>
    <th style="width:30%"></th>
    <th style="width:70%"></th>
</tr>
<tr>
    <td><iframe src="/assets/images/projects/{{ project.image }}" frameborder="0" width="100%"></iframe></td>
    <td><p>{{ project.content | markdownify }}</p></td>
</tr>
</table>
{% else %}
<table>
<tr>
    <th></th>
</tr>
<tr>
    <td><p>{{ project.content | markdownify }}</p></td>
</tr>
</table>
{% endif %}
{% endfor %}

---

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
--->
