---
layout: page
permalink: /research/
title: Research
pubs:

    - title:   "Adjoint-Matching Neural Network Surrogates for Fast 4D-Var Data Assimilation"
      author:  "A. Chennault, A. Popov, A. Subrahmanya, R. Cooper, A. Karpatne, A. Sandu"
      journal: "Virginia Tech"
      #note:    ""
      year:    "2021"
      url:     "http://hdl.handle.net/10919/108892"
      #doi:     ""
      #image:   ""
      #media:
      #  - name: ""
      #    url:  ""

    - title:   "Investigation of Nonlinear Model Order Reduction of the Quasigeostrophic Equations through a Physics-Informed Convolutional Autoencoder"
      author:  "R. Cooper, A. Popov, A. Sandu"
      journal: "Virginia Tech"
      #note:    ""
      year:    "2021"
      url:     "http://hdl.handle.net/10919/108894"
      #doi:     ""
      #image:   ""
      #media:
      #  - name: ""
      #    url:  ""

    - title:   "Augmented Neural Network Surrogate Models for Polynomial Chaos Expansions and Reduced Order Modeling"
      author:  "R. Cooper"
      journal: "Virginia Tech"
      note:    "Thesis"
      year:    "2021"
      url:     "http://hdl.handle.net/10919/103423"
      #doi:     ""
      #image:   ""
      #media:
      #  - name: ""
      #    url:  ""

    - title:   "Machine Learning applications in Uncertainty Quanitification"
      author:  "R. Cooper, A. Moosavi, A. Sandu, V. Rao"
      journal: "SIAM CSE Conference"
      note:    "Minisymposia talk"
      year:    "2019"
      url:     "http://meetings.siam.org/sess/dsp_talk.cfm?p=96948"
      #doi:     ""
      #image:   ""
      media:
        - name: "Presentation"
          url:  "https://www.pathlms.com/siam/courses/10878/sections/14353/video_presentations/127335"

curr:

    - title:   "ML Autotuning of CFD Simulation"
      author:  "R. Cooper, A. Sandu, D. Tafti, P. Windes"
      #note:    ""
      year:    "2017-2019"
      #image:   ""
---

I previously was a graduate student researcher within the [Computational Science Laboritory] at
Virginia Tech, focusing on machine learning applications within numeriacal
analysis and uncertainty quanitfication.

## Publications & Presentations

{% assign thumbnail="left" %}

{% for pub in page.pubs %}
{% if pub.image %}
{% include image.html url=pub.image caption="" height="100px" align=thumbnail %}
{% endif %}
[**{{pub.title}}**]({% if pub.internal %}{{pub.url | prepend: site.baseurl}}{% else %}{{pub.url}}{% endif %})<br />
{{pub.author}}<br />
*{{pub.journal}}*
{% if pub.note %} *({{pub.note}})*
{% endif %} *{{pub.year}}* {% if pub.doi %}[[doi]({{pub.doi}})]{% endif %}
{% if pub.media %}<br />Media: {% for article in pub.media %}[[{{article.name}}]({{article.url}})]{% endfor %}{% endif %}

{% endfor %}

## Projects

{% assign thumbnail="left" %}

{% for curr in page.curr %}
{% if curr.image %}
{% include image.html url=curr.image caption="" height="100px" align=thumbnail %}
{% endif %}
**{{curr.title}}**<br />
{{curr.author}}<br />
{% if curr.note %} *({{curr.note}})*
{% endif %} *{{curr.year}}*

{% endfor %}


[Computational Science Laboritory]: http://csl.cs.vt.edu