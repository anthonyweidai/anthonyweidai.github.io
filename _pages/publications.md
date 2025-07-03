---
layout: archive
title: "Selected Publications"
permalink: /publications/
author_profile: true
---

{% if site.author.googlescholar %}
  <div class="wordwrap">My complete list of publications can be found on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</div>
{% endif %}

Mentees’ names were underlined. Asterisk indicates dual first-author position.
Open access articles or preprints (<i class="ai ai-fw ai-open-access-square"></i>)
are linked below; all other PDFs (<i class="fa fa-file-pdf-o" aria-hidden="true">
</i>) are provided for **personal use only.** Supplementary materials on GitHub
(<i class="fab fa-github"></i>) and OSF
(<i class="ai ai-fw ai-osf"></i>) for each publication are linked below the citation.

Peer-reviewed Journals
======

{% for post in site.journals reversed %}
  {% include archive-single-publications.html %}
{% endfor %}

Refereed Conference Proceedings
======
{% for post in site.proceedings reversed %}
  {% include archive-single-publications.html %}
{% endfor %}
