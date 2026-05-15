<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Conference Name</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <!-- Google Font (minimal academic feel) -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500&family=Libre+Baskerville&display=swap" rel="stylesheet">

  <style>
    :root {
      --accent: #b23a48;       /* softened Rutgers scarlet */
      --accent-light: #f7e9eb;
      --text: #222;
      --muted: #666;
      --bg: #f9f9f9;
      --white: #ffffff;
      --border: #e5e5e5;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      margin: 0;
      font-family: "Inter", sans-serif;
      background: var(--bg);
      color: var(--text);
      line-height: 1.65;
    }

    /* HEADER NAVBAR */
    header {
      position: fixed;
      top: 0;
      width: 100%;
      background: rgba(255,255,255,0.95);
      border-bottom: 1px solid var(--border);
      z-index: 1000;
    }

    nav {
      max-width: 1100px;
      margin: 0 auto;
      padding: 0.8rem 1rem;
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
    }

    nav a {
      text-decoration: none;
      color: var(--muted);
      margin: 0.3rem 1rem;
      font-size: 0.95rem;
    }

    nav a:hover {
      color: var(--accent);
    }

    /* MAIN CONTAINER */
    .container {
      max-width: 900px;
      margin: 0 auto;
      padding: 6rem 1.2rem 2rem;
    }

    /* HERO */
    .hero {
      text-align: center;
      margin-bottom: 3rem;
    }

    .hero h1 {
      font-family: "Libre Baskerville", serif;
      font-size: 2.4rem;
      margin-bottom: 1rem;
      font-weight: 400;
    }

    .hero img {
      max-width: 100%;
      border-radius: 6px;
      margin-top: 1rem;
    }

    /* FULL-WIDTH SECTION HEADERS */
    .section-header {
      width: 100%;
      background: var(--accent-light);
      border-top: 1px solid var(--border);
      border-bottom: 1px solid var(--border);
      margin: 3rem 0 1.5rem;
    }

    .section-header h2 {
      max-width: 900px;
      margin: 0 auto;
      padding: 0.8rem 1.2rem;
      font-family: "Libre Baskerville", serif;
      font-size: 1.4rem;
      font-weight: 400;
      color: var(--accent);
    }

    section {
      margin-bottom: 2rem;
    }

    p {
      color: var(--text);
    }

    /* GRID */
    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 1.2rem;
      margin-top: 1rem;
    }

    /* CARDS (more minimal) */
    .card {
      padding: 0.9rem 0.2rem;
      border-bottom: 1px solid var(--border);
    }

    .card h3 {
      margin: 0;
      font-size: 1.05rem;
      font-weight: 500;
    }

    .card p {
      margin: 0.2rem 0;
      color: var(--muted);
      font-size: 0.95rem;
    }

    .card a {
      font-size: 0.9rem;
      color: var(--accent);
      text-decoration: none;
    }

    .card a:hover {
      text-decoration: underline;
    }

    /* BUTTON */
    .button {
      display: inline-block;
      margin-top: 1rem;
      padding: 0.5rem 1rem;
      border: 1px solid var(--accent);
      color: var(--accent);
      text-decoration: none;
      font-size: 0.9rem;
      border-radius: 4px;
    }

    .button:hover {
      background: var(--accent-light);
    }

    footer {
      text-align: center;
      padding: 2rem 1rem;
      color: var(--muted);
      font-size: 0.85rem;
    }

  </style>
</head>

<body>

<header>
  <nav>
    <a href="#about">About</a>
    <a href="#speakers">Speakers</a>
    <a href="#program">Program</a>
    <a href="#venue">Venue & Travel</a>
    <a href="#registration">Registration</a>
    <a href="#organizers">Organizers</a>
  </nav>
</header>

<div class="container">

  <!-- HERO -->
  <div class="hero">
    <h1>Conference Name</h1>
    <img src="conference-image.jpg" alt="Conference Image">
  </div>

  <!-- ABOUT -->
</div>
<div class="section-header"><h2 id="about">About</h2></div>
<div class="container">
  <section>
    <p>
      This conference brings together researchers in combinatorics and related areas.
      Include a short description of the themes, goals, and mathematical focus.
    </p>
  </section>
</div>

<!-- SPEAKERS -->
<div class="section-header"><h2 id="speakers">Confirmed Speakers</h2></div>
<div class="container">
  <section>
    <div class="grid">

      <div class="card">
        <h3>Speaker Name</h3>
        <p>University Name</p>
        <a href="#">website</a>
      </div>

      <div class="card">
        <h3>Speaker Name</h3>
        <p>University Name</p>
        <a href="#">website</a>
      </div>

    </div>
  </section>
</div>

<!-- PROGRAM -->
<div class="section-header"><h2 id="program">Program</h2></div>
<div class="container">
  <section>
    <p>Schedule coming soon.</p>
  </section>
</div>

<!-- VENUE -->
<div class="section-header"><h2 id="venue">Venue & Travel</h2></div>
<div class="container">
  <section>
    <p>Details about venue, travel, and accommodation.</p>
  </section>
</div>

<!-- REGISTRATION -->
<div class="section-header"><h2 id="registration">Registration</h2></div>
<div class="container">
  <section>
    <p>Please register using the form below.</p>
    <a class="button" href="https://forms.gle/YOUR-FORM-LINK">Register</a>
  </section>
</div>

<!-- ORGANIZERS -->
<div class="section-header"><h2 id="organizers">Organizers</h2></div>
<div class="container">
  <section>
    <div class="grid">

      <div class="card">
        <h3>Organizer Name</h3>
        <p>University Name</p>
        <a href="#">website</a>
      </div>

      <div class="card">
        <h3>Organizer Name</h3>
        <p>University Name</p>
        <a href="#">website</a>
      </div>

    </div>
  </section>
</div>

<footer>
  © 2026 Conference Name
</footer>

</body>
</html>
