---
layout: single
title: Publications
permalink: /publications/
author_profile: true
---

{% for group in site.data.publications %}

## {{ group.year }}

{% for paper in group.papers %}

### {{ paper.title }}

{{ paper.authors }}

*{{ paper.venue }}*

{% if paper.pdf %}
[PDF]({{ paper.pdf }})
{% endif %}

{% if paper.code %}
| [Code]({{ paper.code }})
{% endif %}

{% if paper.slides %}
| [Slides]({{ paper.slides }})
{% endif %}

{% endfor %}

{% endfor %}