---
layout: standalone_project
title: FlowMDM&#58; Seamless Human Motion Composition with<br>Blended Positional Encodings
permalink: /FlowMDM/
description: FlowMDM
venue: arXiv 2024
horizontal: false
nav: false
navbar_fixed: false
---

<!---------------------------- HEADER ---------------------------->
<header class="project-title" style="text-align: center; ">
<!--h1 class="project-title title" style="font-weight: bold; color: #404040">{{ page.title }}</h1-->
<h1 class="project-title title" style="font-weight: bold;">
    <span class="gradient-text" style="background: linear-gradient(90deg, #ff0000, 15%, #00a1ff, 60%, #00D70C); -webkit-background-clip: text; color: transparent; font-size: 2.5rem">{{ page.title }}</span> 
  </h1>
<p class="project-venue" style="font-size: 1.5em;">{{ page.venue }}</p>
    <h3>
                    <a href="https://scholar.google.com/citations?user=pRC8DwcAAAAJ&hl=en">German Barquero</a>, 
                    <a href="https://scholar.google.com/citations?user=oI6AIkMAAAAJ&hl=en&oi=ao">Sergio Escalera</a>, and 
                    <a href="https://scholar.google.com/citations?user=V0c9xx0AAAAJ&hl=en&oi=ao">Cristina Palmero</a>
    </h3>
<h5>University of Barcelona and Computer Vision Center, Spain</h5>
<div class="publications project-links">
    <a href="" class="btn" role="button">arXiv</a>
    <a href="https://github.com/BarqueroGerman/FlowMDM" class="btn" role="button">Code</a>
</div>
</header>

<div style="margin-top:20px">
{% include figure.liquid path="assets/img/flowmdm/teaser.png" title="teaser" class="figure-padding img-fluid rounded" %}
</div>


<!---------------------------- ABSTRACT ---------------------------->
<div class="d-flex align-items-center justify-content-center" style="margin-top: 30px">
    <div class="project-narrow" id="abstract" style="text-align: justify;">
    <h3 style="text-align: center;">📌 Abstract</h3>
    <i>
    Conditional human motion generation is an important topic with many applications in virtual reality, gaming, and robotics. While prior works have focused on generating motion guided by text, music, or scenes, these typically result in isolated motions confined to short durations. Instead, we address the generation of long, continuous sequences guided by a series of varying textual descriptions.
    <br><br>
    In this context, we introduce <b>FlowMDM</b>, the first diffusion-based model that generates seamless Human Motion Compositions (HMC) without any postprocessing or redundant denoising steps. For this, we introduce the <b>Blended Positional Encodings</b>, a technique that leverages both absolute and relative positional encodings in the denoising chain. More specifically, global motion coherence is recovered at the absolute stage, whereas smooth and realistic transitions are built at the relative stage. As a result, we achieve state-of-the-art results in terms of accuracy, realism, and smoothness on the Babel and HumanML3D datasets. FlowMDM excels when trained with only a single description per motion sequence thanks to its <b>Pose-Centric Cross-ATtention</b>, which makes it robust against varying text descriptions at inference time.
    <br><br>
    Finally, to address the limitations of existing HMC metrics, we propose two new metrics: the Peak Jerk and the Area Under the Jerk, to detect abrupt transitions.
    </i>
    </div>
</div>


<!---------------------------- COMPOSITION VIDEOS ---------------------------->

<div class="align-items-center" style="max-width: site.max_project_width; margin-top:50px; text-align: center;">
    <h3 style="text-align: center; margin-bottom:20px">🎬 Human Motion Composition (🏃🏻‍♀️➜🚶🏻‍♀️➜🧎🏻‍♀️➜🧘🏻‍♀️)</h3>
    <div id="carouselCompositions" class="carousel slide" data-ride="carousel" data-interval="false">
        <ol class="carousel-indicators">
            <li data-target="#carouselCompositions" data-slide-to="0" class="active"></li>
            <li data-target="#carouselCompositions" data-slide-to="1"></li>
            <li data-target="#carouselCompositions" data-slide-to="2"></li>
            <li data-target="#carouselCompositions" data-slide-to="3"></li>
            <li data-target="#carouselCompositions" data-slide-to="4"></li>
            <li data-target="#carouselCompositions" data-slide-to="5"></li>
            <li data-target="#carouselCompositions" data-slide-to="6"></li>
            <li data-target="#carouselCompositions" data-slide-to="7"></li>
        </ol>
        <div class="carousel-inner">
            <div class="carousel-item active">{% include video.liquid path="assets/video/flowmdm/babel_compo_6A.webm" class="img-fluid rounded" controls=true  autoplay=true muted=true loop=true width="100%" %}</div>
            <div class="carousel-item">{% include video.liquid path="assets/video/flowmdm/babel_compo_6B.webm" class="img-fluid rounded" controls=true  autoplay=true muted=true loop=true width="100%" %}</div>
            <div class="carousel-item">{% include video.liquid path="assets/video/flowmdm/babel_compo_CA.webm" class="img-fluid rounded" controls=true  autoplay=true muted=true loop=true width="100%" %}</div>
            <div class="carousel-item">{% include video.liquid path="assets/video/flowmdm/babel_compo_CB.webm" class="img-fluid rounded" controls=true  autoplay=true muted=true loop=true width="100%" %}</div>
            <div class="carousel-item">{% include video.liquid path="assets/video/flowmdm/babel_compo_CC.webm" class="img-fluid rounded" controls=true  autoplay=true muted=true loop=true width="100%" %}</div>
            <div class="carousel-item">{% include video.liquid path="assets/video/flowmdm/babel_compo_CD.webm" class="img-fluid rounded" controls=true  autoplay=true muted=true loop=true width="100%" %}</div>
            <div class="carousel-item">{% include video.liquid path="assets/video/flowmdm/babel_compo_CE.webm" class="img-fluid rounded" controls=true  autoplay=true muted=true loop=true width="100%" %}</div>
            <div class="carousel-item">{% include video.liquid path="assets/video/flowmdm/babel_compo_CF.webm" class="img-fluid rounded" controls=true  autoplay=true muted=true loop=true width="100%" %}</div>
        </div>
        <button class="carousel-control-prev" type="button" data-target="#carouselCompositions" data-slide="prev">
            <span class="carousel-control-prev-icon" aria-hidden="true"></span>
            <span class="sr-only">Previous</span>
        </button>
        <button class="carousel-control-next" type="button" data-target="#carouselCompositions" data-slide="next">
            <span class="carousel-control-next-icon" aria-hidden="true"></span>
            <span class="sr-only">Next</span>
        </button>
    </div>
    <div class="col-10" style="text-align: justify; display: inline-block; margin-top: -20px">
        Solid curves match the trajectories of the <b style="color: blue">global position</b> (<b style="color: blue">blue</b>) and <b style="color: purple">left</b>/<b style="color: green">right</b> hands (<b style="color: purple">purple</b>/<b style="color: green">green</b>). Darker colors indicate instantaneous jerk deviations from the median value, saturating at twice the jerk's standard deviation in the dataset (<b>black segments</b>). 
        Abrupt transitions manifest as black segments amidst lighter ones.
    </div>
</div>


<!---------------------------- EXTRAPOLATION VIDEOS ---------------------------->

<div style="max-width: site.max_project_width; margin-top:50px;">
    <h3 style="text-align: center; margin-bottom:20px">🎬 Human Motion Extrapolation (🚶➜🚶➜🚶➜🚶)</h3>
    <div id="carouselExtrapolations" class="carousel slide" data-ride="carousel" data-interval="false">
        <ol class="carousel-indicators">
            <li data-target="#carouselExtrapolations" data-slide-to="0" class="active"></li>
            <li data-target="#carouselExtrapolations" data-slide-to="1"></li>
            <li data-target="#carouselExtrapolations" data-slide-to="2"></li>
            <li data-target="#carouselExtrapolations" data-slide-to="3"></li>
        </ol>
        <div class="carousel-inner">
            <div class="carousel-item active">{% include video.liquid path="assets/video/flowmdm/babel_extra_6D.webm" class="img-fluid rounded" controls=true  autoplay=true muted=true loop=true width="100%" %}</div>
            <div class="carousel-item">{% include video.liquid path="assets/video/flowmdm/babel_extra_6C.webm" class="img-fluid rounded" controls=true  autoplay=true muted=true loop=true width="100%" %}</div>
            <div class="carousel-item">{% include video.liquid path="assets/video/flowmdm/babel_extra_CH.webm" class="img-fluid rounded" controls=true  autoplay=true muted=true loop=true width="100%" %}</div>
            <div class="carousel-item">{% include video.liquid path="assets/video/flowmdm/babel_extra_CG.webm" class="img-fluid rounded" controls=true  autoplay=true muted=true loop=true width="100%" %}</div>
        </div>
        <button class="carousel-control-prev" type="button" data-target="#carouselExtrapolations" data-slide="prev">
            <span class="carousel-control-prev-icon" aria-hidden="true"></span>
            <span class="sr-only">Previous</span>
        </button>
        <button class="carousel-control-next" type="button" data-target="#carouselExtrapolations" data-slide="next">
            <span class="carousel-control-next-icon" aria-hidden="true"></span>
            <span class="sr-only">Next</span>
        </button>
    </div>
</div>

<!---------------------------- ARCHITECTURE ---------------------------->

<div class="d-flex align-items-center justify-content-center" style="margin-top: 0px">
    <div class="project-narrow" id="motivations" style="text-align: justify;">
    <h3 style="text-align: center;">🌟 Key contributions 🌟</h3>
    </div>
</div>

<div id="accordion" style="margin-top:20px">
  <div class="card">
    <div class="card-header" id="headingTwo" style="text-align: center; padding:0px">
        <button class="btn btn-link collapsed dropdown-toggle" data-toggle="collapse" data-target="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo" style="text-align: center;" style="font-size: 16px">
          #1 - Blended positional encodings (BPE)
        </button>
    </div>
    <div id="collapseTwo" class="collapse" aria-labelledby="headingTwo" data-parent="#accordion">
      <div class="card-body" style="text-align: center;">        
            <div style="text-align: justify;">
            <b>Key observation:</b> at early denoising phases, motion diffusion models prioritize global inter-frame dependencies, shifting towards local relative dependencies as the process unfolds.
        </div>
      {% include figure.liquid path="assets/img/flowmdm/local_vs_global_attention.png" title="local_vs_global_att" class="figure-padding rounded col-7"%}
      <div style="margin-bottom: 20px; text-align: justify;">
            The BPE exploits this observation to seamlessly build human motion compositions from different textual descriptions:
            <br>
            1) <b>At early denoising stages</b>: absolute positional encodings + global attention restricted to each textual description.
            <br>
            2) <b>At later denoising stages</b>: relative positional encodings + unrestricted windowed attention.
            <br><br>
            <b><u>Consequence</u></b>: intra-subsequence global dependencies are recovered at the beginning of the denoising, and intra- and inter-subsequences motion smoothness and realism are promoted later.
            <br>
            <b><u>How?</u></b> To make the model understand APE and RPE at inference, we expose it to both encodings by randomly alternating them during training. As a result, the BPE schedule can be tuned at inference time to balance the intra-subsequence coherence and the inter-subsequence realism trade-off.
        </div>
      </div>
    </div>
  </div>
  <div class="card">
    <div class="card-header" id="headingOne" style="text-align: center; padding:0px;">
        <button class="btn btn-link dropdown-toggle" data-toggle="collapse" data-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne" style="font-size: 16px">
            #2 - Pose-centric cross-attention (PCCATT)
        </button>
    </div>
    <div id="collapseOne" class="collapse" aria-labelledby="headingOne" data-parent="#accordion">
      <div class="card-body">
        <div class="row">
            <div class="col-7">
            {% include figure.liquid path="assets/img/flowmdm/arch.png" title="Motion" class="figure-padding img-fluid rounded" %}
            </div>
            <div class="col-5" style="text-align: justify;">
                The PCCATT minimizes the entanglement between the control signal (e.g., text, objects) and the noisy motion by feeding the former only to the query. Consequently, our model denoises each frame’s noisy pose only leveraging its own condition, and the neighboring noisy poses.
                <br><br>
                <b><u>Consequence</u></b>: the PCCATT makes our model robust against varying text descriptions at inference time, and it excels when trained with only a single description per motion sequence. → FlowMDM can be applied to <b>both supervised and unsupervised</b> human motion composition scenarios.
            </div>
        </div>
      </div>
    </div>
  </div>
</div>


<!---------------------------- FIGURE vs. SOTA ---------------------------->

<div class="d-flex align-items-center justify-content-center" style="margin-top: 50px;">
    <div class="project-narrow" id="motivations" style="text-align: justify;">
        <h3 style="text-align: center;">🥇 State-of-the-art composition and extrapolation 🥇</h3>
    </div>
</div>

<div class="card d-flex align-items-center justify-content-center" style="margin-top: 30px; padding:1rem">
    <div style="">
    {% include figure.liquid path="assets/img/flowmdm/qualitative_results.png" title="Qualitative Results" class="figure-padding img-fluid rounded" %}
    </div>
    <div style="text-align: justify;">
    Solid curves match the trajectories of the <b style="color: blue">global position</b> (<b style="color: blue">blue</b>) and <b style="color: purple">left</b>/<b style="color: green">right</b> hands (<b style="color: purple">purple</b>/<b style="color: green">green</b>). Darker colors indicate instantaneous jerk deviations from the median value, saturating at twice the jerk's standard deviation in the dataset (<b>black segments</b>). 
    Abrupt transitions manifest as black segments amidst lighter ones. 
    FlowMDM exhibits the most fluid motion and preserves the staticity or periodicity of extrapolated actions, in contrast to other methods that show spontaneous high jerk values and fail to keep the motion coherence in extrapolations.
    </div>
</div>


<!---------------------------- BIBLIOGRAPHY ---------------------------->

<div class="d-flex align-items-center justify-content-center" style="margin-top: 30px">
    <div class="project-narrow" id="bibtex" style="text-align: justify;">
        <h3 style="text-align: center;">🔗 BibTeX</h3>
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

<style>
    .carousel-control-next-icon {
        background-image: url("/assets/img/others/arrow_right_black.svg") !important;
    }

    .carousel-control-prev-icon {
        background-image: url("/assets/img/others/arrow_left_black.svg") !important;
    }

    .carousel-control-next-icon, .carousel-control-prev-icon {
        width: 3rem !important;
        height: 3rem !important;
    }

    .carousel-control-next {
        justify-content: flex-end;
        width: fit-content !important;
    }

    .carousel-control-prev {
        justify-content: flex-start;
        width: fit-content !important;
    }

    .carousel-inner {
        margin-bottom: 10%;
        width: 90%;
        margin-left: 5%;
    }

    .carousel-indicators {
        bottom: -2.5rem;
    }

    .carousel .carousel-indicators li {
        background-color: #777
    }

</style>