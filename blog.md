---
layout: default
title: "Frank's Footprints"
permalink: /blog/
---

<style>
.blog-list{display:grid;grid-template-columns:1fr;gap:1.6rem;max-width:52em}
.blog-card{border:1px solid var(--edge);background:rgba(255,255,255,.02);display:grid;grid-template-columns:1fr;overflow:hidden;transition:border-color .25s ease}
.blog-card:hover{border-color:var(--red)}
.blog-card.has-image{grid-template-columns:160px 1fr}
.blog-thumb-link{display:block;overflow:hidden}
.blog-thumb{display:block;width:160px;height:100%;min-height:160px;object-fit:cover;border-right:1px solid var(--edge)}
.blog-card-body{padding:1.5rem 1.8rem}
.blog-card-meta{font-family:'Bebas Neue',sans-serif;letter-spacing:.18em;font-size:.78rem;color:var(--red);margin-bottom:.7rem;display:flex;align-items:center;gap:.5rem;flex-wrap:wrap}
.blog-card-loc{color:var(--fg3)}
.blog-card-loc::before{content:'·';color:var(--fg3);margin-right:.4rem}
.blog-card-title{font-family:'Fraunces',serif;font-weight:600;font-size:clamp(1.3rem,2.2vw,1.65rem);line-height:1.2;margin-bottom:.75rem;letter-spacing:-.01em}
.blog-card-title a{color:var(--paper);text-decoration:none;transition:color .25s}
.blog-card-title a:hover{color:var(--red)}
.blog-card-excerpt{font-family:'Lora',serif;font-size:.98rem;color:var(--fg2);line-height:1.7;margin-bottom:1rem}
.blog-card-cta{font-family:'Bebas Neue',sans-serif;letter-spacing:.16em;font-size:.85rem;color:var(--fg);text-decoration:none;border-bottom:1px solid var(--red);padding-bottom:1px;transition:color .2s}
.blog-card-cta:hover{color:var(--red)}
@media(max-width:640px){
  .blog-card.has-image{grid-template-columns:1fr}
  .blog-thumb{width:100%;height:180px;min-height:unset;border-right:none;border-bottom:1px solid var(--edge)}
}
</style>

<section style="padding:clamp(2.5rem,5vw,4.5rem) 0 clamp(2rem,3vw,3rem)">
  <div class="section-label">From the road</div>
  <h1 class="section-title">Frank's Footprints.<br><em>Every stop. Every smile.</em></h1>

  <div class="blog-list">
    {% for post in site.posts %}
    <article class="blog-card{% if post.image %} has-image{% endif %}">
      {% if post.image %}
      <a class="blog-thumb-link" href="{{ post.url | relative_url }}" tabindex="-1" aria-hidden="true">
        <img class="blog-thumb" src="{{ post.image }}" alt="{{ post.image_alt | default: post.title }}" loading="lazy">
      </a>
      {% endif %}
      <div class="blog-card-body">
        <div class="blog-card-meta">
          <time datetime="{{ post.date | date: '%Y-%m-%d' }}">{{ post.date | date: "%B %-d, %Y" }}</time>
          {% if post.location %}<span class="blog-card-loc">{{ post.location }}</span>{% endif %}
        </div>
        <h2 class="blog-card-title"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
        <p class="blog-card-excerpt">{{ post.excerpt | strip_html | truncate: 220 }}</p>
        <a class="blog-card-cta" href="{{ post.url | relative_url }}">Read the full post &rarr;</a>
      </div>
    </article>
    {% endfor %}
  </div>
</section>
