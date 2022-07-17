---
permalink: /research/
title: "Research"
layout: single
modified: 2022-07-16
---


{% for project in site.projects %}
<div class="jumbotron">
  <h2>{{ project.name }} - {{ project.startdate }}</h2>
  <p>{{ project.content | markdownify }}</p>
</div>
{% endfor %}


<!-- {% include a-loop-test.html %}

projects:
    - name: alpha
      description: Search and rescue at sea

 -->
<!-- <div class="jumbotron">
  <h4>Benchmarking of Iterative Quantum Algorithms</h4>
  <p></p>
  <div class="row align-items-end">
    <div class="col-md-9 col-sm-12">
      <ul>
        <li>Our group works on <strong>quantum algorithms</strong> for the PDEs that govern fluid flows and other phenomena to gain exponential speedups</li>
        <li>We develop quantum lattice-based algorithms like quantum lattice Boltzmann and lattice gas</li>
        <li>Quantum <em>simulation</em> is used to scale our algorithms to large HPC resources for analysis</li>
      </ul>
    </div>
    <div class="col-md-3 col-sm-12" style="background-color:transparent">
      <p><img width="20%" src="/assets/images/bio-photo.jpg" /></p>
    </div>
  </div>
</div>
 -->