---
title: SuperLoc
subtitle: The Key to Robust LiDAR-Inertial Localization Lies in Predicting Alignment Risks
layout: page
show_sidebar: false
hide_footer: false
hero_height: is-large
hero_image: img/superloc/superloc_title.gif
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
        .bonus-video h4 {
            text-align: center;
            margin-top: 10px;
            font-size: 1em;
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
            border-radius: 5px;
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
        body, html {
            background-color: white;
        }
        .hero.is-light {
            background-color: white;
        }
        .carousel-container {
            position: relative;
            width: 100%;
            max-width: 800px;
            margin: 0 auto;
            overflow: hidden;
        }
        .carousel {
            display: flex;
            transition: transform 0.5s ease-in-out;
        }
        .item {
            flex: 0 0 100%;
        }
        .item video {
            width: 100%;
            height: auto;
            max-height: 600px;
            object-fit: contain;
        }
        .item img {
            width: 100%;
            height: auto;
            max-height: 600px;
            object-fit: contain;
        }
        .nav-button {
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            background-color: rgba(0, 0, 0, 0.5);
            color: white;
            border: none;
            padding: 10px 15px;
            cursor: pointer;
            z-index: 10;
        }
        .nav-button.prev {
            left: 10px;
        }
        .nav-button.next {
            right: 10px;
        }
        .item-description {
            text-align: center;
            margin-top: 1rem;
            padding: 0 1rem;
            font-size: 1.6rem;
            color: #333;
        }
        .columns {
            display: flex;
            flex-wrap: wrap;
            margin: -0.75rem;
        }
        .column {
            flex: 1 1 45%;
            padding: 0.75rem;
        }
        @media screen and (max-width: 768px) {
            .column {
                flex: 1 1 100%;
            }
        }
        .comparison-video {
            width: 100%;
            height: auto;
            max-height: 450px;
            object-fit: contain;
        }
        .drag-bar {
            position: relative;
            width: 100%;
            height: 120px;
            background-color: #f0f0f0;
            margin-top: 20px;
            border-radius: 30px;
            overflow: hidden;
        }
        .preview-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 100%;
            padding: 0 30px;
        }
        .preview-image {
            width: 200px;
            height: 200px;
            object-fit: contain;
            border-radius: 5px;
            cursor: pointer;
            transition: transform 0.3s ease;
        }
        .preview-image:hover, .preview-image.active {
            transform: scale(1.1);
        }
        .drag-handle {
            position: absolute;
            top: 0;
            left: 0;
            width: 33.33%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.2);
            border-radius: 30px;
            cursor: grab;
            transition: left 0.3s ease;
        }
        .drag-handle:active {
            cursor: grabbing;
        }
        .preview-wrapper {
        width: 33.33%;
        height: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
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
        <a href="https://github.com/adrienzhh/Robustness_Metric" class="button is-info"> &nbsp;<i class="fab fa-github" style="font-size:24px"></i>Robustness Metrics</a >
        &nbsp;
        </center>
    </div>
</body>
<style>
.small-logo {
  width: 16px;
  height: auto;
}
</style>
</html>
<body>

<section class="hero is-light is-small">
    <div class="hero-body">
        <div class="container">
            <div class="carousel-container">
                <div id="results-carousel" class="carousel">
                    <div class="item">
                        <video muted loop playsinline controls>
                            <source src="video/superloc/website_intro3.mp4" type="video/mp4">
                            Your browser does not support the video tag.
                        </video>
                        <p class="item-description">Predict Alignment Risks✅</p>
                    </div>
                    <div class="item">
                        <video muted loop playsinline controls>
                            <source src="video/superloc/website_intro1.mp4" type="video/mp4">
                            Your browser does not support the video tag.
                        </video>
                        <p class="item-description">Real World Degraded Environment❓</p>
                    </div>
                    <div class="item">
                        <video muted loop playsinline controls>
                            <source src="video/superloc/website_intro2.mp4" type="video/mp4">
                            Your browser does not support the video tag.
                        </video>
                        <p class="item-description">ICP Failure under Degeneracy❓</p>
                    </div>
                </div>
            </div>
            <div class="drag-bar">
                <div class="preview-container">
                    <div class="preview-wrapper">
                        <img src="img/superloc/preview3.png" alt="Preview 1" class="preview-image active" data-index="0">
                    </div>
                    <div class="preview-wrapper">
                        <img src="img/superloc/preview1.png" alt="Preview 2" class="preview-image" data-index="1">
                    </div>
                    <div class="preview-wrapper">
                        <img src="img/superloc/preview2.png" alt="Preview 3" class="preview-image" data-index="2">
                    </div>
                </div>
                <div class="drag-handle"></div>
            </div>
        </div>
    </div>
</section>

<script>
document.addEventListener('DOMContentLoaded', function() {
    const carousel = document.querySelector('#results-carousel');
    const dragBar = document.querySelector('.drag-bar');
    const dragHandle = document.querySelector('.drag-handle');
    const previewImages = document.querySelectorAll('.preview-image');
    const items = carousel.querySelectorAll('.item');
    const videos = carousel.querySelectorAll('video');
    let isDragging = false;
    let startX, startLeft;

    function showItem(index) {
        carousel.style.transform = `translateX(-${index * 100}%)`;
        videos.forEach(video => {
            video.pause();
            video.currentTime = 0;
        });
        videos[index].play().catch(e => console.error("Error playing video:", e));
        previewImages.forEach((img, i) => {
            img.classList.toggle('active', i === index);
        });
        dragHandle.style.left = `${index * 33.33}%`;
    }

    dragHandle.addEventListener('mousedown', (e) => {
        isDragging = true;
        startX = e.clientX - dragHandle.offsetLeft;
        startLeft = dragHandle.offsetLeft;
    });

    document.addEventListener('mousemove', (e) => {
        if (!isDragging) return;
        e.preventDefault();
        let newLeft = e.clientX - startX;
        newLeft = Math.max(0, Math.min(newLeft, dragBar.offsetWidth - dragHandle.offsetWidth));
        dragHandle.style.left = `${newLeft}px`;
        
        const progress = newLeft / (dragBar.offsetWidth - dragHandle.offsetWidth);
        const index = Math.round(progress * (items.length - 1));
        showItem(index);
    });

    document.addEventListener('mouseup', () => {
        isDragging = false;
    });

    previewImages.forEach((img, index) => {
        img.addEventListener('click', () => {
            showItem(index);
        });
    });

    // Initialize
    showItem(0);
});
</script>
</body>

<h1 class="centered-title">Overview Video</h1>
<div>
<br>
    <iframe width="100%" height="400" style="display: block; margin-left: auto; margin-right: auto; width: 50%;"  src="https://www.youtube.com/embed/HqoDL2xiaZA" title="Website - Sensor Video" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
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


<h1>Cave</h1>
<div class="about-section">
</div>
<div class="bonus-videos">
    <div class="bonus-video">
        <video class="lazy-video" data-src="./video/superloc/cave_website1.mp4" muted loop playsinline controls>
        </video>
    </div>
    <div class="bonus-video">
        <video class="lazy-video" data-src="./video/superloc/cave_comparsion_website.mp4" muted loop playsinline controls>
        </video>
    </div>
</div>

<h1>Multi-floor</h1>
<div class="about-section">
</div>
<div class="bonus-videos">
    <div class="bonus-video">
        <video class="lazy-video" data-src="./video/superloc/multi_floor_website1.mp4" muted loop playsinline controls>
        </video>
    </div>
    <div class="bonus-video">
        <video class="lazy-video" data-src="./video/superloc/multi_floor_comparsion_wesbite.mp4" muted loop playsinline controls>
        </video>
    </div>
</div>


<h1>Long Corridor</h1>
<div class="about-section">
</div>
<div class="bonus-videos">
    <div class="bonus-video">
        <video class="lazy-video" data-src="./video/superloc/long_corridor_website1.mp4" muted loop playsinline controls>
        </video>
    </div>
    <div class="bonus-video">
        <video class="lazy-video" data-src="./video/superloc/long_corridor_comparsion_website.mp4" muted loop playsinline controls>
        </video>
    </div>
</div>

<h1 class="centered-title">Comparison with other methods</h1>
<div class="about-section">
</div>
<div class="carousel-container">
    <div id="comparison-carousel" class="carousel">
        <div class="item">
            <video class="comparison-video" muted loop playsinline controls>
                <source src="./video/superloc/cave_failure_website.mp4" type="video/mp4">
                Your browser does not support the video tag.
            </video>
            <p class="item-description">Cave</p>
        </div>
        <div class="item">
            <video class="comparison-video" muted loop playsinline controls>
                <source src="./video/superloc/multi_floor_failure_website.mp4" type="video/mp4">
                Your browser does not support the video tag.
            </video>
            <p class="item-description">Multi-Floor</p>
        </div>
        <div class="item">
            <video class="comparison-video" muted loop playsinline controls>
                <source src="./video/superloc/long_corridor_failure_website.mp4" type="video/mp4">
                Your browser does not support the video tag.
            </video>
            <p class="item-description">Long Corridor</p>
        </div>
    </div>
    <button class="nav-button prev" id="comparison-prev">&#10094;</button>
    <button class="nav-button next" id="comparison-next">&#10095;</button>
</div>

<script>
document.addEventListener('DOMContentLoaded', function() {
    const carousel = document.querySelector('#comparison-carousel');
    const items = carousel.querySelectorAll('.item');
    const prevButton = document.querySelector('#comparison-prev');
    const nextButton = document.querySelector('#comparison-next');
    const videos = carousel.querySelectorAll('video');
    let currentIndex = 0;

    function showItem(index) {
        carousel.style.transform = `translateX(-${index * 100}%)`;
        videos.forEach(video => {
            video.pause();
        });
        videos[index].play().catch(e => console.error("Error playing video:", e));
    }

    prevButton.addEventListener('click', () => {
        currentIndex = (currentIndex - 1 + items.length) % items.length;
        showItem(currentIndex);
    });

    nextButton.addEventListener('click', () => {
        currentIndex = (currentIndex + 1) % items.length;
        showItem(currentIndex);
    });

    videos.forEach(video => {
        video.addEventListener('click', () => {
            if (video.paused) {
                video.play();
            } else {
                video.pause();
            }
        });
    });

    showItem(currentIndex);
});
</script>

<br>

<h4>To benefit the open community, our localization package also includes following features,</h4>
<div class="about-section">
</div>
<div class="bonus-videos">
    <div class="bonus-video">
        <h3>Robust Initialization</h3>
        <video class="lazy-video" data-src="./video/superloc/cic_robust_initialization_10.mp4" muted loop playsinline controls>
        </video>
    </div>
    <div class="bonus-video">
        <h3>Transition between mapped and unmapped region</h3>
        <video class="lazy-video" data-src="./video/superloc/cic_mapped_unmapped_4.mp4" muted loop playsinline controls>
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

## Ground Truth Map 
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ground Truth Maps</title>
    <style>
        .map-container {
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
        }
        .map-item {
            width: 48%;
            min-width: 300px;
            margin-bottom: 20px;
        }
        h3 {
            text-align: center;
        }
        @media (max-width: 768px) {
            .map-item {
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <h4>To benefit the open community, we release the following ground truth maps for localization:</h4>
    <div class="map-container">
        <div class="map-item">
            <h3><a href="https://hawkins-gt-map.s3.us-east-2.amazonaws.com/hawkins.html" target="_blank">Hawkins</a></h3>
            <iframe src="https://hawkins-gt-map.s3.us-east-2.amazonaws.com/hawkins.html" width="100%" height="600"></iframe>
        </div>
        <div class="map-item">
            <h3><a href="https://laurel-craven-gt-map.s3.us-east-2.amazonaws.com/laurel_craven.html" target="_blank">Laurel Craven</a></h3>
            <iframe src="https://laurel-craven-gt-map.s3.us-east-2.amazonaws.com/laurel_craven.html" width="100%" height="600"></iframe>
        </div>
    </div>
</body>


## Dataset

All datasets from our paper is released as follow, 

| Name | Source    | Location  | Robot     |Sensor     | Trajectory | Duration  |  Rosbag | Calibration (Extrinsics) | Calibration (Intrinsics) | GT Map | GT Traj. |
|------|-----------|-----------|-----------|-----------|-------------|-----------|-------------|-----------|---------------|--------------|--------------|
|Cave01    |SuperLoc|Laurel Craven|Handheld|RGB,LiDAR,IMU|416|838|[link](https://drive.google.com/file/d/1cyHbmxmJQGuK5UCm_f7SXomr8Gd6GEww/view?usp=sharing)| [Google](https://drive.google.com/file/d/1TzIvJuJ3ulYSOdrXRy9wRm1E2Y5AE7g1/view?usp=sharing) Baidu | [Google](https://drive.google.com/file/d/1XfWfpjMqfPHUO8JNy1u9Ysky6vvTpn8_/view?usp=sharing) Baidu | [link](https://drive.google.com/file/d/1JYSVgunLJj6Fj-MsDoNIDHRDx51YWsQP/view?usp=sharing) | [link](https://drive.google.com/file/d/17JiwUXJ6xZMkL7GSNQg_kV-ZJfKczxak/view?usp=sharing)
|Cave02    |SuperLoc|Laurel Craven|Handheld|RGB,LiDAR,IMU|475|986|[link](https://drive.google.com/file/d/1HwUYboHbCh4_GfyvZYQn25KmA12yiuMR/view?usp=sharing)| [Google](https://drive.google.com/file/d/1TzIvJuJ3ulYSOdrXRy9wRm1E2Y5AE7g1/view?usp=sharing) Baidu | [Google](https://drive.google.com/file/d/1XfWfpjMqfPHUO8JNy1u9Ysky6vvTpn8_/view?usp=sharing) Baidu | [link](https://drive.google.com/file/d/1JYSVgunLJj6Fj-MsDoNIDHRDx51YWsQP/view?usp=sharing) | [link](https://drive.google.com/file/d/1_7D70MVcUbaJqlzN_xlDkguF1qiyZCqF/view?usp=sharing)
|Cave03    |SubT-MRS|Laurel Craven|Handheld|RGB,LiDAR,IMU|490|768|[link](https://drive.google.com/file/d/1cO5fStkj1oKpQojfrF8sji-Pbu8LqxPF/view?usp=drive_link)| [Google](https://drive.google.com/file/d/1TzIvJuJ3ulYSOdrXRy9wRm1E2Y5AE7g1/view?usp=sharing) Baidu | [Google](https://drive.google.com/file/d/1XfWfpjMqfPHUO8JNy1u9Ysky6vvTpn8_/view?usp=sharing) Baidu | [link](https://drive.google.com/file/d/1JYSVgunLJj6Fj-MsDoNIDHRDx51YWsQP/view?usp=sharing) | [link](https://drive.google.com/file/d/1Rgm5JC4Nq2mm8s6tafY5w-LvxLrt1oPG/view?usp=sharing)
|Cave04    |SuperLoc|Laurel Craven|Handheld|RGB,LiDAR,IMU|597|959|[link](https://drive.google.com/file/d/19DXx6mspWBXiEqqZOa34b2bHz7cc1jTN/view?usp=sharing)| [Google](https://drive.google.com/file/d/1TzIvJuJ3ulYSOdrXRy9wRm1E2Y5AE7g1/view?usp=sharing) Baidu | [Google](https://drive.google.com/file/d/1XfWfpjMqfPHUO8JNy1u9Ysky6vvTpn8_/view?usp=sharing) Baidu | [link](https://drive.google.com/file/d/1JYSVgunLJj6Fj-MsDoNIDHRDx51YWsQP/view?usp=sharing) | [link](https://drive.google.com/file/d/11EnNKVYfHJV3P9i0MUrbV4tYqC5z-PSM/view?usp=sharing)
|Corridor01  |SubT-MRS|Hawkins|RC2     |RGB,LiDAR IMU|617|279|[link](https://drive.google.com/file/d/1aIIqPiE10nX3IhidpxKhc4Psq-AMER1X/view?usp=drive_link)| [Google](https://drive.google.com/file/d/13WmYOrqbT6VNkIGL13cRuLiENeanI6oY/view?usp=sharing) Baidu | [Google](https://drive.google.com/file/d/1guy4Sa1jdfOdxmqBIGFiXX-X2qvXQLGa/view?usp=sharing) Baidu |[link](https://drive.google.com/file/d/1EH4NzINNLkHrneIxstrzkY9XTZ1JP5bf/view?usp=sharing) | [link](https://drive.google.com/file/d/1QbQamSktPAzJkf0GduAPTqQlxuxM0DBK/view?usp=sharing)
|Corridor02  |SuperLoc|Hawkins|RC1     |RGB,LiDAR IMU|690|893|[link](https://drive.google.com/file/d/1fbQIjza6zCVZ719VvXfNhAONDZflqGnf/view?usp=sharing)| [Google](https://drive.google.com/file/d/1FzepVzxan_9GjS0Rg_3f1LIjjwm2VZrR/view?usp=sharing) Baidu | [Google](https://drive.google.com/file/d/1gCjmOVcwhm55Rwosel79FMxG_WzvnV8g/view?usp=sharing) Baidu | [link](https://drive.google.com/file/d/1d5vv4kfrTyntZw-82fGeTyih3H7DWxg5/view?usp=sharing) | [link](https://drive.google.com/file/d/1hb3IVu1OqyPZA61kBZG1raGTBcTv_h3H/view?usp=sharing)
|Floor01    |SubT-MRS|Hawkins|SP1|RGB,LiDAR,IMU|270|480|[link](https://drive.google.com/file/d/13QQ8a-dEy56aHg8D0RNW0bfywWz6LKn9/view?usp=drive_link)| [Google](https://drive.google.com/file/d/1FAtf5IkUzNNrwxyqVAV6Vre5Pmvbp8Mj/view?usp=sharing) Baidu | [Google](https://drive.google.com/file/d/1uH4wFmLeQNrIGlsUsO--PQuyEIOSOGvR/view?usp=drive_link) Baidu | [link](https://drive.google.com/file/d/1F46g0wnJVSedTJubFD_Ne1IwgZAGYvsU/view?usp=sharing) | [link](https://drive.google.com/file/d/1T-p9TgDwD_9us7U94cT0guwPNTvx3KkI/view?usp=sharing)
|Floor02 (bonus)    |SuperLoc|Hawkins|SP1|RGB,LiDAR,IMU|410|2190|[link](https://drive.google.com/file/d/1RnlqpHVG1I-BD0T7pxNkKELAGy_Vp0oI/view?usp=sharing)| [Google](https://drive.google.com/file/d/1FAtf5IkUzNNrwxyqVAV6Vre5Pmvbp8Mj/view?usp=sharing) Baidu | [Google](https://drive.google.com/file/d/1uH4wFmLeQNrIGlsUsO--PQuyEIOSOGvR/view?usp=drive_link) Baidu | [link](https://drive.google.com/file/d/1F46g0wnJVSedTJubFD_Ne1IwgZAGYvsU/view?usp=sharing) | link

<b>Ground truth trajecotry</b> follows [TUM](https://github.com/MichaelGrupp/evo/wiki/Formats) format, 
<pre><code>timestamp x y z q_x q_y q_z q_w</code></pre>

## Acknowledgments

The authors would like to express sincere thanks to [Guofei Chen](https://gfchen01.cc/) for helping us collect the dataset. The authors would like to thank Professor [Ji Zhang](https://frc.ri.cmu.edu/~zhangji/) for letting us borrow the Diablo platform and offering constructive advice.

## Citation

coming soon

## Contacts

If you have any question or want to contribute this work, please feel free to send email to Shibo Zhao (shiboz@andrew.cmu.edu).  Thank you! :)