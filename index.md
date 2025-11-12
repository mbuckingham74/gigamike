<style>
  .grid{display:grid;grid-template-columns:320px 1fr;gap:2.5rem;padding:4rem 8vw;}
  .posts{background:#1e293b;color:#f8fafc;border-radius:1rem;padding:2rem;}
  .post{padding:1rem 0;border-bottom:1px solid rgba(248,250,252,.15);}
  .featured{background:linear-gradient(135deg,#4f46e5,#9333ea);border-radius:1.5rem;padding:3rem;color:#fff;}
</style>

<div class="grid">
  <aside class="posts">
    <h3>Posts</h3>
    {% for post in site.posts %}
    <article class="post">
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <div>{{ post.date | date: "%b %-d, %Y" }}</div>
      <p>{{ post.excerpt | strip_html | truncate: 80 }}</p>
    </article>
    {% endfor %}
  </aside>

  <section class="featured">
    <p class="eyebrow">Latest</p>
    <h1>{{ site.posts.first.title }}</h1>
    <p>{{ site.posts.first.excerpt | strip_html }}</p>
    <a href="{{ site.posts.first.url | relative_url }}">Keep reading →</a>
  </section>
</div>
