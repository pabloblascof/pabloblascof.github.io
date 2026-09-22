---
layout: modern
title: "Publications"
permalink: /publications/
description: "Publications by Pablo Blasco Fernandez on medical image analysis, diffusion models, and AI for healthcare."
---

<header class="page-head">
  <h1>Publications</h1>
  <p class="muted">An up-to-date list is always on <a href="{{ site.author.googlescholar }}"><i class="ai ai-google-scholar"></i> Google Scholar</a>. <span class="me-key">Highlighted</span> = me.</p>
</header>

{% assign by_year = site.data.publications | group_by: "year" | sort: "name" | reverse %}
{% for group in by_year %}
<section class="section section--tight">
  <h2 class="year">{{ group.name }}</h2>
  <ol class="pubs">
    {% for pub in group.items %}{% include pub-item.html pub=pub %}{% endfor %}
  </ol>
</section>
{% endfor %}
