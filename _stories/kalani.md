---
layout: story
title: Kalani's story
author: kalani
featureditem: 2016-03-04-ID0002
selecteditems:
 - 2016-03-04-ID0002
 - 2016-03-04-ID0002
 - 2016-03-04-ID0002
categories: [ Sentimental ]
---

{% for item in page.selecteditems %}
{% if item.shortdesc != null %}
{% include itembox.html %}
{% endif %}
{% endfor %}
{% endfor %}
