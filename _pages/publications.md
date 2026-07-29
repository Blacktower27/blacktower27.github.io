---
title: "Publications"
permalink: /publications/
description: "Publications by Jingxi Lu in robotics, safe learning, vision-language model inference, and learning-based optimization."
---

<div class="page-shell">
  <header class="page-hero">
    <p class="eyebrow">Publications</p>
    <h1>Research across robotics, learning, and systems.</h1>
    <p>
      Publications and preprints in safe robot autonomy, bipedal navigation,
      efficient multimodal inference, and learning-assisted optimization.
      An asterisk denotes equal contribution.
    </p>
    <div class="button-row">
      <a class="portfolio-button portfolio-button--primary" href="https://scholar.google.com/citations?hl=en&amp;user=UbDB6c4AAAAJ">Google Scholar</a>
      <a class="portfolio-button" href="https://www.semanticscholar.org/author/Jingxi-Lu/2379791176">Semantic Scholar</a>
      <a class="portfolio-button" href="https://openreview.net/profile?id=~Jingxi_Lu1">OpenReview</a>
    </div>
  </header>

  {% assign publication_groups = site.publications | group_by: "year" | sort: "name" | reverse %}
  {% for group in publication_groups %}
    <section class="publication-year-group" aria-labelledby="year-{{ group.name }}">
      <h2 id="year-{{ group.name }}">{{ group.name }}</h2>
      <div>
        {% assign year_publications = group.items | sort: "order" %}
        {% for post in year_publications %}
          <article class="publication-item">
            <p class="publication-meta">{{ post.status }}{% if post.selected %} · Selected publication{% endif %}</p>
            <h3>{{ post.title }}</h3>
            <p class="authors">{{ post.authors }}</p>
            <p class="venue">{{ post.venue }}</p>
            {% if post.excerpt %}<p class="excerpt">{{ post.excerpt }}</p>{% endif %}
            <div class="button-row">
              {% if post.projecturl %}<a class="portfolio-button" href="{{ post.projecturl }}">Project</a>{% endif %}
              {% if post.paperurl %}<a class="portfolio-button" href="{{ post.paperurl }}">Paper</a>{% endif %}
              {% if post.doiurl %}<a class="portfolio-button" href="{{ post.doiurl }}">DOI</a>{% endif %}
              {% if post.codeurl %}<a class="portfolio-button" href="{{ post.codeurl }}">Code</a>{% endif %}
              {% if post.videourl %}<a class="portfolio-button" href="{{ post.videourl }}">Video</a>{% endif %}
            </div>
          </article>
        {% endfor %}
      </div>
    </section>
  {% endfor %}
</div>
