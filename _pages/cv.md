---
layout: modern
title: "CV"
permalink: /cv/
description: "Curriculum vitae of Pablo Blasco Fernandez: education, research experience, publications, and awards."
redirect_from:
  - /resume
---

<header class="page-head page-head--row">
  <div>
    <h1>Curriculum Vitae</h1>
    <p class="muted">A short version. The full CV is available as a PDF.</p>
  </div>
  <a class="btn btn--primary" href="{{ site.author.cv | relative_url }}"><i class="fa-solid fa-file-arrow-down"></i> Download PDF</a>
</header>

<section class="section">
  <h2 class="section__title">Education</h2>
  <ol class="timeline">
    {% for e in site.data.cv.education %}
    <li class="timeline__item">
      <div class="timeline__dates">{{ e.dates }}</div>
      <div class="timeline__body">
        <h3 class="timeline__role">{{ e.degree }} <span class="timeline__org">· {{ e.org }}</span></h3>
        {% for d in e.details %}<p>{{ d }}</p>{% endfor %}
      </div>
    </li>
    {% endfor %}
  </ol>
</section>

<section class="section">
  <h2 class="section__title">Research &amp; industry experience</h2>
  {% include experience-list.html detailed=true %}
</section>

<section class="section">
  <div class="section__head">
    <h2 class="section__title">Publications</h2>
    <a class="link-arrow" href="{{ '/publications/' | relative_url }}">Details <i class="fa-solid fa-arrow-right"></i></a>
  </div>
  <ol class="pubs">
    {% for pub in site.data.publications %}{% include pub-item.html pub=pub %}{% endfor %}
  </ol>
</section>

<section class="section">
  <h2 class="section__title">Awards &amp; honors</h2>
  <ul class="kv">
    {% for a in site.data.cv.awards %}<li><span class="kv__k">{{ a.year }}</span><span class="kv__v">{{ a.text }}</span></li>{% endfor %}
  </ul>
</section>

<div class="two-col">
  <section class="section">
    <h2 class="section__title">Service &amp; leadership</h2>
    <ul class="kv kv--stack">
      {% for s in site.data.cv.service %}<li><span class="kv__k">{{ s.dates }}</span><span class="kv__v">{{ s.text }}</span></li>{% endfor %}
    </ul>
  </section>
  <section class="section">
    <h2 class="section__title">Summer schools</h2>
    <ul class="plain">
      {% for s in site.data.cv.schools %}<li>{{ s }}</li>{% endfor %}
    </ul>
  </section>
</div>

<section class="section">
  <h2 class="section__title">Skills</h2>
  <ul class="kv">
    {% for s in site.data.cv.skills %}<li><span class="kv__k">{{ s.label }}</span><span class="kv__v">{{ s.text }}</span></li>{% endfor %}
  </ul>
</section>
