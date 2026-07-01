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
  <button class="pub-pill active" onclick="filterPubs('all')">All topics</button>
  <button class="pub-pill" onclick="filterPubs('diffusion')">Diffusion Models</button>
  <button class="pub-pill" onclick="filterPubs('language')">Language Modeling</button>
</div>

<div class="pub-list">

  <div class="pub-item" data-topic="diffusion">
    <h4>Masked Visual Fine-Tuning for Encoder-based Diffusion Models.</h4>
    <p><u>Aditya Sarkar</u>, <a href="https://shwai-he.github.io/">Shwai He</a>, <a href="https://jiacheng-cheng.github.io/">Jiacheng Cheng</a>, <a href="http://www.svcl.ucsd.edu/people/yili/">Yi Li</a>, <a href="https://shlokk.github.io/shlokmishra.github.io/">Shlok Mishra</a>, <a href="https://www.ang-li.com/">Ang Li</a>, <a href="https://www.cs.umd.edu/~djacobs/">David Jacobs</a>, <a href="http://www.svcl.ucsd.edu/people/nuno/">Nuno Vasconcelos</a>.</p>
    <p class="pub-links">Preprint&nbsp;&nbsp;<a href="#">arXiv</a>&nbsp;&nbsp;<a href="#">Project Page</a></p>
  </div>

  <div class="pub-item" data-topic="language">
    <h4>An Attribute-Based Measure of Video Complexity.</h4>
    <p><u>Aditya Sarkar</u>, <a href="http://www.svcl.ucsd.edu/people/yili/">Yi Li</a>, <a href="#">Z. Wang</a>, <a href="https://jiacheng-cheng.github.io/">Jiacheng Cheng</a>, <a href="#">V.N. Sai</a>, <a href="#">Aashu Singh</a>, <a href="https://shlokk.github.io/shlokmishra.github.io/">Shlok Mishra</a>, <a href="https://www.cs.umd.edu/~djacobs/">David Jacobs</a>, <a href="http://www.svcl.ucsd.edu/people/nuno/">Nuno Vasconcelos</a>.</p>
    <p class="pub-links">Preprint&nbsp;&nbsp;<a href="#">arXiv</a>&nbsp;&nbsp;<a href="#">Project Page</a></p>
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
    <h3>[Video Complexity Measures]()</h3>
    <p>Analyzing attribute-based metrics to map frame-by-frame structural density.</p>
  </div>
</div>

<div class="moving-box">
  <div class="box-image">
    <img src="images/rain_book.jpg" alt="Project Image">
  </div>
  <div class="box-text">
    <h3>[Masked Visual Fine-Tuning]()</h3>
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