---
layout: page
title: Committee
permalink: /committee/
---

Here are your duly-elected members of the 2016–17 committee!

{% for member in site.data.committee %}
<img class="headshot" src="{{ "/assets/headshots/" | append: member.username | append: ".jpg"  | relative_url }}">

## {{ member.name }}
{{ member.position }}
{% if member.username %}
[{{member.username}}@surrey.ac.uk](mailto:{{member.username}}@surrey.ac.uk)
{% endif %}
{% endfor %}
