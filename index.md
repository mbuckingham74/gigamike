---
title: The Story of Michael
---

<style>
  :root {
    --bg: #f5f3ff;
    --bg-alt: #ffffff;
    --accent: #7b5cff;
    --accent-soft: #ebe5ff;
    --text: #222222;
  }

  * {
    box-sizing: border-box;
  }

  body {
    margin: 0;
    font-family: system-ui, -apple-system, BlinkMacSystemFont, "SF Pro Text",
      "Helvetica Neue", Arial, sans-serif;
    background: radial-gradient(circle at top left, #fef6e7 0, #f5f3ff 40%, #f7f7f5 100%);
    color: var(--text);
  }

  a {
    color: var(--accent);
    text-decoration: none;
  }

  a:hover {
    text-decoration: underline;
  }

  .wrap {
    min-height: 100vh;
    padding: 4rem 6vw;
    display: flex;
    gap: 3rem;
    max-width: 1200px;
    margin: 0 auto;
  }

  .posts {
    flex: 0 0 260px;
    position: sticky;
    top: 3rem;
    align-self: flex-start;
    background: var(--bg-alt);
    border-radius: 18px;
    padding: 1.5rem 1.25rem;
    box-shadow: 0 18px 40px rgba(0, 0, 0, 0.06);
    border: 1px solid rgba(0, 0, 0, 0.03);
  }

  .posts h2 {
    margin: 0 0 1.25rem;
    font-size: 0.9rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: #777;
  }

  .posts ul {
    list-style: none;
    padding: 0;
    margin: 0;
  }

  .posts li {
    margin: 0 0 1rem;
    padding: 0 0 0.9rem;
    border-bottom: 1px solid #eee;
  }

  .posts li:last-child {
    border-bottom: none;
    padding-bottom: 0;
  }

  .posts a {
    display: block;
    font-size: 0.98rem;
    font-weight: 500;
    margin-bottom: 0.15rem;
  }

  .posts a:hover {
    color: #4b36c9;
  }

  .posts small {
    display: block;
    font-size: 0.78rem;
    color: #999;
  }

  .content {
    flex: 1;
    font-size: 1.05rem;
    line-height: 1.8;
    background: var(--bg-alt);
    border-radius: 18px;
    padding: 2.5rem 2.4rem;
    box-shadow: 0 18px 40px rgba(0, 0, 0, 0.04);
    border: 1px solid rgba(0, 0, 0, 0.03);
  }

  .content h1 {
    margin-top: 0;
    font-size: 2.3rem;
    letter-spacing: 0.03em;
  }

  .content p.intro {
    font-size: 1.05rem;
    color: #555;
    background: var(--accent-soft);
    border-radius: 12px;
    padding: 1rem 1.1rem;
    border-left: 4px solid var(--accent);
  }

  @media (max-width: 820px) {
    .wrap {
      flex-direction: column;
      padding: 2.5rem 5vw;
    }
    .posts {
      position: static;
      width: 100%;
      order: -1;
    }
  }
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
    <p class="intro">
      Intro text or latest story goes here. This is where you set the tone for
      whoever somehow stumbled into this corner of the internet.
    </p>

    <p>
      Replace this with whatever you want on the landing page: a note about what
      this site is, your latest post, or a short “start here” story.
    </p>
  </main>
</div>
