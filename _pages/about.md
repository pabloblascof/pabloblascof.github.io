---
layout: modern
permalink: /
title: ""
description: "Pablo Blasco Fernandez is a PhD student in EECS at MIT working on AI for healthcare, medical image analysis, and robust machine learning."
redirect_from:
  - /about/
  - /about.html
---

<section class="hero">
  <img class="hero__photo" src="{{ '/images/' | append: site.author.avatar | relative_url }}" alt="Portrait of Pablo Blasco Fernandez" width="180" height="180">
  <div class="hero__text">
    <p class="eyebrow">PhD Student · MIT EECS</p>
    <h1 class="hero__name">{{ site.author.name }}</h1>
    <p class="hero__tagline">I build AI for medical imaging that holds up in real clinics, where data shifts, labels disagree, and robustness matters.</p>
    <div class="hero__links">
      <a class="btn btn--primary" href="{{ site.author.cv | relative_url }}"><i class="fa-solid fa-file-arrow-down"></i> CV</a>
      <a class="btn" href="mailto:{{ site.author.email }}"><i class="fa-solid fa-envelope"></i> Email</a>
      <a class="btn" href="{{ site.author.googlescholar }}"><i class="ai ai-google-scholar"></i> Scholar</a>
      <a class="btn" href="https://github.com/{{ site.author.github }}"><i class="fa-brands fa-github"></i> GitHub</a>
      <a class="btn" href="https://www.linkedin.com/in/{{ site.author.linkedin }}"><i class="fa-brands fa-linkedin"></i> LinkedIn</a>
    </div>
  </div>
</section>

<section class="section prose" markdown="1">

I'm a PhD student in **Electrical Engineering and Computer Science at [MIT](https://www.eecs.mit.edu/)**, advised by [Prof. Regina Barzilay](https://www.rbg.mit.edu/). I work on AI for healthcare and medical image analysis, focusing on **distribution shift, robustness, and clinical deployment**.

Before MIT, I earned an MSc in Biomedical Engineering from **ETH Zurich** as a ['la Caixa' Fellow](https://becarios.fundacionlacaixa.org/es/pablo-blasco-fernandez-B005814), and a BSc in Biomedical Engineering from **Universidad Carlos III de Madrid** (top 2%). My research has taken me across academia, hospitals, and industry:

- tuberculosis screening from chest X-rays with the Sri Lanka Ministry of Health at **MIT**
- ulcerative colitis endoscopy models at **Roche**
- cardiac digital twins at **Harvard Medical School & Brigham and Women's Hospital**
- cortical parcellation at the **Martinos Center**
- diffusion models for cardiac signals at **ETH Zurich**

</section>

<section class="section">
  <h2 class="section__title">Research interests</h2>
  <div class="cards">
    <div class="card">
      <i class="fa-solid fa-shield-halved card__icon" aria-hidden="true"></i>
      <h3>Robust &amp; trustworthy ML</h3>
      <p>Out-of-distribution detection, distribution shift, and uncertainty for models that meet unseen hospitals and populations.</p>
    </div>
    <div class="card">
      <i class="fa-solid fa-x-ray card__icon" aria-hidden="true"></i>
      <h3>Medical image analysis</h3>
      <p>Segmentation, classification, and shape modeling across X-ray, CT, MRI, endoscopy, and physiological signals.</p>
    </div>
    <div class="card">
      <i class="fa-solid fa-hospital card__icon" aria-hidden="true"></i>
      <h3>Clinical deployment</h3>
      <p>Working with clinicians on data curation, annotation reliability, and evaluation that reflects real clinical needs.</p>
    </div>
  </div>
</section>

<section class="section">
  <h2 class="section__title">News</h2>
  <ul class="news">
    {% for n in site.data.news limit: 6 %}
    <li><span class="news__date">{{ n.date }}</span><span class="news__text">{{ n.text | markdownify | remove: '<p>' | remove: '</p>' }}</span></li>
    {% endfor %}
  </ul>
  {% if site.data.news.size > 6 %}
  <details class="more">
    <summary>Older news</summary>
    <ul class="news">
      {% for n in site.data.news offset: 6 %}
      <li><span class="news__date">{{ n.date }}</span><span class="news__text">{{ n.text | markdownify | remove: '<p>' | remove: '</p>' }}</span></li>
      {% endfor %}
    </ul>
  </details>
  {% endif %}
</section>

<section class="section">
  <div class="section__head">
    <h2 class="section__title">Selected publications</h2>
    <a class="link-arrow" href="{{ '/publications/' | relative_url }}">All publications <i class="fa-solid fa-arrow-right"></i></a>
  </div>
  <ol class="pubs">
    {% for pub in site.data.publications %}{% if pub.selected %}{% include pub-item.html pub=pub %}{% endif %}{% endfor %}
  </ol>
</section>

<section class="section">
  <div class="section__head">
    <h2 class="section__title">Experience</h2>
    <a class="link-arrow" href="{{ '/cv/' | relative_url }}">Full CV <i class="fa-solid fa-arrow-right"></i></a>
  </div>
  {% include experience-list.html %}
</section>

<section class="section contact">
  <h2 class="section__title">Get in touch</h2>
  <p>I'm always happy to talk about research and collaborations. Email me at <a href="mailto:{{ site.author.email }}">{{ site.author.email }}</a> or connect on <a href="https://www.linkedin.com/in/{{ site.author.linkedin }}">LinkedIn</a>.</p>
</section>
