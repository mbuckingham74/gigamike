---
title: The Story of Michael
---

<style>
  body{font-family:system-ui;background:#f7f7f5;margin:0;}
  .wrap{display:flex;min-height:100vh;padding:4rem 6vw;gap:3rem;}
  .posts{flex:0 0 260px;position:sticky;top:3rem;}
  .posts li{margin:0 0 1rem;padding-bottom:.8rem;border-bottom:1px solid #ddd;}
  .content{flex:1;font-size:1.1rem;line-height:1.7;}
</style>

<div class="wrap">
  <aside class="posts">
    <h2>Writing</h2>
    <ul>
      {% for post in site.posts %}
      <li>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        <small>{{ post.date | date: "%b %-d, %Y" }}</small>
      </li>
      {% endfor %}
    </ul>
  </aside>

  <main class="content">
    <h1>{{ page.title }}</h1>
    <p>Intro text or latest story goes here.</p>
  </main>
</div>
