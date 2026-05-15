<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Conference Name</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <style>
    :root {
      --rutgers-red: #cc0033;
      --dark-red: #990026;
      --black: #111;
      --gray: #f4f4f4;
      --white: #ffffff;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      margin: 0;
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
      background: var(--gray);
      color: var(--black);
      line-height: 1.6;
    }

    /* HEADER */
    header {
      position: fixed;
      top: 0;
      width: 100%;
      background: var(--black);
      z-index: 1000;
      padding: 0.7rem 0;
    }

    nav {
      max-width: 1100px;
      margin: 0 auto;
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
    }

    nav a {
      color: var(--white);
      text-decoration: none;
      margin: 0.3rem 1rem;
      font-weight: 500;
    }

    nav a:hover {
      color: var(--rutgers-red);
    }

    /* MAIN CONTENT */
    .container {
      max-width: 1000px;
      margin: 0 auto;
      padding: 6rem 1rem 2rem; /* space for fixed header */
      background: var(--white);
    }

    .hero {
      text-align: center;
      margin-bottom: 2rem;
    }

    .hero h1 {
      font-size: 2.5rem;
      margin-bottom: 1rem;
      color: var(--rutgers-red);
    }

    .hero img {
      max-width: 100%;
      height: auto;
      border-radius: 8px;
    }

    section {
      margin-bottom: 3rem;
    }

    h2 {
      color: var(--rutgers-red);
      border-bottom: 2px solid var(--rutgers-red);
      padding-bottom: 0.3rem;
    }

    /* CARD GRID */
    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 1rem;
      margin-top: 1rem;
    }

    .card {
      border: 1px solid #ddd;
      padding: 1rem;
      border-radius: 8px;
      background: #fafafa;
    }

    .card h3 {
      margin-top: 0;
      margin-bottom: 0.3rem;
    }

    .card a {
      color: var(--rutgers-red);
      text-decoration: none;
      font-weight: 500;
    }

    .card a:hover {
      text-decoration: underline;
    }

    /* BUTTON */
    .button {
      display: inline-block;
      background: var(--rutgers-red);
      color: white;
      padding: 0.7rem 1.2rem;
      border-radius: 5px;
      text-decoration: none;
      font-weight: 500;
      margin-top: 1rem;
    }

    .button:hover {
      background: var(--dark-red);
    }

    footer {
      text-align: center;
      padding: 1rem;
      background: var(--black);
      color: white;
      font-size: 0.9rem;
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
  <section id="about">
    <h2>About</h2>
    <p>
      This conference brings together researchers in combinatorics and related areas.
      Include a short description of the goals, themes, and intended audience.
    </p>
  </section>

  <!-- SPEAKERS -->
  <section id="speakers">
    <h2>Confirmed Speakers</h2>
    <div class="grid">

      <div class="card">
        <h3>Speaker Name</h3>
        <p>University Name</p>
        <a href="#">Personal Website</a>
      </div>

      <div class="card">
        <h3>Speaker Name</h3>
        <p>University Name</p>
        <a href="#">Personal Website</a>
      </div>

    </div>
  </section>

  <!-- PROGRAM -->
  <section id="program">
    <h2>Program</h2>
    <p>
      Detailed schedule coming soon.
    </p>
  </section>

  <!-- VENUE -->
  <section id="venue">
    <h2>Venue & Travel</h2>
    <p>
      Provide details about the venue, directions, nearby airports, and accommodations.
    </p>
  </section>

  <!-- REGISTRATION -->
  <section id="registration">
    <h2>Registration</h2>
    <p>
      Please register using the link below:
    </p>

    <a class="button" href="https://forms.gle/YOUR-FORM-LINK">
      Register Here
    </a>
  </section>

  <!-- ORGANIZERS -->
  <section id="organizers">
    <h2>Organizers</h2>
    <div class="grid">

      <div class="card">
        <h3>Organizer Name</h3>
        <p>University Name</p>
        <a href="#">Personal Website</a>
      </div>

      <div class="card">
        <h3>Organizer Name</h3>
        <p>University Name</p>
        <a href="#">Personal Website</a>
      </div>

    </div>
  </section>

</div>

<footer>
  © 2026 Conference Name · GitHub Pages
</footer>

</body>
</html>
