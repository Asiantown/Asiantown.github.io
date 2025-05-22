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
  
  body {
    margin: 0;
    padding: 0;
    overflow-x: hidden;
  }
  
  /* The permanent hero text at top of page */
  #hero-text {
    font-family: 'Inter', sans-serif;
    font-size: 4rem;
    font-weight: 800;
    color: #fff;
    text-align: center;
    padding: 2rem 1rem;
    margin: 0;
    background: #111;
    opacity: 1;
  }
  
  /* Fullscreen overlay that covers everything during intro */
  #intro-overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100vh;
    background: #111;
    z-index: 9999;
    opacity: 1;
    transition: opacity 1.5s ease;
  }
  
  #intro-overlay.fade-out {
    opacity: 0;
    pointer-events: none;
  }
  
  #intro-overlay.hidden {
    display: none;
  }
  
  /* Hide page content initially */
  .page-content {
    opacity: 0;
    transition: opacity 1s ease;
  }
  
  .page-content.visible {
    opacity: 1;
  }
  
  /* Responsive text sizing */
  @media (max-width: 768px) {
    #hero-text {
      font-size: 2.5rem;
      padding: 1.5rem 1rem;
    }
  }
</style>

<!-- Permanent hero text that stays at top -->
<div id="hero-text">Hi, I'm Ryan Yin</div>

<!-- Fullscreen overlay for intro animation -->
<div id="intro-overlay"></div>

{% raw %}
<script>
  document.addEventListener("DOMContentLoaded", function () {
    const overlay = document.getElementById("intro-overlay");
    const pageContent = document.querySelector(".page-content");
    
    // After 4 seconds, start fading out the overlay
    setTimeout(() => {
      overlay.classList.add("fade-out");
      if (pageContent) {
        pageContent.classList.add("visible");
      }
    }, 4000);
    
    // Remove overlay completely after fade
    setTimeout(() => {
      overlay.classList.add("hidden");
    }, 5500);
  });
</script>
{% endraw %}

<!-- Page Content (will fade in after intro) -->
<div class="page-content">

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

I like building things, improving things, and making things that last. Whether it's launching a new project, running an AAU basketball team, or writing late at night — I'm always chasing that next idea worth committing to.

Let's build something cool.

<section id="contactme">
  <h2>Contact Me</h2>
  {% include contactme.html %}
</section>

</div>
