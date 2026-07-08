<!-- ---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
 -->

 ---
layout: single
title: Publications
permalink: /publications/
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