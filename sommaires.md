---
layout: default
title: Sommaires des magazines de l’école des lettres
type: website
permalink: sommaires/index.html
---

<div class="index">
{%- assign sommaires-group = site.sommaires | group_by: "annee" -%}
{%- for sommaire in sommaires-group reversed -%}
<div class="index--item">
<strong>Année {{ sommaire.name }}</strong>
{%- for item in sommaire.items -%}
<a class="tooltip" href="/pages{{ item.url }}.html">{{ item.numero }}<span>{{ item.title }}</span>  </a>
{%- endfor -%}
</div>
{%- endfor -%}
</div>

{%- assign sommaires = site.sommaires | sort: 'annee', 'first' -%}
{%- for sommaire in sommaires reversed -%}
{%- if forloop.index0 == 0 -%}
 <h1 class="summary-title">{{sommaire.title}}</h1>
 {{sommaire.content}}
 {%- endif -%}
{%- endfor -%}
