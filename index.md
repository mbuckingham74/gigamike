---
title: The Story of Michael
---

<style>
  :root {
    --bg-main: #050712;
    --bg-main-2: #0b1020;
    --card: #11131c;
    --card-soft: #181a25;
    --accent: #7dd3fc;
    --accent-soft: #0f172a;
    --text: #e5e7eb;
    --muted: #9ca3af;
    --reading-width: 880px;
  }

  * {
    box-sizing: border-box;
  }

  body {
    margin: 0;
    font-family: system-ui, -apple-system, BlinkMacSystemFont, "SF Pro Text",
      "Helvetica Neue", Arial, sans-serif;
    background:
      radial-gradient(circle at top left, #1e293b 0, transparent 45%),
      radial-gradient(circle at bottom right, #0f172a 0, transparent 55%),
      linear-gradient(135deg, var(--bg-main) 0%, var(--bg-main-2) 100%);
    background-attachment: fixed;
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
    max-width: calc(var(--reading-width) + 320px);
    margin: 0 auto;
  }

  .posts {
    flex: 0 0 260px;
    position: sticky;
    top: 3rem;
    align-self: flex-start;
    background: var(--card);
    border-radius: 18px;
    padding: 1.6rem 1.3rem;
    box-shadow: 0 18px 40px rgba(0, 0, 0, 0.45);
    border: 1px solid rgba(148, 163, 184, 0.25);
  }

  .posts h2 {
    margin: 0 0 1.25rem;
    font-size: 0.9rem;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    color: var(--muted);
  }

  .posts ul {
    list-style: none;
    padding: 0;
    margin: 0;
  }

  .posts li {
    margin: 0 0 1rem;
    padding: 0 0 0.9rem;
    border-bottom: 1px solid rgba(148, 163, 184, 0.25);
  }

  .posts li:last-child {
    border-bottom: none;
    padding-bottom: 0;
  }

  .posts a {
    display: block;
    font-size: 0.97rem;
    font-weight: 500;
    margin-bottom: 0.2rem;
  }

  .posts small {
    display: block;
    font-size: 0.78rem;
    color: var(--muted);
  }

  .content {
    flex: 1;
    font-size: 1.12rem;
    line-height: 1.8;
    background: var(--card-soft);
    border-radius: 20px;
    padding: 3rem 3rem;
    max-width: var(--reading-width);
    box-shadow: 0 20px 45px rgba(0, 0, 0, 0.6);
    border: 1px solid rgba(148, 163, 184, 0.3);
  }

  .content h1 {
    margin-top: 0;
    font-size: 2.5rem;
    letter-spacing: 0.03em;
  }

  .content p.intro {
    font-size: 1.08rem;
    color: var(--muted);
    background: var(--accent-soft);
    border-radius: 12px;
    padding: 1rem 1.1rem;
    border-left: 4px solid var(--accent);
    margin-bottom: 2rem;
  }

  .content p,
  .content li {
    color: #e5e7eb;
  }

  @media (max-width: 900px) {
    .wrap {
      flex-direction: column;
      max-width: 100%;
      padding: 2.5rem 5vw 3.5rem;
    }
    .posts {
      position: static;
      width: 100%;
      order: -1;
    }
    .content {
      padding: 2rem 1.6rem;
      max-width: 100%;
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
      whoever stumbles into this corner of the internet.
    </p>

    <p>
      Replace this with your “start here” note, an explanation of the project,
      or the opening of whatever story you want front and center.
    </p>
  </main>
</div>
