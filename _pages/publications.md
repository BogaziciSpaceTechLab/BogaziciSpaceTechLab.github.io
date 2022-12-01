---
layout: archive
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

<div style="display: flex;
    flex-direction: row;
    align-items:center;
    font-size: 28px;
    font-weight: 600;">
Journal Papers
</div>
{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}

<div style="display: flex;
    flex-direction: row;
    align-items:center;
    height: 60px;
    font-size: 28px;
    font-weight: 600;
    margin-top: 40px;">
Conference Preceedings
</div>
{% for post in site.conferences reversed %}
  {% include archive-single.html %}
{% endfor %}

<div style="display: flex;
    flex-direction: row;
    align-items:center;
    height: 60px;
    font-size: 28px;
    font-weight: 600;
    margin-top: 40px;">
Dissertations
</div>
{% for post in site.dissertations reversed %}
  {% include archive-single.html %}
{% endfor %}
