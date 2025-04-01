---
layout: page
title: Activities
permalink: /activities/
---

{% assign activities = site.data.activities | group_by_exp: "item", "item.startdate | date: '%Y'" %}

{% for y in activities %}

### {{ y.name }}

{% assign thisyear = y.items | sort: "date" %}
{% for act in thisyear %}

{% include activities.md activity=act %}
{% endfor %}
{% endfor %}