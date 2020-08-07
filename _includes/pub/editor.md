{% if include.e %}{{ include.e | join: ", " }} (ed{%if include.e.size > 1 %}s{%endif%}.){{ include.end }}{% endif %}
