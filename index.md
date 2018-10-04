---
layout: default
---
{::options parse_block_html="true" /}
<h1 id="name-header"><a href="{{ site.url }}">{{ site.title }}</a></h1>

<section id="contact">
<img src="/assets/headshot.jpg" id="main-photo" />
## Contact
Email
:    [krzysd@cs.washington.edu](mailto:krzysd@cs.washington.edu)

Office
:    Allen Center (CSE) 324

Github
:    [krzysz00](https://github.com/krzysz00/)

CV
:    [pdf](/cv.pdf)

ORCID
:    [0000-0002-7054-1238](https://orcid.org/0000-0002-7054-1238)
</section>

<section id="about">
## About me
I'm a PhD student and I'll be writing this in a bit.
</section>

{::options parse_block_html="false" /}
<section id="news">
<h2>News</h2>
{% for post in site.posts %}
<div class="news-item">
<span class="date"> {{ post.date | date: "%Y-%m-%d" }} </span>
<div class="content"> {{ post.content }}</div>
</div>
{% endfor %}
</section>

<section id="papers">
<h2>Papers</h2>
{% assign bibs-newest-first = site.bib | reverse %}
{% for paper in bibs-newest-first %}
  {% include paper.html paper=paper %}
{% endfor %}
</section>
