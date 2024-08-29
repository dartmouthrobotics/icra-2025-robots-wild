---
layout: default
title: Organizers
---

{% for organizer in site.data.organizers %}
  {% include organizer.html name=organizer.name site=organizer.site email=organizer.email pic_url=organizer.pic_url lab=organizer.lab department=organizer.department institution=organizer.institution %}
  <hr>
{% endfor %}
