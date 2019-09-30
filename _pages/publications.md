---
layout: page
permalink: /publications/
title: publications
description: 
pubyears:   [2019, 2018, 2016, 2014, 2013]
evalyears:  [2019, 2017, 2016, 2015, 2014, 2013]
pressyears: [2016]
---


{% for y in page.pubyears %}
  <h3 class="year">{{y}}</h3>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

<h2 id="evalpapers">evaluation campaigns</h2>

{% for y in page.evalyears %}
  <h3 class="year">{{y}}</h3>
  {% bibliography -f evalpapers -q @*[year={{y}}]* %}
{% endfor %}

<h2 id="press">press</h2>

{% for y in page.pressyears %}
  <h3 class="year">{{y}}</h3>
  {% bibliography -f press -q @*[year={{y}}]* %}
{% endfor %}
