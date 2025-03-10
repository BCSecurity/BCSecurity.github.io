---
layout: home
title: "Home"
---

<div class="text-box">
  <div class="row align-items-center justify-content-center">
    <div class="col-md-4 text-center mb-4 mb-md-0">
      <div class="profile-pic-container">
        <img
          src="/assets/images/biophoto.jpg"
          alt="Profile Picture of BCSecurity"
          class="myprofile-pic"
        />
      </div>
    </div>
    <div class="col-md-6 text-start">
      <h1 class="display-4 glitch-text">BCSecurity</h1>
      <h4>CSOC Engineer - MDR</h4>
      <p>
        Hello! I'm currently a Cyber Security Engineer focusing on Incident Response 
        and Threat Intelligence. I also enjoy learning about malware behaviors. What this blog is all about:
      </p>
      <ul>
         <li>Static/Dynamic Malware Analysis</li>
         <li>Sharing IoCs</li>
         <li>Incident Response Reports</li>
         <li>Threat Reports</li>
      </ul>
      <p>Check out my <a href="/blog/">latest posts</a>!</p>
      <p class="mt-4">
        <strong>Find me on:</strong> 
        <a 
          href="www.linkedin.com/in/augustin-a-5a9a72160" 
          target="_blank" 
          rel="noopener noreferrer"
        >
          <i class="fab fa-linkedin"></i> LinkedIn
        </a>
      </p>
      <div class="mt-4" id="quote-widget">
        <strong>Cyber Quote of the Moment:</strong>
        <div id="quote-text" style="margin-top: 0.5rem;">
          <!-- Quote will load via JavaScript -->
        </div>
      </div>
    </div>
  </div>
</div>

<script>
  // Array of cybersecurity quotes
  const quotes = [
    "“The quieter you become, the more you are able to hear.” — Kali Linux motto",
    "“Hackers are today's explorers.” — Paul Graham",
    "“The only system which is truly secure is one which is switched off and unplugged.” — Gene Spafford",
    "“If you think technology can solve your security problems, then you don’t understand the problems and you don’t understand the technology.” — Bruce Schneier",
    "“Hackers are breaking the systems for profit. Before, it was about intellectual curiosity and pursuit of knowledge.” — Kevin Mitnick"
  ];

  // Display a random quote on page load
  document.addEventListener("DOMContentLoaded", () => {
    const randomQuote = quotes[Math.floor(Math.random() * quotes.length)];
    const quoteText = document.getElementById("quote-text");
    if (quoteText) {
      quoteText.textContent = randomQuote;
    }
  });
</script>
