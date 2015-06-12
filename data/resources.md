---
layout: default
title: Resources
description: Resources list
keywords: open, resources
---

This list of resource terms is linked to the relevant WRAP material streams and OpenStreetMap tags.

**Note: Any use of the WRAP material streams must adhere to their terms and conditions.**

OpenStreetMap tags are defined as `recycling:[material]=yes/no` on the OpenStreetMap, e.g. `recycling:paper=yes`. The table below just shows the `[material]` part. See the [amenity=recycling](http://wiki.openstreetmap.org/wiki/Tag:amenity%3Drecycling) for more information.


<table class="resources-list">
  <thead>
    <td>Name</td>
    <td>WRAP material stream</td>
    <td>WRAP colour</td>
    <td>OpenStreetMap tag</td>
  <thead>
  <tbody>
    {% for resource in site.data.resources %}
    <tr>
      <td>{{ resource.name }}</td>
      {% assign color = site.data.material_streams[resource.material_stream].color %}
      <td>{{ resource.material_stream }}</td>
      <td><div style="background: #{{ color }}; width: 40px; height: 30px"></div></td>
      <td>{{ resource.osm_tag }}</td>
    </tr>
    {% endfor %}
  </tbody>
</table>
