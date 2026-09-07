---
layout: default
title: Writing
description: "Articles by Dallin Nielson on measurement integrity, knowledge systems, KCS, and human-centered AI."
---

<div class="page-header">
  <div class="page-header-inner">
    <h1>Writing</h1>
    <p>Thinking out loud on knowledge systems, measurement, and the people side of AI.</p>
  </div>
</div>

<section class="page-section">

  <p class="section-intro">
    Most of what I write sits at the same intersection as my technical work: where AI meets
    real knowledge workflows, and where the human decisions around a system matter as much
    as the system itself.
  </p>

  <!-- ============================================================
       ARTICLES HOSTED HERE
       Pulled automatically from _posts/. Nothing to edit — a new
       article appears as soon as you commit it.
       ============================================================ -->
  {% if site.posts.size > 0 %}
  <div class="tag-filter" id="tag-filter">
    <button class="tag-chip is-active" data-tag="all" type="button">All</button>
    {% for tag in site.tags %}
    <button class="tag-chip" data-tag="{{ tag[0] | slugify }}" type="button">{{ tag[0] | replace: '-', ' ' }}</button>
    {% endfor %}
  </div>

  <div class="projects-list" id="article-list">
    {% for post in site.posts %}
    <article class="project-card article-card" data-tags="{% for tag in post.tags %}{{ tag | slugify }} {% endfor %}">
      <div class="project-card-header">
        <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
        <span class="project-label">
          <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %Y" }}</time>
        </span>
      </div>
      <p>{{ post.description | default: post.excerpt | strip_html | truncate: 280 }}</p>
      {% if post.tags.size > 0 %}
      <p class="article-tags">
        {% for tag in post.tags %}<span class="post-tag">{{ tag | replace: '-', ' ' }}</span>{% endfor %}
      </p>
      {% endif %}
    </article>
    {% endfor %}
  </div>

  <p class="no-results" id="no-results" hidden>No articles with that tag yet.</p>
  {% endif %}

  <!-- ============================================================
       PUBLISHED ELSEWHERE
       Edit _data/writing.yml to change this list.
       ============================================================ -->
  {% if site.data.writing.size > 0 %}
  <h2 class="elsewhere-heading">Published elsewhere</h2>
  <p class="section-lede">Earlier pieces that live on other platforms.</p>

  <div class="projects-list">
    {% for item in site.data.writing %}
    <a class="project-card" href="{{ item.url }}" target="_blank" rel="noopener">
      <div class="project-card-header">
        <h3>{{ item.title }}</h3>
        <span class="project-label">{{ item.platform }} &middot; {{ item.date }}</span>
      </div>
      <p>{{ item.summary }}</p>
    </a>
    {% endfor %}
  </div>
  {% endif %}

  <p class="feed-link">
    <a href="{{ '/feed.xml' | relative_url }}">Subscribe via RSS &rarr;</a>
  </p>

</section>

<script>
(function () {
  var filter = document.getElementById('tag-filter');
  if (!filter) return;
  var cards = Array.prototype.slice.call(document.querySelectorAll('#article-list .article-card'));
  var empty = document.getElementById('no-results');

  filter.addEventListener('click', function (e) {
    var btn = e.target.closest('.tag-chip');
    if (!btn) return;
    var tag = btn.getAttribute('data-tag');

    Array.prototype.forEach.call(filter.querySelectorAll('.tag-chip'), function (c) {
      c.classList.toggle('is-active', c === btn);
    });

    var shown = 0;
    cards.forEach(function (card) {
      var tags = ' ' + card.getAttribute('data-tags') + ' ';
      var match = tag === 'all' || tags.indexOf(' ' + tag + ' ') > -1;
      card.hidden = !match;
      if (match) shown++;
    });
    if (empty) empty.hidden = shown !== 0;
  });
})();
</script>
