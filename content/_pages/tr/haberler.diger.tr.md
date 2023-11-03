---
layout: page
title: Diğer Haberler
lang: tr
permalink: /tr/haberler/diger-haberler
---

{% assign haberler = site.diger_haberler | where:"lang", page.lang | sort: 'date' | reverse %}
{% for haber in haberler %}
<div class="d-flex align-items-stretch pb-2">
    <div><i class="bx bx-chevron-right"></i></div>
    <div class="article">
        <div>
        <a href="{{ site.baseurl }}{{ haber.permalink }}">{{ haber.title }}</a>
        </div>
        <div class="small">
        <span class="small text-muted text"><em>{{ haber.date | date: "%Y-%m-%d" }}</em></span> -
        {{ haber.short_description }}
        </div>
    </div>
</div>
{% endfor %}
