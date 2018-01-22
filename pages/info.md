---
layout: page
title: "Packages and Pricing"
subheadline: "How does our membership work?"
teaser: "refer a friend and get one free week" #"you are not only joining a gym, you are joining a family"
permalink: "/info/"
header:
    image_fullwidth: "headers/packages1.jpg"
    caption: ""
---

{% assign div_count = 0 %}
{% for section in site.data.packages %}
## {{section.name}}
{%if section.description %}{{section.description}}{% endif %}

<table>
  <thead><tr>
  <th id="cat">Categories</th>
  <th>Price</th>
  {% if section.show_mindbody %}<th> <i class="fa fa-shopping-cart fa-lg"></i> </th>{% endif %}
  </tr></thead>
  <tbody>
  {% for item in section.table %}
    <tr>
      <td>
        {% if item.notes %} {% assign div_count = div_count | plus: 1 %}
        <a data-options="align:left" data-dropdown="drop-{{div_count}}" aria-controls="drop-{{div_count}}" aria-expanded="false">{% endif %}
        {{item.category}}
        {% if item.notes %}</a>
        <div id="drop-{{div_count}}" data-dropdown-content class="f-dropdown content medium" aria-hidden="true">
          <p>{{item.notes}}</p>
        </div><!-- dropdown-note -->
        {% endif %}
        </td>
      <td>{{item.price}}</td>
      {% if section.show_mindbody %}
        {% if item.service_id %}
          {% capture serviceid %}{{item.service_id}}{% endcapture %}
      <td> {% include healcode text='Add to Cart' s_id=serviceid  %}</td>
        {% else %}
      <td> Ask Us </td>
        {% endif %}
      {% endif %}
    </tr>
  {% endfor %}
  </tbody>
</table>
{% endfor %}


### All payments must be settled prior to joining classes.
