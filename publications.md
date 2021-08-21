---
layout: page
title: Publications
---
My Google Scholar profile can be found [here](https://scholar.google.co.uk/citations?user=TiVeAN8AAAAJ) and my ORCID is [0000-0001-6134-9351](https://orcid.org/0000-0001-6134-9351). Please [contact me](mailto:andrew.valentine@durham.ac.uk) if you encounter difficulties in accessing any of my papers.

<ol reversed>
{%- for _p in site.data.publications.papers -%}
  <li> {{ _p.authors}}, {{ _p.year }}.<br />{{ _p.title }}.<br />
  {%- if _p.journal or _p.volume or _p.pages -%}
  <i>{{ _p.journal }}</i>{%- if _p.volume -%}, {{ _p.volume }}{%- endif -%}{%- if _p.pages -%}, pp.{{ _p.pages }}{%- endif -%}. {%- if _p.doi -%} &nbsp;doi:<a href="https://dx.doi.org/{{ _p.doi }}">{{ _p.doi }}</a>{%- endif -%} <br />
  {%- endif -%}
  {%- if _p.booktitle -%}
  in{%- if _p.editors -%}&nbsp;{{ _p.editors }} (eds.),{%- endif -%}&nbsp;<i>{{ _p.booktitle }}</i>, {{ _p.publisher }}. {%- if _p.doi -%} &nbsp;doi:<a href="https://dx.doi.org/{{ _p.doi }}">{{ _p.doi }}</a>{%- endif -%}<br />
  {%- endif -%}
  {%- if _p.repository or _p.pdf or _p.supplement or _p.preprint or _p.info or _p.dataset -%}
  {%- if _p.pdf -%}
    <a href="{{ site.baseurl }}/files/{{ _p.pdf }}"><i class="fas fa-file-pdf"></i> Paper</a>&nbsp;&nbsp;
  {%- endif -%}
  {%- if _p.supplement -%}
    <a href="{{ site.baseurl }}/files/{{ _p.supplement }}"><i class="fas fa-file-contract"></i> Supplement</a>&nbsp;&nbsp;
  {%- endif -%}
  {%- if _p.preprint -%}
    <a href="{{ _p.preprint }}"><i class="fas fa-book-reader"></i> Preprint</a>&nbsp;&nbsp;
  {%- endif -%}
  {%- if _p.dataset -%}
    <a href="{{ _p.dataset }}"><i class="fas fa-database"></i> Dataset</a>&nbsp;&nbsp;
  {%- endif -%}
  {%- if _p.repository -%}
    <a href="{{ _p.repository }}"><i class="fab fa-github"></i> Code</a>&nbsp;&nbsp;
  {%- endif -%}
  {%- if _p.info -%}
    <a href="{{ _p.info }}"><i class="fas fa-angle-double-right"></i> More...</a>&nbsp;&nbsp;
  {%- endif -%}
  <br />
  {%- endif -%}
  <br /></li>
{%- endfor -%}
</ol>
