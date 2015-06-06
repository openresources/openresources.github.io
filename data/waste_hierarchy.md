---
layout: default
title: Managing resources
description: Resources list
keywords: open, resources
---

# Managing resources

<h2>Methods</h2>

Various methods are used to process resources at different stages. These can be associated with the waste hierarchy levels below and further linked with elements such as the processing plants or local repair businesses.

<table class="">
  <thead>
    <td>Method</td>
    <td>Hierarchy level</td>
    <td></td>
  </thead>
  <tbody>
    {% for method in site.data.methods %}
    <tr>
      <td>{{ method.name }}</td>

      <td>
        {% for level in site.data.waste_hierarchy %}
        {% if method.hierarchy_level == level.id %}
        {{ level.name }}
        {% endif %}
        {% endfor %}
      </td>
      <td>{{ method.description }}</td>
    </tr>
    {% endfor %}
  </tbody>
</table>


<h2>Waste hierarchy levels</h2>
<p>
See <a href="http://en.wikipedia.org/wiki/European_Waste_Hierarchy">European Waste Hierarchy</a> for more information.
</p>

<table class="">
  <thead>
    <td>Step</td>
    <td>Description</td>
  </thead>
  <tbody>
    {% for level in site.data.waste_hierarchy %}
    <tr>
      <td>{{ level.name }}</td>
      <td>{{ level.description }}</td>
    </tr>
    {% endfor %}
  </tbody>
</table>
