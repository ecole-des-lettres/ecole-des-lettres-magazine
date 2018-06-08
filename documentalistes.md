---
layout: default
title: Professeurs documentalistes
type: website
permalink: documentalistes/index.html
---

<h2>Accéder aux articles</h2>

{%- if site.documentalistes -%}
{%- for documentaliste in site.documentalistes -%}
<section>
<h3><a href="/pages{{ documentaliste.url }}.html">{{ documentaliste.title }}</a></h3>
{{ documentaliste.content }}
</section>
{%- else -%}
<p>Aucun article n'est disponible pour le moment.</p>
{%- endfor -%}
{%- endif -%}
