---
layout: default
title: Accepted contributed papers
---


<h3 id="am">Morning Posters</h3>
<table style="width:100%">
{% for paper in site.data.papers %}
   {% if paper.morning %}
  <tr>
    <!-- <th>10:{{ forloop.index | minus: 1 | times: 15 | plus: 00 | modulo: 60 | prepend: '00' | slice: -2, 2 }}--10:{{ forloop.index | times: 15 | plus: 00 | modulo: 60 | prepend: '00' | slice: -2, 2 }} </th> -->
    <th>{% include papers.html authors=paper.authors title=paper.title id=paper.id %}</th>
  </tr>
  {% endif %}
{% endfor %}
</table>

<h3 id="pm">Afternoon Posters</h3>
<table style="width:100%">
{% for paper in site.data.papers %}
  {% unless paper.morning %}
  <tr>
    <!-- <th>10:{{ forloop.index | minus: 1 | times: 15 | plus: 00 | modulo: 60 | prepend: '00' | slice: -2, 2 }}--10:{{ forloop.index | times: 15 | plus: 00 | modulo: 60 | prepend: '00' | slice: -2, 2 }} </th> -->
    <th>{% include papers.html authors=paper.authors title=paper.title id=paper.id %}</th>
  </tr>
  {% endunless %}
{% endfor %}
</table>