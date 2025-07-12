---
layout: archive
title: "Sitemap"
permalink: /sitemap/
author_profile: true
---

{% include base_path %}

<style>
.sitemap-container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 2rem;
  margin-left: 0;
  width: 100%;
}

.sitemap-column {
  min-height: 0;
}

.sitemap-section h2 {
  margin-top: 1.5rem;
  margin-bottom: 1rem;
  font-size: 1.2rem;
  border-bottom: 2px solid #3498db;
  padding-bottom: 0.5rem;
}

@media (max-width: 768px) {
  .sitemap-container {
    grid-template-columns: 1fr;
    gap: 1rem;
  }
}
</style>

<p>A list of all the posts and pages found on the site. For you robots out there, there is an [XML version]({{ base_path }}/sitemap.xml) available for digesting as well.</p>

<div class="sitemap-container">
  <div class="sitemap-column">
    <div class="sitemap-section">
      <h2>Pages</h2>
      {% for post in site.pages %}
        {% include archive-single.html %}
      {% endfor %}
    </div>

    <div class="sitemap-section">
      <h2>Posts</h2>
      {% for post in site.posts %}
        {% include archive-single.html %}
      {% endfor %}
    </div>
  </div>

  <div class="sitemap-column">
    {% capture written_label %}'None'{% endcapture %}
    {% for collection in site.collections %}
    {% unless collection.output == false or collection.label == "posts" %}
      {% capture label %}{{ collection.label }}{% endcapture %}
      {% if label != written_label %}
        <div class="sitemap-section">
          <h2>{{ label | capitalize }}</h2>
          {% capture written_label %}{{ label }}{% endcapture %}
          {% for post in collection.docs %}
            {% unless collection.output == false or collection.label == "posts" %}
            {% include archive-single.html %}
            {% endunless %}
          {% endfor %}
        </div>
      {% endif %}
    {% endunless %}
    {% endfor %}
  </div>
</div>
