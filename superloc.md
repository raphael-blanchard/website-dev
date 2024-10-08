---
title: SuperLoc
subtitle: The Key to Robust LiDAR-Inertial Localization Lies in Predicting Alignment Risks
layout: page
show_sidebar: false
hide_footer: false
hero_height: is-large
hero_image: img/tptio/tp-tio.gif
---

<script>

    window.onload = function () {
        let p = document.getElementsByClassName("title is-2")[0].parentElement;
        p.style.background = "rgba(10, 10, 10, 0.5)";
        p.style.borderRadius = "20px";
        p.style.padding = "20px";
        p.style.width = "fit-content";
        p.style.margin = "0px";
    }

    let p = document.getElementsByClassName("title is-2")[0].parentElement;
    p.style.background = "rgba(10, 10, 10, 0.5)";
    p.style.borderRadius = "20px";
    p.style.padding = "20px";
    p.style.width = "fit-content";
    p.style.margin = "0px";
</script>

<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SuperLoc</title>
    <style>
        .centered-content {
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
        }
        .links {
            display: flex;
            justify-content: center;
            gap: 10px;
        }
        .figure-container {
            display: flex;
            justify-content: center;
            width: 100%;
            margin: 20px 0;
        }
        .figure-container img {
            width: 100%;
            height: auto;
            max-width: 800px; /* Adjust this value to make the GIF smaller or larger */
        }
        .video-container {
            width: 100%;
            max-width: 800px; /* Adjust this value to make the video smaller */
            margin: 0 auto;
        }
        .video-container video {
            width: 100%;
            height: auto;
        }
        .centered-title {
            text-align: center;
            width: 100%;
        }
        .bonus-videos {
            display: flex;
            justify-content: space-between;
            max-width: 1200px;
            margin: 20px auto;
        }
        .bonus-video {
            width: 48%;
        }
        .bonus-video h3 {
            text-align: center;
            margin-top: 10px;
            font-size: 1.17em;
        }
        .bonus-video video {
            width: 100%;
            height: auto;
            display: block;
        }
        .figure-container img {
            width: 90%;
            max-width: 1000px; 
            height: auto;
        }
        .figure-description {
            margin-top: 20px;
            text-align: justify;
            font-style: italic;
            color: #555;
            max-width: 90%;
            margin-left: auto;
            margin-right: auto;
        }
    </style>
</head>
<body>
    <div class="centered-content">
        <h1>SuperLoc: The Key to Robust LiDAR-Inertial Localization Lies in Predicting Alignment Risks</h1>
        <p class="authors">
            Shibo Zhao*, Honghao Zhu*, Yuanjun Gao, Beomsoo Kim, Yuheng Qiu, Aaron M. Johnson, Sebastian Scherer
        </p>
        <p class="affiliation">
            *Equal contribution<br>
            Carnegie Mellon University
        </p>
        <center>
        <a href="#" class="button is-info"> &nbsp;📄Paper</a >
        &nbsp;
        <a href="#" class="button is-info"> &nbsp;<img src="/img/logos/arxiv.png" class="small-logo">arXiv</a >
        &nbsp;
        <a href="#" class="button is-info"> &nbsp;<i class="fab fa-github" style="font-size:24px"></i>Code</a >
        &nbsp;
        </center>
    </div>
    <div class="figure-container">
        <img src="img/superloc/superloc_title.gif" alt="SuperLoc demonstration">
    </div>
</body>
<style>
.small-logo {
  width: 16px;
  height: auto;
}
</style>
</html>

<h1 class="centered-title">Overview Video</h1>
<div>
<br>
    <iframe width="100%" height="400" style="display: block; margin-left: auto; margin-right: auto; width: 50%;"  src="https://www.youtube.com/embed/G05INI0eIug" title="Website - Sensor Video" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

 <h1 class="centered-title">About SuperLoc</h1>
<div class="about-section">
    <p>Map-based LiDAR localization, while widely used in autonomous systems, faces significant challenges in degraded environments due to lacking distinct geometric features. This paper introduces SuperLoc, a robust LiDAR localization package that addresses key limitations in existing methods. SuperLoc features a novel predictive alignment risk assessment technique, enabling early detection and mitigation of potential failures before optimization. This approach significantly improves performance in challenging scenarios such as corridors, tunnels, and caves. Unlike existing degeneracy mitigation algorithms that rely on post-optimization analysis and heuristic thresholds, SuperLoc evaluates the localizability of raw sensor measurements. Experimental results demonstrate significant performance improvements over state-of-the-art methods across various degraded environments. Our approach achieves a 49.7% increase in accuracy and exhibits the highest robustness. To facilitate further research, we will release our implementation along with datasets from eight challenging scenarios.</p>
    <div class="figure-container">
        <img src="/img/superloc/first_figure_compress.png" alt="SuperLoc Figure" />
    </div>
    <p class="figure-description">
    SuperLoc is to our knowledge the first open-source LiDAR-inertial localization system that not only predicts alignment
    risks, and estimates the observability of scan, but also can actively incorporate pose priors from other odometry sources
    before failure occurs. The entire process doesn't require predefined heuristic thresholds to detect degeneration and it has
    been evaluated in various challenging environments including caves, long corridors, flat open areas, and staircases.
    </p>
</div>

<h1>Bonus</h1>
<div class="about-section">
    <p>To benefit the open community, our localization package also includes following features:</p>
</div>
<div class="bonus-videos">
    <div class="bonus-video">
        <h3>Robust Initialization</h3>
        <video class="lazy-video" data-src="/video/superloc/cic_robust_initialization_10.mp4" muted loop playsinline controls>
        </video>
    </div>
    <div class="bonus-video">
        <h3>Transition between mapped and unmapped region</h3>
        <video class="lazy-video" data-src="/video/superloc/cic_mapped_unmapped_4.mp4" muted loop playsinline controls>
        </video>
    </div>
</div>

<script>
document.addEventListener("DOMContentLoaded", function() {
    var lazyVideos = [].slice.call(document.querySelectorAll("video.lazy-video"));

    if ("IntersectionObserver" in window) {
        var lazyVideoObserver = new IntersectionObserver(function(entries, observer) {
            entries.forEach(function(video) {
                if (video.isIntersecting) {
                    video.target.src = video.target.dataset.src;
                    video.target.load();
                    video.target.play(); // Auto-play when in view
                    video.target.classList.remove("lazy-video");
                    lazyVideoObserver.unobserve(video.target);
                }
            });
        });

        lazyVideos.forEach(function(lazyVideo) {
            lazyVideoObserver.observe(lazyVideo);
        });
    }
});
</script>



## Citation

## Acknowledgments
[KTIO](https://onlinelibrary.wiley.com/doi/abs/10.1002/rob.21932) Keyframe‐based thermal–inertial odometry Journal of Field Robotics 37.4 (2020): 552-579.

[VINS-MONO](https://ieeexplore.ieee.org/document/8421746?arnumber=8421746&source=authoralert) A Robust and Versatile Monocular Visual-Inertial State Estimator, Tong Qin, Peiliang Li, Zhenfei Yang, Shaojie Shen, IEEE Transactions on Robotic 

[GTSAM](https://github.com/borglab/gtsam) Georgia Tech Smoothing and Mapping Library

## Contacts

If you have any question or want to contribute this work, please feel free to send email to Shibo Zhao (shiboz@andrew.cmu.edu).  Thank you! :)