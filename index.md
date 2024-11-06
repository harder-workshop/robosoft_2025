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
    "Humanitarian Assistance",
    "Reconnaissance",
    "Disasters",
    "Exploration",
    "Recovery"
  ];
  let lineIndex = 0;
  let charIndex = 0;
  const typingSpeed = 100;   // Typing speed in ms
  const delayBetweenLines = 1500; // Delay before switching to next line

  function typeLine() {
    const lineElement = document.getElementById("line");
    lineElement.innerHTML = `${lines[lineIndex].slice(0, charIndex + 1)}`;

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

# Abstract

Soft robotics, due to their adaptable materials and unique morphologies, promise novel capabilities for field applications. This workshop, inspired by the RoboSoft 2024 keynote, will focus on leveraging soft robotics for real-world challenges in humanitarian aid, disaster relief, environmental monitoring, and exploration. The HARDER workshop will pair academic researchers with field practitioners to explore these applications.