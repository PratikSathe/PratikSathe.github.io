---
permalink: /research/
title: "Research"
layout: single
sidebar:
  nav: "research_nav"
author_profile: False
modified: 2022-10-31
---

{% assign projects = site.projects | sort: 'end_year' | reverse %}
{% for project in projects %}
### {{ project.name }}
{% if project.image %}
<table>
<tr>
    <th style="width:25%"></th>
    <th style="width:75%"></th>
</tr>
<tr>
    <td><img src="/assets/images/projects/{{ project.image }}" frameborder="0"></td>
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


