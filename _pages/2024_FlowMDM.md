---
layout: standalone_project
title: FlowMDM&#58; Seamless Human Motion Composition with Blended Positional Encodings
permalink: /FlowMDM/
description: Seamless Human Motion Composition with Blended Positional Encodings
venue: arXiv
horizontal: false
nav: false
navbar_fixed: false
---

<!---------------------------- HEADER ---------------------------->
<header class="project-title" style="text-align: center; ">
<h1 class="project-title" style="font-weight: bold; color: #404040">{{ page.title }}</h1>
<p class="project-venue" style="font-size: 2.5em;">{{ page.venue }}</p>
    <h3>
                    <a href="https://scholar.google.com/citations?user=pRC8DwcAAAAJ&hl=en">German Barquero</a>, 
                    <a href="https://scholar.google.com/citations?user=oI6AIkMAAAAJ&hl=en&oi=ao">Sergio Escalera</a>, and 
                    <a href="https://scholar.google.com/citations?user=V0c9xx0AAAAJ&hl=en&oi=ao">Cristina Palmero</a>
    </h3>
<h5>University of Barcelona and Computer Vision Center, Spain</h5>
<div class="publications project-links">
    <!--a href="https://openaccess.thecvf.com/content/ICCV2023/html/Barquero_BeLFusion_Latent_Diffusion_for_Behavior-Driven_Human_Motion_Prediction_ICCV_2023_paper.html" class="btn" role="button">Paper</a-->
    <!--a href="https://arxiv.org/abs/2211.14304" class="btn" role="button">arXiv</a-->
    <a href="https://github.com/BarqueroGerman/FlowMDM" class="btn" role="button">Code</a>
</div>
</header>

<!--div style="margin-top:20px">
{% include figure.html path="assets/img/belfusion/intro.png" title="BeLFusion" class="figure-padding img-fluid rounded z-depth-1" %}
</div-->

<!---------------------------- ABSTRACT ---------------------------->
<div class="h-100 d-flex align-items-center justify-content-center" style="margin-top: 30px">
    <div class="project-narrow" id="abstract" style="text-align: justify;">
    <h3 style="text-align: center;">Abstract</h3>
    <!--i>
    Stochastic human motion prediction (HMP) has generally been tackled with generative adversarial networks and variational autoencoders. Most prior works aim at predicting highly diverse movements in terms of the skeleton joints’ dispersion. This has led to methods predicting fast and motion-divergent movements, which are often unrealistic and incoherent with past motion. Such methods also neglect contexts that need to anticipate diverse low-range behaviors, or actions, with subtle joint displacements. To address these issues, we present BeLFusion, a model that, for the first time, leverages latent diffusion models in HMP to sample from a latent space where behavior is disentangled from pose and motion. As a result, diversity is encouraged from a behavioral perspective. Thanks to our behavior coupler’s ability to transfer sampled behavior to ongoing motion, BeLFusion’s predictions display a variety of behaviors that are significantly more realistic than the state of the art. To support it, we introduce two metrics, the Area of the Cumulative Motion Distribution, and the Average Pairwise Distance Error, which are correlated to our definition of realism according to a qualitative study with 126 participants. Finally, we prove BeLFusion’s generalization power in a new cross-dataset scenario for stochastic HMP.
    </i-->
    </div>
</div>

<!---------------------------- BIBLIOGRAPHY ---------------------------->

<div class="h-100 d-flex align-items-center justify-content-center" style="margin-top: 30px">
    <div class="project-narrow" id="bibtex" style="text-align: justify;">
        <h3 style="text-align: center;">BibTeX</h3>
        <div class="bibtex">
        {% highlight bibtex %}
@inproceedings{barquero2024seamless,
  title={Seamless Human Motion Composition with Blended Positional Encodings},
  author={Barquero, German and Escalera, Sergio and Palmero, Cristina},
  booktitle={arXiv},
  year={2024}
}
{% endhighlight %}

        </div>
    </div>
</div>
