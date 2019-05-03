---
layout: default
---
{::options parse_block_html="true" /}
<h1 id="name-header"><a href="{{ site.url }}">{{ site.title }}</a></h1>

<section id="contact">
<img src="/assets/headshot.jpg" id="main-photo" alt="A photo of me" />
## Contact
Email
:    [krzysd@cs.washington.edu](mailto:krzysd@cs.washington.edu)

Office
:    Gates Center (CSE2) 279

Github
:    [krzysz00](https://github.com/krzysz00/)

CV
:    [pdf](/cv.pdf)

ORCID
:    [0000-0002-7054-1238](https://orcid.org/0000-0002-7054-1238)

PGP
:    [837E 880C 11FF 99D9 F0C0  9BA1 2A14 2308 2388 E924](/pubkey.asc)
</section>

<section id="about">
## About me
I'm a first-year PhD student at the University of Washington Paul G. Allen School of Computer Science & Engineering.
I work in the [Programming Languages and Software Engineering][plse] group, and am advised by [Rastislav Bodik][ras].

My overall research focus is on using program synthesis to improve low-level performance, especially of numerical code and programs used in high-performance computing.
Currently, I'm developing abstract dynamic programming, a new synthesis technique that can be used to accelerate enumerative searches through a space of programs, and applying it to the problem of automatically filling in the details of numeric kernels on GPUs and other similar hardware.

[plse]:  http://uwplse.org
[ras]: https://homes.cs.washington.edu/~bodik/
</section>

{::options parse_block_html="false" /}
<section id="news">
<h2>News</h2>
{% for post in site.posts %}
<div class="news-item">
<span class="date"> {{ post.date | date: "%Y-%m-%d" }} </span>
<span class="content"> {{ post.content | remove: "<p>" | remove: "</p>" }}</span>
</div>
{% endfor %}
</section>

<section id="papers">
<h2>Papers</h2>
{%- assign bibs-newest-first = site.bib | reverse -%}
{% for paper in bibs-newest-first %}
  {% include paper.html paper=paper %}
{% endfor %}
</section>
