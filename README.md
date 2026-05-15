<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <meta name="description" content="[Conference Name], [dates], [location]. Replace this description with a concise summary of the conference.">
  <title>[Conference Name] • [Dates] • Rutgers University</title>
  <style>
    /*
      Reusable single-file conference template.
      Replace every bracketed placeholder, for example [Conference Name].

      Accessibility reminders for editors:
      - Keep meaningful link text; avoid “click here.”
      - Add specific alt text to any real images you add.
      - Preserve the skip link, semantic headings, table captions, form labels, and focus styles.
      - Keep white text on Rutgers Red; avoid black text on red.
      - Check any newly added color pairings for WCAG AA contrast.
    */

    :root {
      --rutgers-red: #cc0033;
      --rutgers-red-dark: #8e0d18;
      --rutgers-black: #000000;
      --rutgers-white: #ffffff;
      --rutgers-gray: #5f6a72;
      --rutgers-dark-gray: #222222;
      --rutgers-mid-gray: #666666;
      --rutgers-light-gray: #efefef;
      --rutgers-border-gray: #d8d8d8;
      --soft-red: #fff5f7;
      --soft-yellow: #fff6d4;
      --page-width: 72rem;
      --radius: 1rem;
      --shadow: 0 1rem 2.5rem rgb(34 34 34 / 12%);
      --focus-ring: 0 0 0 0.25rem rgb(204 0 51 / 28%);
    }

    *,
    *::before,
    *::after {
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      margin: 0;
      color: var(--rutgers-dark-gray);
      background: var(--rutgers-white);
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      font-size: 1rem;
      line-height: 1.6;
    }

    a {
      color: var(--rutgers-red-dark);
      text-decoration-thickness: 0.12em;
      text-underline-offset: 0.18em;
    }

    a:hover,
    a:focus-visible {
      color: var(--rutgers-red);
    }

    :focus-visible {
      outline: 0.1875rem solid var(--rutgers-black);
      outline-offset: 0.1875rem;
      box-shadow: var(--focus-ring);
    }

    .skip-link {
      position: absolute;
      top: 0.75rem;
      left: 0.75rem;
      z-index: 1000;
      transform: translateY(-200%);
      padding: 0.7rem 1rem;
      color: var(--rutgers-white);
      background: var(--rutgers-black);
      border-radius: 0.5rem;
      font-weight: 800;
    }

    .skip-link:focus {
      transform: translateY(0);
    }

    .site-header {
      position: sticky;
      top: 0;
      z-index: 50;
      border-bottom: 0.0625rem solid var(--rutgers-border-gray);
      background: rgb(255 255 255 / 96%);
      backdrop-filter: blur(0.6rem);
    }

    .topbar {
      color: var(--rutgers-white);
      background: var(--rutgers-red);
    }

    .topbar .wrap {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 1rem;
      max-width: var(--page-width);
      margin: 0 auto;
      padding: 0.55rem 1.25rem;
      font-size: 0.95rem;
      font-weight: 700;
    }

    .topbar a {
      color: var(--rutgers-white);
    }

    .nav-wrap {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 1.25rem;
      max-width: var(--page-width);
      margin: 0 auto;
      padding: 0.95rem 1.25rem;
    }

    .brand {
      display: inline-flex;
      align-items: center;
      gap: 0.75rem;
      color: var(--rutgers-dark-gray);
      text-decoration: none;
    }

    .brand-mark {
      display: grid;
      width: 2.5rem;
      height: 2.5rem;
      place-items: center;
      color: var(--rutgers-white);
      background: var(--rutgers-red);
      border-radius: 0.6rem;
      font-weight: 900;
      letter-spacing: -0.08em;
      line-height: 1;
    }

    .brand-text {
      display: grid;
      line-height: 1.15;
    }

    .brand-text strong {
      font-size: 1rem;
    }

    .brand-text span {
      color: var(--rutgers-gray);
      font-size: 0.9rem;
    }

    .site-nav ul {
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      justify-content: flex-end;
      gap: 0.35rem;
      margin: 0;
      padding: 0;
      list-style: none;
    }

    .site-nav a {
      display: inline-flex;
      min-height: 2.75rem;
      align-items: center;
      padding: 0.55rem 0.7rem;
      border-radius: 999rem;
      color: var(--rutgers-dark-gray);
      font-weight: 750;
      text-decoration: none;
    }

    .site-nav a:hover,
    .site-nav a:focus-visible {
      color: var(--rutgers-white);
      background: var(--rutgers-red);
    }

    main section {
      scroll-margin-top: 9rem;
    }

    .hero {
      position: relative;
      overflow: hidden;
      color: var(--rutgers-white);
      background:
        radial-gradient(circle at 15% 15%, rgb(255 255 255 / 18%), transparent 16rem),
        linear-gradient(135deg, var(--rutgers-red) 0%, var(--rutgers-red-dark) 60%, var(--rutgers-black) 100%);
    }

    .hero::after {
      position: absolute;
      inset: auto -8rem -16rem auto;
      width: 32rem;
      height: 32rem;
      content: "";
      background: repeating-linear-gradient(135deg, rgb(255 255 255 / 14%) 0 0.4rem, transparent 0.4rem 1.3rem);
      border-radius: 50%;
      transform: rotate(12deg);
    }

    .hero .wrap {
      position: relative;
      z-index: 1;
      display: grid;
      grid-template-columns: minmax(0, 1.45fr) minmax(16rem, 0.75fr);
      gap: clamp(2rem, 5vw, 4rem);
      max-width: var(--page-width);
      margin: 0 auto;
      padding: clamp(4rem, 10vw, 7rem) 1.25rem;
    }

    .eyebrow {
      margin: 0 0 0.85rem;
      color: var(--rutgers-white);
      font-size: 0.95rem;
      font-weight: 850;
      letter-spacing: 0.08em;
      text-transform: uppercase;
    }

    h1,
    h2,
    h3 {
      line-height: 1.15;
    }

    h1 {
      max-width: 13ch;
      margin: 0;
      font-size: clamp(3rem, 8vw, 6.4rem);
      letter-spacing: -0.06em;
    }

    .hero-subtitle {
      max-width: 48rem;
      margin: 1.25rem 0 0;
      color: rgb(255 255 255 / 92%);
      font-size: clamp(1.25rem, 2.5vw, 1.75rem);
      line-height: 1.35;
    }

    .hero-details {
      display: flex;
      flex-wrap: wrap;
      gap: 0.8rem;
      margin: 2rem 0 0;
    }

    .hero-details span {
      display: inline-flex;
      align-items: center;
      min-height: 2.5rem;
      padding: 0.45rem 0.8rem;
      color: var(--rutgers-white);
      background: rgb(0 0 0 / 28%);
      border: 0.0625rem solid rgb(255 255 255 / 32%);
      border-radius: 999rem;
      font-weight: 750;
    }

    .hero-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 0.85rem;
      margin-top: 2rem;
    }

    .button {
      display: inline-flex;
      min-height: 2.75rem;
      align-items: center;
      justify-content: center;
      padding: 0.72rem 1rem;
      border: 0.125rem solid transparent;
      border-radius: 999rem;
      font-weight: 850;
      text-decoration: none;
    }

    .button.primary {
      color: var(--rutgers-red-dark);
      background: var(--rutgers-white);
    }

    .button.primary:hover,
    .button.primary:focus-visible {
      color: var(--rutgers-white);
      background: var(--rutgers-black);
    }

    .button.secondary {
      color: var(--rutgers-white);
      border-color: rgb(255 255 255 / 70%);
      background: transparent;
    }

    .button.secondary:hover,
    .button.secondary:focus-visible {
      color: var(--rutgers-red-dark);
      background: var(--rutgers-white);
    }

    .hero-card {
      align-self: end;
      padding: 1.25rem;
      color: var(--rutgers-dark-gray);
      background: var(--rutgers-white);
      border-radius: var(--radius);
      box-shadow: var(--shadow);
    }

    .hero-card h2 {
      margin: 0 0 0.6rem;
      color: var(--rutgers-red-dark);
      font-size: 1.25rem;
    }

    .hero-card p {
      margin: 0;
      color: var(--rutgers-dark-gray);
    }

    .hero-card ul {
      margin: 1rem 0 0;
      padding-left: 1.2rem;
    }

    .section {
      max-width: var(--page-width);
      margin: 0 auto;
      padding: clamp(3rem, 6vw, 5rem) 1.25rem;
    }

    .section + .section {
      border-top: 0.0625rem solid var(--rutgers-border-gray);
    }

    .section-header {
      display: grid;
      gap: 0.6rem;
      max-width: 52rem;
      margin-bottom: 2rem;
    }

    .section-kicker {
      margin: 0;
      color: var(--rutgers-red-dark);
      font-size: 0.9rem;
      font-weight: 850;
      letter-spacing: 0.08em;
      text-transform: uppercase;
    }

    h2 {
      margin: 0;
      color: var(--rutgers-black);
      font-size: clamp(2rem, 4vw, 3rem);
      letter-spacing: -0.04em;
    }

    h3 {
      margin: 0;
      color: var(--rutgers-black);
      font-size: 1.25rem;
    }

    .lead {
      margin: 0;
      color: var(--rutgers-dark-gray);
      font-size: 1.18rem;
    }

    .notice {
      padding: 1rem 1.1rem;
      background: var(--soft-yellow);
      border: 0.0625rem solid #f5d36a;
      border-left: 0.45rem solid var(--rutgers-red);
      border-radius: 0.8rem;
    }

    .notice strong {
      color: var(--rutgers-red-dark);
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 1rem;
    }

    .card {
      min-width: 0;
      padding: 1.2rem;
      background: var(--rutgers-white);
      border: 0.0625rem solid var(--rutgers-border-gray);
      border-radius: var(--radius);
      box-shadow: 0 0.5rem 1.5rem rgb(34 34 34 / 6%);
    }

    .card p:last-child,
    .card ul:last-child {
      margin-bottom: 0;
    }

    .muted {
      color: var(--rutgers-gray);
    }

    .person-grid {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 1rem;
      margin: 0;
      padding: 0;
      list-style: none;
    }

    .person-card {
      display: grid;
      gap: 0.45rem;
      padding: 1.05rem;
      background: var(--rutgers-white);
      border: 0.0625rem solid var(--rutgers-border-gray);
      border-top: 0.35rem solid var(--rutgers-red);
      border-radius: var(--radius);
    }

    .person-card p {
      margin: 0;
      color: var(--rutgers-gray);
    }

    .tag-list {
      display: flex;
      flex-wrap: wrap;
      gap: 0.5rem;
      margin: 1rem 0 0;
      padding: 0;
      list-style: none;
    }

    .tag-list li {
      padding: 0.35rem 0.65rem;
      color: var(--rutgers-red-dark);
      background: var(--soft-red);
      border: 0.0625rem solid rgb(204 0 51 / 22%);
      border-radius: 999rem;
      font-weight: 750;
    }

    .schedule-day {
      margin-top: 1.5rem;
    }

    .table-wrap {
      overflow-x: auto;
      border: 0.0625rem solid var(--rutgers-border-gray);
      border-radius: var(--radius);
    }

    table {
      width: 100%;
      min-width: 38rem;
      border-collapse: collapse;
      background: var(--rutgers-white);
    }

    caption {
      padding: 0.85rem 1rem;
      color: var(--rutgers-dark-gray);
      background: var(--rutgers-light-gray);
      font-weight: 800;
      text-align: left;
    }

    th,
    td {
      padding: 0.85rem 1rem;
      border-top: 0.0625rem solid var(--rutgers-border-gray);
      text-align: left;
      vertical-align: top;
    }

    thead th {
      color: var(--rutgers-white);
      background: var(--rutgers-red-dark);
    }

    tbody th {
      width: 9rem;
      color: var(--rutgers-black);
      font-weight: 850;
    }

    .two-column {
      display: grid;
      grid-template-columns: minmax(0, 1fr) minmax(16rem, 0.72fr);
      gap: 1.5rem;
      align-items: start;
    }

    .callout {
      padding: 1.25rem;
      color: var(--rutgers-white);
      background: var(--rutgers-red-dark);
      border-radius: var(--radius);
    }

    .callout h3 {
      color: var(--rutgers-white);
    }

    .callout a {
      color: var(--rutgers-white);
      font-weight: 850;
    }

    .access-list {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 1rem;
      margin: 1.25rem 0 0;
      padding: 0;
      list-style: none;
    }

    .access-list li {
      padding: 1rem;
      background: var(--rutgers-light-gray);
      border-left: 0.35rem solid var(--rutgers-red);
      border-radius: 0.8rem;
    }

    .sponsors {
      display: flex;
      flex-wrap: wrap;
      gap: 0.75rem;
      margin: 1rem 0 0;
      padding: 0;
      list-style: none;
    }

    .sponsors li {
      min-height: 3.25rem;
      display: inline-flex;
      align-items: center;
      justify-content: center;
      padding: 0.75rem 1rem;
      background: var(--rutgers-light-gray);
      border: 0.0625rem solid var(--rutgers-border-gray);
      border-radius: 0.75rem;
      font-weight: 850;
    }

    .footer {
      color: var(--rutgers-white);
      background: var(--rutgers-black);
    }

    .footer .wrap {
      display: grid;
      grid-template-columns: 1.2fr 1fr;
      gap: 2rem;
      max-width: var(--page-width);
      margin: 0 auto;
      padding: 2.5rem 1.25rem;
    }

    .footer h2,
    .footer h3 {
      color: var(--rutgers-white);
    }

    .footer a {
      color: var(--rutgers-white);
    }

    .footer p {
      margin-top: 0.4rem;
      color: rgb(255 255 255 / 88%);
    }

    .footer-nav ul {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 0.4rem 1rem;
      margin: 0;
      padding: 0;
      list-style: none;
    }

    .footer-small {
      border-top: 0.0625rem solid rgb(255 255 255 / 18%);
    }

    .footer-small .wrap {
      display: block;
      padding-top: 1.1rem;
      padding-bottom: 1.1rem;
      font-size: 0.9rem;
    }

    .sr-only {
      position: absolute;
      width: 1px;
      height: 1px;
      padding: 0;
      margin: -1px;
      overflow: hidden;
      clip: rect(0, 0, 0, 0);
      white-space: nowrap;
      border: 0;
    }

    @media (max-width: 56rem) {
      .topbar .wrap,
      .nav-wrap,
      .two-column,
      .footer .wrap,
      .hero .wrap {
        grid-template-columns: 1fr;
      }

      .nav-wrap {
        align-items: flex-start;
      }

      .site-nav ul {
        justify-content: flex-start;
      }

      .grid,
      .person-grid,
      .access-list {
        grid-template-columns: 1fr 1fr;
      }
    }

    @media (max-width: 38rem) {
      .topbar .wrap,
      .nav-wrap {
        display: grid;
      }

      .grid,
      .person-grid,
      .access-list,
      .footer-nav ul {
        grid-template-columns: 1fr;
      }

      h1 {
        font-size: clamp(2.55rem, 14vw, 4rem);
      }

      .hero-details span,
      .button {
        width: 100%;
      }
    }

    @media (prefers-reduced-motion: reduce) {
      *,
      *::before,
      *::after {
        scroll-behavior: auto !important;
        transition-duration: 0.01ms !important;
        animation-duration: 0.01ms !important;
        animation-iteration-count: 1 !important;
      }
    }

    @media print {
      .site-header,
      .skip-link,
      .hero-actions,
      .footer-nav {
        display: none;
      }

      a::after {
        content: " (" attr(href) ")";
        font-size: 0.9em;
      }

      body {
        color: #000;
        background: #fff;
      }

      .hero,
      .callout,
      .footer {
        color: #000;
        background: #fff;
      }
    }
  </style>
</head>
<body>
  <a class="skip-link" href="#main-content">Skip to main content</a>

  <header class="site-header">
    <div class="topbar" aria-label="Conference dates and host">
      <div class="wrap">
        <span>[Month Day–Day, Year] • [City, State]</span>
        <a href="mailto:[contact-email@example.edu]">[contact-email@example.edu]</a>
      </div>
    </div>

    <div class="nav-wrap">
      <a class="brand" href="#top" aria-label="[Conference Name] home">
        <span class="brand-mark" aria-hidden="true">R</span>
        <span class="brand-text">
          <strong>[Conference Name]</strong>
          <span>[Host Unit], Rutgers University</span>
        </span>
      </a>

      <nav class="site-nav" aria-label="Main navigation">
        <ul>
          <li><a href="#about">About</a></li>
          <li><a href="#speakers">Speakers</a></li>
          <li><a href="#program">Program</a></li>
          <li><a href="#venue">Venue &amp; Travel</a></li>
          <li><a href="#registration">Registration</a></li>
          <li><a href="#accessibility">Accessibility</a></li>
          <li><a href="#organizers">Organizers</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <main id="main-content" tabindex="-1">
    <section class="hero" id="top" aria-labelledby="conference-title">
      <div class="wrap">
        <div>
          <p class="eyebrow">[Conference subtitle or theme]</p>
          <h1 id="conference-title">[Conference Name]</h1>
          <p class="hero-subtitle">[One- or two-sentence description of the conference, its mathematical or scientific themes, and the audience it will bring together.]</p>

          <div class="hero-details" aria-label="Conference details">
            <span>[Month Day–Day, Year]</span>
            <span>[Rutgers University Campus]</span>
            <span>[City, State]</span>
          </div>

          <div class="hero-actions">
            <a class="button primary" href="https://example.com/registration">Register</a>
            <a class="button secondary" href="#program">View preliminary program</a>
          </div>
        </div>

        <aside class="hero-card" aria-labelledby="important-dates-heading">
          <h2 id="important-dates-heading">Important dates</h2>
          <p>Replace these placeholders with confirmed deadlines.</p>
          <ul>
            <li><strong>[Date]:</strong> Registration opens</li>
            <li><strong>[Date]:</strong> Travel funding deadline</li>
            <li><strong>[Date]:</strong> Poster abstract deadline</li>
            <li><strong>[Date]:</strong> Accessibility accommodation request deadline</li>
          </ul>
        </aside>
      </div>
    </section>

    <section class="section" id="about" aria-labelledby="about-heading">
      <div class="section-header">
        <p class="section-kicker">About</p>
        <h2 id="about-heading">A conference placeholder with room for a strong public summary.</h2>
        <p class="lead">[Conference Name] will bring together researchers working in [topic areas]. The meeting will feature invited talks, contributed sessions, a poster session, and time for informal collaboration.</p>
      </div>

      <div class="grid" aria-label="Conference highlights">
        <article class="card">
          <h3>[Theme 1]</h3>
          <p>[Brief description of a main theme, area, or motivation.]</p>
        </article>
        <article class="card">
          <h3>[Theme 2]</h3>
          <p>[Brief description of a second theme, area, or motivation.]</p>
        </article>
        <article class="card">
          <h3>[Theme 3]</h3>
          <p>[Brief description of a third theme, area, or motivation.]</p>
        </article>
      </div>

      <ul class="tag-list" aria-label="Topic keywords">
        <li>[Keyword]</li>
        <li>[Keyword]</li>
        <li>[Keyword]</li>
        <li>[Keyword]</li>
        <li>[Keyword]</li>
      </ul>
    </section>

    <section class="section" id="speakers" aria-labelledby="speakers-heading">
      <div class="section-header">
        <p class="section-kicker">Speakers</p>
        <h2 id="speakers-heading">Confirmed speakers</h2>
        <p class="lead">Replace the placeholder cards with speaker names, affiliations, and links. Use descriptive link text for screen reader users.</p>
      </div>

      <ul class="person-grid" aria-label="Confirmed speaker list">
        <li class="person-card">
          <h3>[Speaker Name]</h3>
          <p>[Institution]</p>
          <a href="https://example.com/speaker-1">[Speaker Name] webpage</a>
        </li>
        <li class="person-card">
          <h3>[Speaker Name]</h3>
          <p>[Institution]</p>
          <a href="https://example.com/speaker-2">[Speaker Name] webpage</a>
        </li>
        <li class="person-card">
          <h3>[Speaker Name]</h3>
          <p>[Institution]</p>
          <a href="https://example.com/speaker-3">[Speaker Name] webpage</a>
        </li>
        <li class="person-card">
          <h3>[Speaker Name]</h3>
          <p>[Institution]</p>
          <a href="https://example.com/speaker-4">[Speaker Name] webpage</a>
        </li>
        <li class="person-card">
          <h3>[Speaker Name]</h3>
          <p>[Institution]</p>
          <a href="https://example.com/speaker-5">[Speaker Name] webpage</a>
        </li>
        <li class="person-card">
          <h3>[Speaker Name]</h3>
          <p>[Institution]</p>
          <a href="https://example.com/speaker-6">[Speaker Name] webpage</a>
        </li>
      </ul>
    </section>

    <section class="section" id="program" aria-labelledby="program-heading">
      <div class="section-header">
        <p class="section-kicker">Program</p>
        <h2 id="program-heading">Preliminary schedule</h2>
        <p class="lead">This structure is accessible to screen readers because each table has a caption, column headers, and row headers for times.</p>
      </div>

      <p class="notice"><strong>Placeholder:</strong> A detailed schedule will be posted closer to the event. Please replace the sample entries below when the program is finalized.</p>

      <section class="schedule-day" aria-labelledby="day-one-heading">
        <h3 id="day-one-heading">[Day 1: Weekday, Month Day]</h3>
        <div class="table-wrap">
          <table>
            <caption>Schedule for [Day 1]</caption>
            <thead>
              <tr>
                <th scope="col">Time</th>
                <th scope="col">Session</th>
                <th scope="col">Location</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <th scope="row">9:00–9:30</th>
                <td>Registration and coffee</td>
                <td>[Building and room]</td>
              </tr>
              <tr>
                <th scope="row">9:30–10:30</th>
                <td>[Opening lecture: Speaker Name]</td>
                <td>[Auditorium]</td>
              </tr>
              <tr>
                <th scope="row">11:00–12:00</th>
                <td>[Invited lecture or parallel session]</td>
                <td>[Room]</td>
              </tr>
              <tr>
                <th scope="row">14:00–17:30</th>
                <td>[Conference program]</td>
                <td>[Rooms]</td>
              </tr>
            </tbody>
          </table>
        </div>
      </section>

      <section class="schedule-day" aria-labelledby="day-two-heading">
        <h3 id="day-two-heading">[Day 2: Weekday, Month Day]</h3>
        <div class="table-wrap">
          <table>
            <caption>Schedule for [Day 2]</caption>
            <thead>
              <tr>
                <th scope="col">Time</th>
                <th scope="col">Session</th>
                <th scope="col">Location</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <th scope="row">9:30–10:30</th>
                <td>[Invited lecture: Speaker Name]</td>
                <td>[Room]</td>
              </tr>
              <tr>
                <th scope="row">11:00–12:00</th>
                <td>[Parallel sessions]</td>
                <td>[Rooms]</td>
              </tr>
              <tr>
                <th scope="row">15:30–17:00</th>
                <td>[Poster session]</td>
                <td>[Atrium or hall]</td>
              </tr>
            </tbody>
          </table>
        </div>
      </section>
    </section>

    <section class="section" id="venue" aria-labelledby="venue-heading">
      <div class="section-header">
        <p class="section-kicker">Venue &amp; Travel</p>
        <h2 id="venue-heading">Getting to Rutgers</h2>
        <p class="lead">Replace these placeholders with the exact campus, building, accessible entrance, hotel, and transportation information.</p>
      </div>

      <div class="two-column">
        <div class="grid" aria-label="Venue and travel details">
          <article class="card">
            <h3>Venue</h3>
            <p><strong>[Building Name]</strong><br>[Street Address]<br>[Campus], Rutgers University</p>
          </article>
          <article class="card">
            <h3>Transportation</h3>
            <p>[Airport, train, shuttle, parking, public transit, and accessible transit information.]</p>
          </article>
          <article class="card">
            <h3>Lodging</h3>
            <p>[Hotel block information, booking deadline, accessible room information, and nearby alternatives.]</p>
          </article>
        </div>

        <aside class="callout" aria-labelledby="venue-access-heading">
          <h3 id="venue-access-heading">Accessible routes</h3>
          <p>Before publishing, add a link to an accessible campus map and describe step-free entrances, elevators, accessible restrooms, parking, and room-to-room routes.</p>
          <p><a href="https://example.com/access-map">Replace with accessible campus map link</a></p>
        </aside>
      </div>
    </section>

    <section class="section" id="registration" aria-labelledby="registration-heading">
      <div class="section-header">
        <p class="section-kicker">Registration</p>
        <h2 id="registration-heading">Registration and support</h2>
        <p class="lead">Use this section for fees, deadlines, travel support, poster applications, and any participation policies.</p>
      </div>

      <div class="two-column">
        <div>
          <p>[Registration is open / will open on Date]. Please register by <strong>[Date]</strong> to apply for travel funding, submit a poster abstract, or receive the early registration rate.</p>
          <p><strong>Registration fee:</strong> [Fee details].</p>
          <p><strong>Travel support:</strong> [Brief description of eligibility and application materials].</p>
          <p><a class="button primary" href="https://example.com/registration">Go to registration form</a></p>
        </div>
        <aside class="card" aria-labelledby="policies-heading">
          <h3 id="policies-heading">Participation policies</h3>
          <ul>
            <li>[Code of conduct link]</li>
            <li>[Poster submission instructions]</li>
            <li>[Childcare or dependent-care support information]</li>
            <li>[Public health or safety policies, if applicable]</li>
          </ul>
        </aside>
      </div>
    </section>

    <section class="section" id="accessibility" aria-labelledby="accessibility-heading">
      <div class="section-header">
        <p class="section-kicker">Accessibility</p>
        <h2 id="accessibility-heading">Accessibility and disability accommodations</h2>
        <p class="lead">[Conference Name] is committed to making the meeting accessible. Participants are encouraged to request disability-related accommodations as early as possible.</p>
      </div>

      <div class="notice" role="note" aria-label="Accommodation request instructions">
        <strong>Accommodation requests:</strong> Please contact <a href="mailto:[accessibility-contact@example.edu]">[accessibility-contact@example.edu]</a> by <strong>[Date]</strong> with requests for accommodations such as CART/live captioning, ASL interpretation, accessible seating, dietary needs, large-print materials, mobility assistance, or quiet space. We will make every reasonable effort to support requests received after this date.
      </div>

      <ul class="access-list">
        <li><strong>Step-free access:</strong> [Describe elevators, ramps, accessible entrances, and accessible restrooms.]</li>
        <li><strong>Communication access:</strong> [Describe microphones, captions, interpretation, or assistive listening availability.]</li>
        <li><strong>Dietary access:</strong> [Explain how to request allergy-aware, vegetarian, vegan, halal, kosher, or other options.]</li>
        <li><strong>Low-sensory space:</strong> [Describe any quiet room or low-sensory area.]</li>
      </ul>
    </section>

    <section class="section" id="related-events" aria-labelledby="related-events-heading">
      <div class="section-header">
        <p class="section-kicker">Related events</p>
        <h2 id="related-events-heading">Nearby or related meetings</h2>
        <p class="lead">Use this section for satellite meetings, workshops, or partner events.</p>
      </div>

      <div class="grid">
        <article class="card">
          <h3>[Related Event]</h3>
          <p>[Dates] • [Location]</p>
          <p><a href="https://example.com/related-event-1">[Related Event] website</a></p>
        </article>
        <article class="card">
          <h3>[Related Event]</h3>
          <p>[Dates] • [Location]</p>
          <p><a href="https://example.com/related-event-2">[Related Event] website</a></p>
        </article>
        <article class="card">
          <h3>[Partner Organization]</h3>
          <p>[Brief description of partnership or support.]</p>
          <p><a href="https://example.com/partner">[Partner Organization] website</a></p>
        </article>
      </div>
    </section>

    <section class="section" id="organizers" aria-labelledby="organizers-heading">
      <div class="section-header">
        <p class="section-kicker">Organizers</p>
        <h2 id="organizers-heading">Organizing committee</h2>
        <p class="lead">Replace these cards with the committee members and affiliations.</p>
      </div>

      <ul class="person-grid" aria-label="Organizing committee">
        <li class="person-card">
          <h3>[Organizer Name]</h3>
          <p>[Institution]</p>
          <a href="https://example.com/organizer-1">[Organizer Name] webpage</a>
        </li>
        <li class="person-card">
          <h3>[Organizer Name]</h3>
          <p>[Institution]</p>
          <a href="https://example.com/organizer-2">[Organizer Name] webpage</a>
        </li>
        <li class="person-card">
          <h3>[Organizer Name]</h3>
          <p>[Institution]</p>
          <a href="https://example.com/organizer-3">[Organizer Name] webpage</a>
        </li>
      </ul>

      <div class="card" style="margin-top: 1rem;">
        <h3>Sponsors and acknowledgments</h3>
        <p>[Conference Name] gratefully acknowledges support from [sponsors, departments, grants, institutes].</p>
        <ul class="sponsors" aria-label="Sponsor placeholders">
          <li>[Sponsor]</li>
          <li>[Sponsor]</li>
          <li>[Sponsor]</li>
        </ul>
      </div>
    </section>
  </main>

  <footer class="footer">
    <div class="wrap">
      <div>
        <h2>[Conference Name]</h2>
        <p>[Host Unit], Rutgers University<br>[Campus or city]</p>
        <address>
          Contact: <a href="mailto:[contact-email@example.edu]">[contact-email@example.edu]</a>
        </address>
      </div>

      <nav class="footer-nav" aria-label="Footer navigation">
        <h3>Site sections</h3>
        <ul>
          <li><a href="#about">About</a></li>
          <li><a href="#speakers">Speakers</a></li>
          <li><a href="#program">Program</a></li>
          <li><a href="#venue">Venue &amp; Travel</a></li>
          <li><a href="#registration">Registration</a></li>
          <li><a href="#accessibility">Accessibility</a></li>
          <li><a href="#organizers">Organizers</a></li>
        </ul>
      </nav>
    </div>

    <div class="footer-small">
      <div class="wrap">
        <p><strong>Accessibility statement:</strong> [Conference Name] is committed to equal access for participants with disabilities. Please report website accessibility issues or accommodation needs to <a href="mailto:[accessibility-contact@example.edu]">[accessibility-contact@example.edu]</a>.</p>
        <p class="muted">Last updated: [Month Day, Year]. Replace all placeholders before publishing.</p>
      </div>
    </div>
  </footer>
</body>
</html>
