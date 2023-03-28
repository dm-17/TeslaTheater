---
title: Tesla Theater
layout: theater-front
bodyclass: front
---

<section class="theater-front">
<h1 class="mainpage">Theater apps</h1>
{% if site.data.theaters[0].name %}
  <div class="theater-grid">
    <div class="grid-container">
      {% assign theaters = site.data.theaters | sort: 'name' %}
      {% for theater in theaters %}
        {% if theater.display %}
        <div class="grid-item">
          <a href="https://{% if theater.redirect %}www.youtube.com/redirect?q={% endif %}{{theater.url}}"><img class="theatericons" src="assets/images/{{theater.image}}"></a></div>
        {% endif %}
      {% endfor %}
    </div>
  </div>
{% endif %}
<br>
<h1 class="mainpage">Navigation and recharge</h1>
{% if site.data.navapps[0].name %}
  <div class="theater-grid">
    <div class="grid-container">
      {% assign items = site.data.navapps | sort: 'prio' %}
      {% for item in items %}
        {% if item.display %}
        <div class="grid-item">
          <a href="https://{{item.url}}"><img class="theatericons" src="assets/images/{{item.image}}"></a></div>
        {% endif %}
      {% endfor %}
    </div>
  </div>
{% endif %}

</section>
