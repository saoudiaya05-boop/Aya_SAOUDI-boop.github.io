# Aya_SAOUDI-boop.github.io
# My personal portfolio
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <title>Aya Saoudi | Portfolio</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />

    <!-- Fonts & Icons -->
    <link
      href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&family=Playfair+Display:wght@600&display=swap"
      rel="stylesheet"
    />
    <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css"
    />

    <style>
      :root {
        --primary: #e38cb7;
        --secondary: #5b2a86;
        --bg: #fff7f0;
        --dark: #2e2e2e;
      }

      * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
      }
      html {
        scroll-behavior: smooth;
      }
      body {
        font-family: Poppins, sans-serif;
        background: var(--bg);
        color: var(--dark);
        overflow-x: hidden;
      }

      /* CUSTOM CURSOR */
      .cursor {
        width: 18px;
        height: 18px;
        border: 2px solid var(--primary);
        border-radius: 50%;
        position: fixed;
        pointer-events: none;
        transform: translate(-50%, -50%);
        z-index: 9999;
        transition: 0.15s ease;
      }

      /* NAVBAR */
      header {
        position: fixed;
        top: 0;
        width: 100%;
        background: #fff;
        padding: 15px 50px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        z-index: 1000;
      }
      header h2 {
        font-family: "Playfair Display";
        color: var(--secondary);
      }
      nav a {
        margin-left: 25px;
        text-decoration: none;
        color: #444;
        font-weight: 500;
      }
      nav a:hover {
        color: var(--primary);
      }

      /* SECTIONS */
      section {
        padding: 110px 10%;
        opacity: 0;
        transform: translateY(50px);
        transition: 1s ease;
      }
      section.show {
        opacity: 1;
        transform: translateY(0);
      }

      /* HOME */
      #home {
        min-height: 100vh;
        background: linear-gradient(135deg, #fff1f7, #f6ecff);
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
        position: relative;
        overflow: hidden;
      }

      .home-content h1 {
        font-size: 3.2rem;
        color: var(--secondary);
      }
      #typing {
        font-size: 1.3rem;
        color: #555;
        font-weight: 500;
      }

      /* PROFILE IMAGE */
     .profile-wrapper {
  width: 180px;
  height: 180px;
  margin: 0 auto 25px;
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
}

.profile-wrapper i {
  font-size: 120px;
  color: var(--secondary);
  animation: spin 4s linear infinite;
}

@keyframes spin {
  from { transform: rotate(0deg); }
  to { transform: rotate(360deg); }
}


      /* SOCIAL */
      .social-icons a {
        margin: 0 12px;
        font-size: 1.6rem;
        color: var(--primary);
      }

      /* FLOATING ICONS */
      .bg-icons i {
        position: absolute;
        font-size: 60px;
        color: rgba(227, 140, 183, 0.18);
        animation: float 7s infinite;
      }
      .bg-icons i:nth-child(1) {
        top: 10%;
        left: 10%;
      }
      .bg-icons i:nth-child(2) {
        bottom: 15%;
        right: 15%;
      }
      .bg-icons i:nth-child(3) {
        top: 30%;
        right: 8%;
      }

      @keyframes float {
        0%,
        100% {
          transform: translateY(0);
        }
        50% {
          transform: translateY(-25px);
        }
      }

      /* ABOUT */
      .about-container {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 50px;
      }
      .formation {
        border-left: 4px solid var(--primary);
        padding-left: 20px;
        margin-bottom: 25px;
      }
      .formation span {
        font-weight: 600;
        color: var(--secondary);
      }
      .about-text p {
        line-height: 1.9;
      }

      /* SKILLS */
      #skills {
        background: #fff0f8;
        text-align: center;
      }
      .skills-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
        gap: 25px;
        margin-top: 40px;
      }
      .skill-card {
        background: rgba(255, 255, 255, 0.55);
        backdrop-filter: blur(14px);
        padding: 25px;
        border-radius: 20px;
        box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15);
        transition: 0.4s;
      }
      .skill-card:hover {
        transform: translateY(-12px);
      }
      .skill-card i {
        font-size: 2.2rem;
        color: var(--primary);
      }

      /* CONTACT */
      form {
        max-width: 450px;
        margin: auto;
      }
      input,
      textarea {
        width: 100%;
        padding: 12px;
        margin-bottom: 15px;
        border-radius: 8px;
        border: 1px solid #ccc;
      }
      button {
        background: var(--secondary);
        color: white;
        border: none;
        padding: 12px 35px;
        border-radius: 30px;
        cursor: pointer;
      }
      button:hover {
        transform: scale(1.05);
        box-shadow: 0 10px 30px rgba(227, 140, 183, 0.6);
      }

      /* RESPONSIVE */
      @media (max-width: 768px) {
        .about-container {
          grid-template-columns: 1fr;
        }
        header {
          padding: 15px 25px;
        }
      }
    </style>
  </head>
  <body>
    <div class="cursor"></div>

    <header>
      <h2>Aya Saoudi</h2>
      <nav>
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#skills">Skills</a>
        <a href="#contact">Contact</a>
      </nav>
    </header>

   <!-- HOME -->
<section id="home">
  <div class="bg-icons">
    <i class="fas fa-code"></i>
    <i class="fas fa-shield-halved"></i>
    <i class="fas fa-laptop-code"></i>
  </div>

  <div class="home-content">
    <div class="profile-wrapper">
      <i class="fas fa-user-shield"></i>
    </div>

    <h1>Aya Saoudi</h1>
    <p><span id="typing"></span></p>

    <div class="social-icons">
      <a href="mailto:aya@email.com"><i class="fas fa-envelope"></i></a>
      <a href="#"><i class="fab fa-instagram"></i></a>
      <a href="#"><i class="fab fa-linkedin"></i></a>
    </div>
  </div>
</section>

    <!-- ABOUT -->
    <section id="about">
      <div class="about-container">
        <div>
          <h3>Formations</h3>
          <div class="formation">
            <span>2023 – 2025</span>
            <p>Web Development</p>
          </div>
          <div class="formation">
            <span>2025 – Present</span>
            <p>Cybersecurity Analyst</p>
          </div>
        </div>

        <div class="about-text">
          <h3>About Me</h3>
          <p>
            I am Aya Saoudi, a passionate web developer with a creative eye and
            growing expertise in cybersecurity. I love crafting elegant
            interfaces while ensuring secure and reliable digital solutions.
          </p>
        </div>
      </div>
    </section>

    <!-- SKILLS -->
    <section id="skills">
      <h2>Skills</h2>
      <div class="skills-grid">
        <div class="skill-card">
          <i class="fab fa-html5"></i>
          <p>HTML</p>
        </div>
        <div class="skill-card">
          <i class="fab fa-css3-alt"></i>
          <p>CSS</p>
        </div>
        <div class="skill-card">
          <i class="fab fa-js"></i>
          <p>JavaScript</p>
        </div>
        <div class="skill-card">
          <i class="fab fa-react"></i>
          <p>React</p>
        </div>
        <div class="skill-card">
          <i class="fas fa-lock"></i>
          <p>Cybersecurity</p>
        </div>
      </div>
    </section>

    <!-- CONTACT -->
    <section id="contact">
      <h2>Contact</h2>
      <form>
        <input type="text" placeholder="Your Name" />
        <input type="email" placeholder="Your Email" />
        <textarea rows="5" placeholder="Your Message"></textarea>
        <button>Send</button>
      </form>
    </section>

    <script>
      // CURSOR
      const cursor = document.querySelector(".cursor");
      document.addEventListener("mousemove", (e) => {
        cursor.style.left = e.clientX + "px";
        cursor.style.top = e.clientY + "px";
      });

      // SCROLL ANIMATION
      const sections = document.querySelectorAll("section");
      const observer = new IntersectionObserver(
        (entries) => {
          entries.forEach((entry) => {
            if (entry.isIntersecting) {
              entry.target.classList.add("show");
            }
          });
        },
        { threshold: 0.15 }
      );
      sections.forEach((sec) => observer.observe(sec));

      // TYPING EFFECT
      const texts = [
        "Web Developer",
        "Cybersecurity Analyst",
        "Creative Designer",
      ];
      let i = 0,
        j = 0,
        isDeleting = false;
      const typing = document.getElementById("typing");

      function type() {
        let current = texts[i];
        typing.textContent = isDeleting
          ? current.substring(0, j--)
          : current.substring(0, j++);
        if (!isDeleting && j === current.length) {
          setTimeout(() => (isDeleting = true), 1500);
        }
        if (isDeleting && j === 0) {
          isDeleting = false;
          i = (i + 1) % texts.length;
        }
        setTimeout(type, isDeleting ? 70 : 120);
      }
      type();
    </script>
  </body>
</html>
