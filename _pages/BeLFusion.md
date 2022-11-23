---
layout: standalone_project
title: BeLFusion&#58; Latent Diffusion for Behavior-Driven Human Motion Prediction
permalink: /BeLFusion/
description: Latent Diffusion for Behavior-Driven Human Motion Prediction
venue:
horizontal: false
nav: false
navbar_fixed: false
---



<!---------------------------- HEADER ---------------------------->
<header class="project-title" style="text-align: center; ">
<h1 class="project-title" style="font-weight: bold; color: #404040">{{ page.title }}</h1>
<p class="project-venue">{{ page.venue }}</p>
    <h3>
                    <a href="https://scholar.google.com/citations?user=pRC8DwcAAAAJ&hl=en">German Barquero</a>, 
                    <a href="https://scholar.google.com/citations?user=oI6AIkMAAAAJ&hl=en&oi=ao">Sergio Escalera</a>, and 
                    <a href="https://scholar.google.com/citations?user=V0c9xx0AAAAJ&hl=en&oi=ao">Cristina Palmero</a>
    </h3>
<h5>University of Barcelona and Computer Vision Center, Spain</h5>
<div class="publications project-links">
    <a href="ARXIV LINK" class="btn" role="button">arXiv</a>
    <a href="https://github.com/BarqueroGerman/BeLFusion" class="btn" role="button">Code</a>
</div>
</header>

<div style="margin-top:20px">
{% include figure.html path="assets/img/belfusion/intro.png" title="BeLFusion" class="figure-padding img-fluid rounded z-depth-1" %}
</div>

<!---------------------------- ABSTRACT ---------------------------->
<div class="h-100 d-flex align-items-center justify-content-center" style="margin-top: 30px">
    <div class="project-narrow" id="abstract" style="text-align: justify;">
    <h3 style="text-align: center;">Abstract</h3>
    <i>
    Stochastic human motion prediction (HMP) has generally been tackled with generative adversarial networks and variational autoencoders. Most prior works aim at predicting highly diverse movements in terms of the skeleton joints’ dispersion. This has led to methods predicting fast and motion-divergent movements, which are often unrealistic and incoherent with past motion. Such methods also neglect contexts that need to anticipate diverse low-range behaviors, or actions, with subtle joint displacements. To address these issues, we present BeLFusion, a model that, for the first time, leverages latent diffusion models in HMP to sample from a latent space where behavior is disentangled from pose and motion. As a result, diversity is encouraged from a behavioral perspective. Thanks to our behavior coupler’s ability to transfer sampled behavior to ongoing motion, BeLFusion’s predictions display a variety of behaviors that are significantly more realistic than the state of the art. To support it, we introduce two metrics, the Area of the Cumulative Motion Distribution, and the Average Pairwise Distance Error, which are correlated to our definition of realism according to a qualitative study with 126 participants. Finally, we prove BeLFusion’s generalization power in a new cross-dataset scenario for stochastic HMP.
    </i>
    </div>
</div>


<!---------------------------- ARCHITECTURE ---------------------------->
<div class="h-100 d-flex align-items-center justify-content-center" style="margin-top: 30px">
    <div class="project-narrow" id="architecture" style="text-align: justify;">
        <h3 style="text-align: center;">Architecture</h3>
    </div>
</div>
<div style="margin-top:20px">
{% include figure.html path="assets/img/belfusion/arch.png" title="BeLFusion" class="figure-padding img-fluid rounded z-depth-1" %}
</div>

A latent diffusion model conditioned on an encoding $$x=2$$ of the observation, $$\mathbf{X}$$, progressively denoises a sample from a zero-mean unit variance multivariate normal distribution into a behavior code. Then, the behavior coupler $$\mathcal{B}_{\phi}$$ decodes the prediction by transferring the sampled behavior to the target motion, $$\mathbf{x}_{m}$$. In our implementation, $$f_{\Phi}$$ is a conditional U-Net with cross-attention, and $$h_{\lambda}$$, $$g_{\alpha}$$, and $$\mathcal{B}_{\phi}$$ are one-layer recurrent neural networks.


<!---------------------------- GIFS ---------------------------->
<div style="max-width: site.max_project_width" style="margin-top:50px; padding: 0px !important">
    <h3 style="text-align: center; margin-bottom:20px">Examples <i>in motion</i></h3>
    <div class="justify-content-center list-group list-group-horizontal" id="list-tab" role="tablist">
        <div class="list-group list-group-horizontal" style="max-width:600px">
        <a class="list-group-item list-group-item-action active" id="h36m-list" data-toggle="list" href="#h36m" role="tab" aria-controls="h36m" style="text-align: center;">Human3.6M</a>
        <a class="list-group-item list-group-item-action" id="amass-list" data-toggle="list" href="#amass" role="tab" aria-controls="amass" style="text-align: center;">AMASS</a>
        </div>
    </div>
    <div class="tab-content figure" id="nav-tabContent" style="margin-top:20px" style="padding: 0px !important">
        <div class="tab-pane fade show active" id="h36m" role="tabpanel" aria-labelledby="h36m-list" style="padding: 0px !important">
            <div class="h-100 d-flex align-items-center justify-content-center">
                <div class="dropdown list-group">
                    <button class="btn dropdown-toggle" style="max-width:600px" type="button" id="h36m-btn" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                        <span class="selection">H_4_Sitting</span>
                    </button>
                    <div class="dropdown-menu" aria-labelledby="dropdownMenuButton" id="list-tab" role="tablist">
                        <a class="dropdown-item dropdown-item-action" href="#H_4_Sitting" id="h36m-dropdown" data-toggle="list" role="tab" aria-controls="home">H_4_Sitting</a>
                        <a class="dropdown-item dropdown-item-action" href="#H_148_WalkDog" id="h36m-dropdown" data-toggle="list" role="tab" aria-controls="profile">H_148_WalkDog</a>
                        <a class="dropdown-item dropdown-item-action" href="#H_402_Smoking" id="h36m-dropdown" data-toggle="list" role="tab" aria-controls="messages">H_402_Smoking</a>
                        <a class="dropdown-item dropdown-item-action" href="#H_446_Smoking" id="h36m-dropdown" data-toggle="list" role="tab" aria-controls="messages">H_446_Smoking</a>
                        <a class="dropdown-item dropdown-item-action" href="#H_541_Phoning" id="h36m-dropdown" data-toggle="list" role="tab" aria-controls="messages">H_541_Phoning</a>
                        <a class="dropdown-item dropdown-item-action" href="#H_608_Walking" id="h36m-dropdown" data-toggle="list" role="tab" aria-controls="messages">H_608_Walking</a>
                        <a class="dropdown-item dropdown-item-action" href="#H_861_SittingDown" id="h36m-dropdown" data-toggle="list" role="tab" aria-controls="messages">H_861_SittingDown</a>
                        <a class="dropdown-item dropdown-item-action" href="#H_910_SittingDown" id="h36m-dropdown" data-toggle="list" role="tab" aria-controls="messages">H_910_SittingDown</a>
                        <a class="dropdown-item dropdown-item-action" href="#H_962_WalkTogether" id="h36m-dropdown" data-toggle="list" role="tab" aria-controls="messages">H_962_WalkTogether</a>
                        <a class="dropdown-item dropdown-item-action" href="#H_1928_Eating" id="h36m-dropdown" data-toggle="list" role="tab" aria-controls="messages">H_1928_Eating</a>
                        <a class="dropdown-item dropdown-item-action" href="#H_2103_Photo" id="h36m-dropdown" data-toggle="list" role="tab" aria-controls="messages">H_2103_Photo</a>
                    </div>
                </div>
            </div>
            <div class="col-12" style="padding: 0px !important">
                <div class="tab-content figure" id="nav-tabContent">
                    <div class="tab-pane fade show active gif" id="H_4_Sitting" role="tabpanel"><img class="gif" src="/assets/img/belfusion/hmp_videos/H_4_Sitting.gif"></div>
                    <div class="tab-pane fade" id="H_148_WalkDog" role="tabpanel"><img class="gif" src="/assets/img/belfusion/hmp_videos/H_148_WalkDog.gif"></div>
                    <div class="tab-pane fade" id="H_402_Smoking" role="tabpanel"><img class="gif" src="/assets/img/belfusion/hmp_videos/H_402_Smoking.gif"></div>
                    <div class="tab-pane fade" id="H_446_Smoking" role="tabpanel"><img class="gif" src="/assets/img/belfusion/hmp_videos/H_446_Smoking.gif"></div>
                    <div class="tab-pane fade" id="H_541_Phoning" role="tabpanel"><img class="gif" src="/assets/img/belfusion/hmp_videos/H_541_Phoning.gif"></div>
                    <div class="tab-pane fade" id="H_608_Walking" role="tabpanel"><img class="gif" src="/assets/img/belfusion/hmp_videos/H_608_Walking.gif"></div>
                    <div class="tab-pane fade" id="H_861_SittingDown" role="tabpanel"><img class="gif" src="/assets/img/belfusion/hmp_videos/H_861_SittingDown.gif"></div>
                    <div class="tab-pane fade" id="H_910_SittingDown" role="tabpanel"><img class="gif" src="/assets/img/belfusion/hmp_videos/H_910_SittingDown.gif"></div>
                    <div class="tab-pane fade" id="H_962_WalkTogether" role="tabpanel"><img class="gif" src="/assets/img/belfusion/hmp_videos/H_962_WalkTogether.gif"></div>
                    <div class="tab-pane fade" id="H_1928_Eating" role="tabpanel"><img class="gif" src="/assets/img/belfusion/hmp_videos/H_1928_Eating.gif"></div>
                    <div class="tab-pane fade" id="H_2103_Photo" role="tabpanel"><img class="gif" src="/assets/img/belfusion/hmp_videos/H_2103_Photo.gif"></div>
                </div>
            </div>
        </div>
        <div class="tab-pane fade" id="amass" role="tabpanel" aria-labelledby="amass-list" style="padding: 0px !important">
            <div class="h-100 d-flex align-items-center justify-content-center">
                <div class="dropdown list-group">
                    <button class="btn dropdown-toggle" style="max-width:600px" type="button" id="h36m-btn" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                        <span class="selection">A_103_Transitions</span>
                    </button>
                    <div class="dropdown-menu" aria-labelledby="dropdownMenuButton" id="list-tab" role="tablist">
                        <a class="dropdown-item dropdown-item-action" href="#A_103_Transitions" id="h36m-dropdown" data-toggle="list" role="tab" aria-controls="home">A_103_Transitions</a>
                        <a class="dropdown-item dropdown-item-action" href="#A_1087_DanceDB" id="h36m-dropdown" data-toggle="list" role="tab" aria-controls="home">A_1087_DanceDB</a>
                        <a class="dropdown-item dropdown-item-action" href="#A_1402_DanceDB" id="h36m-dropdown" data-toggle="list" role="tab" aria-controls="home">A_1402_DanceDB</a>
                        <a class="dropdown-item dropdown-item-action" href="#A_1899_DanceDB" id="h36m-dropdown" data-toggle="list" role="tab" aria-controls="profile">A_1899_DanceDB</a>
                        <a class="dropdown-item dropdown-item-action" href="#A_2054_DanceDB" id="h36m-dropdown" data-toggle="list" role="tab" aria-controls="messages">A_2054_DanceDB</a>
                        <a class="dropdown-item dropdown-item-action" href="#A_2284_DanceDB" id="h36m-dropdown" data-toggle="list" role="tab" aria-controls="messages">A_2284_DanceDB</a>
                        <a class="dropdown-item dropdown-item-action" href="#A_2545_DanceDB" id="h36m-dropdown" data-toggle="list" role="tab" aria-controls="messages">A_2545_DanceDB</a>
                        <a class="dropdown-item dropdown-item-action" href="#A_7750_GRAB" id="h36m-dropdown" data-toggle="list" role="tab" aria-controls="messages">A_7750_GRAB</a>
                        <a class="dropdown-item dropdown-item-action" href="#A_9274_GRAB" id="h36m-dropdown" data-toggle="list" role="tab" aria-controls="messages">A_9274_GRAB</a>
                        <a class="dropdown-item dropdown-item-action" href="#A_10929_HUMAN4D" id="h36m-dropdown" data-toggle="list" role="tab" aria-controls="messages">A_10929_HUMAN4D</a>
                        <a class="dropdown-item dropdown-item-action" href="#A_11074_HUMAN4D" id="h36m-dropdown" data-toggle="list" role="tab" aria-controls="messages">A_11074_HUMAN4D</a>
                        <a class="dropdown-item dropdown-item-action" href="#A_12321_SOMA" id="h36m-dropdown" data-toggle="list" role="tab" aria-controls="messages">A_12321_SOMA</a>
                        <a class="dropdown-item dropdown-item-action" href="#A_12391_SOMA" id="h36m-dropdown" data-toggle="list" role="tab" aria-controls="messages">A_12391_SOMA</a>
                    </div>
                </div>
            </div>
            <div style="padding: 0px !important">
                <div class="tab-content figure" id="nav-tabContent">
                    <div class="tab-pane fade show active gif" id="A_103_Transitions" role="tabpanel"><img class="gif" src="/assets/img/belfusion/hmp_videos/A_103_Transitions.gif"></div>
                    <div class="tab-pane fade" id="A_1087_DanceDB" role="tabpanel"><img class="gif" src="/assets/img/belfusion/hmp_videos/A_1087_DanceDB.gif"></div>
                    <div class="tab-pane fade" id="A_1402_DanceDB" role="tabpanel"><img class="gif" src="/assets/img/belfusion/hmp_videos/A_1402_DanceDB.gif"></div>
                    <div class="tab-pane fade" id="A_1899_DanceDB" role="tabpanel"><img class="gif" src="/assets/img/belfusion/hmp_videos/A_1899_DanceDB.gif"></div>
                    <div class="tab-pane fade" id="A_2054_DanceDB" role="tabpanel"><img class="gif" src="/assets/img/belfusion/hmp_videos/A_2054_DanceDB.gif"></div>
                    <div class="tab-pane fade" id="A_2284_DanceDB" role="tabpanel"><img class="gif" src="/assets/img/belfusion/hmp_videos/A_2284_DanceDB.gif"></div>
                    <div class="tab-pane fade" id="A_2545_DanceDB" role="tabpanel"><img class="gif" src="/assets/img/belfusion/hmp_videos/A_2545_DanceDB.gif"></div>
                    <div class="tab-pane fade" id="A_7667_GRAB" role="tabpanel"><img class="gif" src="/assets/img/belfusion/hmp_videos/A_7667_GRAB.gif"></div>
                    <div class="tab-pane fade" id="A_7750_GRAB" role="tabpanel"><img class="gif" src="/assets/img/belfusion/hmp_videos/A_7750_GRAB.gif"></div>
                    <div class="tab-pane fade" id="A_9274_GRAB" role="tabpanel"><img class="gif" src="/assets/img/belfusion/hmp_videos/A_9274_GRAB.gif"></div>
                    <div class="tab-pane fade" id="A_10929_HUMAN4D" role="tabpanel"><img class="gif" src="/assets/img/belfusion/hmp_videos/A_10929_HUMAN4D.gif"></div>
                    <div class="tab-pane fade" id="A_11074_HUMAN4D" role="tabpanel"><img class="gif" src="/assets/img/belfusion/hmp_videos/A_11074_HUMAN4D.gif"></div>
                    <div class="tab-pane fade" id="A_12321_SOMA" role="tabpanel"><img class="gif" src="/assets/img/belfusion/hmp_videos/A_12321_SOMA.gif"></div>
                    <div class="tab-pane fade" id="A_12391_SOMA" role="tabpanel"><img class="gif" src="/assets/img/belfusion/hmp_videos/A_12391_SOMA.gif"></div>
                </div>
            </div>
        </div>
    </div>
</div>
          



<!---------------------------- BIBLIOGRAPHY ---------------------------->

<div class="h-100 d-flex align-items-center justify-content-center" style="margin-top: 30px">
    <div class="project-narrow" id="bibtex" style="text-align: justify;">
        <h3 style="text-align: center;">BibTeX</h3>
        <div class="bibtex">
        {% highlight bibtex %}
@article{barquero2020rimnet,
  title={RimNet: A deep 3D multimodal MRI architecture for paramagnetic rim lesion assessment in multiple sclerosis},
  author={Barquero, Germ{\'a}n and La Rosa, Francesco and Kebiri, Hamza and Lu, Po-Jui and Rahmanzadeh, Reza and Weigel, Matthias and Fartaria, M{\'a}rio Jo{\~a}o and Kober, Tobias and Th{\'e}audin, Marie and Du Pasquier, Renaud and others},
  journal={NeuroImage: Clinical},
  volume={28},
  pages={102412},
  year={2020},
  publisher={Elsevier}
}
{% endhighlight %}

        </div>
    </div>
</div>
