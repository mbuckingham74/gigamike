<style>
  :root {
    --bg: #f7f5ff;
    --bg2: #fffdf8;
    --accent: #7b5cff;
    --accent-soft: #ebe5ff;
    --text: #222;
    --reading-width: 880px;
  }

  body {
    margin: 0;
    font-family: system-ui, -apple-system, BlinkMacSystemFont, "SF Pro Text",
      "Helvetica Neue", Arial, sans-serif;
    background: linear-gradient(135deg, var(--bg) 0%, var(--bg2) 100%);
    background-attachment: fixed;
    color: var(--text);
  }

  /* Optional soft noise overlay */
  body::before {
    content: "";
    position: fixed;
    inset: 0;
    pointer-events: none;
    background-image: url("data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAgAAAAICAYAAADED76LAAAAE0lEQVQoU2NkQAP/Gf4nBjBgAADnJgG5cDIeAAAAAElFTkSuQmCC");
    opacity: 0.08;
    mix-blend-mode: multiply;
  }

  .wrap {
    min-height: 100vh;
    padding: 4rem 6vw;
    display: flex;
    gap: 3rem;
    max-width: calc(var(--reading-width) + 300px);
    margin: 0 auto;
  }

  .posts {
    flex: 0 0 260px;
    position: sticky;
    top: 3rem;
    align-self: flex-start;
    background: white;
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
    color: var(--accent);
    margin-bottom: 0.15rem;
  }

  .posts small {
    font-size: 0.78rem;
    color: #999;
  }

  .content {
    flex: 1;
    font-size: 1.14rem;
    line-height: 1.8;
    background: white;
    border-radius: 20px;
    padding: 3rem 3rem;
    max-width: var(--reading-width);
    box-shadow: 0 20px 45px rgba(0, 0, 0, 0.07);
    border: 1px solid rgba(0, 0, 0, 0.03);
  }

  .content h1 {
    margin-top: 0;
    font-size: 2.5rem;
    letter-spacing: 0.02em;
  }

  .content p.intro {
    font-size: 1.12rem;
    color: #555;
    background: var(--accent-soft);
    border-radius: 12px;
    padding: 1rem 1.1rem;
    border-left: 4px solid var(--accent);
    margin-bottom: 2rem;
  }

  @media (max-width: 900px) {
    .wrap {
      flex-direction: column;
      max-width: 100%;
      padding: 2.5rem 5vw;
    }
    .posts {
      position: static;
      width: 100%;
      order: -1;
    }
    .content {
      padding: 2rem;
      max-width: 100%;
    }
  }
</style>
