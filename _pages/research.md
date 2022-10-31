---
permalink: /research/
title: "Research"
layout: single
modified: 2022-07-16
---

{% assign projects = site.projects | sort: 'end_year' | reverse %}
{% for project in projects %}
<h3>{{ project.name }}</h3>
{% if project.image %}
<table>
<tr>
    <th style="width:25%"></th>
    <th style="width:75%"></th>
</tr>
<tr>
    <td><img style="height:100%; width:100%" width="100%" src="/assets/images/projects/{{ project.image }}" frameborder="0"></td>
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


