---
layout: standalone_project
title: BeLFusion&#58; Latent Diffusion for Behavior-Driven Human Motion Prediction
permalink: /BeLFusion_old/
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
{% include figure.html path="assets/img/belfusion/intro.png" title="BeLFusion" class="img-fluid rounded z-depth-1" %}
</div>

<!---------------------------- ABSTRACT ---------------------------->
<div class="h-100 d-flex align-items-center justify-content-center" style="margin-top: 30px">
    <div class="col-8" id="abstract" style="text-align: justify;">
    <h3 style="text-align: center;">Abstract</h3>
    <i>
    Stochastic human motion prediction (HMP) has generally been tackled with generative adversarial networks and variational autoencoders. Most prior works aim at predicting highly diverse movements in terms of the skeleton joints’ dispersion. This has led to methods predicting fast and motion-divergent movements, which are often unrealistic and incoherent with past motion. Such methods also neglect contexts that need to anticipate diverse low-range behaviors, or actions, with subtle joint displacements. To address these issues, we present BeLFusion, a model that, for the first time, leverages latent diffusion models in HMP to sample from a latent space where behavior is disentangled from pose and motion. As a result, diversity is encouraged from a behavioral perspective. Thanks to our behavior coupler’s ability to transfer sampled behavior to ongoing motion, BeLFusion’s predictions display a variety of behaviors that are significantly more realistic than the state of the art. To support it, we introduce two metrics, the Area of the Cumulative Motion Distribution, and the Average Pairwise Distance Error, which are correlated to our definition of realism according to a qualitative study with 126 participants. Finally, we prove BeLFusion’s generalization power in a new cross-dataset scenario for stochastic HMP.
    </i>
    </div>
</div>



<!---------------------------- GIFS BACKUP ---------------------------->
<div style="max-width: site.max_project_width" style="margin-top:50px">
    <h3 style="text-align: center; margin-bottom:20px">Examples <i>in motion</i></h3>
    <div class="col-12 list-group list-group-horizontal justify-content-center" id="list-tab" role="tablist">
        <a class="col-2 list-group-item list-group-item-action active" id="h36m-list" data-toggle="list" href="#h36m" role="tab" aria-controls="h36m" style="text-align: center;">Human3.6M</a>
        <a class="col-2 list-group-item list-group-item-action" id="amass-list" data-toggle="list" href="#amass" role="tab" aria-controls="amass" style="text-align: center;">AMASS</a>
    </div>
    <div class="col-12 tab-content figure" id="nav-tabContent" style="margin-top:20px">
        <div class="tab-pane fade show active" id="h36m" role="tabpanel" aria-labelledby="h36m-list">
            <div class="row">
                <div class="col-2">
                    <div class="list-group" id="list-tab" role="tablist">
                    <a class="list-group-item list-group-item-action active" id="list-home-list" data-toggle="list" href="#list-home" role="tab" aria-controls="home">232323</a>
                    <a class="list-group-item list-group-item-action" id="list-profile-list" data-toggle="list" href="#list-profile" role="tab" aria-controls="profile">Profile</a>
                    <a class="list-group-item list-group-item-action" id="list-messages-list" data-toggle="list" href="#list-messages" role="tab" aria-controls="messages">Messages</a>
                    <a class="list-group-item list-group-item-action" id="list-settings-list" data-toggle="list" href="#list-settings" role="tab" aria-controls="settings">Settings</a>
                    </div>
                </div>
                <div class="col-10">
                    <div class="tab-content figure" id="nav-tabContent">
                    <div class="tab-pane fade show active gif" id="list-home" role="tabpanel" aria-labelledby="list-home-list"><img class="gif" src="/assets/img/belfusion/hmp_videos/A_103_Transitions.gif"></div>
                    <div class="tab-pane fade" id="list-profile" role="tabpanel" aria-labelledby="list-profile-list">...</div>
                    <div class="tab-pane fade" id="list-messages" role="tabpanel" aria-labelledby="list-messages-list">...</div>
                    <div class="tab-pane fade" id="list-settings" role="tabpanel" aria-labelledby="list-settings-list">...</div>
                    </div>
                </div>
            </div>
        </div>
        <div class="tab-pane fade" id="amass" role="tabpanel" aria-labelledby="amass-list">
            <div class="row">
                <div class="col-2">
                    <div class="list-group" id="list-tab" role="tablist">
                        <a class="list-group-item list-group-item-action active" id="a1-list" data-toggle="list" href="#a1" role="tab" aria-controls="home">sdfs</a>
                        <a class="list-group-item list-group-item-action" id="a2-list" data-toggle="list" href="#a2" role="tab" aria-controls="profile">Profile</a>
                        <a class="list-group-item list-group-item-action" id="a3-list" data-toggle="list" href="#a3" role="tab" aria-controls="messages">Messages</a>
                        <a class="list-group-item list-group-item-action" id="a4-list" data-toggle="list" href="#a4" role="tab" aria-controls="settings">Settings</a>
                        <a class="list-group-item list-group-item-action" id="a5-list" data-toggle="list" href="#a5" role="tab" aria-controls="settings">Settings</a>
                        <a class="list-group-item list-group-item-action" id="a6-list" data-toggle="list" href="#a6" role="tab" aria-controls="settings">Settings</a>
                        <a class="list-group-item list-group-item-action" id="a7-list" data-toggle="list" href="#a7" role="tab" aria-controls="settings">Settings</a>
                        <a class="list-group-item list-group-item-action" id="a8-list" data-toggle="list" href="#a8" role="tab" aria-controls="settings">Settings</a>
                        <a class="list-group-item list-group-item-action" id="a9-list" data-toggle="list" href="#a9" role="tab" aria-controls="settings">Settings</a>
                        <a class="list-group-item list-group-item-action" id="a10-list" data-toggle="list" href="#a10" role="tab" aria-controls="settings">Settings</a>
                        <a class="list-group-item list-group-item-action" id="a11-list" data-toggle="list" href="#a11" role="tab" aria-controls="settings">Settings</a>
                        <a class="list-group-item list-group-item-action" id="a12-list" data-toggle="list" href="#a12" role="tab" aria-controls="settings">Settings</a>
                        <a class="list-group-item list-group-item-action" id="a13-list" data-toggle="list" href="#a13" role="tab" aria-controls="settings">Settings</a>
                        <a class="list-group-item list-group-item-action" id="a14-list" data-toggle="list" href="#a14" role="tab" aria-controls="settings">Settings</a>
                    </div>
                </div>
                <div class="col-10">
                    <div class="tab-content figure" id="nav-tabContent">
                        <div class="tab-pane fade show active gif" id="a1" role="tabpanel" aria-labelledby="a1-list"><img class="gif" src="/assets/img/belfusion/hmp_videos/A_103_Transitions.gif"></div>
                        <div class="tab-pane fade gif" id="a2" role="tabpanel" aria-labelledby="a2-list"><img class="gif" src="/assets/img/belfusion/hmp_videos/A_1087_DanceDB.gif"></div>
                        <div class="tab-pane fade gif" id="a3" role="tabpanel" aria-labelledby="a3-list"><img class="gif" src="/assets/img/belfusion/hmp_videos/A_1402_DanceDB.gif"></div>
                        <div class="tab-pane fade gif" id="a4" role="tabpanel" aria-labelledby="a4-list"><img class="gif" src="/assets/img/belfusion/hmp_videos/A_1899_DanceDB.gif"></div>
                        <div class="tab-pane fade gif" id="a5" role="tabpanel" aria-labelledby="a5-list"><img class="gif" src="/assets/img/belfusion/hmp_videos/A_2054_DanceDB.gif"></div>
                        <div class="tab-pane fade gif" id="a6" role="tabpanel" aria-labelledby="a6-list"><img class="gif" src="/assets/img/belfusion/hmp_videos/A_2284_DanceDB.gif"></div>
                        <div class="tab-pane fade gif" id="a7" role="tabpanel" aria-labelledby="a7-list"><img class="gif" src="/assets/img/belfusion/hmp_videos/A_2545_DanceDB.gif"></div>
                        <div class="tab-pane fade gif" id="a8" role="tabpanel" aria-labelledby="a8-list"><img class="gif" src="/assets/img/belfusion/hmp_videos/A_7667_GRAB.gif"></div>
                        <div class="tab-pane fade gif" id="a9" role="tabpanel" aria-labelledby="a9-list"><img class="gif" src="/assets/img/belfusion/hmp_videos/A_7750_GRAB.gif"></div>
                        <div class="tab-pane fade gif" id="a10" role="tabpanel" aria-labelledby="a10-list"><img class="gif" src="/assets/img/belfusion/hmp_videos/A_9274_GRAB.gif"></div>
                        <div class="tab-pane fade gif" id="a11" role="tabpanel" aria-labelledby="a11-list"><img class="gif" src="/assets/img/belfusion/hmp_videos/A_10929_HUMAN4D.gif"></div>
                        <div class="tab-pane fade gif" id="a12" role="tabpanel" aria-labelledby="a12-list"><img class="gif" src="/assets/img/belfusion/hmp_videos/A_11074_HUMAN4D.gif"></div>
                        <div class="tab-pane fade gif" id="a13" role="tabpanel" aria-labelledby="a13-list"><img class="gif" src="/assets/img/belfusion/hmp_videos/A_12321_SOMA.gif"></div>
                        <div class="tab-pane fade gif" id="a14" role="tabpanel" aria-labelledby="a14-list"><img class="gif" src="/assets/img/belfusion/hmp_videos/A_12391_SOMA.gif"></div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>


<!---------------------------- BIBLIOGRAPHY ---------------------------->

<div class="h-100 d-flex align-items-center justify-content-center" style="margin-top: 30px">
    <div class="col-8" id="bibtex" style="text-align: justify;">
        <h3 style="text-align: center;">BibTeX</h3>
        <div class="bibtex">
        {% highlight bibtex %}
TO BE UPDATED
{% endhighlight %}

        </div>
    </div>
</div>
