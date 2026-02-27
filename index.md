---
layout: default
title: Home
---

<div class="welcome-section">
  <h1>InSight</h1>
  <p class="welcome-subtitle">Stock &amp; News Analysis</p>
</div>

<div class="post-feed">
  {% for post in site.posts %}
  <div class="post-card-wrapper">
    <a class="post-card" href="{{ post.url | relative_url }}">
      <div class="pc-meta">
        <span class="pc-avatar">{{ post.author | default: site.author | slice: 0 | upcase }}</span>
        <span>{{ post.date | date: "%Y. %m. %d" }}</span>
        {% if post.categories and post.categories.size > 0 %}
        <span style="opacity:0.4;">·</span>
        <span>{{ post.categories | join: ", " }}</span>
        {% endif %}
      </div>
      <div class="pc-title">{{ post.title }}</div>
      {% if post.excerpt %}
      <div class="pc-excerpt">{{ post.excerpt | strip_html | truncatewords: 30 }}</div>
      {% endif %}
    </a>
    <button class="card-copy-btn" data-url="{{ post.url | relative_url }}" title="Copy content">
      {% include icons/copy.html %}
      {% include icons/check.html %}
    </button>
  </div>
  {% endfor %}
</div>

<script>
document.querySelectorAll('.card-copy-btn').forEach(function(btn) {
  btn.addEventListener('click', function(e) {
    e.preventDefault();
    e.stopPropagation();
    var url = this.dataset.url;
    var btnEl = this;
    fetch(url)
      .then(function(res) { return res.text(); })
      .then(function(html) {
        var parser = new DOMParser();
        var doc = parser.parseFromString(html, 'text/html');
        var content = doc.querySelector('.post-content');
        if (content) {
          var text = content.innerText || content.textContent;
          navigator.clipboard.writeText(text).then(function() {
            btnEl.classList.add('copied');
            setTimeout(function() { btnEl.classList.remove('copied'); }, 2000);
          });
        }
      });
  });
});
</script>
