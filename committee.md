---
layout: page
title: Committee
permalink: /committee/
---

Here are your duely-elected members of the 2016&en;17 committee!

{% for member in site.data.committee %}
## {{ member.name }}
{{ member.position }}
{% if member.username %}
[{{member.username}}@surrey.ac.uk](mailto:{{member.username}}@surrey.ac.uk)
{% endif %}
{% endfor %}
