---
title: Home
---

{% include figure.html img="harder_combined_logo.png" alt="Workshop Logo" width="100%" %}

<div id="typewriter">
  <h1>Soft Robots for...</h1>
  <i><h2 id="line" class="line"></h2></i>
</div>

<script>
  const lines = [
    "Humanitarian Assistance ",
    "Reconnaissance ",
    "Disasters ",
    "Exploration ",
    "Recovery ",
    "",
    "HARD Problems ",
  ];
  let lineIndex = 0;
  let charIndex = 0;
  const typingSpeed = 100;   // Typing speed in ms
  const delayBetweenLines = 1500; // Delay before switching to next line

  function typeLine() {
    const lineElement = document.getElementById("line");
    lineElement.innerHTML = `${lines[lineIndex].slice(0, charIndex + 1)}&nbsp;`;

    if (charIndex < lines[lineIndex].length) {
      charIndex++;
      setTimeout(typeLine, typingSpeed);
    } else {
      setTimeout(() => {
        charIndex = 0;
        lineIndex = (lineIndex + 1) % lines.length;
        lineElement.innerHTML = "<br>";
        setTimeout(typeLine, typingSpeed);
      }, delayBetweenLines);
    }
  }

  typeLine();
</script>


## Abstract

Soft robots, with their adaptable materials and unique morphologies, promise novel capabilities for field applications. This workshop, inspired by the RoboSoft 2024 keynote, will focus on leveraging soft robotics for real-world challenges in humanitarian assistance, reconnaissance, disasters, exploration, and recovery (HARDER). The HARDER workshop will pair academic researchers with field practitioners to explore exciting applications and unmet needs in purposeful, inter-disciplinary conversations.

> "It takes a soft robot to solve HARD problems"

**Location:** Lausanne, Switzerland  
**Date:** April 23, 2025  
**Duration:** Full Day

<div style="text-align: center;">
  <a href="./2-contributing.html" class="button">Submit Your Work!</a>
  <a href="https://web.cvent.com/event/a4d97fd0-fa93-4129-bb7b-81c7eb9987bc/summary" class="button">Register</a>
  <a href="https://forms.gle/3dRso1c3vBp9bHTt6" class="button">Get Updates</a>
</div>

<style>
.button {
  display: inline-block;
  padding: 15px 30px;
  font-size: 24px;
  color: white;
  background-color: #d42525;
  text-decoration: none;
  border-radius: 5px;
  transition: background 0.3s;
}

.button:hover {
  background-color: #ff95a1;
}

.button:visited,
.button:active,
.button:focus {
  color: white !important;
  text-decoration: none;
}
</style>