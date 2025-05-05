---
layout: default
title: Spotlight talks from accepted contributed papers
---

([Eastern Daylight Time EDT--UTC/GMT-4](https://www.timeanddate.com/time/zones/edt))

Morning Spotlight Talks

<table style="width:100%">
{% for paper in site.data.spotlights %}
  <tr>
    <th>10:{{ forloop.index | minus: 1 | times: 15 | plus: 00 | modulo: 60 | prepend: '00' | slice: -2, 2 }}--10:{{ forloop.index | times: 15 | plus: 00 | modulo: 60 | prepend: '00' | slice: -2, 2 }} </th>
    <th>{% include spotlight-talks.html authors=paper.authors title=paper.title id=paper.id %}</th>
  </tr>
{% endfor %}
</table>

Afternoon Spotlight Talks

<table style="width:100%">
{% for paper in site.data.spotlights_pm %}
  <tr>
    <!-- <th>14:{{ forloop.index | minus: 1 | times: 15 | plus: 25 | modulo: 60 | prepend: '00' | slice: -2, 2 }}--14:{{ forloop.index | times: 15 | plus: 25 | modulo: 60 | prepend: '00' | slice: -2, 2 }} </th> -->
    <th>{ paper.time }</th>
    <th>{% include spotlight-talks.html authors=paper.authors title=paper.title id=paper.id %}</th>
  </tr>
{% endfor %}
</table>

