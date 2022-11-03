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
<img src="/assets/images/projects/{{ project.image }}" style="padding: 0px 20px 10px 0px;" frameborder="0" align=left width="35%" /> 
<div>
{{ project.content | markdownify | remove: '<p>' | remove: '</p>' }}
</div>
{% else %}
{{ project.content | markdownify }}
{% endif %}
{% endfor %}


