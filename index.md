---
layout: default
---
{::options parse_block_html="true" /}
<h1 id="name-header"><a href="{{ site.url }}">{{ site.title }}</a></h1>

<section id="contact">
<img src="/assets/headshot.jpg" id="main-photo" alt="A photo of me" />
## Contact
Email
:    [krzysdrewniak@gmail.com](mailto:krzysdrewniak@gmail.com)

Work Email
:    [Krzysztof.Drewniak@amd.com](mailto:Krzysztof.Drewniak@amd.com)

Github
:    [krzysz00](https://github.com/krzysz00/)

Resume
:   [pdf](/resume.pdf)
<!---
CV
:    [pdf](/cv.pdf)
-->
PGP
:    [837E 880C 11FF 99D9 F0C0  9BA1 2A14 2308 2388 E924](/pubkey.asc)

Ham radio
:    KF5SOQ
</section>

<section id="about">
## About me
I am a senior engineer on the machine learning compiler team at AMD.
There, I contribute to [rocMLIR, a MLIR-based generator for high performance machine lerning kernels.](https://github.com/ROCmSoftwarePlatform/llvm-project-mlir).
I have taken the lead on improvements throughout the project, including refactroing, new hardware bringup, and contributing back to the upstream MLIR projects.
I've also branched out up and down the stack, handling both improvements to buffer resource support in the AMDGPU LLVM backend and, most recently (July 2023) the team's integration with MIGraphX.

I'm not looking for work right now and **do not want to hear from recruiters**.

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

Also listed at ORCID [0000-0002-7054-1238](https://orcid.org/0000-0002-7054-1238)
</section>
