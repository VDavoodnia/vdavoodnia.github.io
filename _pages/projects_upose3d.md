---
layout: standalone
title: "UPose3D"
permalink: /projects/upose3d/
description: "UPose3D: uncertainty-aware 3D human pose estimation with cross-view and temporal cues."
head_defer_scripts:
  - "/projects/upose3d/static/js/fontawesome.all.min.js"
head_scripts:
  - "https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"
  - "/projects/upose3d/static/js/bulma-carousel.min.js"
  - "/projects/upose3d/static/js/bulma-slider.min.js"
  - "/projects/upose3d/static/js/index.js"
  - "/projects/upose3d/static/js/magnifier.js"
stylesheet_links:
  - "https://fonts.googleapis.com/css?family=Google+Sans|Noto+Sans|Castoro"
  - "/projects/upose3d/static/css/bulma.min.css"
  - "/projects/upose3d/static/css/bulma-carousel.min.css"
  - "/projects/upose3d/static/css/bulma-slider.min.css"
  - "/projects/upose3d/static/css/tab_gallery.css"
  - "/projects/upose3d/static/css/fontawesome.all.min.css"
  - "https://cdn.jsdelivr.net/gh/jpswalsh/academicons@1/css/academicons.min.css"
  - "/projects/upose3d/static/css/index.css"
  - "https://fonts.cdnfonts.com/css/menlo"
  - "/projects/upose3d/static/css/image_card_fader.css"
  - "/projects/upose3d/static/css/image_card_slider.css"
script_name: "upose3d"
---


<html>
<body>
<!-- Some margin. -->
<div style="height: 100px;">&nbsp;</div>

<!-- Banner. -->
<section class="hero banner">
<div class="hero-body">
<div class="container is-max-desktop">
  <div class="columns is-centered">
    <div class="column has-text-centered">
      <h1 class="title is-2 publication-title">UPose3D: <br> Uncertainty-aware 3D Human Pose Estimation with Cross-view and Temporal Cues</h1>
      <div class="is-size-5 publication-authors">
        <span class="author-block">
          <a href="https://vdavoodnia.github.io/">Vandad Davoodnia</a><sup>1,2</sup>,
        </span>
        <span class="author-block">
          <a href="https://saeed1262.github.io/">Saeed Ghorbani</a><sup>2</sup>,
        </span>
        <span class="author-block">
          <a href="https://macarbonneau.github.io/">Marc-André Carbonneau</a><sup>2</sup>,
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
            <a href="./static/paper/upose3d_arxiv.pdf"
               class="external-link button is-normal is-rounded is-dark">
              <span class="icon">
                  <i class="fas fa-file-pdf"></i>
              </span>
              <span>Paper</span>
            </a>
          </span>
          <span class="link-block">
            <a href="https://doi.org/10.48550/arXiv.2404.14634"
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
      <div class="column is-four-fifths">
      <div id="results-carousel" class="carousel results-carousel">
        <video autoplay="" controls="" muted="" loop="" playsinline="" height="100%">
            <source src="./static/images/demo_cmu.mp4" type="video/mp4">
        </video>
        <div class="item item-t2i0">
          <img id="myt2i0" src="./static/images/demo_1.png" class="interpolation-image"/>
        </div>
        <div class="item item-t2i0">
          <img id="myt2i0" src="./static/images/demo_2.png" class="interpolation-image"/>
        </div>
      </div>
    </div>
    </div>
    <h3 class="title is-4">Upose3D Accurately Predicts 3D Keypoints From Multiple Views</h3>
    <h4 class="title is-5">It scales well with additional camera views at constant runtime</h4>
    <div class="columns is-centered has-text-centered">
      <div class="column is-four-fifths">
        <div class="item item-t2i0">
          <img id="myt2i0" src="./static/images/scaling.png" class="interpolation-image"/>
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
            We introduce UPose3D, a novel approach for multi-view 3D human pose estimation, 
            addressing challenges in accuracy and scalability. Our method advances existing 
            pose estimation frameworks by improving robustness and flexibility without requiring 
            direct 3D annotations. At the core of our method, a pose compiler module refines 
            predictions from a 2D keypoints estimator that operates on a single image by 
            leveraging temporal and cross-view information. Our novel cross-view fusion strategy 
            is scalable to any number of cameras, while our synthetic data generation strategy 
            ensures generalization across diverse actors, scenes, and viewpoints. Finally, 
            UPose3D leverages the prediction uncertainty of both the 2D keypoint estimator 
            and the pose compiler module. This provides robustness to outliers and noisy data, 
            resulting in state-of-the-art performance in out-of-distribution settings. In 
            addition, for in-distribution settings, UPose3D yields a performance rivaling 
            methods that rely on 3D annotated data, while being the state-of-the-art among 
            methods relying only on 2D supervision.
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
        </div> -->
        <div class="content publication-video">
        <video autoplay="" controls="" muted="" loop="" playsinline="" height="100%">
            <source src="./static/images/2418-video.mp4" type="video/mp4">
        </video>
        </div>
      </div>
    </div>
    </div>
</section>

<!-- BibTeX. -->
<section class="section" id="BibTeX">
  <div class="container is-max-desktop content">
    <h2 class="title"><a id="bibtex">BibTeX</a></h2>
    <pre><code>@misc{davoodnia2024upose3d,
      title={UPose3D: Uncertainty-Aware 3D Human Pose Estimation with Cross-View and Temporal Cues}, 
      author={Vandad Davoodnia and Saeed Ghorbani and Marc-André Carbonneau and Alexandre Messier and Ali Etemad},
      year={2024},
      eprint={2404.14634},
      archivePrefix={arXiv},
      primaryClass={cs.CV},
      url={https://arxiv.org/abs/2404.14634}, 
      doi={https://doi.org/10.48550/arXiv.2404.14634}
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