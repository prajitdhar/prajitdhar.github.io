---
layout: page
title: Talks
permalink: /talks/
---

{% if site.data.talks.invited.size > 0 %}

## Invited Talks

{% assign talks = site.data.talks.invited | group_by_exp: "item", "item.date | date: '%Y'" %}

{% for y in talks %}

### {{ y.name }}

{% assign thisyear = y.items | sort: "date" | reverse %}

{% for pub in thisyear %}
{% include talks.md talk=pub %}
{% endfor %}

{% endfor %}
{% endif %}

{% if site.data.talks.conference.size > 0 %}

## Conference Talks

{% assign talks = site.data.talks.conference | group_by_exp: "item", "item.date | date: '%Y'" %}

{% for y in talks %}

### {{ y.name }}

{% assign thisyear = y.items | sort: "date" %}

{% for pub in thisyear %}
{% include talks.md talk=pub %}
{% endfor %}

{% endfor %}
{% endif %}
