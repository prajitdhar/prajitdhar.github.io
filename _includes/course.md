{% assign c = include.course %}
{% assign inst=site.data.locations[c.inst] %}
{% if inst.name %}
{% else %}
{% assign inst = c.inst %}
{% endif %}

{{c.date}}: **{{ c.title }}** at {% if c.venue.link %}[{{c.venue.name}}]({{c.venue.link}}){% elsif c.venue.deadlink %}{{c.venue.name}} ({{c.venue.deadlink}}){% else %}{{c.venue.name}}{% endif %}{% if c.inst %}, {% if inst.link %}[{{inst.name}}]({{inst.link}}){% else %}{{inst.name}}{% if inst.city %}, {{inst.city}}{% if inst.country %}, {{inst.country}}{% endif %}{% endif %}{% endif %}{% endif %}. {% if c.program %} ({{ c.program | join: ", " }}). {% endif %}{% if c.with %}Taught jointly with {{c.with | join: ", " }}.{% endif %}<br/>{% if c.material %}[[material]]({{c.material}}){% endif %}
