---
layout: standalone
title: "SkelFormer"
permalink: /projects/skelformer/
description: "Project page for SkelFormer: Markerless 3D Pose and Shape Estimation using Skeletal Transformers
."
head_defer_scripts:
  - "/projects/skelformer/static/js/fontawesome.all.min.js"
head_scripts:
  - "https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"
  - "/projects/skelformer/static/js/bulma-carousel.min.js"
  - "/projects/skelformer/static/js/bulma-slider.min.js"
  - "/projects/skelformer/static/js/index.js"
  - "/projects/skelformer/static/js/magnifier.js"
stylesheet_links:
  - "https://fonts.googleapis.com/css?family=Google+Sans|Noto+Sans|Castoro"
  - "/projects/skelformer/static/css/bulma.min.css"
  - "/projects/skelformer/static/css/bulma-carousel.min.css"
  - "/projects/skelformer/static/css/bulma-slider.min.css"
  - "/projects/skelformer/static/css/tab_gallery.css"
  - "/projects/skelformer/static/css/fontawesome.all.min.css"
  - "https://cdn.jsdelivr.net/gh/jpswalsh/academicons@1/css/academicons.min.css"
  - "/projects/skelformer/static/css/index.css"
  - "https://fonts.cdnfonts.com/css/menlo"
  - "/projects/skelformer/static/css/image_card_fader.css"
  - "/projects/skelformer/static/css/image_card_slider.css"
script_name: "skelformer"
---




<html>
<body>

<!-- Banner. -->
<section class="hero banner">
<div class="hero-body">
<div class="container is-max-desktop">
  <div class="columns is-centered">
    <div class="column has-text-centered">
      <h1 class="title is-2 publication-title">SkelFormer: <br> Markerless 3D Pose and Shape Estimation using Skeletal Transformers</h1>
      <div class="is-size-5 publication-authors">
        <span class="author-block">
          <a href="https://vdavoodnia.github.io/">Vandad Davoodnia</a><sup>1,2</sup>,
        </span>
        <span class="author-block">
          <a href="https://saeed1262.github.io/">Saeed Ghorbani</a><sup>2</sup>,
        </span>
        <span class="author-block">
          Alexandre Messier<sup>2</sup>,
        </span>
        <span class="author-block">
          <a href="https://www.aiimlab.com/ali-etemad/">Ali Etemad</a><sup>1</sup>
        </span>
      </div>
      <div class="is-size-5 publication-authors">
        <span class="author-block"><sup>1</sup><a href="https://www.queensu.ca/">Queen's University</a></span>
        <span class="author-block"><sup>2</sup><a href="https://www.ubisoft.com/en-us/studio/laforge">Ubisoft LaForge</a></span>
      </div>
      <div class="is-size-3 publication-venue">
        in ECCV 2024
      </div>
      <div class="column has-text-centered">
        <div class="publication-links">
          <span class="link-block">
            <a href="./static/paper/skelformer_arxiv.pdf"
               class="external-link button is-normal is-rounded is-dark">
              <span class="icon">
                  <i class="fas fa-file-pdf"></i>
              </span>
              <span>Paper</span>
            </a>
          </span>
          <span class="link-block">
            <a href="https://doi.org/10.48550/arXiv.2404.12625"
               class="external-link button is-normal is-rounded is-dark">
              <span class="icon">
                  <i class="ai ai-arxiv"></i>
              </span>
              <span>arXiv</span>
            </a>
          </span>
          <!-- Code Link. -->
          <!--  
          <span class="link-block">
            <a href="https://github.com/vdavoodnia/markerless-neo"
               class="external-link button is-normal is-rounded is-dark">
              <span class="icon">
                  <i class="fab fa-github"></i>
              </span>
              <span>Evaluation</span>
              </a>
          </span>
          -->
          <span class="link-block">
            <a href="#bibtex"
               class="external-link button is-normal is-rounded is-dark">
              <span class="icon">
                  <i class="ai ai-obp"></i>
              </span>
              <span>BibTex</span>
            </a>
          </span> 
        </div>
      </div>
    </div>
  </div>
</div>
</div>
</section>

<!-- Demo Image. -->
<section class="hero is-light is-small">
  <div class="hero-body">
    <div class="container is-max-desktop has-text-centered">
    <div class="columns is-centered has-text-centered">
    <h3 class="title is-4">Waiting on paper acceptance.</h3>
    <div class="column is-four-fifths">
      <div id="results-carousel" class="carousel results-carousel">
        <div class="item item-t2i0">
          <img id="myt2i0" src="/assets/images/wip_dalle.png" class="interpolation-image"/>
        </div>
        <div class="item item-t2i0">
          <img id="myt2i0" src="/assets/images/wip_dalle.png" class="interpolation-image"/>
        </div>
      </div>
    </div>
    </div>
    </div>
  </div>
</section>

<!-- Abstract. -->
<section class="section">
  <div class="container is-max-desktop">
    <!-- Abstract. -->
    <div class="columns is-centered has-text-centered">
      <div class="column is-four-fifths">
        <h2 class="title is-3">Abstract</h2>
        <div class="content has-text-justified">
          <p>
            We introduce SkelFormer, a novel markerless motion capture pipeline for 
            multi-view human pose and shape estimation. Our method first uses off-the-shelf 2D 
            keypoint estimators, pre-trained on large-scale in-the-wild data, to obtain 3D 
            joint positions. Next, we design a regression-based inverse-kinematic skeletal 
            transformer that maps the joint positions to pose and shape representations from 
            heavily noisy observations. This module integrates prior knowledge about pose 
            space and infers the full pose state at runtime. Separating the 3D keypoint 
            detection and inverse-kinematic problems, along with the expressive representations 
            learned by our skeletal transformer, enhance the generalization of our method 
            to unseen noisy data. We evaluate our method on three public datasets in both 
            in-distribution and out-of-distribution settings using three datasets, and 
            observe strong performance with respect to prior works. Moreover, ablation 
            experiments demonstrate the impact of each of the modules of our architecture. 
            Finally, we study the performance of our method in dealing with noise and heavy 
            occlusions and find considerable robustness with respect to other solutions.
          </p>
        </div>
      </div>
    </div>
    <!--/ Abstract. -->
  </div>
</section>

<!-- Technical Video. -->
<section class="section">
    <div class="container is-max-desktop ">
    <div class="columns is-centered is-full-width ">
      <div class="column is-full-width">
        <h2 class="title is-3 has-text-centered" >Technical Video</h2>
        <!-- <div class="content publication-video">
            <iframe src="https://www.youtube.com/embed/KsiZpUFPqIU" allowfullscreen style="top:0;left:0;width:100%;height:100%;"></iframe>
        </div> 
        <div class="content publication-video">
        <video autoplay="" controls="" muted="" loop="" playsinline="" height="100%">
            <source src="./static/images/2418-video.mp4" type="video/mp4">
        </video> 
        </div> -->
        <div class="content publication-video">
        <img id="myt2i0" src="/assets/images/wip_dalle.png" class="interpolation-image"/>
        </div>
      </div>
    </div>
    </div>
</section>

<!-- BibTeX. -->
<section class="section" id="BibTeX">
  <div class="container is-max-desktop content">
    <h2 class="title"><a id="bibtex">BibTeX</a></h2>
    <pre><code>@misc{davoodnia2024skelformermarkerless3dpose,
      title={SkelFormer: Markerless 3D Pose and Shape Estimation using Skeletal Transformers}, 
      author={Vandad Davoodnia and Saeed Ghorbani and Alexandre Messier and Ali Etemad},
      year={2024},
      eprint={2404.12625},
      archivePrefix={arXiv},
      primaryClass={cs.CV},
      url={https://arxiv.org/abs/2404.12625}, 
      doi={10.48550/arXiv.2404.12625}, 
}</code></pre>
  </div>
</section>

<!-- footer. -->
<footer class="footer">
    <div class="columns is-centered">
      <div class="column is-8">
        <div class="content">
          <p>
            This website is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">CC BY-SA 4.0 License</a>:            
            Website adapted from <a href="https://nerfies.github.io/">NeRFies</a>, powered by <a href="https://jekyllrb.com/">Jekyll</a> & <a href="https://mademistakes.com/work/jekyll-themes/minimal-mistakes/">Minimal Mistakes</a>.
          </p>
        </div>
      </div>
    </div>
</footer>

</body>
</html>