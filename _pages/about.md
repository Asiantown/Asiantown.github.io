---
permalink: /
title: "About Me"
excerpt: "About Me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<style>
  @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800&display=swap');
  body {
    font-family: 'Inter', sans-serif;
    margin: 0;
    padding: 0;
  }
  /* Animation bar at top */
  #intro-bar {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    background: #111;
    color: #fff;
    text-align: center;
    font-size: 2.5rem;
    font-weight: 800;
    padding: 2rem 0 2rem 0;
    z-index: 9999;
    transition: opacity 1s ease;
    pointer-events: none;
  }
  #intro-bar.fade-out {
    opacity: 0;
  }
  /* Push down main content so it doesn't hide behind intro-bar */
  #main-content {
    margin-top: 5.5rem;
  }
  #hero-section {
    background: #111;
    color: #fff;
    text-align: center;
    padding: 3rem 1rem;
    font-size: 4rem;
    font-weight: 800;
    margin-bottom: 2rem;
  }
  @media (max-width: 768px) {
    #intro-bar {
      font-size: 1.5rem;
      padding: 1.2rem 0;
    }
    #main-content {
      margin-top: 3.5rem;
    }
    #hero-section {
      font-size: 2rem;
      padding: 2rem 0.5rem;
    }
  }
</style>

<!-- Animated intro bar at the top -->
<div id="intro-bar">
  Hi, I'm Ryan Yin
</div>

{% raw %}
<script>
  // Fade out the intro bar after 4 seconds
  setTimeout(() => {
    document.getElementById("intro-bar").classList.add("fade-out");
  }, 4000);
  // Optionally remove the bar after fade
  setTimeout(() => {
    const el = document.getElementById("intro-bar");
    if(el) el.style.display = "none";
  }, 5000);
</script>
{% endraw %}

<div id="main-content">
  <section id="hero-section">
    Hi, I'm Ryan Yin
  </section>

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
