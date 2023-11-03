---
layout: page
title: Etkinlikler
lang: tr
permalink: /tr/etkinlikler/
---

{% assign etkinlikler = site.etkinlikler | where:"lang", page.lang | sort: 'date' | reverse %}

{% for etkinlik in etkinlikler %}
  {% if etkinlik.lang == page.lang %}
<div class="d-flex align-items-stretch pb-2">
    <div><i class="bx bx-chevron-right"></i></div>
    <div class="article">
        <div>
        <a href="{{ site.baseurl }}{{ etkinlik.permalink }}">{{ etkinlik.title }}</a>
        </div>
        <div class="small">
        <span class="small text-muted text"><em>{{ etkinlik.date | date: "%Y-%m-%d" }}</em></span> -
        {{ etkinlik.short_description }}
        </div>
    </div>
</div>
  {% endif %}
{% endfor %}
