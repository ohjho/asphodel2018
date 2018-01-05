---
layout: page-fullwidth
title: "Coaches"
subheadline: "about our coaching staff"
teaser: "It is also interesting to notice that the health professional maintains your health with drugs and surgery, each with potentially undesirable side effects, whereas the CrossFit trainer typically achieves a superior result always with “side beneft” versus side effect."
header: no
---

{% assign div_count = 0 %}
{% for coach in site.data.coaches %}

  {% if coach.display %}

    {% assign div_count = div_count | plus: 1 %}

    {% capture modulo %}{{ div_count | mod:2 }}{% endcapture %}
    {% if modulo != '0' or forloop.first %}
<div class="row t60">
    {% endif %}

  <div class="medium-6 columns">
    <img src="{{site.urlimg}}{{coach.img_url}}" alt="{{coach.name}} profile picture">
    <h5>{{coach.name}}</h5>

    <p>{{coach.title}}<br>
      <a data-dropdown="drop{{div_count}}-bio" aria-controls="drop{{div_count}}-bio" aria-expanded="false">Bio</a> |
      <a data-dropdown="drop{{div_count}}-cert" aria-controls="drop{{div_count}}-cert" aria-expanded="false">Cert</a>
      </p>

    <div id="drop{{div_count}}-bio" data-dropdown-content class="f-dropdown content mega" aria-hidden="true" tabindex="-1">
      <p>{{coach.bio}}</p>
    </div><!-- dropdown-bio -->
    <div id="drop{{div_count}}-cert" data-dropdown-content class="f-dropdown content mega" aria-hidden="true" tabindex="-1">
      <p>{{coach.cert}}</p>
    </div><!-- dropdown-cert -->

  </div><!-- /.medium-6.columns -->

    {% if modulo == '0' or forloop.last %}
</div><!-- /.row -->
    {% endif %}

  {% endif %}
{% endfor %}
