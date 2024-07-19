---
permalink: /
title: "About Me"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---
# This is a template test for academic pages, the following informaiton is nothing about me

<!-- 
A data-driven personal website
====== -->

<!-- **I'm actively recruiting lab members**, so please send me your CV and a brief
description of your research interests if you'd like to be considered! -->

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