---
hide:
  - navigation
  - toc
---
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">

<div class="custom-tab-navbar-container">
  <div class="tab-navbar-wrapper sliding-nav">
    <div class="pill-slider"></div>
    <a href="#performance" class="tab-link active"><i class="fa-solid fa-house"></i></a>
    <a href="#capabilities" class="tab-link">Publications</a>
    <a href="#appleSlider" class="tab-link">Blogs</a>
  </div>

  <div class="tab-navbar-wrapper news-dropdown-wrapper">
    <a href="#news" class="tab-link news-pill" id="news-toggle">News</a>

  <div class="glassy-dialog-box" id="news-dialog">
    <div class="dialog-content">
      <h3>News & Updates</h3>
      <p>This is your placeholder text for the glassy dialog box. The content is set to pure black, and the container perfectly matches your heavy glassmorphism aesthetics.</p>
    </div>
  </div>
  </div>
</div>

<script>
document.addEventListener("DOMContentLoaded", () => {
  const navWrapper = document.querySelector(".sliding-nav");
  if (!navWrapper) return;

  const links = Array.from(navWrapper.querySelectorAll(".tab-link"));
  const slider = navWrapper.querySelector(".pill-slider");

  // Dynamically fetch target target DIV elements based on link hrefs
  function getTargets() {
    return links
      .map(link => {
        const id = link.getAttribute("href");
        if (id && id.startsWith("#")) {
          return document.querySelector(id);
        }
        return null;
      })
      .filter(Boolean);
  }

  // Moves the black pill indicator directly to the active tab
  function moveSliderToLink(targetLink) {
    if (!targetLink || !slider) return;

    const navRect = navWrapper.getBoundingClientRect();
    const linkRect = targetLink.getBoundingClientRect();

    const left = linkRect.left - navRect.left;
    const width = linkRect.width;

    slider.style.left = `${left}px`;
    slider.style.width = `${width}px`;

    links.forEach(l => l.classList.remove("active"));
    targetLink.classList.add("active");
  }

  // Calculates which div is currently on screen
  function updateScrollSpy() {
    const targetDivs = getTargets();
    if (targetDivs.length === 0) return;

    // Trigger threshold: 30% down the visible window
    const scrollPosition = window.scrollY + window.innerHeight * 0.3;

    let currentDiv = null;

    targetDivs.forEach(div => {
      const top = div.offsetTop;
      const height = div.offsetHeight;

      if (scrollPosition >= top && scrollPosition < top + height) {
        currentDiv = div;
      }
    });

    // Default to first link if scrolled back to top
    if (window.scrollY < 100) {
      currentDiv = targetDivs[0];
    }

    if (currentDiv) {
      const activeId = `#${currentDiv.getAttribute("id")}`;
      const matchingLink = links.find(l => l.getAttribute("href") === activeId);
      if (matchingLink) {
        moveSliderToLink(matchingLink);
      }
    }
  }

  // Initial positioning
  const initialActive = navWrapper.querySelector(".tab-link.active") || links[0];
  moveSliderToLink(initialActive);

  // Listen for scroll & window resize events
  window.addEventListener("scroll", updateScrollSpy, { passive: true });
  window.addEventListener("resize", () => {
    const activeLink = navWrapper.querySelector(".tab-link.active") || links[0];
    moveSliderToLink(activeLink);
  });

  // Smooth scroll animation when clicking nav tabs
  links.forEach(link => {
    link.addEventListener("click", (e) => {
      const targetId = link.getAttribute("href");
      if (targetId && targetId.startsWith("#")) {
        const targetElement = document.querySelector(targetId);
        if (targetElement) {
          e.preventDefault();
          targetElement.scrollIntoView({ behavior: "smooth" });
          moveSliderToLink(link);
        }
      }
    });
  });
});
</script>

<!-- <div class="custom-top-banner">
  <div class="banner-center-content">
    <span>MA-PaPSP got accepted to ICLR 2026!</span>
    <a href="#" class="banner-btn">Read Paper &rarr;</a>
</div>
</div> -->

<div id="performance" class="intro-grid-container">
  
  <div class="intro-text-column">
  
  <h1 class="dynamic-name" id="dynamicName">Aditya Sarkar</h1>
  <p class="intro-bio">
    <mark class="aesthetic-highlight">PhD Student</mark> at University of Maryland; IIT Mandi '23.
  </p>
  <p class="intro-bio">
    Hello! I broadly work on improving the alignment between vision and language in vision-language models, with a particular focus on temporal reasoning and world modeling. I am currently a <mark class="aesthetic-highlight">second-year Ph.D. student</mark> at the <a href="https://www.umd.edu/" class="inline-link" target="_blank">University of Maryland</a>, where I collaborate with Profs. <a href="http://www.svcl.ucsd.edu/people/nuno/" class="inline-link">Nuno Vasconcelos</a> and <a href="https://www.cs.umd.edu/~djacobs/" class="inline-link">David Jacobs</a>. I am grateful to be supported by the University of Maryland Graduate Fellowship.</p>
  <p class="intro-bio">
  Prior to joining UMD, I graduated as the top student at IIT Mandi SCEE department. Throughout my academic journey, I have had the privilege of being mentored by <a href="https://faculty.iitmandi.ac.in/~sreelakshmi/" class="inline-link" target="_blank">Sreelakshmi Manjunath</a> and <a href="https://mangul-lab-usc.github.io/members/serghei-mangul.html" class="inline-link" target="_blank">Serghei Mangul</a>.
  </p>

  <div class="status-indicator">
    <span class="status-dot pulsing"></span>
    <span class="status-text">Available for Fall '26 Research Internships</span>
  </div>
  
  <div class="minimal-social-links">
  <a href="#" class="social-icon-link" title="Homepage">
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M3 9l9-7 9 7v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z"></path><polyline points="9 22 9 12 15 12 15 22"></polyline></svg>
  </a>

  <a href="#" class="social-icon-link" title="LinkedIn">
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"></path><rect x="2" y="9" width="4" height="12"></rect><circle cx="4" cy="4" r="2"></circle></svg>
  </a>

  <a href="#" class="social-icon-link" title="GitHub">
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"></path></svg>
  </a>

  <a href="#" class="social-icon-link" title="X">
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M23 3a10.9 10.9 0 0 1-3.14 1.53 4.48 4.48 0 0 0-7.86 3v1A10.66 10.66 0 0 1 3 4s-4 9 5 13a11.64 11.64 0 0 1-7 2c9 5 20 0 20-11.5a4.5 4.5 0 0 0-.08-.83A7.72 7.72 0 0 0 23 3z"></path></svg>
  </a>

  <a href="mailto:asarkar6@umd.edu" class="social-icon-link" title="Email">
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"></path><polyline points="22,6 12,13 2,6"></polyline></svg>
  </a>

  <a href="#" class="social-icon-link" title="CV / Resume">
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"></path><polyline points="14 2 14 8 20 8"></polyline><line x1="16" y1="13" x2="8" y2="13"></line><line x1="16" y1="17" x2="8" y2="17"></line><polyline points="10 9 9 9 8 9"></polyline></svg>
  </a>
</div>
  </div>
  
  <div class="intro-image-column">
    <div class="premium-image-frame">
      <img src="images/por.jpg" alt="Aditya Sarkar" class="profile-portrait">
    </div>
    
  <div class="photo-sub-info">
    <span class="contact-tag">Office</span>
    <span class="contact-detail">
      4112-D15, Brendan Iribe Center<br>
      <span class="sub-detail">8125 Paint Branch Dr, College Park, MD</span>
    </span>
  </div>
  </div>
  
</div>

<!-- <span style=font-size:2em;">[:academicons-google-scholar:](https://scholar.google.com/citations?user=jLJJn6sAAAAJ&hl=en) [:fontawesome-brands-linkedin:](https://www.linkedin.com/in/aditya-sarkar-970620315/) [:fontawesome-brands-github:](https://github.com/kingston-aditya) [:fontawesome-brands-x-twitter:](https://x.com/sarkar8073) [:fontawesome-solid-chalkboard-user:](SanDiego_Aditya_CV8.pdf)</span> -->

<!-- <div class="academic-squircles-container">
  <a href="https://scholar.google.com/citations?user=jLJJn6sAAAAJ&hl=en" class="academic-squircle-btn" title="Google Scholar">
    <i class="fa-brands fa-google-scholar"></i>
  </a>
  <a href="https://www.linkedin.com/in/aditya-sarkar-970620315/" class="academic-squircle-btn" title="LinkedIn">
    <i class="fa-brands fa-linkedin"></i>
  </a>
  <a href="https://github.com/kingston-aditya" class="academic-squircle-btn" title="GitHub">
    <i class="fa-brands fa-github"></i>
  </a>
  <a href="https://x.com/sarkar8073" class="academic-squircle-btn" title="X (Twitter)">
    <i class="fa-brands fa-square-x-twitter"></i>
  </a>
  <a href="SanDiego_Aditya_CV8.pdf" class="academic-squircle-btn" title="CV / Teaching">
    <i class="fa-regular fa-file"></i>
  </a>
</div>

<br>

Hello! I am a second-year Ph.D. student at the [__University of Maryland__](https://www.umiacs.umd.edu/), where I am engaged in research collaborations with Profs. [__Nuno Vasconcelos__](http://www.svcl.ucsd.edu/people/nuno/) and [__David Jacobs__](https://www.cs.umd.edu/~djacobs/). My research aims to build better computer vision algorithms, specifically for temporal understanding in LLMs, action and world modeling. I am grateful to be supported by University of Maryland __Graduate Fellowship__.

<span style="color: red;">I am looking for research internships for summer '26. Please reach out if you're interested in my profile.</span> -->

<!-- <br>
<br> -->

<!-- ## News

=== "2026"
    
    [01/2026] :party_popper: MA-PaPSP got accepted at ICLR '26. See you in Rio de Janeiro, Brazil.

=== "2024"

    [09/2024] :party_popper: Excited to start my Ph.D. at [University of Maryland](https://umd.edu/) advised by Prof. [Ang Li](https://www.ang-li.com/).

    [09/2023] :party_popper: Graduated from IIT Mandi with B.Tech. (Honors) in Electrical Engineering. -->

<h1 class="calligraphy-heading">selected works</h1>

<nav class="invisible-dock-container">
  <div class="nav-dynamic-tracker" id="nav-tracker"></div>
  
  <div class="dock-links">

  <a href="#news" class="dock-item news-item" onmouseenter="moveTracker(this)" onclick="setActive(this)">
    Research Topics
  </a>

  <span class="dock-separator"></span>

  <a href="#" class="dock-item" onmouseenter="moveTracker(this)" onclick="setActive(this)">Diffusion</a>
  <a href="#" class="dock-item" onmouseenter="moveTracker(this)" onclick="setActive(this)">Language Modelling</a>
  <a href="#" class="dock-item" onmouseenter="moveTracker(this)" onclick="setActive(this)">Contrastive Learning</a>
  </div>
</nav>


<div id="capabilities" class="publications-bento-grid">

  <div class="bento-pub-card pub-card-blue">
    <div class="bento-ambient-graphic">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
      <path d="M2 6c2.5 0 2.5 3 5 3s2.5-3 5-3 2.5 3 5 3 2.5-3 5-3M2 12c2.5 0 2.5 3 5 3s2.5-3 5-3 2.5 3 5 3 2.5-3 5-3M2 18c2.5 0 2.5 3 5 3s2.5-3 5-3 2.5 3 5 3 2.5-3 5-3" stroke-linecap="round" stroke-linejoin="round"/>
    </svg>
    </div>
    
  <div class="bento-pub-meta">
    <span class="bento-badge">Ongoing</span>
    <span class="bento-year">2026</span>
  </div>
  <h3 class="bento-title">Selected Language Modeling Distillation</h3>
  <p class="bento-authors"><strong>Aditya Sarkar</strong>, Co-Author One</p>
  <div class="bento-links">
    <a href="#" class="bento-link">Paper <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><line x1="7" y1="17" x2="17" y2="7"></line><polyline points="7 7 17 7 17 17"></polyline></svg></a>
    <a href="#" class="bento-link">Code <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><line x1="7" y1="17" x2="17" y2="7"></line><polyline points="7 7 17 7 17 17"></polyline></svg></a>
    <a href="#" class="bento-link">Blog <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><line x1="7" y1="17" x2="17" y2="7"></line><polyline points="7 7 17 7 17 17"></polyline></svg></a>
    <a href="#" class="bento-link">Demo <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><line x1="7" y1="17" x2="17" y2="7"></line><polyline points="7 7 17 7 17 17"></polyline></svg></a>
  </div>
  </div>

  <div class="bento-pub-card pub-card-blue">
    <div class="bento-ambient-graphic">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
      <path d="M2 6c2.5 0 2.5 3 5 3s2.5-3 5-3 2.5 3 5 3 2.5-3 5-3M2 12c2.5 0 2.5 3 5 3s2.5-3 5-3 2.5 3 5 3 2.5-3 5-3M2 18c2.5 0 2.5 3 5 3s2.5-3 5-3 2.5 3 5 3 2.5-3 5-3" stroke-linecap="round" stroke-linejoin="round"/>
    </svg>
    </div>
    
  <div class="bento-pub-meta">
    <span class="bento-badge">Ongoing</span>
    <span class="bento-year">2026</span>
  </div>
  <h3 class="bento-title">Selected Language Modeling Distillation</h3>
  <p class="bento-authors"><strong>Aditya Sarkar</strong>, Co-Author One</p>
  <div class="bento-links">
    <a href="#" class="bento-link">Paper <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><line x1="7" y1="17" x2="17" y2="7"></line><polyline points="7 7 17 7 17 17"></polyline></svg></a>
    <a href="#" class="bento-link">Code <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><line x1="7" y1="17" x2="17" y2="7"></line><polyline points="7 7 17 7 17 17"></polyline></svg></a>
    <a href="#" class="bento-link">Blog <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><line x1="7" y1="17" x2="17" y2="7"></line><polyline points="7 7 17 7 17 17"></polyline></svg></a>
    <a href="#" class="bento-link">Demo <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><line x1="7" y1="17" x2="17" y2="7"></line><polyline points="7 7 17 7 17 17"></polyline></svg></a>
  </div>
  </div>
  
  <div class="bento-pub-card pub-card-teal">
    <div class="bento-ambient-graphic">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
      <path d="M2 6c2.5 0 2.5 3 5 3s2.5-3 5-3 2.5 3 5 3 2.5-3 5-3M2 12c2.5 0 2.5 3 5 3s2.5-3 5-3 2.5 3 5 3 2.5-3 5-3M2 18c2.5 0 2.5 3 5 3s2.5-3 5-3 2.5 3 5 3 2.5-3 5-3" stroke-linecap="round" stroke-linejoin="round"/>
    </svg>
    </div>
    
  <div class="bento-pub-meta">
    <span class="bento-badge">Preprint</span>
    <span class="bento-year">2026</span>
  </div>
  <h3 class="bento-title">Selected Language Modeling Distillation</h3>
  <p class="bento-authors"><strong>Aditya Sarkar</strong>, Co-Author One</p>
  <div class="bento-links">
    <a href="#" class="bento-link">Paper <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><line x1="7" y1="17" x2="17" y2="7"></line><polyline points="7 7 17 7 17 17"></polyline></svg></a>
    <a href="#" class="bento-link">Code <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><line x1="7" y1="17" x2="17" y2="7"></line><polyline points="7 7 17 7 17 17"></polyline></svg></a>
    <a href="#" class="bento-link">Blog <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><line x1="7" y1="17" x2="17" y2="7"></line><polyline points="7 7 17 7 17 17"></polyline></svg></a>
    <a href="#" class="bento-link">Demo <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><line x1="7" y1="17" x2="17" y2="7"></line><polyline points="7 7 17 7 17 17"></polyline></svg></a>
  </div>
  </div>

  <div class="bento-pub-card pub-card-purple">
    <div class="bento-ambient-graphic">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
        <path d="M9 18V5l12-2v13" stroke-linecap="round" stroke-linejoin="round"/>
        <circle cx="6" cy="18" r="3"/>
        <circle cx="18" cy="16" r="3"/>
      </svg>
    </div>

  <div class="bento-pub-meta">
    <span class="bento-badge">Conference</span>
    <span class="bento-year">2025</span>
  </div>
  <h3 class="bento-title">Temporal Understanding in Multimodal Large Language Models</h3>
  <p class="bento-authors"><strong>Aditya Sarkar</strong>, Vasconcelos, N.</p>
  <div class="bento-links">
    <a href="#" class="bento-link">Paper <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><line x1="7" y1="17" x2="17" y2="7"></line><polyline points="7 7 17 7 17 17"></polyline></svg></a>
  </div>
  </div>

</div>

<!-- ## Testin -->

<script>
  function animateAndGo(element, url, event) {
  event.preventDefault(); // Stop the browser from leaving the page instantly
  
  // Find the parent moving-box element
  const box = element.closest('.moving-box');
  
  if (box) {
    // Add the bounce animation class
    box.classList.add('box-clicked');
    
    // Wait 400ms for the smooth animation to finish, then navigate
    setTimeout(() => {
      window.location.href = url;
    }, 400);
  }
}

function filterPubs(topic, element) {
  // 1. Update active state on tracking pills safely using the passed element
  const buttons = document.querySelectorAll('.pub-pill');
  buttons.forEach(btn => btn.classList.remove('active'));
  
  if (element) {
    element.classList.add('active');
  }

  // 2. Filter the elements cleanly
  const items = document.querySelectorAll('.pub-item');
  items.forEach(item => {
    if (topic === 'all' || item.getAttribute('data-topic') === topic) {
      item.style.display = 'block';
    } else {
      item.style.display = 'none';
    }
  });
}

function moveSlider(element) {
    // 1. Remove the 'active' class (white text) from all options
    const options = document.querySelectorAll('.nav-option');
    options.forEach(opt => opt.classList.remove('active'));

    // 2. Add the 'active' class to the exact button that was clicked
    element.classList.add('active');

    // 3. Find the slider element
    const slider = document.getElementById('navSlider');

    // 4. Calculate where the clicked button is and how wide it is
    const leftPosition = element.offsetLeft;
    const elementWidth = element.offsetWidth;

    // 5. Move and resize the purple slider to match
    slider.style.left = `${leftPosition}px`;
    slider.style.width = `${elementWidth}px`;
  }

  // 6. Run this once when the page loads so the purple box starts on "Overview"
  window.addEventListener('DOMContentLoaded', () => {
    const firstOption = document.querySelector('.nav-option.active');
    if (firstOption) {
      moveSlider(firstOption);
    }
  });


  function moveTracker(element) {
    const tracker = document.getElementById('nav-tracker');
    const container = element.closest('.invisible-dock-container');
    
    const targetRect = element.getBoundingClientRect();
    const containerRect = container.getBoundingClientRect();
    
    const relativeLeft = targetRect.left - containerRect.left;
    const relativeTop = targetRect.top - containerRect.top;
    
    tracker.style.left = `${relativeLeft}px`;
    tracker.style.top = `${relativeTop}px`;
    tracker.style.width = `${targetRect.width}px`;
    tracker.style.height = `${targetRect.height}px`;
  }

  function setActive(element) {
    // 1. Strip the active class from whichever item currently holds it
    const currentActive = document.querySelector('.dock-item.active-item');
    if (currentActive) {
      currentActive.classList.remove('active-item');
    }
    
    // 2. Add the active styling class to the clicked link
    element.classList.add('active-item');
    
    // 3. Instantly tell the background tracker to resize and fit the new text size
    moveTracker(element);
  }

  // Hide or reset to active item when mouse leaves the navigation dock completely
  document.querySelector('.invisible-dock-container').addEventListener('mouseleave', () => {
    const activeItem = document.querySelector('.dock-item.active-item');
    if (activeItem) {
      moveTracker(activeItem);
    }
  });

  // Initialize position on page load
  window.addEventListener('load', () => {
    const activeItem = document.querySelector('.dock-item.active-item');
    if (activeItem) {
      moveTracker(activeItem);
    }
  });

document.addEventListener("DOMContentLoaded", function() {
    const tabLinks = document.querySelectorAll('.sliding-nav .tab-link');
    const slider = document.querySelector('.pill-slider');

    // Function to calculate and move the sliding background pill
    function updateSlider(activeTab) {
      if (!activeTab || !slider) return;
      
      const navRect = activeTab.closest('.sliding-nav').getBoundingClientRect();
      const tabRect = activeTab.getBoundingClientRect();
      
      // Set the width to match the specific word and slide it to the exact relative coordinate
      slider.style.width = `${tabRect.width}px`;
      slider.style.left = `${tabRect.left - navRect.left}px`;
    }

    // 1. Initialize the slider position instantly on page load
    const initialActive = document.querySelector('.sliding-nav .tab-link.active');
    if (initialActive) {
      // Slight delay ensures custom fonts are fully loaded before calculating width
      setTimeout(() => updateSlider(initialActive), 50); 
    }

    // 2. Listen for clicks to trigger the slide
    tabLinks.forEach(link => {
      link.addEventListener('click', function(event) {
        
        // Remove active class from all links
        tabLinks.forEach(t => t.classList.remove('active'));
        
        // Add active class to the clicked tab to turn the text white
        this.classList.add('active');
        
        // Slide the pill to wrap the new active tab
        updateSlider(this);
      });
    });
  });

document.addEventListener("DOMContentLoaded", function() {
  const newsToggle = document.getElementById('news-toggle');
  const newsDialog = document.getElementById('news-dialog');

  if (newsToggle && newsDialog) {
    // 1. Toggle dialog on pill click
    newsToggle.addEventListener('click', function(event) {
      event.preventDefault(); // Prevents the page from jumping
      event.stopPropagation(); // Stops the click from immediately triggering the document listener below
      
      this.classList.toggle('active-purple');
      newsDialog.classList.toggle('show');
    });

    // 2. Prevent clicks inside the dialog from closing it
    newsDialog.addEventListener('click', function(event) {
      event.stopPropagation();
    });

    // 3. Close the dialog if the user clicks anywhere outside of it
    document.addEventListener('click', function(event) {
      if (newsDialog.classList.contains('show')) {
        newsToggle.classList.remove('active-purple');
        newsDialog.classList.remove('show');
      }
    });
  }
});

document.addEventListener("DOMContentLoaded", () => {
  const nameElement = document.getElementById("dynamicName");
  if (!nameElement) return;

  const originalText = nameElement.textContent.trim();
  nameElement.innerHTML = ""; // Clear original text

  // Split the name into individual characters (preserving spaces)
  const characters = Array.from(originalText).map(char => {
    const span = document.createElement("span");
    if (char === " ") {
      span.innerHTML = "&nbsp;"; // Maintain proper spacing
    } else {
      span.textContent = char;
    }
    nameElement.appendChild(span);
    return span;
  });

  // Function to apply random states to characters
  function randomizeText() {
    characters.forEach(span => {
      // Don't animate spaces
      if (span.innerHTML === "&nbsp;") return;

      // Generate a random roll to decide the state
      const roll = Math.random();

      if (roll < 0.20) {
        // 20% chance to go Bold
        span.classList.add("is-bold");
        span.classList.remove("is-crossed");
      } else if (roll < 0.35) {
        // 15% chance to go Crossed out
        span.classList.add("is-crossed");
        span.classList.remove("is-bold");
      } else {
        // 65% chance to stay/return to Normal
        span.classList.remove("is-bold", "is-crossed");
      }
    });
  }

  // Initial run
  randomizeText();

  // Change the letters dynamically every 2.5 seconds
  setInterval(randomizeText, 2500);
});

document.addEventListener("DOMContentLoaded", () => {
  const track = document.getElementById("carouselTrack");
  const dots = document.querySelectorAll(".dot");
  const originalSlides = Array.from(track.children);
  const totalOriginals = originalSlides.length;
  
  // Clone elements to create infinite illusion buffers (3 before, 3 after)
  for (let i = totalOriginals - 1; i >= 0; i--) {
    const clone = originalSlides[i].cloneNode(true);
    clone.classList.add("carousel-clone");
    track.insertBefore(clone, track.firstChild);
  }
  originalSlides.forEach(slide => {
    const clone = slide.cloneNode(true);
    clone.classList.add("carousel-clone");
    track.appendChild(clone);
  });

  const allSlides = Array.from(track.children);
  let currentIndex = totalOriginals; // Points directly to the first original slide
  
  document.getElementById("appleSlider").style.overflowX = "hidden";

  function updateCarousel(animated = true) {
    if (animated) {
      track.style.transition = "transform 0.5s cubic-bezier(0.25, 1, 0.5, 1)";
    } else {
      track.style.transition = "none";
    }

    // 1. Get the width of the container on your website, NOT the monitor screen
    const container = document.getElementById("appleSlider");
    const containerWidth = container.offsetWidth;
    
    // 2. Get the actual width of the box
    const slideWidth = allSlides[0].getBoundingClientRect().width;
    const gap = 16; 
    
    // 3. Calculate perfect center offset based on the container
    const centerOffset = (containerWidth - slideWidth) / 2;
    const targetLeft = (currentIndex * (slideWidth + gap)) - centerOffset;

    track.style.transform = `translateX(${-targetLeft}px)`;

    // Update dots
    const currentOriginalIndex = parseInt(allSlides[currentIndex].getAttribute("data-index"));
    dots.forEach((dot, idx) => {
      if (idx === currentOriginalIndex) {
        dot.classList.add("active");
      } else {
        dot.classList.remove("active");
      }
    });
  }

  track.addEventListener("transitionend", () => {
    if (currentIndex >= totalOriginals * 2) {
      currentIndex = totalOriginals;
      updateCarousel(false);
    } else if (currentIndex < totalOriginals) {
      currentIndex = totalOriginals * 2 - 1;
      updateCarousel(false);
    }
  });

  window.jumpToSlide = function(targetOriginalIndex) {
    currentIndex = totalOriginals + targetOriginalIndex;
    updateCarousel(true);
  };

  let isDragging = false, startX;
  
  track.addEventListener("mousedown", (e) => {
    isDragging = true;
    startX = e.pageX;
    track.style.transition = "none";
  });

  window.addEventListener("mousemove", (e) => {
    if (!isDragging) return;
    const currentX = e.pageX;
    const diff = currentX - startX;
    if (Math.abs(diff) > 80) {
      isDragging = false;
      if (diff > 0) currentIndex--;
      else currentIndex++;
      updateCarousel(true);
    }
  });

  window.addEventListener("mouseup", () => { isDragging = false; });
  
  window.addEventListener("resize", () => updateCarousel(false));
  setTimeout(() => updateCarousel(false), 150);
});
</script>

<br>

<h1 class="calligraphy-heading">latest posts</h1>

<div class="apple-carousel-container" id="appleSlider">
  <div class="apple-carousel-stage">
    <div class="apple-carousel-track" id="carouselTrack">
      
  <div class="apple-moving-box" data-index="2">
    <div class="apple-box-image">
      <img src="https://images.unsplash.com/photo-1620712943543-bcc4688e7485?w=1200&auto=format&fit=crop&q=80" alt="Slide 3">
    </div>
    <div class="apple-box-overlay">
      <h3>Diffusion Models</h3>
      <p>Exploring state-of-the-art tokenization layers across generative pipelines.</p>
      <a href="#" class="apple-btn">Read paper</a>
    </div>
  </div>

  <div class="apple-moving-box" data-index="0">
    <div class="apple-box-image">
      <img src="https://images.unsplash.com/photo-1507842217343-583bb7270b66?w=1200&auto=format&fit=crop&q=80" alt="Slide 1">
    </div>
    <div class="apple-box-overlay">
      <h3>Friday Night Baseball</h3>
      <p>We stream MLB games live every Saturday.</p>
      <a href="#" class="apple-btn">Check the schedule</a>
    </div>
  </div>

  <div class="apple-moving-box" data-index="1">
    <div class="apple-box-image">
      <img src="https://images.unsplash.com/photo-1618005182384-a83a8bd57fbe?w=1200&auto=format&fit=crop&q=80" alt="Slide 2">
    </div>
    <div class="apple-box-overlay">
      <h3>Video Complexity Measures</h3>
      <p>Analyzing structural frameworks across active frame sequences.</p>
      <a href="#" class="apple-btn">Stream now</a>
    </div>
  </div>

  <div class="apple-moving-box" data-index="2">
    <div class="apple-box-image">
      <img src="https://images.unsplash.com/photo-1620712943543-bcc4688e7485?w=1200&auto=format&fit=crop&q=80" alt="Slide 3">
    </div>
    <div class="apple-box-overlay">
      <h3>Diffusion Models</h3>
      <p>Exploring state-of-the-art tokenization layers across generative pipelines.</p>
      <a href="#" class="apple-btn">Read paper</a>
    </div>
  </div>

  <div class="apple-moving-box" data-index="0">
    <div class="apple-box-image">
      <img src="https://images.unsplash.com/photo-1507842217343-583bb7270b66?w=1200&auto=format&fit=crop&q=80" alt="Slide 1">
    </div>
    <div class="apple-box-overlay">
      <h3>Friday Night Baseball</h3>
      <p>We stream MLB games live every Saturday.</p>
      <a href="#" class="apple-btn">Check the schedule</a>
    </div>
  </div>

</div>
  </div>
</div>

<div class="carousel-navigation-container">
  <div class="carousel-indicators">
    <button class="indicator-dot active" onclick="goToSlide(0)"><span class="progress-fill"></span></button>
    <button class="indicator-dot" onclick="goToSlide(1)"><span class="progress-fill"></span></button>
    <button class="indicator-dot" onclick="goToSlide(2)"><span class="progress-fill"></span></button>
  </div>

  <button class="carousel-control-toggle" onclick="togglePlayPause()" aria-label="Play/Pause">
    <svg class="icon-pause" viewBox="0 0 24 24"><path d="M6 19h4V5H6v14zm8-14v14h4V5h-4z"/></svg>
    <svg class="icon-play" viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg>
  </button>
</div>

<script>
  let currentSlideIndex = 0; 
  let carouselTimer = null;
  let isPaused = false;
  const slideIntervalTime = 5000;

  const track = document.getElementById('carouselTrack');
  const container = document.querySelector('.apple-carousel-container');
  const indicators = document.querySelectorAll('.indicator-dot');
  const totalRealSlides = indicators.length;

  // DYNAMIC LOOKUP ENGINE: Measures the exact active size layout of your container bounds
  function getPhysicalOffset(index) {
    if (!track || !container) return '0px';

    const firstCard = track.children[0];
    if (!firstCard) return '0px';

    // 1. Read real element layout values directly from the browser viewport engine
    const containerWidth = container.getBoundingClientRect().width;
    const cardWidth = firstCard.getBoundingClientRect().width;

    // 2. Discover the exact structural margin padding added by your theme layout container
    const leftPadOffset = container.getBoundingClientRect().left;

    // 3. Perfect Centering Calculus Vector Anchor
    // (Container Center Line) - (Half of One Card Width) - (Calculated Movement Steps * (Card width + Gap))
    const centerPoint = (containerWidth / 2) - (cardWidth / 2);
    const stepMoveDistance = (index + 1) * (cardWidth + 16); 

    return `${centerPoint - stepMoveDistance}px`;
  }

  function startTimer() {
    clearInterval(carouselTimer);
    if (!isPaused && totalRealSlides > 0) {
      carouselTimer = setInterval(() => { advanceSlide(); }, slideIntervalTime);
    }
  }

  function advanceSlide() {
    currentSlideIndex++;
    track.style.transition = 'transform 0.6s cubic-bezier(0.25, 1, 0.5, 1)';
    track.style.transform = `translateX(${getPhysicalOffset(currentSlideIndex)})`;

    setTimeout(() => {
      if (currentSlideIndex >= totalRealSlides) {
        currentSlideIndex = 0; 
        track.style.transition = 'none'; 
        track.style.transform = `translateX(${getPhysicalOffset(currentSlideIndex)})`;
      }
    }, 600);

    updateIndicatorsUI();
  }

  function goToSlide(index) {
    currentSlideIndex = index;
    track.style.transition = 'transform 0.6s cubic-bezier(0.25, 1, 0.5, 1)';
    track.style.transform = `translateX(${getPhysicalOffset(currentSlideIndex)})`;
    updateIndicatorsUI();
    startTimer();
  }

  function updateIndicatorsUI() {
    indicators.forEach((indicator, index) => {
      indicator.classList.remove('active');
      const fill = indicator.querySelector('.progress-fill');
      if (fill) {
        fill.style.animation = 'none';
        void fill.offsetHeight; 
        fill.style.animation = null;
        if (isPaused) fill.style.animationPlayState = 'paused';
      }
      
      let normalizedIndex = currentSlideIndex % totalRealSlides;
      if (index === normalizedIndex) {
        indicator.classList.add('active');
      }
    });
  }

  function togglePlayPause() {
    isPaused = !isPaused;
    const toggleButton = document.querySelector('[onclick="togglePlayPause()"]');
    const activeFill = document.querySelector('.indicator-dot.active .progress-fill');

    if (isPaused) {
      clearInterval(carouselTimer);
      if (toggleButton) toggleButton.classList.add('paused');
      if (activeFill) activeFill.style.animationPlayState = 'paused';
    } else {
      if (toggleButton) toggleButton.classList.remove('paused');
      if (activeFill) activeFill.style.animationPlayState = 'running';
      startTimer();
    }
  }

  // Double layout trigger hooks to lock centering on window resize changes
  function syncCarouselPosition() {
    if (track) {
      track.style.transition = 'none';
      track.style.transform = `translateX(${getPhysicalOffset(currentSlideIndex)})`;
    }
  }

  window.addEventListener('resize', syncCarouselPosition);

  document.addEventListener("DOMContentLoaded", () => {
    // Wait a brief browser millisecond thread loop for MkDocs layout structures to complete rendering
    setTimeout(() => {
      syncCarouselPosition();
      startTimer();
    }, 50);
  });
</script>

<br>