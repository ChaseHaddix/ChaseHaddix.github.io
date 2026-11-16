---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% include base_path %}

<style>
/* Publications page only: companion to the Media page card design. */
.publications-page .pub-card {
  display: flex;
  align-items: flex-start;
  gap: 1.35rem;
  padding: 1.35rem 0;
  border-bottom: 1px solid #e2e8f0;
}
.publications-page .pub-logo {
  flex: 0 0 120px;
  width: 120px;
  height: 100px;
  box-sizing: border-box;
  padding: 12px;
  border: 1px solid #e2e8f0;
  border-radius: 8px;
  background: #fff;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 5px;
  text-align: center;
}
.publications-page .pub-logo img {
  display: block;
  width: auto;
  height: auto;
  max-width: 72px;
  max-height: 54px;
  object-fit: contain;
}
.publications-page .pub-logo-label {
  color: #243b53;
  font-size: .71rem;
  font-weight: 700;
  line-height: 1.15;
  overflow-wrap: anywhere;
}
.publications-page .pub-details { min-width: 0; flex: 1; }
.publications-page .pub-venue {
  margin: 0 0 .35rem;
  color: #52687a;
  font-size: .79rem;
  font-weight: 700;
  letter-spacing: .02em;
}
.publications-page .pub-title {
  color: #243b53;
  font-size: 1.12rem;
  line-height: 1.35;
  margin: 0 0 .45rem;
  padding: 0;
  border: 0;
  font-weight: 700;
}
.publications-page .pub-title a { color: inherit; text-decoration: none; }
.publications-page .pub-title a:hover { color: #2563a6; text-decoration: underline; }
.publications-page .pub-date { color: #637283; font-size: .87rem; margin: 0 0 .7rem; }
.publications-page .pub-summary { line-height: 1.6; margin-bottom: .8rem; }
.publications-page .pub-summary p { margin: 0 0 .5rem; }
.publications-page .pub-citation { font-size: .9rem; line-height: 1.5; margin: 0; }
.publications-page .pub-citation a { overflow-wrap: anywhere; }
@media (max-width: 540px) {
  .publications-page .pub-card { gap: .85rem; }
  .publications-page .pub-logo { flex-basis: 78px; width: 78px; height: 78px; padding: 6px; }
  .publications-page .pub-logo img { max-width: 49px; max-height: 38px; }
  .publications-page .pub-logo-label { font-size: .59rem; }
  .publications-page .pub-title { font-size: 1rem; }
}
</style>

<div class="publications-page">
{% if author.googlescholar %}
  <p>You can also find my articles on <a href="{{ author.googlescholar }}">my Google Scholar profile</a>.</p>
{% endif %}

{% for post in site.publications reversed %}
  {% assign logo_domain = '' %}
  {% assign logo_label = '' %}
  {% assign venue_downcase = post.venue | downcase %}
  {% if venue_downcase contains 'npj microgravity' %}
    {% assign logo_domain = 'nature.com' %}
    {% assign logo_label = 'npj Microgravity' %}
  {% elsif venue_downcase contains 'nasa technical memorandum' %}
    {% assign logo_label = 'NASA' %}
  {% elsif venue_downcase contains 'biomedical physics' %}
    {% assign logo_domain = 'iopscience.iop.org' %}
    {% assign logo_label = 'IOP Publishing' %}
  {% elsif venue_downcase contains 'journal of neural engineering' %}
    {% assign logo_domain = 'iopscience.iop.org' %}
    {% assign logo_label = 'IOP Publishing' %}
  {% elsif venue_downcase contains 'neurosurgery' %}
    {% assign logo_domain = 'wolterskluwer.com' %}
    {% assign logo_label = 'Neurosurgery' %}
  {% elsif venue_downcase contains 'university of kentucky' %}
    {% assign logo_label = 'University of Kentucky' %}
  {% elsif venue_downcase contains 'ieee' %}
    {% assign logo_domain = 'ieee.org' %}
    {% assign logo_label = 'IEEE' %}
  {% elsif venue_downcase contains 'non-integer order calculus' %}
    {% assign logo_domain = 'springer.com' %}
    {% assign logo_label = 'Springer' %}
  {% elsif venue_downcase contains 'disability and rehabilitation' %}
    {% assign logo_domain = 'tandfonline.com' %}
    {% assign logo_label = 'Taylor & Francis' %}
  {% else %}
    {% assign logo_label = 'Research' %}
  {% endif %}

  <article class="pub-card">
    <div class="pub-logo" aria-label="{{ logo_label | escape }} publisher identification">
      {% if logo_label == 'NASA' %}
        <img src="https://commons.wikimedia.org/wiki/Special:FilePath/NASA_logo.svg" alt="NASA logo" loading="lazy" onerror="this.style.display='none'">
      {% elsif logo_domain != '' %}
        <img src="https://www.google.com/s2/favicons?domain={{ logo_domain }}&amp;sz=128" alt="{{ logo_label | escape }} publisher icon" loading="lazy" onerror="this.style.display='none'">
      {% endif %}
      <span class="pub-logo-label">{{ logo_label }}</span>
    </div>
    <div class="pub-details">
      <p class="pub-venue">{{ post.venue }}</p>
      <h2 class="pub-title">
        {% if post.link %}
          <a href="{{ post.link }}">{{ post.title }}</a>
        {% else %}
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        {% endif %}
      </h2>
      <p class="pub-date">{{ post.date | default: '1900-01-01' | date: '%Y' }}</p>
      {% if post.excerpt %}
        <div class="pub-summary">{{ post.excerpt | markdownify }}</div>
      {% endif %}
      {% if post.citation or post.paperurl %}
        <p class="pub-citation">
          {% if post.citation %}<strong>Recommended citation:</strong> {{ post.citation }}{% endif %}
          {% if post.paperurl %}<a href="{{ post.paperurl }}">{{ post.paperurl }}</a>{% endif %}
        </p>
      {% endif %}
    </div>
  </article>
{% endfor %}
</div>
