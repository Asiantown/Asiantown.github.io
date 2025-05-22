---
permalink: /
title: "About Me"
excerpt: "About Me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<!-- Minimal Hero Cover -->
<style>
  #intro-cover {
    position: fixed;
    inset: 0;
    background: #111;
    color: #fff;
    font-family: sans-serif;
    display: flex;
    align-items: center;
    justify-content: center;
    z-index: 9999;
    transition: opacity 1s ease;
    text-align: center;
  }

  #intro-text {
    font-size: 3rem;
    opacity: 0;
    transition: opacity 2s ease;
  }

  #intro-text.visible {
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
  <div id="intro-text">Hi, I’m Ryan Yin</div>
</div>

{% raw %}
<script>
  document.addEventListener("DOMContentLoaded", function () {
    const text = document.getElementById("intro-text");
    const cover = document.getElementById("intro-cover");

    // Fade in title
    setTimeout(() => {
      text.classList.add("visible");
    }, 100);

    // Fade out cover after 4 seconds
    setTimeout(() => {
      cover.classList.add("hidden");
      document.body.classList.add("revealed");
    }, 4000);
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

