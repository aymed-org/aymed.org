---
layout: page
title: Duyurular
lang: tr
permalink: /tr/duyurular
---

<h4>{{ page.title }}</h4>

{% assign duyurular = site.duyurular | where:"lang", page.lang | sort: 'date' | reverse %}

{% for duyuru in duyurular %}
  {% if duyuru.lang == page.lang %}
<div class="d-flex align-items-stretch pb-2">
    <div><i class="bx bx-chevron-right"></i></div>
    <div class="article">
        <div>
        <a href="{{ site.baseurl }}{{ duyuru.permalink }}">{{ duyuru.title }}</a>
        </div>
        <div class="small">
        <span class="small text-muted text"><em>{{ duyuru.date | date: "%Y-%m-%d" }}</em></span> -
        {{ duyuru.short_description }}
        </div>
    </div>
</div>
  {% endif %}
{% endfor %}
