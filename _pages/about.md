---
permalink: /
title: "About Me"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---
# This is a template test for academic pages, the following informaiton is nothing about me

This is the front page of a website that is powered by the [Academic Pages template](https://github.com/academicpages/academicpages.github.io) and hosted on GitHub pages. [GitHub pages](https://pages.github.com) is a free service in which websites are built and hosted from code and data stored in a GitHub repository, automatically updating when a new commit is made to the respository. This template was forked from the [Minimal Mistakes Jekyll Theme](https://mmistakes.github.io/minimal-mistakes/) created by Michael Rose, and then extended to support the kinds of content that academics have: publications, talks, teaching, a portfolio, blog posts, and a dynamically-generated CV. You can fork [this repository](https://github.com/academicpages/academicpages.github.io) right now, modify the configuration and markdown files, add your own PDFs and other content, and have your own site for free, with no ads! An older version of this template powers my own personal website at [stuartgeiger.com](http://stuartgeiger.com), which uses [this Github repository](https://github.com/staeiou/staeiou.github.io).

A data-driven personal website
======
Like many other Jekyll-based GitHub Pages templates, Academic Pages makes you separate the website's content from its form. The content & metadata of your website are in structured markdown files, while various other files constitute the theme, specifying how to transform that content & metadata into HTML pages. You keep these various markdown (.md), YAML (.yml), HTML, and CSS files in a public GitHub repository. Each time you commit and push an update to the repository, the [GitHub pages](https://pages.github.com/) service creates static HTML pages based on these files, which are hosted on GitHub's servers free of charge.

As a cognitive scientist and data scientist, I take a **data-rich approach** to
understanding **how people collaborate, bond, and fight**. To do that, I
weave together a **variety of data sources from the lab and the real world**
for a converging tapestry of the many ways in which our language, movement,
decisions, and emotions change during social contact. Understanding how
context---including conversational goals, social connections, and physical
spaces---shape our emerging behaviors is a primary goal of my research, embedded
within **rich traditions of dynamical and ecological perspectives** on human
behavior and cognition broadly.

I also **develop methods** to quantify social interaction,
promote **open science** research and education, and
create opportunities for cognitive scientists and psychologists who are
interested in **data science, naturally occurring data, and big data**,
with a special focus on **data ethics**.

**I'm actively recruiting lab members**, so please send me your CV and a brief
description of your research interests if you'd like to be considered!

## About me

I'm an assistant professor in the
[University of Connecticut](https://uconn.edu/)’s
[Department of Psychological Sciences](https://psych.uconn.edu/), specifically
 within the
[Perception, Action, Cognition division](https://psych.uconn.edu/perception-action-cognition-division/).
I am affiliated with
the [Center for the Ecological Study of Perception and Action](https://cespa.uconn.edu/);
the [Institute for Collaboration on Health, Intervention, and Policy](https://chip.uconn.edu/);
the [Connecticut Institute for the Brain and Cognitive Sciences](https://ibacs.uconn.edu/);
and the [Cognitive Science program](https://cogsci.uconn.edu/).
I am also a faculty mentor in the
[Science of Learning and Art of Communication](https://slac.uconn.edu/)
training program.

I have also created [a set of Jupyter notebooks](https://github.com/academicpages/academicpages.github.io/tree/master/markdown_generator
) that converts a CSV containing structured data about talks or presentations into individual markdown files that will be properly formatted for the Academic Pages template. The sample CSVs in that directory are the ones I used to create my own personal website at stuartgeiger.com. My usual workflow is that I keep a spreadsheet of my publications and talks, then run the code in these notebooks to generate the markdown files, then commit and push them to the GitHub repository.

Previously, I was a postdoctoral scholar working with
[Tom Griffiths](http://cocosci.princeton.edu/tom/index.php) in the
[Institute of Cognitive and Brain Sciences](http://icbs.berkeley.edu/)
at the [University of California, Berkeley](http://www.berkeley.edu/)
and a [Moore-Sloan Data Science Fellow](http://msdse.org/)
at the [Berkeley Institute for Data Science](http://bids.berkeley.edu/). I
received my Ph.D in
[Cognitive and Information Sciences](http://cogsci.ucmerced.edu/) working with
[Rick Dale](http://co-mind.org/rick/) at the
[University of California, Merced](https://www.ucmerced.edu/).

## Some recent work

{% for post in site.recent %}
  {% include archive-recent.html %}
{% endfor %}