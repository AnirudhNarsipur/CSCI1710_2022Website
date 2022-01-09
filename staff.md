---
layout: page
title: Staff
description: A listing of all the course staff members.
---

# Staff
<div style="text-align: justify">
The calendar below lists office and TA hours. Contact all TAs and Professor at cs1710tas@lists.brown.edu. Contact only the Head TAs and Professor at cs1710headtas@lists.brown.edu. However in most cases it is preferable if you post a private message on Edstem.
</div>

<div class="hours-calendar">
  <iframe src="https://calendar.google.com/calendar/embed?src=c_nr4j9tk5p8kpbu1ajubr6d8ne4%40group.calendar.google.com&ctz=Asia%2FKolkata" style="border: 0" width="800" height="600" frameborder="0" scrolling="no"></iframe>
</div>

## Instructors

{% assign instructors = site.staffers | where: 'role', 'Instructor' | sort: 'name' %}
{% for staffer in instructors %}
{{ staffer }}
{% endfor %}

{% assign hta = site.staffers | where: 'role', 'HTA' | sort: 'name' %}
{% assign num_hta = hta | size %}
{% if num_hta != 0 %}
## HTA

{% for staffer in hta %}
{{ staffer }}
{% endfor %}
{% endif %}

{% assign uta = site.staffers | where: 'role', 'UTA' | sort: 'name' %}
{% assign num_uta = uta | size %}
{% if num_uta != 0 %}
## UTA 

{% for staffer in uta %}
{{ staffer }}
{% endfor %}
{% endif %}

{% assign uta_sta = site.staffers | where: 'role', 'UTA/STA' | sort: 'name' %}
{% assign num_uta_sta = uta_sta | size %}
{% if num_uta_sta != 0 %}
## UTA/STA 

{% for staffer in uta_sta %}
{{ staffer }}
{% endfor %}
{% endif %}


{% assign sta = site.staffers | where: 'role', 'STA' | sort: 'name' %}
{% assign num_sta = sta | size %}
{% if num_sta != 0 %}
## STA 

{% for staffer in sta %}
{{ staffer }}
{% endfor %}
{% endif %}
