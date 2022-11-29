---
layout: default
---
Welcome to Andrew Valentine's home page!

I am currently an Assistant Professor in the [Department of Earth Sciences](https://www.durham.ac.uk/departments/academic/earth-sciences/), [Durham University](https://www.durham.ac.uk). You can view my CV [here]({{ site.home }}/cv.html).

My research focusses primarily on the mathematical and statistical tools that allow us to extract information from observational data: inverse theory, inference, machine learning and data science. My background lies in geophysics and global seismology, but I work on a wide range of different geoscience questions. Read more about my research [here]({{ site.home }}/research.html), or browse and read my papers [here]({{ site.home }}/publications.html).

---

Some posts about things that don't fit elsewhere:
<ul>
  {% for post in site.posts limit:5 %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a> <small>{{ post.date | date: "%-d %B %Y" }}</small>
    </li>
  {% endfor %}
</ul>
See [the archive]({{ site.home }}/archive.html) for a full listing.