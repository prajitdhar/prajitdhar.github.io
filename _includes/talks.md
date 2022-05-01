{% assign talk = include.talk %}
{% assign inst=site.data.locations[talk.institution] %}
{% if inst.name %}
{% else %}
{% assign inst = talk.institution %}
{% endif %}

- **{{ talk.title }}**{% if talk.type %}. {{ talk.type }}{% endif %}{% if talk.with %}. With {{ talk.with | join: ", " }}{% endif %}{% if talk.venue.link %}. [{{ talk.venue.label }}]({{talk.venue.link}}){% elsif talk.venue.deadlink %}. {{ talk.venue.label }} ({{talk.venue.deadlink}}){% else %}. {{ talk.venue.label }}{% endif %}{% if talk.venue.online %}, {{talk.venue.online}}{% else %} in {{ talk.venue.city }}, {{ talk.venue.country }}{% endif %} on {{ talk.date | date: "%B %e, %Y" }}.{% if talk.comment %} {{ talk.comment }}.{% endif %}<br/>{% if talk.abstract %}[[abstract]]({{ talk.abstract }}) {% endif %}{% if talk.slides %}[[slides]]({{ talk.slides }}) {% endif %}{% if talk.poster %} [[poster]]({{ talk.poster }}){% endif %}{% if talk.paper %} [[paper]](/publications/{{ talk.paper}}.html){% endif %}
