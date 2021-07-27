---
title: "Mitra Lab - Publications"
layout: gridlay
excerpt: "Mitra Lab -- Publications."
sitemap: false
permalink: /publications/
---


# Publications

## Group highlights

(For a full list of publications and patents see [below](#full-list-of-publications) or go to [Google Scholar](https://scholar.google.ch/citations?user=1gRtTPkAAAAJ&hl=en))

{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ publi.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ publi.description }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p><strong><a href="../media/pub_pdf/{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p> {{ publi.news2 }}</p>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>


## Patents

Super agonists, Partial Agonists and Antagonists of Interleukin-2 <br /> Patent no: WO2015164815A1. <br /><em>Suman Mitra, co-inventor</em><br />

Methods of treating graft versus host disease with an IL-2 meutin <br /> US-10654905-B2.<br /><em>Suman Mitra, co-inventor</em><br />

Novel IL-10 agonists for application in immunotherapy <br /> PE960351(GB).<br /><em>Suman Mitra, co-inventor</em><br />

## Full List of publications

{% for publi in site.data.publist %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="../media/pub_pdf/{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}
