---
layout: page
title: Item Groups
permalink: /groups
---
{% assign current_cat = page.dir | split: "/" | last%}
{% assign posts = site.categories[current_cat] | where: 'lang',page.lang %}
{% assign current_cat = page.dir | split: "/" | last%}
{% assign posts = site.categories[current_cat] | where: 'lang',page.lang %}
<ul>
{% for item in posts %}
<li><a href="{{item.url | absolute_url}}">{{item.title}}</a></li>
{% endfor %}
</ul>

__________


{% assign categories =  site.items | map: 'categories' | join: ','  | split: ',' | uniq %}
{% for category in categories %}
<div class="section-title col-md-12 mt-4">
<h2 id="{{ category }}"><span class="text-capitalize">{{ category }}</span></h2>
</div> 

<div class="row listrecent"> 
{% for item in site.items %}
{% if item.categories contains category %}
{% if item.shortdesc != null %}
{% include itembox.html %}
{% endif %}
{% endif %}
{% endfor %}
</div>
{% endfor %}