---
permalink: /
title: "About Me"
excerpt: "About Me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<!-- Hero Intro Cover -->
<style>
  @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800&display=swap');

  html, body {
    margin: 0;
    padding: 0;
  }

  #intro-cover {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: #1e1e1e;
    color: #eaeaea;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    z-index: 9999;
    transition: opacity 1s ease;
    font-family: 'Inter', sans-serif;
    text-align: center;
    padding: 2rem;
  }

  #intro-title, #intro-subtitle {
    opacity: 0;
    transition: opacity 1.5s ease;
  }

  #intro-title {
    font-size: 4rem;
    font-weight: 800;
    margin: 0;
  }

  #intro-subtitle {
    font-size: 1.75rem;
    font-weight: 400;
    margin-top: 1rem;
    max-width: 90%;
  }

  .visible {
    opacity: 1;
  }

  #intro-cover.hidden {
    opacity: 0;
    pointer-events: none;
  }

  body {
    overflow: hidden;
  }

  body.revealed {
    overflow: auto;
  }
</style>

<div id="intro-cover">
  <h1 id="intro-title">Hi, I’m Ryan Yin</h1>
  <h2 id="intro-subtitle">I use optimization and operations research to power smarter decisions in tech, business, and beyond.</h2>
</div>

{% raw %}
<script>
  document.addEventListener("DOMContentLoaded", () => {
    const title = document.getElementById("intro-title");
    const subtitle = document.getElementById("intro-subtitle");
    const cover = document.getElementById("intro-cover");

    // Fade in title
    setTimeout(() => {
      title.classList.add("visible");
    }, 100);

    // Fade in subtitle after 3s
    setTimeout(() => {
      subtitle.classList.add("visible");
    }, 3000);

    // Hide entire intro after 6s
    setTimeout(() => {
      cover.classList.add("hidden");
      document.body.classList.add("revealed");
    }, 6000);
  });
</script>
{% endraw %}





Hi! I'm Ryan Yin — a sophomore at [The Village School](https://www.nordangliaeducation.com/village-houston) in Houston, TX.  
I’m someone who loves thinking in systems, optimizing workflows, and solving messy problems — whether through code, strategy, or good old trial and error.

Lately, I've been exploring operations research, applied math, and startup design — figuring out how smart processes and great tools can make life simpler, faster, or just cooler.

But outside of school and projects, I’m pretty much everywhere:
- 🎮 Playing Brawlhalla (Platinum) or Fortnite (Unreal)
- 🏸 Getting competitive with **badminton, tennis, football, pickleball**, and random gym PRs
- 🎾 Coaching tennis 
- 🎧 Listening to [NIKI](https://open.spotify.com/artist/2kxP07DLgs4xlWz8YHlvfh) and vibing to late-night lo-fi playlists
- 🥩 Perfecting my steak-searing skills — cast iron > nonstick

I like building things, improving things, and making things that last. Whether it's launching a new project, running an AAU basketball team, or writing late at night — I’m always chasing that next idea worth committing to.

Let’s build something cool.

<section id="contactme">
  <h2>Contact Me</h2>
  {% include contactme.html %}
</section>

