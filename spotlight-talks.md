---
layout: default
title: Spotlight talks from accepted contributed papers
---

The first column indicates the time, where "xx" indicates the hour in the respective time zone.

<table style="width:100%">
{% for paper in site.data.spotlights %}
  <tr>
    <th>10:{{ forloop.index | minus: 1 | times: 15 | plus: 00 | modulo: 60 | prepend: '00' | slice: -2, 2 }}--10:{{ forloop.index | times: 15 | plus: 00 | modulo: 60 | prepend: '00' | slice: -2, 2 }} </th>
    <th>{% include spotlight-talks.html authors=paper.authors title=paper.title id=paper.id %}</th>
  </tr>
{% endfor %}
</table>
