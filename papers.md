---
layout: default
title: Accepted contributed papers
---

<table style="width:100%">
{% for paper in site.data.papers %}
  <tr>
    <!-- <th>10:{{ forloop.index | minus: 1 | times: 15 | plus: 00 | modulo: 60 | prepend: '00' | slice: -2, 2 }}--10:{{ forloop.index | times: 15 | plus: 00 | modulo: 60 | prepend: '00' | slice: -2, 2 }} </th> -->
    <th>{% include papers.html authors=paper.authors title=paper.title id=paper.id %}</th>
  </tr>
{% endfor %}
</table>


