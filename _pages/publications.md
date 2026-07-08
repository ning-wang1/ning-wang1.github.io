---
layout: single
title: Publications
permalink: /publications/
author_profile: true
---

{% for group in site.data.publications %}

## {{ group.year }}

{% for paper in group.papers %}

<div class="pub-entry">

<div class="pub-title">
<strong>{{ paper.title }}</strong>
{% if paper.pdf %}
&nbsp;<a href="{{ paper.pdf }}">[PDF]</a>
{% endif %}
</div>

<div class="pub-authors">
{{ paper.authors }}
</div>

<div class="pub-venue">
<em>{{ paper.venue }}</em>
</div>

</div>

{% endfor %}

{% endfor %}