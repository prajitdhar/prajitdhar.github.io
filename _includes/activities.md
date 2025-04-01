{% assign activity = include.activity %}
{% assign inst=site.data.locations[activity.location] %}
{% if inst.name %}
{% else %}
{% assign inst = activity.location %}
{% endif %}
{% assign startmonth =  activity.startdate | date: "%B" %}
{% assign endmonth =  activity.enddate | date: "%B" %}

- **{{ activity.title }}** {% if activity.type %} {{ activity.type }}{% endif %} at [{{inst.name}}]({{inst.link}}) on {% if activity.startdate == activity.enddate %}{{ activity.startdate | date: "%B %e, %Y"}}{% else %}{% if startmonth == endmonth %}{{ activity.startdate | date: "%B" }} {{ activity.startdate | date: "%e" }}-{{ activity.enddate | date: "%e" }}, {{ activity.startdate | date: "%Y" }}{% elsif startmonth != endmonth %}{{ activity.startdate | date: "%B %e" }} -- {{ activity.enddate | date: "%B %e" }}, {{ activity.startdate | date: "%Y" }}{% endif %}{% endif %}\
\
    {% if activity.description %} {{ activity.description }}{% endif %}