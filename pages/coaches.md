---
layout: page-fullwidth
title: "Coaches"
subheadline: "about our coaching staff"
teaser: "It is also interesting to notice that the health professional maintains your health with drugs and surgery, each with potentially undesirable side effects, whereas the CrossFit trainer typically achieves a superior result always with “side beneft” versus side effect."
header: no
---

{% assign div_count = 0 %}
{% for coach in site.data.coaches %}
  {% capture modulo %}{{ div_count | mod:3 }}{% endcapture %}
  {% if modulo == '0' or forloop.first %}
<div class="row t30">
  {% endif %}

  {% if coach.display %}
    {% assign div_count = div_count | plus: 1 %}
  <div class="medium-4 columns">
    <img src="{{site.urlimg}}{{coach.img_url}}" alt="{{coach.name}} profile picture">
    <h5><a data-dropdown="drop{{div_count}}" aria-controls="drop{{div_count}}" aria-expanded="false">
      {{coach.name}}</a></h5>
    <p>{{coach.title}}</p>
    <div id="drop{{div_count}}" data-dropdown-content class="f-dropdown content" aria-hidden="true" tabindex="-1">
      <p>{{coach.bio}}</p>
    </div><!-- dropdown -->
  </div><!-- /.medium-4.columns -->
  {% endif %}

  {% capture modulo %}{{ div_count | mod:3 }}{% endcapture %}
  {% if modulo == '0' or forloop.last %}
</div><!-- /.row -->
  {% endif %}
{% endfor %}
