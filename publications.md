---
layout: page
title: Publications
---
My Google Scholar profile can be found [here](https://scholar.google.co.uk/citations?user=TiVeAN8AAAAJ) and my ORCID is [0000-0001-6134-9351](https://orcid.org/0000-0001-6134-9351). Please [contact me](mailto:andrew.valentine@durham.ac.uk) to request a copy of any of my papers.

<ol reversed>
{%- for _p in site.data.publications.papers -%}
  <li> {{ _p.authors}}, {{ _p.year }}.<br />{{ _p.title }}.<br /><i>{{ _p.journal }}</i>, {{ _p.volume }}{%- if _p.pages -%}, pp.{{ _p.pages }}{%- endif -%}. doi:<a href="https://dx.doi.org/{{ _p.doi }}">{{ _p.doi }}</a> <br /><br /></li>
{%- endfor -%}
</ol>
