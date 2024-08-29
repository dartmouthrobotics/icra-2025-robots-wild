---
layout: default
title: Invited Speakers 
---

<h2 id="invited">Invited talks</h2>

{% for speaker in site.data.speakers %}
  {% include speaker.html name=speaker.name site=speaker.site pic_url=speaker.pic_url lab=speaker.lab institution=speaker.institution topic=speaker.topic  abstract=speaker.abstract bio=speaker.bio id=speaker.id %}
  <hr>
{% endfor %}


<!-- <h2 id="panel">Panel discussion</h2>

A **Panel Discussion** will be held as part of the program: 

{% for panelist in site.data.panelists %}
  {% include panelist.html name=panelist.name site=panelist.site pic_url=panelist.pic_url  institution=panelist.institution topic=panelist.topic %}
  <hr>
{% endfor %} -->
