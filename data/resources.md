---
layout: default
title: Resources
description: Resources list
keywords: open, resources
---

This list of resource terms is linked to the relevant WRAP material streams.

**Note: Any use of the WRAP material streams must adhere to their terms and conditions.**

<table class="resources-list">
  <thead>
    <td>Name</td>
    <td>Material stream</td>
    <td>Colour</td>
  <thead>
  <tbody>
    {% for resource in site.data.resources %}
    <tr>
      <td>{{ resource.name }}</td>
      {% assign color = site.data.material_streams[resource.material_stream].color %}
      <td>{{ resource.material_stream }}</td>
      <td><div style="background: #{{ color }}; width: 40px; height: 30px"></div></td>
    </tr>
    {% endfor %}
  </tbody>
</table>
