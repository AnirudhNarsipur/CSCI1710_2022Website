---
layout: page
title: Staff
description: A listing of all the course staff members.
---

# Staff

Staff information is stored in the `_staffers` directory and rendered according to the layout file, `_layouts/staffer.html`.

## Instructors

{% assign instructors = site.staffers | where: 'role', 'Instructor' %}
{% for staffer in instructors %}
{{ staffer }}
{% endfor %}

{% assign hta = site.staffers | where: 'role', 'HTA' %}
{% assign num_hta = hta | size %}
{% if num_hta != 0 %}
## HTA

{% for staffer in hta %}
{{ staffer }}
{% endfor %}
{% endif %}

{% assign uta = site.staffers | where: 'role', 'UTA' %}
{% assign num_uta = uta | size %}
{% if num_uta != 0 %}
## UTA 

{% for staffer in uta %}
{{ staffer }}
{% endfor %}
{% endif %}

{% assign uta_sta = site.staffers | where: 'role', 'UTA/STA' %}
{% assign num_uta_sta = uta_sta | size %}
{% if num_uta_sta != 0 %}
## UTA/STA 

{% for staffer in uta_sta %}
{{ staffer }}
{% endfor %}
{% endif %}


{% assign sta = site.staffers | where: 'role', 'STA' %}
{% assign num_sta = sta | size %}
{% if num_sta != 0 %}
## STA 

{% for staffer in sta %}
{{ staffer }}
{% endfor %}
{% endif %}
