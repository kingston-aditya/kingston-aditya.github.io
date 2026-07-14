---
hide:
  - navigation
  - toc
---
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">

<div class="custom-tab-navbar-container">
  <div class="tab-navbar-wrapper">
    <a href="#news" class="tab-link">Home</a>
  </div>

  <div class="tab-navbar-wrapper sliding-nav">
    <div class="pill-slider"></div>
    <a href="#capabilities" class="tab-link active">Topic 1</a>
    <a href="#performance" class="tab-link">Topic 2</a>
    <a href="#safety" class="tab-link">Topic 3</a>
    <a href="#download" class="tab-link">Topic 4</a>
    <a href="#download" class="tab-link">Read More</a>
  </div>

  <div class="tab-navbar-wrapper">
    <a href="#news" class="tab-link">News</a>
  </div>
</div>

<script>
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
</script>

<div class="landing-hero-container">
  <div class="hero-squircle-card">
    
  <div class="hero-badge-row">
    <span class="status-badge"><span class="dot"></span>Out of publication · April 2026</span>
    <span class="funding-badge">ACCEPTED AS CONFERENCE PAPER AT ICLR 2026</span>
  </div>
  
  <h2 class="hero-title">
    <span class="italic-accent">Leveraging Data to Say No:</span>Memory Augmented Plug-and-Play Selective Prediction.
  </h2>
  
  <p class="hero-description">
    <span class="quote-mark">&#8220;</span> Selective prediction is a classic problem in machine learning in which a model is allowed to decide when to make a prediction and when to abstain. The objective is to achieve high accuracy on the predictions it does make, while avoiding uncertain or potentially risky inputs.
  </p>

  <div class="hero-text-list-block">
  
  <h3 class="list-block-title">Project Highlights</h3>
  
  <ul class="list-block-items">
    <li>Selective prediction is a classic problem in machine learning.</li>
    <li>The objective is to achieve high accuracy on the predictions it does make.</li>
    <li>The objective is to achieve high accuracy on the predictions it does make.</li>
  </ul>

  </div>
    
  </div>
</div>

<section class="testimonial-section">
  <div class="video-player-container" id="video-container">
    
  <div class="video-overlay" id="video-overlay">
    <h2 class="overlay-text">What's new in<br>Gemma 4</h2>
    
  <button class="play-button" id="play-button">
    <svg viewBox="0 0 24 24" fill="currentColor">
      <path d="M8 5v14l11-7z"/>
    </svg>
  </button>
  </div>

  <iframe 
    id="youtube-iframe"
    src="https://www.youtube.com/embed/dQw4w9WgXcQ" 
    title="YouTube video player" 
    frameborder="0" 
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
    allowfullscreen>
  </iframe>
  </div>
</section>

<script>
  document.addEventListener("DOMContentLoaded", function() {
    const playBtn = document.getElementById('play-button');
    const overlay = document.getElementById('video-overlay');
    const iframe = document.getElementById('youtube-iframe');

    if (playBtn && overlay && iframe) {
      playBtn.addEventListener('click', function() {
        // 1. Fade out the overlay cleanly
        overlay.style.opacity = '0';
        overlay.style.visibility = 'hidden';
        
        // 2. Append the autoplay command to the YouTube URL
        let videoSrc = iframe.src;
        if (videoSrc.indexOf('?') === -1) {
          iframe.src = videoSrc + '?autoplay=1';
        } else {
          iframe.src = videoSrc + '&autoplay=1';
        }
      });
    }
  });
</script>

<section class="testimonial-section">

  <h1> Motivation for Research. </h1>

  <div class="testimonial-squircle-card">
    
  <div class="quote-content-block">
    <p class="quote-text">
  Selective prediction is a classic problem in machine learning in which a model is allowed to decide when to make a prediction and when to abstain. The objective is to achieve high accuracy on the predictions it does make, while avoiding uncertain or potentially risky inputs.

  Traditionally, one common (and widely used) approach relies on thresholding the model’s output confidence, often derived from logits or predicted probabilities. For instance, consider a classifier that must distinguish between a dog and a cat image. Now suppose the model produces a probability distribution over the two classes of say, 0.1 for dog and 0.9 for cat. This maximum probability (0.9) reflects the model’s confidence in its prediction. In selective prediction, we compare this confidence score to a predefined threshold (e.g., 0.6) and output the predicted class (cat here) when the confidence exceeds the threshold. Otherwise, the model simply abstains from making a prediction, signaling uncertainty.
  </p>
  </div>

  <div class="profile-meta-footer">
    <div class="profile-details">
      <h3 class="profile-name">Traditionally, one common (and widely used).</h3>
      <p class="profile-credentials">
        Selective prediction is a classic problem in machine learning in which a model is allowed to decide when to make a prediction and when to abstain.
      </p>
    </div>
  </div>

  </div>

</section>

<section class="testimonial-section">
  
  <h1> Keep Reading. </h1>

  <div class="articles-flex-row">

  <div class="reading-squircle-card">
    <span class="card-meta-tag">Diffusion</span>
    <h3 class="card-title">
      Traditionally, one common (and widely used) approach relies on thresholding the model’s output confidence, often derived from logits or predicted probabilities.
    </h3>
    <p class="card-excerpt">
      Selective prediction is a classic problem in machine learning in which a model is allowed to decide when to make a prediction and when to abstain. The objective is to achieve high accuracy on the predictions it does make, while avoiding uncertain or potentially risky inputs.
    </p>
  </div>

  <div class="reading-squircle-card">
    <span class="card-meta-tag">Language Modelling</span>
    <h3 class="card-title">
      Selective prediction is a classic problem in machine learning in which a model is allowed to decide when to make a prediction and when to abstain.
    </h3>
    <p class="card-excerpt">
      Selective prediction is a classic problem in machine learning in which a model is allowed to decide when to make a prediction and when to abstain. The objective is to achieve high accuracy on the predictions it does make, while avoiding uncertain or potentially risky inputs.
    </p>
  </div>

  </div>
</section>



<!-- # Similar instances enhances rejection. ![](./../images/rain_book.jpg){ align=right style="width:7.5em; margin-left: 7.5em; margin-top: 0.5em; border-radius: 1em;"}

<br> -->

<!-- <p style="color: blue;">Special thanks to Yi Li, Jiacheng Cheng and Nuno Vasconcelos for a lot of super valuable feedback and discussion on this post.</p>

## Motivation. 

Selective prediction is a classic problem in machine learning in which a model is allowed to decide when to make a prediction and when to abstain. The objective is to achieve high accuracy on the predictions it does make, while avoiding uncertain or potentially risky inputs.

Traditionally, one common (and widely used) approach relies on thresholding the model’s output confidence, often derived from logits or predicted probabilities. For instance, consider a classifier that must distinguish between a dog and a cat image. Now suppose the model produces a probability distribution over the two classes of say, 0.1 for dog and 0.9 for cat. This maximum probability (0.9) reflects the model’s confidence in its prediction. In selective prediction, we compare this confidence score to a predefined threshold (e.g., 0.6) and output the predicted class (cat here) when the confidence exceeds the threshold. Otherwise, the model simply abstains from making a prediction, signaling uncertainty.

While such a paradigm works well for option-based tasks with a fixed set of answers, it breaks down in the context of generative tasks (e.g. dense caption an image), where outputs are open-ended and confidence estimates are far less reliable. Why? Well, this is because we have a confidence score for each output token. 

How can one solve this problem? Has anyone solved this before? Will discuss some works and one solution in my subsequent posts.



## Existing works. -->








