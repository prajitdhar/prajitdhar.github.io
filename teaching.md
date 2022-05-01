---
layout: page
title: Teaching
permalink: /teaching/
---

{% for loc in site.data.locations %}
{% assign courses = site.data.courses.regular | where: "inst", loc[0] %}

{% if courses.size > 0 %}
## {{ loc[1].name }}

{% for c in courses %}

- ### {{ c.date }}
  - **{{ c.title }}** {% if c.program %} ({{ c.program | join: ", " }}){% endif %} at [{{ loc[1].name }}]({{ loc[1].link }}){% if c.role %} as a {{ c.role }}{% endif %}. {% if c.with %}Taught jointly with {{c.with | join: ", " }}.{% endif %}

{% endfor %}
{% endif %}
{% endfor %}

{% if site.data.courses.external.size > 0 %}

## Workshops, Tutorials, etc.

{% assign courses = site.data.courses.external %}
{% for c in courses %}
{% assign inst=site.data.locations[c.inst] %}
{% if inst.name %}
{% else %}
{% assign inst = c.inst %}
{% endif %}
- ### {{ c.year }}
  - {{c.date}}: **{{ c.title }}** at {% if c.venue.link %}[{{c.venue.name}}]({{c.venue.link}}){% elsif c.venue.deadlink %}{{c.venue.name}} ({{c.venue.deadlink}}){% else %}{{c.venue.name}}{% endif %}{% if c.inst %}, {% if inst.link %}[{{inst.name}}]({{inst.link}}){% else %}{{inst.name}}{% endif %}{% if inst.city %}, {{inst.city}}{% endif %}{% if inst.country %}, {{inst.country}}{% endif %}{% endif %}. {% if c.program %} ({{ c.program | join: ", " }}). {% endif %}{% if c.with %}Taught jointly with {{c.with | join: ", " }}.{% endif %}<br/>{% if c.material %}[[material]]({{c.material}}){% endif %}
{% endfor %}
{% endif %}
