---
hide:
  - navigation
  - toc
---

# Aditya Sarkar ![](images/por.jpg){ align=right style="width:7.5em; margin-left: 7.5em; margin-top: 0.5em; border-radius: 1em;"}

:fontawesome-solid-building: Office: [4112-D15, Brendan Iribe Center, 8125 Paint Branch Dr, College Park, MD 20742](https://maps.app.goo.gl/xWjQWVVnpTVoWaQw8)

:fontawesome-solid-inbox: Work Email: [asarkar6 [at] umd [dot] edu](mailto:asarkar6@umd.edu)

:fontawesome-solid-inbox: Personal Email: [asnov2k [at] gmail [dot] com](mailto:asnov2k@gmail.com)

<span style=font-size:2em;">[:academicons-google-scholar:](https://scholar.google.com/citations?user=jLJJn6sAAAAJ&hl=en) [:fontawesome-brands-linkedin:](https://www.linkedin.com/in/aditya-sarkar-970620315/) [:fontawesome-brands-github:](https://github.com/kingston-aditya) [:fontawesome-brands-x-twitter:](https://x.com/sarkar8073) [:fontawesome-solid-chalkboard-user:](SanDiego_Aditya_CV8.pdf)</span>

<br>

Hello! I am a second-year Ph.D. student at the [__University of Maryland__](https://www.umiacs.umd.edu/), where I am engaged in research collaborations with Profs. [__Nuno Vasconcelos__](http://www.svcl.ucsd.edu/people/nuno/) and [__David Jacobs__](https://www.cs.umd.edu/~djacobs/). My research aims to build better computer vision algorithms, specifically for temporal understanding in LLMs, action and world modeling. I am grateful to be supported by University of Maryland __Graduate Fellowship__.

<span style="color: red;">I am looking for research internships for summer '26. Please reach out if you're interested in my profile.</span>

<!-- ## News

=== "2026"
    
    [01/2026] :party_popper: MA-PaPSP got accepted at ICLR '26. See you in Rio de Janeiro, Brazil.

=== "2024"

    [09/2024] :party_popper: Excited to start my Ph.D. at [University of Maryland](https://umd.edu/) advised by Prof. [Ang Li](https://www.ang-li.com/).

    [09/2023] :party_popper: Graduated from IIT Mandi with B.Tech. (Honors) in Electrical Engineering. -->

## Publications
<sup>\*</sup> denotes equal contribution

<div class="pub-filter-container">
  <span class="filter-label">Topics:</span>

  <button class="pub-pill active" onclick="filterPubs('all', event)">Selected</button>
  <button class="pub-pill" onclick="filterPubs('tokenization', event)">Tokenization</button>
  <button class="pub-pill" onclick="filterPubs('video', event)">Video Modeling</button>
  <button class="pub-pill" onclick="filterPubs('multimodal', event)">Multi-modal ML</button>
  <button class="pub-pill" onclick="filterPubs('diffusion', event)">Diffusion Models</button>
  <button class="pub-pill" onclick="filterPubs('optimization', event)">Optimization</button>
</div>

<div class="pub-list">

  <div class="pub-item" data-topic="diffusion">
    <h4>Masked Visual Fine-Tuning for Encoder-based Diffusion Models.</h4>
    <p><u>Aditya Sarkar</u>, <a href="https://shwai-he.github.io/">Shwai He</a>, <a href="https://jiacheng-cheng.github.io/">Jiacheng Cheng</a>, <a href="http://www.svcl.ucsd.edu/people/yili/">Yi Li</a>, <a href="https://shlokk.github.io/shlokmishra.github.io/">Shlok Mishra</a>, <a href="https://www.ang-li.com/">Ang Li</a>, <a href="https://www.cs.umd.edu/~djacobs/">David Jacobs</a>, <a href="http://www.svcl.ucsd.edu/people/nuno/">Nuno Vasconcelos</a>.</p>
    <p class="pub-links">Preprint 2026</p>
    <div class="pub-actions">
      <a href="#" class="pub-btn-outline"><i class="fa-solid fa-blog"></i> Blog</a>
      <a href="#" class="pub-btn-outline"><i class="fa-solid fa-blog"></i> Paper</a>
      <a href="#" class="pub-btn-outline"><i class="fa-solid fa-code"></i> HF Demo</a>
      <a href="#" class="pub-btn-outline"><i class="fa-solid fa-code"></i> Code</a>
      <a href="#" class="pub-btn-outline"><i class="fa-solid fa-quote-right"></i> BibTeX</a>
    </div>
  </div>

  <div class="pub-item" data-topic="language">
    <h4>An Attribute-Based Measure of Video Complexity.</h4>
    <p><u>Aditya Sarkar</u>, <a href="http://www.svcl.ucsd.edu/people/yili/">Yi Li</a>, <a href="#">Z. Wang</a>, <a href="https://jiacheng-cheng.github.io/">Jiacheng Cheng</a>, <a href="#">V.N. Sai</a>, <a href="#">Aashu Singh</a>, <a href="https://shlokk.github.io/shlokmishra.github.io/">Shlok Mishra</a>, <a href="https://www.cs.umd.edu/~djacobs/">David Jacobs</a>, <a href="http://www.svcl.ucsd.edu/people/nuno/">Nuno Vasconcelos</a>.</p>
    <p class="pub-links">Preprint 2026</p>
    <div class="pub-actions">
      <a href="#" class="pub-btn-outline"><i class="fa-solid fa-blog"></i> Blog</a>
      <a href="#" class="pub-btn-outline"><i class="fa-solid fa-blog"></i> Paper</a>
      <a href="#" class="pub-btn-outline"><i class="fa-solid fa-code"></i> HF Demo</a>
      <a href="#" class="pub-btn-outline"><i class="fa-solid fa-code"></i> Code</a>
      <a href="#" class="pub-btn-outline"><i class="fa-solid fa-quote-right"></i> BibTeX</a>
    </div>
  </div>

</div>

<script>
function filterPubs(topic) {
  // Update active state on buttons
  const buttons = document.querySelectorAll('.pub-pill');
  buttons.forEach(btn => btn.classList.remove('active'));
  event.target.classList.add('active');

  // Filter items
  const items = document.querySelectorAll('.pub-item');
  items.forEach(item => {
    if (topic === 'all' || item.getAttribute('data-topic') === topic) {
      item.style.display = 'block';
    } else {
      item.style.display = 'none';
    }
  });
}

function animateAndGo(element, url, event) {
  event.preventDefault(); // Stop instant redirect
  
  const box = element.closest('.moving-box');
  
  if (box) {
    // 1. Remove the class first just in case it was left behind
    box.classList.remove('box-clicked');
    
    // 2. Trigger a tiny DOM reflow to trick the browser into resetting the animation clock
    void box.offsetWidth; 
    
    // 3. Re-apply the smooth animation class
    box.classList.add('box-clicked');
    
    // 4. Navigate after the animation settles down
    setTimeout(() => {
      // If the URL is just an anchor link on the same page, reset the class so it works again right away
      if (url.startsWith('#') || url === '') {
        box.classList.remove('box-clicked');
      }
      window.location.href = url;
    }, 400); // Matches your 0.4s CSS animation timeline
  }
}
</script>


## Blog

<div class="carousel-container">
  <div class="carousel-track">
    
<div class="moving-box">
  <div class="box-image">
    <img src="images/rain_book.jpg" alt="Project Image">
  </div>
  <div class="box-text">
    <h3>[Compute Optimal Tokenization]()</h3>
    <p>A deep dive into cross-modal latent alignment strategies for diffusion backbones.</p>
  </div>
</div>

<div class="moving-box">
  <div class="box-image">
    <img src="images/rain_book.jpg" alt="Project Image">
  </div>
  <div class="box-text">
    <h3>
      <a href="#" onclick="animateAndGo(this, '2026-02-05-retrieval', event)" class="box-title-link">
      Video Complexity Measures
    </a>
    </h3>
    <p>Analyzing attribute-based metrics to map frame-by-frame structural density.</p>
  </div>
</div>

<div class="moving-box">
  <div class="box-image">
    <img src="images/rain_book.jpg" alt="Project Image">
  </div>
  <div class="box-text">
    <h3>
      <a href="#" onclick="animateAndGo(this, '2026-02-05-retrieval', event)" class="box-title-link">
      Representation learning.
    </a>
    </h3>
    <p>Efficient tuning mechanisms keeping fundamental representations completely frozen.</p>
  </div>
</div>

<div class="moving-box">
  <div class="box-image">
    <img src="images/rain_book.jpg" alt="Project Image">
  </div>
  <div class="box-text">
    <h3>[Generative Pre-training]()</h3>
    <p>Scaling data generation pipelines using autoregressive multi-modal anchors.</p>
  </div>
</div>

  </div>
</div>

<br>