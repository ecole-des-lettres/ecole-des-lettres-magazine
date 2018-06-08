---
layout: default
title: Zoom sur
type: website
permalink: zoomsur/index.html
---

<h2>Accéder aux articles</h2>

{%- if site.zoomsur -%}
{%- for zoomsur in site.zoomsur -%}
<section>
<h3><a href="/pages{{ zoomsur.url }}.html">{{ zoomsur.title }}</a></h3>
{{ zoomsur.content }}
</section>
{%- else -%}
<p>Aucun article n'est disponible pour le moment.</p>
{%- endfor -%}
{%- endif -%}
