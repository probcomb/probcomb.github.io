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
      --black: #111111;
      --gray: #f5f5f5;
      --white: #ffffff;
    }

    body {
      margin: 0;
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
      line-height: 1.6;
      color: var(--black);
      background-color: var(--gray);
    }

    header {
      background: var(--rutgers-red);
      color: var(--white);
      padding: 2rem 1rem;
      text-align: center;
    }

    header h1 {
      margin: 0;
      font-size: 2.5rem;
    }

    header p {
      margin-top: 0.5rem;
      font-size: 1.2rem;
    }

    nav {
      background: var(--black);
      text-align: center;
      padding: 0.5rem;
    }

    nav a {
      color: var(--white);
      text-decoration: none;
      margin: 0 1rem;
      font-weight: 500;
    }

    nav a:hover {
      color: var(--rutgers-red);
    }

    .container {
      max-width: 900px;
      margin: 2rem auto;
      padding: 0 1rem;
      background: var(--white);
    }

    section {
      margin-bottom: 2rem;
    }

    h2 {
      color: var(--rutgers-red);
      border-bottom: 2px solid var(--rutgers-red);
      padding-bottom: 0.3rem;
    }

    footer {
      text-align: center;
      padding: 1rem;
      background: var(--black);
      color: var(--white);
      font-size: 0.9rem;
    }

    .highlight {
      background: #ffe5eb;
      padding: 1rem;
      border-left: 4px solid var(--rutgers-red);
    }

    ul {
      padding-left: 1.2rem;
    }
  </style>
</head>

<body>

<header>
  <h1>Conference Name</h1>
  <p>Dates · Location</p>
</header>

<nav>
  <a href="#about">About</a>
  <a href="#speakers">Speakers</a>
  <a href="#schedule">Schedule</a>
  <a href="#travel">Travel</a>
  <a href="#contact">Contact</a>
</nav>

<div class="container">

  <section id="about">
    <h2>About</h2>
    <p>
      This conference brings together researchers in combinatorics and related fields.
      Add a short description of the theme, goals, and audience.
    </p>

    <div class="highlight">
      <strong>Registration Deadline:</strong> Month Day, Year
    </div>
  </section>

  <section id="speakers">
    <h2>Speakers</h2>
    <ul>
      <li>Speaker One (Affiliation)</li>
      <li>Speaker Two (Affiliation)</li>
      <li>Speaker Three (Affiliation)</li>
    </ul>
  </section>

  <section id="schedule">
    <h2>Schedule</h2>
    <p>Detailed schedule coming soon.</p>

    <!-- Example -->
    <ul>
      <li><strong>Day 1:</strong> Talks + reception</li>
      <li><strong>Day 2:</strong> Full day of lectures</li>
    </ul>
  </section>

  <section id="travel">
    <h2>Travel & Accommodation</h2>
    <p>
      Provide information about airports, hotels, and directions.
    </p>
  </section>

  <section id="contact">
    <h2>Contact</h2>
    <p>Email: yourname@university.edu</p>
  </section>

</div>

<footer>
  © 2026 Conference Name · Hosted on GitHub Pages
</footer>

</body>
</html>
