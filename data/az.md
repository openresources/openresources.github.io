---
layout: default
title: Council A-Z lists
description: Resources list
keywords: open, resources
locations: [aberdeen_city_council, brentwood,bristol,calderdale,cambridge_city council,cardiff_council,carmarthenshire_county_council,city_of_westminster,city_of_york,clackmannanshire_council,derbyshire_dales,fife,lambeth,norfolk,north_herts,north_somerset,oxfordshire,recycle_now (wrap)]
---

# Council A-Z lists

This lists a collection of terms from a selection of council A-Z resources lists.

* There are many terms repeated with slightly different names.
* Some terms are common while many appear in one or a few places.


<table class="resources-list">
  <thead>
    <td>Name</td>
    <td colspan="{{page.locations | size}}">Where used</td>
  <thead>
  <tbody>
    {% for resource in site.data.az %}
    <tr>
      <td>{{ resource.name }}</td>
      {% for loc in page.locations %}
      {% if resource[loc] %}
      <td>&#9679;</td>
      {% else %}
      <td>&nbsp;</td>
      {% endif %}
      {% endfor %}
    </tr>
    {% endfor %}
  </tbody>
</table>

