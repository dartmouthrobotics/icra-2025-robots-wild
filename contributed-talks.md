---
layout: default
title: Lightning talks from accepted contributed papers
---

The first column indicates the time, where "xx" indicates the hour in the respective time zone.

<table style="width:100%">
{% for paper in site.data.papers %}
  <tr>
    <th>xx:{{ forloop.index | minus: 1 | times: 3 | plus: 45 | modulo: 60 | prepend: '00' | slice: -2, 2 }}--xx:{{ forloop.index | times: 3 | plus: 45 | modulo: 60 | prepend: '00' | slice: -2, 2 }} </th>
    <th>{% include contributed-talks.html authors=paper.authors title=paper.title id=paper.id %}</th>
  </tr>
{% endfor %}
</table>

