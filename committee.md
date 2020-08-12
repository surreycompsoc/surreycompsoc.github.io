---
layout: page
title: Committee
header: Committee
display_in_sidebar: true
permalink: /committee/
---

Here are your duly-elected members of the 2020-21 committee!
<div id="committee">
{% for member in site.data.committee %}
<div class="committee-member">
{% if member.image %}
<img class="headshot" src="{{ "/assets/headshots/" | append: member.image | relative_url }}">
{% else %}
<img class="headshot" src="{{ "/assets/profile_frame.png"  | relative_url }}">
{% endif %}
<p class="committee-position">{{ member.position }}</p>
<p class="committee-name">{{ member.name }}</p>
<p class="committee-links">
{% for link in member.links %}
<a href="{{ link.link }}"><i class="fa fa-{{ link.icon }}"></i></a>
{% endfor %}
</p>
<p class="committee-description">
{{ member.description }}
</p>
</div>
{% endfor %}
</div>
