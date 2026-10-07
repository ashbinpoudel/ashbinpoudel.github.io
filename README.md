# ashbinpoudel.github.io/home.html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <title>Aashwin Poudel — Agriculture • Research • Data</title>

  <meta
    name="description"
    content="Personal portfolio of Aashwin Poudel — Agriculture, crop protection, entomology, data analysis and creative design."
  />

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

  <link
    href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Space+Grotesk:wght@400;500;600;700&display=swap"
    rel="stylesheet"
  />

  <style>

    /* =========================
       RESET
    ========================= */

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      background: #0b0e0c;
      color: #f1f3ed;
      font-family: "DM Sans", sans-serif;
      line-height: 1.6;
      overflow-x: hidden;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    img {
      width: 100%;
      display: block;
    }

    button {
      font-family: inherit;
    }


    /* =========================
       VARIABLES
    ========================= */

    :root {
      --bg: #0b0e0c;
      --bg-soft: #111612;
      --card: #151b16;
      --card-light: #1a211b;

      --white: #f1f3ed;
      --muted: #9da69d;

      --green: #a6c47c;
      --green-dark: #718d50;

      --orange: #e56a2f;

      --border: rgba(255,255,255,0.09);

      --radius: 24px;
    }


    /* =========================
       CUSTOM SCROLLBAR
    ========================= */

    ::-webkit-scrollbar {
      width: 8px;
    }

    ::-webkit-scrollbar-track {
      background: var(--bg);
    }

    ::-webkit-scrollbar-thumb {
      background: #303a31;
      border-radius: 20px;
    }


    /* =========================
       NAVIGATION
    ========================= */

    nav {
      position: fixed;
      top: 18px;
      left: 50%;
      transform: translateX(-50%);

      width: min(92%, 1100px);

      display: flex;
      justify-content: space-between;
      align-items: center;

      padding: 13px 18px;

      background: rgba(15, 19, 16, 0.78);
      backdrop-filter: blur(18px);

      border: 1px solid var(--border);
      border-radius: 100px;

      z-index: 1000;
    }

    .logo {
      font-family: "Space Grotesk", sans-serif;
      font-weight: 700;
      font-size: 19px;
      letter-spacing: -0.5px;

      display: flex;
      align-items: center;
      gap: 8px;
    }

    .logo-dot {
      width: 9px;
      height: 9px;
      background: var(--green);
      border-radius: 50%;
      box-shadow: 0 0 18px rgba(166,196,124,0.5);
    }

    .nav-links {
      display: flex;
      gap: 28px;
      list-style: none;
      color: #b9c0b8;
      font-size: 14px;
    }

    .nav-links a {
      transition: 0.25s;
    }

    .nav-links a:hover {
      color: var(--white);
    }

    .nav-button {
      background: var(--green);
      color: #10140f;
      padding: 9px 17px;
      border-radius: 100px;
      font-weight: 700;
      font-size: 13px;
      transition: 0.25s;
    }

    .nav-button:hover {
      transform: translateY(-2px);
      background: #bad88d;
    }


    /* =========================
       HERO
    ========================= */

    .hero {
      min-height: 100vh;
      position: relative;

      display: flex;
      align-items: center;

      padding: 150px 7% 100px;

      overflow: hidden;
    }

    .hero::before {
      content: "";

      position: absolute;

      width: 600px;
      height: 600px;

      left: -200px;
      top: 100px;

      background: rgba(113,141,80,0.13);

      filter: blur(100px);
      border-radius: 50%;
    }

    .hero-grid {
      position: absolute;
      inset: 0;

      background-image:
        linear-gradient(rgba(255,255,255,0.025) 1px, transparent 1px),
        linear-gradient(90deg, rgba(255,255,255,0.025) 1px, transparent 1px);

      background-size: 70px 70px;

      mask-image: linear-gradient(to bottom, black, transparent 80%);

      pointer-events: none;
    }

    .hero-content {
      width: min(1200px, 100%);
      margin: auto;

      display: grid;
      grid-template-columns: 1.15fr 0.85fr;

      align-items: center;
      gap: 70px;

      position: relative;
      z-index: 2;
    }

    .eyebrow {
      color: var(--green);
      text-transform: uppercase;
      letter-spacing: 3px;
      font-size: 11px;
      font-weight: 700;

      margin-bottom: 22px;

      display: flex;
      align-items: center;
      gap: 10px;
    }

    .eyebrow::before {
      content: "";
      width: 30px;
      height: 1px;
      background: var(--green);
    }

    h1 {
      font-family: "Space Grotesk", sans-serif;

      font-size: clamp(55px, 7.5vw, 105px);

      line-height: 0.93;
      letter-spacing: -5px;

      max-width: 850px;
    }

    h1 span {
      color: var(--green);
    }

    .hero-description {
      margin-top: 30px;

      max-width: 620px;

      color: var(--muted);

      font-size: 17px;
      line-height: 1.8;
    }

    .hero-actions {
      display: flex;
      gap: 13px;
      margin-top: 35px;
      flex-wrap: wrap;
    }

    .primary-button {
      padding: 14px 22px;
      background: var(--green);
      color: #11150f;

      border-radius: 100px;

      font-size: 14px;
      font-weight: 700;

      transition: 0.25s;
    }

    .primary-button:hover {
      transform: translateY(-3px);
      box-shadow: 0 12px 30px rgba(166,196,124,0.15);
    }

    .secondary-button {
      padding: 14px 22px;

      border: 1px solid var(--border);
      border-radius: 100px;

      color: var(--white);

      font-size: 14px;
      font-weight: 600;

      transition: 0.25s;
    }

    .secondary-button:hover {
      background: rgba(255,255,255,0.05);
    }


    /* HERO IMAGE */

    .hero-image {
      position: relative;
    }

    .hero-image img {
      height: 590px;
      object-fit: cover;

      border-radius: 35px;

      filter: saturate(0.75) contrast(1.05);
    }

    .hero-image::after {
      content: "";

      position: absolute;
      inset: 0;

      border-radius: 35px;

      background:
        linear-gradient(
          180deg,
          rgba(10,15,11,0.05),
          rgba(10,15,11,0.6)
        );
    }

    .hero-tag {
      position: absolute;

      bottom: 22px;
      left: 22px;

      z-index: 3;

      padding: 12px 15px;

      background: rgba(12,16,13,0.75);
      backdrop-filter: blur(15px);

      border: 1px solid var(--border);

      border-radius: 15px;

      font-size: 12px;
      color: #d9dfd5;
    }


    /* =========================
       SECTION
    ========================= */

    section {
      padding: 120px 7%;
    }

    .section-inner {
      max-width: 1200px;
      margin: auto;
    }

    .section-heading {
      max-width: 700px;
      margin-bottom: 55px;
    }

    .section-label {
      color: var(--green);

      text-transform: uppercase;
      letter-spacing: 2.5px;

      font-size: 11px;
      font-weight: 700;

      margin-bottom: 15px;
    }

    h2 {
      font-family: "Space Grotesk", sans-serif;

      font-size: clamp(38px, 5vw, 66px);

      line-height: 1;
      letter-spacing: -3px;
    }

    .section-heading p {
      color: var(--muted);
      margin-top: 20px;
      font-size: 16px;
    }


    /* =========================
       ABOUT
    ========================= */

    .about {
      background: var(--bg-soft);
    }

    .about-grid {
      display: grid;

      grid-template-columns: 0.9fr 1.1fr;

      gap: 80px;

      align-items: start;
    }

    .about-photo {
      height: 520px;

      overflow: hidden;
      border-radius: var(--radius);

      position: relative;
    }

    .about-photo img {
      height: 100%;
      object-fit: cover;
      filter: saturate(0.7);
    }

    .about-photo::after {
      content: "";

      position: absolute;
      inset: 0;

      background: linear-gradient(
        180deg,
        transparent 45%,
        rgba(5,9,6,0.65)
      );
    }

    .about-content h3 {
      font-family: "Space Grotesk", sans-serif;

      font-size: 31px;
      line-height: 1.15;

      margin-bottom: 25px;
    }

    .about-content p {
      color: var(--muted);

      font-size: 16px;
      line-height: 1.85;

      margin-bottom: 18px;
    }

    .about-highlight {
      margin-top: 35px;

      display: grid;
      grid-template-columns: repeat(3, 1fr);

      gap: 12px;
    }

    .highlight {
      border: 1px solid var(--border);
      background: rgba(255,255,255,0.025);

      padding: 20px;

      border-radius: 17px;
    }

    .highlight strong {
      display: block;

      font-family: "Space Grotesk", sans-serif;
      font-size: 25px;

      color: var(--green);

      margin-bottom: 4px;
    }

    .highlight span {
      color: var(--muted);
      font-size: 12px;
    }


    /* =========================
       INTERESTS
    ========================= */

    .interest-grid {
      display: grid;

      grid-template-columns: repeat(4, 1fr);

      gap: 15px;
    }

    .interest {
      min-height: 250px;

      border: 1px solid var(--border);

      border-radius: var(--radius);

      padding: 28px;

      background: var(--card);

      position: relative;

      overflow: hidden;

      transition: 0.3s;
    }

    .interest:hover {
      transform: translateY(-6px);
      background: var(--card-light);
      border-color: rgba(166,196,124,0.25);
    }

    .interest-number {
      color: #5e675f;
      font-size: 12px;
      font-weight: 700;
    }

    .interest-icon {
      margin-top: 35px;

      width: 44px;
      height: 44px;

      border-radius: 12px;

      display: grid;
      place-items: center;

      background: rgba(166,196,124,0.1);

      color: var(--green);

      font-size: 21px;
    }

    .interest h3 {
      margin-top: 22px;

      font-family: "Space Grotesk", sans-serif;
      font-size: 21px;
    }

    .interest p {
      color: var(--muted);

      margin-top: 10px;

      font-size: 13px;
      line-height: 1.6;
    }


    /* =========================
       PROJECTS
    ========================= */

    .projects {
      background: var(--bg-soft);
    }

    .project-grid {
      display: grid;

      grid-template-columns: repeat(2, 1fr);

      gap: 20px;
    }

    .project {
      background: var(--card);

      border: 1px solid var(--border);

      border-radius: var(--radius);

      overflow: hidden;

      transition: 0.3s;
    }

    .project:hover {
      transform: translateY(-5px);
      border-color: rgba(166,196,124,0.2);
    }

    .project-image {
      height: 300px;

      overflow: hidden;
    }

    .project-image img {
      height: 100%;
      object-fit: cover;

      transition: 0.5s;
    }

    .project:hover .project-image img {
      transform: scale(1.04);
    }

    .project-info {
      padding: 27px;
    }

    .project-type {
      color: var(--green);

      text-transform: uppercase;

      letter-spacing: 2px;

      font-size: 10px;
      font-weight: 700;
    }

    .project h3 {
      margin-top: 10px;

      font-family: "Space Grotesk", sans-serif;

      font-size: 27px;

      letter-spacing: -1px;
    }

    .project p {
      margin-top: 12px;

      color: var(--muted);

      font-size: 14px;
      line-height: 1.7;
    }

    .project-tags {
      margin-top: 22px;

      display: flex;
      flex-wrap: wrap;
      gap: 7px;
    }

    .project-tags span {
      padding: 6px 10px;

      border: 1px solid var(--border);

      border-radius: 100px;

      color: #aeb7ad;

      font-size: 10px;
    }


    /* FEATURED PROJECT */

    .featured-project {
      margin-top: 20px;

      display: grid;
      grid-template-columns: 1fr 1fr;

      background: var(--card);

      border: 1px solid var(--border);

      border-radius: var(--radius);

      overflow: hidden;
    }

    .featured-image {
      min-height: 430px;
    }

    .featured-image img {
      height: 100%;
      object-fit: cover;
    }

    .featured-content {
      padding: 55px;

      display: flex;
      flex-direction: column;
      justify-content: center;
    }

    .featured-content .project-type {
      color: var(--orange);
    }

    .featured-content h3 {
      font-family: "Space Grotesk", sans-serif;

      font-size: clamp(35px, 4vw, 52px);

      line-height: 1;

      letter-spacing: -2px;

      margin-top: 15px;
    }

    .featured-content p {
      color: var(--muted);

      margin-top: 22px;

      line-height: 1.8;
    }

    .research-result {
      margin-top: 28px;

      padding: 18px;

      border-left: 2px solid var(--green);

      background: rgba(166,196,124,0.05);
    }

    .research-result small {
      color: var(--green);

      text-transform: uppercase;
      letter-spacing: 1.5px;

      font-size: 9px;
      font-weight: 700;
    }

    .research-result p {
      margin-top: 6px;
      font-size: 13px;
    }


    /* =========================
       DATA SECTION
    ========================= */

    .data-section {
      padding-top: 100px;
    }

    .data-layout {
      display: grid;

      grid-template-columns: 1fr 1fr;

      gap: 20px;
    }

    .data-card {
      padding: 35px;

      border: 1px solid var(--border);

      border-radius: var(--radius);

      background: var(--card);
    }

    .data-card h3 {
      font-family: "Space Grotesk", sans-serif;

      font-size: 28px;

      margin-bottom: 25px;
    }

    .bar {
      margin-bottom: 20px;
    }

    .bar-top {
      display: flex;
      justify-content: space-between;

      margin-bottom: 8px;

      font-size: 13px;
    }

    .bar-top span:last-child {
      color: var(--green);
    }

    .bar-track {
      height: 5px;

      background: #252c26;

      border-radius: 10px;

      overflow: hidden;
    }

    .bar-fill {
      height: 100%;

      background: var(--green);

      border-radius: 10px;
    }

    .tools {
      display: flex;

      flex-wrap: wrap;

      gap: 9px;
    }

    .tool {
      padding: 11px 14px;

      border: 1px solid var(--border);

      border-radius: 12px;

      color: #c4cbc3;

      font-size: 13px;

      background: rgba(255,255,255,0.02);
    }


    /* =========================
       EDUCATION
    ========================= */

    .timeline {
      position: relative;

      border-left: 1px solid #313831;

      margin-left: 10px;
    }

    .timeline-item {
      position: relative;

      padding: 0 0 55px 45px;
    }

    .timeline-item:last-child {
      padding-bottom: 0;
    }

    .timeline-dot {
      position: absolute;

      left: -6px;
      top: 5px;

      width: 11px;
      height: 11px;

      border-radius: 50%;

      background: var(--green);

      box-shadow: 0 0 0 6px var(--bg);
    }

    .timeline-date {
      color: var(--green);

      font-size: 11px;

      text-transform: uppercase;

      letter-spacing: 2px;

      font-weight: 700;
    }

    .timeline h3 {
      font-family: "Space Grotesk", sans-serif;

      font-size: 25px;

      margin-top: 7px;
    }

    .timeline p {
      color: var(--muted);

      font-size: 14px;

      margin-top: 5px;
    }


    /* =========================
       CREATIVE SIDE
    ========================= */

    .creative {
      background: var(--bg-soft);
    }

    .creative-grid {
      display: grid;

      grid-template-columns: 1.2fr 0.8fr;

      gap: 20px;
    }

    .creative-main {
      min-height: 470px;

      border-radius: var(--radius);

      overflow: hidden;

      position: relative;
    }

    .creative-main img {
      height: 100%;

      object-fit: cover;

      filter: saturate(0.65);
    }

    .creative-main::after {
      content: "";

      position: absolute;

      inset: 0;

      background:
        linear-gradient(
          180deg,
          transparent 30%,
          rgba(4,6,5,0.9)
        );
    }

    .creative-text {
      position: absolute;

      bottom: 35px;
      left: 35px;

      z-index: 2;

      max-width: 480px;
    }

    .creative-text h3 {
      font-family: "Space Grotesk", sans-serif;

      font-size: 43px;

      line-height: 1;

      letter-spacing: -2px;
    }

    .creative-text p {
      color: #c2c8c1;

      margin-top: 13px;

      font-size: 14px;
    }

    .creative-side {
      display: grid;

      grid-template-rows: 1fr 1fr;

      gap: 20px;
    }

    .creative-card {
      border: 1px solid var(--border);

      background: var(--card);

      border-radius: var(--radius);

      padding: 30px;

      display: flex;

      flex-direction: column;

      justify-content: space-between;
    }

    .creative-card span {
      color: var(--orange);

      font-size: 11px;

      text-transform: uppercase;

      letter-spacing: 2px;

      font-weight: 700;
    }

    .creative-card h3 {
      font-family: "Space Grotesk", sans-serif;

      font-size: 27px;

      line-height: 1.1;
    }

    .creative-card p {
      color: var(--muted);

      font-size: 13px;
    }


    /* =========================
       CONTACT
    ========================= */

    .contact {
      text-align: center;

      padding: 150px 7%;
    }

    .contact .section-label {
      justify-content: center;
    }

    .contact h2 {
      max-width: 850px;

      margin: auto;
    }

    .contact h2 span {
      color: var(--green);
    }

    .contact-description {
      max-width: 570px;

      margin: 25px auto 35px;

      color: var(--muted);
    }

    .contact-links {
      display: flex;

      justify-content: center;

      flex-wrap: wrap;

      gap: 10px;
    }

    .contact-link {
      padding: 13px 19px;

      border: 1px solid var(--border);

      border-radius: 100px;

      color: #c7cdc5;

      font-size: 13px;

      transition: 0.25s;
    }

    .contact-link:hover {
      border-color: var(--green);
      color: var(--green);
    }


    /* =========================
       FOOTER
    ========================= */

    footer {
      border-top: 1px solid var(--border);

      padding: 25px 7%;

      display: flex;

      justify-content: space-between;

      align-items: center;

      color: #727a72;

      font-size: 11px;
    }

    .footer-mark {
      font-family: "Space Grotesk", sans-serif;

      color: #b0b8af;

      font-weight: 700;
    }


    /* =========================
       RESPONSIVE
    ========================= */

    @media (max-width: 900px) {

      .nav-links {
        display: none;
      }

      .hero-content,
      .about-grid,
      .featured-project,
      .data-layout,
      .creative-grid {
        grid-template-columns: 1fr;
      }

      .hero {
        padding-top: 130px;
      }

      .hero-image {
        max-width: 650px;
      }

      .hero-image img {
        height: 450px;
      }

      .interest-grid {
        grid-template-columns: repeat(2, 1fr);
      }

      .project-grid {
        grid-template-columns: 1fr;
      }

      .featured-image {
        min-height: 350px;
      }

      .creative-main {
        min-height: 400px;
      }
    }


    @media (max-width: 600px) {

      nav {
        top: 10px;
      }

      .nav-button {
        padding: 8px 13px;
      }

      section {
        padding: 80px 5%;
      }

      .hero {
        padding: 120px 5% 70px;
      }

      h1 {
        font-size: 55px;
        letter-spacing: -3px;
      }

      h2 {
        font-size: 42px;
      }

      .hero-image img {
        height: 400px;
      }

      .about-photo {
        height: 400px;
      }

      .about-highlight {
        grid-template-columns: 1fr;
      }

      .interest-grid {
        grid-template-columns: 1fr;
      }

      .featured-content {
        padding: 30px;
      }

      .featured-image {
        min-height: 300px;
      }

      .creative-side {
        grid-template-rows: auto;
      }

      .creative-card {
        min-height: 220px;
      }

      footer {
        flex-direction: column;
        gap: 10px;
        text-align: center;
      }
    }

  </style>
</head>


<body>


  <!-- =========================
       NAVIGATION
  ========================= -->

  <nav>

    <a href="#" class="logo">
      <span class="logo-dot"></span>
      AASHWIN
    </a>

    <ul class="nav-links">
      <li><a href="#about">About</a></li>
      <li><a href="#interests">Interests</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#skills">Skills</a></li>
    </ul>

    <a href="#contact" class="nav-button">
      Let's connect
    </a>

  </nav>



  <!-- =========================
       HERO
  ========================= -->

  <header class="hero">

    <div class="hero-grid"></div>

    <div class="hero-content">

      <div>

        <div class="eyebrow">
          Agriculture · Research · Data
        </div>

        <h1>
          Growing ideas<br>
          into <span>impact.</span>
        </h1>

        <p class="hero-description">
          I'm Aashwin Poudel — an agriculture graduate interested in
          crop protection, entomology, sustainable agriculture,
          data analysis and the intersection between science and technology.
        </p>

        <div class="hero-actions">

          <a href="#projects" class="primary-button">
            Explore my work →
          </a>

          <a href="#about" class="secondary-button">
            More about me
          </a>

        </div>

      </div>


      <div class="hero-image">

        <img
          src="https://images.unsplash.com/photo-1625246333195-78d9c38ad449?auto=format&fit=crop&w=1200&q=85"
          alt="Agricultural field"
        >

        <div class="hero-tag">
          Based in Nepal · Looking beyond the field
        </div>

      </div>

    </div>

  </header>



  <!-- =========================
       ABOUT
  ========================= -->

  <section class="about" id="about">

    <div class="section-inner">

      <div class="about-grid">

        <div class="about-photo">

          <img
            src="https://images.unsplash.com/photo-1492496913980-501348b61469?auto=format&fit=crop&w=1000&q=85"
            alt="Agricultural plants"
          >

        </div>


        <div class="about-content">

          <div class="section-label">
            01 / About
          </div>

          <h3>
            Agriculture is where my
            curiosity started — research
            is where I want to take it.
          </h3>

          <p>
            With a background in Agriculture, I've developed a strong
            interest in understanding how crops, insects, environments
            and agricultural systems interact.
          </p>

          <p>
            My academic interests have gradually moved toward
            crop protection and entomology, while my work with
            agricultural datasets has introduced me to statistical
            analysis, visualization and reproducible research.
          </p>

          <p>
            Outside the traditional agricultural path, I also enjoy
            creative digital work — particularly visual design,
            email design and building clean digital experiences.
          </p>


          <div class="about-highlight">

            <div class="highlight">
              <strong>72.6%</strong>
              <span>Bachelor's academic result</span>
            </div>

            <div class="highlight">
              <strong>Ag</strong>
              <span>Agriculture background</span>
            </div>

            <div class="highlight">
              <strong>∞</strong>
              <span>Curiosity to learn</span>
            </div>

          </div>

        </div>

      </div>

    </div>

  </section>



  <!-- =========================
       INTERESTS
  ========================= -->

  <section id="interests">

    <div class="section-inner">

      <div class="section-heading">

        <div class="section-label">
          02 / Interests
        </div>

        <h2>
          Where my curiosity lives.
        </h2>

        <p>
          A mix of biological science, agriculture, technology
          and creative problem solving.
        </p>

      </div>


      <div class="interest-grid">


        <div class="interest">

          <span class="interest-number">01</span>

          <div class="interest-icon">⌁</div>

          <h3>Entomology</h3>

          <p>
            Understanding insects, crop–pest interactions
            and sustainable approaches to pest management.
          </p>

        </div>


        <div class="interest">

          <span class="interest-number">02</span>

          <div class="interest-icon">✦</div>

          <h3>Crop Protection</h3>

          <p>
            Exploring practical and sustainable strategies
            for protecting crops and improving productivity.
          </p>

        </div>


        <div class="interest">

          <span class="interest-number">03</span>

          <div class="interest-icon">⌘</div>

          <h3>Agricultural Data</h3>

          <p>
            Turning field experiments and agricultural datasets
            into useful insights through statistical analysis.
          </p>

        </div>


        <div class="interest">

          <span class="interest-number">04</span>

          <div class="interest-icon">↗</div>

          <h3>Digital Design</h3>

          <p>
            Designing visual experiences, marketing emails
            and digital interfaces that communicate clearly.
          </p>

        </div>

      </div>

    </div>

  </section>



  <!-- =========================
       PROJECTS
  ========================= -->

  <section class="projects" id="projects">

    <div class="section-inner">

      <div class="section-heading">

        <div class="section-label">
          03 / Selected work
        </div>

        <h2>
          Projects that shaped my thinking.
        </h2>

        <p>
          From field experiments to statistical analysis,
          these projects connect my academic interests with practical work.
        </p>

      </div>


      <!-- FEATURED RESEARCH -->

      <div class="featured-project">

        <div class="featured-image">

          <img
            src="https://images.unsplash.com/photo-1589923188900-85dae523342b?auto=format&fit=crop&w=1200&q=85"
            alt="Cabbage crop"
          >

        </div>


        <div class="featured-content">

          <div class="project-type">
            Featured research
          </div>

          <h3>
            Botanical approaches
            to diamondback moth
            management
          </h3>

          <p>
            An undergraduate research project investigating the
            efficacy of botanical treatments against diamondback
            moth on cabbage.
          </p>

          <div class="research-result">

            <small>
              Research direction
            </small>

            <p>
              Crop protection · Botanical pesticides ·
              Brassica crops · Insect management
            </p>

          </div>

        </div>

      </div>



      <!-- OTHER PROJECTS -->

      <div class="project-grid" style="margin-top:20px;">


        <article class="project">

          <div class="project-image">

            <img
              src="https://images.unsplash.com/photo-1530267981375-f0de937f5f13?auto=format&fit=crop&w=1000&q=85"
              alt="Wheat field"
            >

          </div>

          <div class="project-info">

            <div class="project-type">
              Data analysis
            </div>

            <h3>
              Wheat genotype × environment analysis
            </h3>

            <p>
              Working with multi-year wheat trial data to
              investigate genotype performance, traits and
              environmental effects.
            </p>

            <div class="project-tags">
              <span>R</span>
              <span>Mixed Models</span>
              <span>Field Trials</span>
              <span>Visualization</span>
            </div>

          </div>

        </article>



        <article class="project">

          <div class="project-image">

            <img
              src="https://images.unsplash.com/photo-1536657464919-892534f60d6e?auto=format&fit=crop&w=1000&q=85"
              alt="Agricultural research"
            >

          </div>

          <div class="project-info">

            <div class="project-type">
              Future research
            </div>

            <h3>
              Sustainable crop protection
            </h3>

            <p>
              Exploring how biological knowledge, integrated pest
              management and modern agricultural technologies can
              work together.
            </p>

            <div class="project-tags">
              <span>IPM</span>
              <span>Entomology</span>
              <span>Biological Control</span>
            </div>

          </div>

        </article>


      </div>

    </div>

  </section>



  <!-- =========================
       DATA / SKILLS
  ========================= -->

  <section id="skills" class="data-section">

    <div class="section-inner">

      <div class="section-heading">

        <div class="section-label">
          04 / Skills
        </div>

        <h2>
          Science meets data.
        </h2>

        <p>
          I'm especially interested in using quantitative tools
          to make agricultural research more understandable and useful.
        </p>

      </div>


      <div class="data-layout">


        <div class="data-card">

          <h3>
            Areas of focus
          </h3>


          <div class="bar">

            <div class="bar-top">
              <span>Agricultural Science</span>
              <span>90%</span>
            </div>

            <div class="bar-track">
              <div class="bar-fill" style="width:90%;"></div>
            </div>

          </div>


          <div class="bar">

            <div class="bar-top">
              <span>Crop Protection</span>
              <span>85%</span>
            </div>

            <div class="bar-track">
              <div class="bar-fill" style="width:85%;"></div>
            </div>

          </div>


          <div class="bar">

            <div class="bar-top">
              <span>Data Analysis</span>
              <span>75%</span>
            </div>

            <div class="bar-track">
              <div class="bar-fill" style="width:75%;"></div>
            </div>

          </div>


          <div class="bar">

            <div class="bar-top">
              <span>Research</span>
              <span>80%</span>
            </div>

            <div class="bar-track">
              <div class="bar-fill" style="width:80%;"></div>
            </div>

          </div>

        </div>



        <div class="data-card">

          <h3>
            Tools & methods
          </h3>

          <div class="tools">

            <div class="tool">R</div>
            <div class="tool">RStudio</div>
            <div class="tool">Statistics</div>
            <div class="tool">Data Visualization</div>
            <div class="tool">Experimental Design</div>
            <div class="tool">Field Research</div>
            <div class="tool">Crop Protection</div>
            <div class="tool">Entomology</div>
            <div class="tool">Figma</div>
            <div class="tool">Email Design</div>
            <div class="tool">Visual Communication</div>

          </div>

        </div>


      </div>

    </div>

  </section>



  <!-- =========================
       EDUCATION
  ========================= -->

  <section>

    <div class="section-inner">

      <div class="section-heading">

        <div class="section-label">
          05 / Journey
        </div>

        <h2>
          From agriculture to research.
        </h2>

      </div>


      <div class="timeline">


        <div class="timeline-item">

          <div class="timeline-dot"></div>

          <div class="timeline-date">
            2021 — 2025
          </div>

          <h3>
            Bachelor of Agriculture
          </h3>

          <p>
            Institute of Agriculture and Animal Science,
            Lamjung Campus — Tribhuvan University.
          </p>

        </div>


        <div class="timeline-item">

          <div class="timeline-dot"></div>

          <div class="timeline-date">
            Undergraduate research
          </div>

          <h3>
            Crop Protection & Entomology
          </h3>

          <p>
            Research focused on botanical approaches for
            managing diamondback moth in cabbage.
          </p>

        </div>


        <div class="timeline-item">

          <div class="timeline-dot"></div>

          <div class="timeline-date">
            Current direction
          </div>

          <h3>
            Graduate Research
          </h3>

          <p>
            Exploring graduate opportunities in agriculture,
            crop protection, entomology, biotechnology and
            agricultural data science.
          </p>

        </div>


      </div>

    </div>

  </section>



  <!-- =========================
       CREATIVE WORK
  ========================= -->

  <section class="creative">

    <div class="section-inner">

      <div class="section-heading">

        <div class="section-label">
          06 / Beyond agriculture
        </div>

        <h2>
          I also build things
          outside the lab.
        </h2>

        <p>
          Design has become another way for me to solve problems —
          visually, simply and creatively.
        </p>

      </div>


      <div class="creative-grid">


        <div class="creative-main">

          <img
            src="https://images.unsplash.com/photo-1558655146-d09347e92766?auto=format&fit=crop&w=1400&q=85"
            alt="Creative design workspace"
          >

          <div class="creative-text">

            <h3>
              Science is only useful
              when people can understand it.
            </h3>

            <p>
              That's why I enjoy combining research,
              visual storytelling and digital design.
            </p>

          </div>

        </div>


        <div class="creative-side">


          <div class="creative-card">

            <span>Creative work</span>

            <h3>
              Email & visual design
            </h3>

            <p>
              Creating clean marketing emails, product
              layouts and visual systems using Figma.
            </p>

          </div>


          <div class="creative-card">

            <span>My approach</span>

            <h3>
              Simple. Useful. Intentional.
            </h3>

            <p>
              Whether it's a research graph or a landing page,
              I prefer clarity over unnecessary complexity.
            </p>

          </div>


        </div>

      </div>

    </div>

  </section>



  <!-- =========================
       CONTACT
  ========================= -->

  <section class="contact" id="contact">

    <div class="section-inner">

      <div class="section-label">
        07 / Let's connect
      </div>

      <h2>
        Interested in agriculture,
        <span>research</span> or
        building something?
      </h2>

      <p class="contact-description">
        I'm always interested in conversations around agricultural
        research, graduate opportunities, crop protection,
        data analysis and creative work.
      </p>


      <div class="contact-links">

        <a
          href="mailto:your-email@example.com"
          class="contact-link"
        >
          Email ↗
        </a>

        <a
          href="#"
          class="contact-link"
        >
          LinkedIn ↗
        </a>

        <a
          href="#"
          class="contact-link"
        >
          GitHub ↗
        </a>

      </div>

    </div>

  </section>



  <!-- =========================
       FOOTER
  ========================= -->

  <footer>

    <div class="footer-mark">
      AASHWIN POUD<span style="color:var(--green);">.</span>EL
    </div>

    <div>
      Agriculture · Research · Data · Design
    </div>

    <div>
      © 2026
    </div>

  </footer>



  <!-- =========================
       SMALL INTERACTION
  ========================= -->

  <script>

    // Add a subtle navigation effect when scrolling

    const nav = document.querySelector("nav");

    window.addEventListener("scroll", () => {

      if (window.scrollY > 50) {

        nav.style.background = "rgba(11, 14, 12, 0.92)";

      } else {

        nav.style.background = "rgba(15, 19, 16, 0.78)";

      }

    });

  </script>


</body>
</html>
