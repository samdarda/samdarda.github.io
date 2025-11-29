<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Our Companies – Coming Soon</title>
  <meta name="viewport" content="width=device-width, initial-scale=1" />

  <!-- Google Fonts (similar feel to Sequoia's serif + sans combo) -->
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@500;600&family=Inter:wght@300;400;500&display=swap" rel="stylesheet" />

  <style>
    :root {
      --bg: #f5f4f0;
      --bg-card: #ffffff;
      --text-main: #111827;
      --text-muted: #6b7280;
      --accent: #0f3d2e;   /* deep green, similar to Sequoia vibe */
      --border-subtle: #e5e7eb;
    }

    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      min-height: 100vh;
      font-family: "Inter", system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      background: radial-gradient(circle at top left, #f8f7f3 0, #f5f4f0 40%, #f2f2ee 100%);
      color: var(--text-main);
      display: flex;
      flex-direction: column;
    }

    .page {
      max-width: 1120px;
      margin: 0 auto;
      padding: 24px 20px 40px;
      display: flex;
      flex-direction: column;
      min-height: 100vh;
    }

    /* Top navigation */
    .nav {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding-bottom: 16px;
      border-bottom: 1px solid rgba(15, 61, 46, 0.07);
    }

    .logo {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      font-size: 0.9rem;
      letter-spacing: 0.18em;
      text-transform: uppercase;
      color: var(--accent);
      font-weight: 500;
    }

    .logo-mark {
      width: 18px;
      height: 18px;
      border-radius: 4px;
      border: 1px solid var(--accent);
      display: inline-flex;
      align-items: center;
      justify-content: center;
      position: relative;
      overflow: hidden;
    }

    .logo-mark::before {
      content: "";
      position: absolute;
      inset: 3px;
      border-radius: 2px;
      background: linear-gradient(135deg, rgba(15, 61, 46, 0.16), rgba(15, 61, 46, 0.0));
    }

    .nav-links {
      display: flex;
      gap: 24px;
      font-size: 0.85rem;
      text-transform: uppercase;
      letter-spacing: 0.18em;
      color: var(--text-muted);
    }

    .nav-links span {
      opacity: 0.9;
    }

    .nav-links span.is-active {
      color: var(--accent);
    }

    /* Main layout */
    .main {
      flex: 1;
      display: flex;
      align-items: center;
      padding: 40px 0 24px;
    }

    .hero {
      width: 100%;
      display: grid;
      grid-template-columns: minmax(0, 3fr) minmax(0, 2fr);
      gap: 56px;
      align-items: center;
    }

    @media (max-width: 900px) {
      .hero {
        grid-template-columns: minmax(0, 1fr);
        gap: 32px;
      }
    }

    .eyebrow {
      text-transform: uppercase;
      letter-spacing: 0.22em;
      font-size: 0.78rem;
      color: var(--text-muted);
      margin-bottom: 14px;
    }

    .title {
      font-family: "Playfair Display", "Times New Roman", serif;
      font-size: clamp(2.4rem, 4vw, 3.1rem);
      line-height: 1.1;
      margin: 0 0 20px;
      color: var(--text-main);
    }

    .title span {
      display: block;
    }

    .subtitle {
      font-size: 0.98rem;
      line-height: 1.6;
      color: var(--text-muted);
      max-width: 32rem;
      margin-bottom: 32px;
    }

    .meta {
      display: flex;
      flex-wrap: wrap;
      gap: 16px 32px;
      font-size: 0.82rem;
      color: var(--text-muted);
      text-transform: uppercase;
      letter-spacing: 0.16em;
    }

    .meta-label {
      font-weight: 500;
      color: var(--accent);
    }

    /* Right side – placeholder / card */
    .panel {
      background: rgba(255, 255, 255, 0.9);
      border-radius: 16px;
      border: 1px solid var(--border-subtle);
      box-shadow:
        0 18px 45px rgba(15, 23, 42, 0.08),
        0 0 0 1px rgba(255, 255, 255, 0.6) inset;
      padding: 24px 24px 28px;
      position: relative;
      overflow: hidden;
    }

    .panel-tag {
      display: inline-flex;
      align-items: center;
      gap: 6px;
      font-size: 0.7rem;
      text-transform: uppercase;
      letter-spacing: 0.16em;
      color: var(--text-muted);
      padding: 6px 10px;
      border-radius: 999px;
      background: #f3f4f6;
      margin-bottom: 16px;
    }

    .dot {
      width: 6px;
      height: 6px;
      border-radius: 999px;
      background: #10b981;
    }

    .panel-title {
      font-family: "Playfair Display", "Times New Roman", serif;
      font-size: 1.2rem;
      margin: 0 0 8px;
      color: var(--text-main);
    }

    .panel-text {
      font-size: 0.9rem;
      color: var(--text-muted);
      margin-bottom: 20px;
    }

    .soon-label {
      font-size: 2.1rem;
      font-weight: 500;
      letter-spacing: 0.28em;
      text-transform: uppercase;
      margin-bottom: 10px;
      color: var(--accent);
    }

    .pill-row {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-top: 8px;
    }

    .pill {
      font-size: 0.75rem;
      padding: 6px 10px;
      border-radius: 999px;
      border: 1px solid #e5e7eb;
      background: #f9fafb;
      color: var(--text-muted);
    }

    .panel-ornament {
      position: absolute;
      inset: auto -40px -60px auto;
      width: 180px;
      height: 180px;
      opacity: 0.12;
      background:
        radial-gradient(circle at 30% 20%, #16a34a 0, transparent 60%),
        radial-gradient(circle at 70% 80%, #0f766e 0, transparent 60%);
      filter: blur(1px);
    }

    /* Footer */
    .footer {
      padding-top: 18px;
      border-top: 1px solid rgba(15, 23, 42, 0.06);
      font-size: 0.78rem;
      color: var(--text-muted);
      display: flex;
      justify-content: space-between;
      gap: 12px;
      flex-wrap: wrap;
    }

    .footer span {
      opacity: 0.9;
    }
  </style>
</head>
<body>
  <div class="page">
    <!-- Top Nav -->
    <header class="nav">
      <div class="logo">
        <span class="logo-mark" aria-hidden="true"></span>
        <span>YOUR FUND</span>
      </div>
      <nav class="nav-links" aria-label="Main navigation">
        <span>Our Founders</span>
        <span class="is-active">Our Companies</span>
        <span>Stories</span>
      </nav>
    </header>

    <!-- Main Content -->
    <main class="main">
      <section class="hero">
        <!-- Left column -->
        <div>
          <div class="eyebrow">Our Companies</div>
          <h1 class="title">
            <span>We’re curating our</span>
            <span>portfolio for you.</span>
          </h1>
          <p class="subtitle">
            A new view of the companies we partner with is on the way. 
            Soon you’ll be able to explore them by category, stage, and markets they’re reshaping.
          </p>

          <div class="meta">
            <div>
              <span class="meta-label">Status&nbsp;&nbsp;</span>
              Coming Soon
            </div>
            <div>
              <span class="meta-label">Launch Window&nbsp;&nbsp;</span>
              2025
            </div>
          </div>
        </div>

        <!-- Right column / Coming Soon Card -->
        <aside class="panel" aria-label="Coming soon">
          <div class="panel-tag">
            <span class="dot"></span>
            In Progress
          </div>
          <div class="soon-label">Coming&nbsp;Soon</div>
          <h2 class="panel-title">A new way to discover our companies</h2>
          <p class="panel-text">
            Filters, spotlights, and stories that surface the people and products 
            behind each investment—all in one place.
          </p>

          <div class="pill-row">
            <div class="pill">Spotlights</div>
            <div class="pill">All Companies</div>
            <div class="pill">Filters</div>
          </div>

          <div class="panel-ornament" aria-hidden="true"></div>
        </aside>
      </section>
    </main>

    <!-- Footer -->
    <footer class="footer">
      <span>© 2025 Your Fund Name</span>
      <span>Portfolio experience currently in development.</span>
    </footer>
  </div>
</body>
</html>
