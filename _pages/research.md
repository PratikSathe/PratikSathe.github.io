---
permalink: /research/
title: "Research"
layout: single
modified: 2022-07-16
---

<!-- <table>
<tr>
<th style="width:20%"></th>
<th></th>
<th></th>
</tr>
<tr>
<td>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.</td>
<td>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.</td>
<td>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.</td>
</tr>
</table> -->

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


