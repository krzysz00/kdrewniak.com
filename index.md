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


Resume
:   [pdf](/resume.pdf)

CV
:    [pdf](/cv.pdf)

PGP
:    [837E 880C 11FF 99D9 F0C0  9BA1 2A14 2308 2388 E924](/pubkey.asc)
</section>

<section id="about">
## About me
I'm currently looking for a full-time software engineering position.
My recent experience, detailed below, has been in using program synthesis to generate programs for high-performance accelerators, and I have experience with high-performance numerical code (and the underlying architectural requirements, though much of my earli experience focused on CPUs) and program synthesis.
However, I've also had experience in other areas of the field, such as contributing to production distributed systems.

I'm open to and capable of expanding my skillset.
I'm most actively searching for positions that focus on high-performance computing, program synthesis/compilers, or developer tooling and infrastructure.
However, I'd be quite happy to take positions that focus on any aspect of systems programming, infrastructure, developer productivity, and, in general, backend, among other similar areas.

I've been a PhD student  at the University of Washington Paul G. Allen School of Computer Science & Engineering for three years, and am leaving the program indefinitely to find a more applied role and gain more real-world experience.
I worked in the [Programming Languages and Software Engineering][plse] group, and am advised by [Rastislav Bodik][ras]. My research focus is on using program synthesis to improve the performance of numerical computations, such as matrix multiplication and convolution, that are used in machine learning and scientific computing.

I have developed a new synthesis technique for fixed-sized mathematical operators on accelerators (such as GPUs) that reduces the problem to synthesis over functional array programs and uses an abstract reachability analysis to quickly prune most incorrect partial candidates.
This has the added advantage of reducing a large amount of the computation to Boolean matrix multiplication, enabling synthesis over larger spaces of functions as compared to previous work.
In the future, this work will be integrated into a larger framework for synthesizing efficient code for machine learning models on accelerators.

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

(ORCID: [0000-0002-7054-1238](https://orcid.org/0000-0002-7054-1238))
</section>
