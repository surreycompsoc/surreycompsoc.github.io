---
layout: page
title: Committee
display_in_sidebar: true
permalink: /committee/
---

Here are your duly-elected members of the 2016–17 committee!

{% for member in site.data.committee %}
<div class="committee-member">
<img class="headshot" src="{{ "/assets/headshots/" | append: member.username | append: ".jpg"  | relative_url }}">
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
