---
layout: page
title: Nachrichten
lang: de
permalink: /de/nachrichten/
---

    {% assign sorted_news = site.haberler | sort: 'date' | reverse %}
    {% for news in sorted_news %}
    {{ news.title }}
    {% endfor %}

