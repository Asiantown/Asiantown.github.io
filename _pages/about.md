---
permalink: /
title: "About Me"
excerpt: "About Me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<!-- Hero Intro Animation -->
<style>
  @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800&display=swap');
  
  /* Full screen intro cover */
  #intro-cover {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100vh;
    background: #111;
    color: #fff;
    font-family: 'Inter', sans-serif;
    display: flex;
    align-items: center;
    justify-content: center;
    z-index: 9999;
    transition: opacity 1s ease;
  }
  #intro-cover.fade-out {
    opacity: 0;
    pointer-events: none;
  }
  #intro-text {
    font-size: 4rem;
    font-weight: 800;
    text-align: center;
  }

  /* Hide main content until intro is done */
  #main-content {
    display: none;
  }
  #main-content.visible {
    display: block;
  }

  /* Hero section that stays at top */
  #hero-section {
    background: #111;
    color: #fff;
    font-family: 'Inter', sans-serif;
    text-align: center;
    padding: 3rem 1rem;
    font-size: 4rem;
    font-weight: 800;
  }
  @media (max-width: 768px) {
    #intro-text, #hero-section {
      font-size: 2.5rem;
    }
  }
</style>

<!-- Fullscreen intro (disappears after animation) -->
<div id="intro-cover">
  <div id="intro-text">Hi, I'm Ryan Yin</div>
</div>

{% raw %}
<script>
  document.addEventListener("DOMContentLoaded", function () {
    const cover = document.getElementById("intro-cover");
    const mainContent = document.getElementById("main-content");

    // After 4 seconds, fade out the intro cover
    setTimeout(() => {
      cover.classList.add("fade-out");
    }, 4000);

    // Remove it and show main content after fade
    setTimeout(() => {
      cover.style.display = "none";
      mainContent.classList.add("visible");
    }, 5000);
  });
</script>
{% endraw %}

<!-- All main page content is wrapped here -->
<div id="main-content">
  <!-- Permanent hero section at top of page -->
  <section id="hero-section">
    Hi, I'm Ryan Yin
  </section>

  <!-- Regular page content -->
  <div style="background: #fff; padding: 2rem;">

  ## About Me

  Hi! I'm Ryan Yin — a sophomore at [The Village School](https://www.nordangliaeducation.com/village-houston) in Houston, TX.  

  I'm someone who loves thinking in systems, optimizing workflows, and solving messy problems — whether through code, strategy, or good old trial and error.

  Lately, I've been exploring operations research, applied math, and startup design — figuring out how smart processes and great tools can make life simpler, faster, or just cooler.

  But outside of school and projects, I'm pretty much everywhere:

  - 🎮 Playing Brawlhalla (Platinum) or Fortnite (Unreal)
  - 🏸 Getting competitive with **badminton, tennis, football, pickleball**, and random gym PRs
  - 🎾 Coaching tennis 
  - 🎧 Listening to [NIKI](https://open.spotify.com/artist/2kxP07DLgs4xlWz8YHlvfh) and vibing to late-night lo-fi playlists
  - 🥩 Perfecting my steak-searing skills — cast iron > nonstick

  I like building things, improving things, and making things that last. Whether it's launching a new project, running an AAU basketball team, or writing late at night — I'm always chasing that n[...]

  Let's build something cool.

  <section id="contactme">
    <h2>Contact Me</h2>
    {% include contactme.html %}
  </section>

  </div>
</div>
