---
hide:
  - navigation
  - toc
---
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">

<div class="custom-top-banner">
  <div class="banner-center-content">
    <span>MA-PaPSP got accepted to ICLR 2026!</span>
    <a href="#" class="banner-btn">Read Paper &rarr;</a>
</div>
</div>

<div class="landing-hero-container">
  <div class="hero-squircle-card">
    
  <div class="hero-badge-row">
    <span class="status-badge"><span class="dot"></span>Out of publication · April 2026</span>
    <span class="funding-badge">ACCEPTED AS CONFERENCE PAPER AT ICLR 2026</span>
  </div>
  
  <h1 class="hero-title">
    <span class="italic-accent">Leveraging Data to Say No:</span>Memory Augmented Plug-and-Play Selective Prediction.
  </h1>
  
  <p class="hero-description">
    Selective prediction is a classic problem in machine learning in which a model is allowed to decide when to make a prediction and when to abstain. The objective is to achieve high accuracy on the predictions it does make, while avoiding uncertain or potentially risky inputs.
  </p>

  <div class="hero-metrics-grid">
    
  <div class="metric-column">
    <h2 class="metric-number">16<span class="metric-unit">hrs</span></h2>
    <p class="metric-text">Selective prediction is a classic problem in machine learning in which a model is allowed to decide when to make a prediction and when to abstain.</p>
  </div>
  
  <div class="metric-column">
    <h2 class="metric-number">$500K ubi<sub>+</sub></h2>
    <p class="metric-subtext">Selective prediction is a classic problem</p>
    <p class="metric-text">Selective prediction is a classic problem in machine learnin.</p>
  </div>
  
  <div class="metric-column">
    <h2 class="metric-number">$200<<sub>+</sub></h2>
    <p class="metric-text">Selective prediction is a classic problem in machine learning.</p>
  </div>

  </div>
    
  </div>
</div>

<section class="video-showcase-section">
  
  <div class="video-section-header">
    <h1 class="video-section-title">
      <span class="italic-accent">Explanation Video</span>.
    </h1>
  </div>

  <div class="video-player-container">
    <iframe 
      src="https://www.youtube.com/embed/dQw4w9WgXcQ" 
      title="YouTube video player" 
      frameborder="0" 
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
      allowfullscreen>
    </iframe >
  </div>
</section>

<section class="testimonial-section">

  <h1 class="testimonial-section-title">
    <span class="italic-accent">Motivation for Research.</span>
  </h1>

  <div class="testimonial-squircle-card">
    
  <div class="quote-content-block">
    <span class="quote-mark">&#8220;</span>
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

<section class="reading-grid-section">
  
  <h1 class="testimonial-section-title">
    <span class="italic-accent">Keep Reading.</span>
  </h1>

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








