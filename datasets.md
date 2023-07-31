---
title: SLAM Datasets
subtitle: Multi-Robot, Multi-Degraded SLAM Datasets
layout: page
show_sidebar: false
hide_footer: false
menubar_toc: true
hero_height: is-large
hero_image: /img/datasets/dataset_video_short.gif
hero_link: /datasets#download
hero_link_text: Download
---

<link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/materialize/1.0.0/css/materialize.min.css">
<script src="https://cdnjs.cloudflare.com/ajax/libs/materialize/1.0.0/js/materialize.min.js"></script>
<script src="https://code.jquery.com/jquery-3.3.1.slim.js"
    integrity="sha256-fNXJFIlca05BIO2Y5zh1xrShK3ME+/lYZ0j+ChxX2DA=" crossorigin="anonymous"></script>
<script src="/datasets/jquery.csv.min.js"></script>
<style> html { scroll-behavior: smooth; }

td th {
text-align: center !important;
vertical-align: middle !important;
}

.tooltip {
position: relative;
display: inline-block;
}

.tooltip .tooltiptext {
opacity: 0%;
width: 120px;
background-color: black;
color: #fff;
text-align: center;
border-radius: 6px;
padding: 5px 0;

position: absolute;
z-index: 1;
top: 100%;
left: 50%;
margin-left: -60px;
}

.tooltip:hover .tooltiptext {
opacity: 40%;
}
</style>


# About

We present the sim to real datasets collected in <b>Tartan Air</b> and <b> SubT-MRS</b>. The datasets contains set of perceptually degraded environments such as darkness, airbone obscurats conditions such as fog, dust, smoke and lack of prominent perceptual features in self-similar areas.

## SubT-MRS Dataset 

<img src="/img/datasets/palette.png" style="display: block; margin-left: auto; margin-right: auto; width: 60%;" />

The SubT-MRS Dataset is an exceptional real-world collection of challenging datasets obtained from Subterranean Environments, encompassing caves, urban areas, and tunnels. Its primary focus lies in testing robust SLAM capabilities and is designed as Multi-Robot Datasets, featuring UGV, UAV, and Spot robots, each demonstrating various motions. The datasets are distinguished as Multi-Spectral, integrating Visual, Lidar, Thermal, and inertial measurements, effectively enabling exploration under demanding conditions such as darkness, smoke, dust, and geometrically degraded environments.Key features of our dataset:

<b> 1. Multiple Modalities: </b>
Our dataset includes hardware time-synchronized data from 4 RGB cameras, 1 LiDAR, 1 IMU, and 1 thermal camera, providing diverse and precise sensor inputs.

<b> 2.Diverse Scenarios: </b>
    Collected from multiple locations, the dataset exhibits varying environmental setups, encompassing indoors, outdoors, mixed indoor-outdoor, underground, off-road, and buildings, among others.

<b> 3.Multi-Degraded: </b>
   By incorporating multiple sensor modalities and challenging conditions like fog, snow, smoke, and illumination changes, the dataset introduces various levels of sensor degradation.

<b> 4. Heterogeneous Kinematic Profiles:</b>
  The SubT-MRS Dataset uniquely features time-synchronized sensor data from diverse vehicles, including RC cars, legged robots, drones, and handheld devices, each operating within distinct speed ranges. 


## Tartan Air Dataset 

 The [TartanAir dataset](http://theairlab.org/tartanair-dataset/) is collected in photo-realistic simulation environments based on the AirSim project. A special goal of this dataset is to focus on the challenging environments with changing light conditions, adverse weather, and dynamic objects. The four most important features of our dataset are:

   <b>  1. Large size diverse realistic data:</b>
     We collect the data in diverse environments with different styles, covering indoor/outdoor, different weather, different seasons, urban/rural.
    
   <b> 2. Multimodal ground truth labels:</b>
     We provide RGB stereo, depth, optical flow, and semantic segmentation images, which facilitates the training and evaluation of various visual SLAM methods. 

  <b>  3. Diversity of motion patterns:</b>
   Our dataset covers much more diverse motion combinations in 3D space, which is significantly more difficult than existing datasets.
   
   <b> 4. Challenging Scenes:</b>
    We include challenging scenes with difficult lighting conditions, day-night alternating, low illumination, weather effects (rain, snow, wind and fog) and seasonal changes.Please refer to the TartanAir Dataset and the paper for more information. 



## ICCV 2023 SLAM Challenge 

🚀 The Challenge is Live! 🚀
Join us for three exciting tracks of challenges from the links below.

<br>

<center>
<a href="/iccv23_challenge_VI" class="button is-info"> &nbsp; Visual Inertial Track </a >
&nbsp;
<a href="/iccv23_challenge_LiI" class="button is-info"> &nbsp; LiDAR Inertial Track </a >
&nbsp;
<a href="/iccv23_challenge_Mul" class="button is-info"> &nbsp; Multi Modal Fusion Track</a >
&nbsp;
</center>


<br>


🚀 Don't Forget: The Sensor Fusion Challenge is a Must!<br>
You can participate either  [Visual-inertial challenge](/iccv23_challenge_VI)+  [Sensor Fusion challenge](/iccv23_challenge_VI) or  
 [LiDAR-inertial challenge](/iccv23_challenge_VI)+  [Sensor Fusion challenge](/iccv23_challenge_VI) Or only participate in [Sensor Fusion challenge](/iccv23_challenge_VI).


Seize this chance to demonstrate your skills and compete among the finest in the field!

Three separate awards will be given for each track.
Your SLAM performance in <b>the Sensor Fusion track will not impact</b> the scores in other tracks.
Join us now to become a vital part of cutting-edge advancements in robotics and sensor fusion! 🤖💡 Let your expertise shine in this thrilling competition!

## Meet our robots!!
<img src="/img/iccv/offroad.png" style="width: 23%;" />
<img src="/img/iccv/spot.png" style="width: 23%;" />
<img src="/img/iccv/ugv.jpg" style="width: 23%;" />
<img src="/img/iccv/uav.png" style="width: 23%;" />

## Sensors 

<iframe width="100%" height="400" style="display: block; margin-left: auto; margin-right: auto; width: 50%;"  src="https://www.youtube.com/embed/G8KaflyapIE" title="Website - Sensor Video" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<img src="/img/datasets/specs.png" style="display: block; margin-left: auto; margin-right: auto; width: 50%;" />


## Download our datasets

Easily search for the datasets you require by inputting <b> "visual" or "lidar" or "subt" </b> to find precisely what you need. Our tool ensures you get the specific datasets you're looking for hassle-free. Try it now and access the data you require for your projects with ease! 📁🔍

<div id="chips" class="chips" onclick="openAutoComplete()">
<input class="custom-class">
</div>
<button style="" class="btn waves-effect waves-light" onclick="onFilterButton()">Filter<i class="material-icons right">filter_list</i></button>
<span id="numResultLabel" style="padding-left: 20px;"></span>
<table class="">
<thead>
    <tr>
        <th>Name</th>
        <th>Location</th>
        <th>Robot</th>
        <th>Sensors</th>
        <th>Description</th>
        <th>Degraded types</th>
        <th>Length</th>
        <th>Return to origin</th>
        <th>Size</th>
        <th>Picture</th>
    </tr>
</thead>

<tbody id="datasetTable"></tbody>
</table>
<br>


## Contact us

If you have any issues on the SLAM challenge, please post issues on this [github](https://github.com/sleepycan/SubT-MRS). 



<!-- # Contribute

We're delighted to receive your challenging datasets! Contributing to this dataset is simple:

1. Have your dataset ready.
2. Use <a href="/rosbagutils" style="color:#cc002b;">Rosbag Utils</a> to filter the topics you want to publish.
3. Rosbag Utils can also provide some statistics for your robot trajectory.
4. Contact Haoxiang Sun (<haoxians@andrew.cmu.edu>) for more information. -->

# Organizers

<hr>
 <table class="customFormat" style="width:100%border-collapse: collapse; border: none;">
  <tr>
    <td style="text-align: center;">
      <img class="circular_image" src="/img/team/shibozNew.png" style="margin-bottom: 6px;"/>
      <p style="margin-bottom: 3px;">
        <a style="margin-bottom: 1px;" href="https://theairlab.org/team/shiboz/">Shibo Zhao</a>
      </p>
      <p style="margin-bottom: 3px;">PhD Candidate </p>
      <p>Carnegie Mellon University</p>
    </td>
    <td style="text-align: center;">
      <img class="circular_image" src="/img/team/lucas_nogueira_crop.png" style="margin-bottom: 6px;"/>
      <p style="margin-bottom: 3px;">
        <a style="margin-bottom: 1px;" href="https://theairlab.org/team/lucas_nogueira/">Lucas Nogueira</a>
      </p>
      <p style="margin-bottom: 3px;">Master's Student</p>
      <p>Carnegie Mellon University</p>
    </td>
    <td style="text-align: center;">
      <img class="circular_image" src="/img/team/ian.jpg" style="margin-bottom: 6px;"/>
      <p style="margin-bottom: 3px;">
        <a style="margin-bottom: 1px;" href="https://theairlab.org/team/ian/">Ian Higgins</a>
      </p>
      <p style="margin-bottom: 3px;">Research Associate</p>
      <p>Carnegie Mellon University</p>
    </td>
    <td style="text-align: center;">
      <img class="circular_image" src="/img/team/haoxiangsun.jpg" style="margin-bottom: 6px;"/>
      <p style="margin-bottom: 3px;">
        <a style="margin-bottom: 1px;" href="https://seansun.org">Haoxiang Sun</a>
      </p>
      <p style="margin-bottom: 3px;">Undergradate Student</p>
      <p>Carnegie Mellon University</p>
    </td>
    <td style="text-align: center;">
      <img class="circular_image" src="/img/team/rushan_jiang.png" style="margin-bottom: 6px;"/>
      <p style="margin-bottom: 3px;">
        <a style="margin-bottom: 1px;" href="https://drive.google.com/file/d/1qWiMQoJsAF4oOikU0akjOOveBn-SUOLl/view">Rushan Jiang</a>
      </p>
      <p style="margin-bottom: 3px;">Undergradate Student</p>
      <p>Carnegie Mellon University</p>
    </td> <td style="text-align: center;">
      <img class="circular_image" src="/img/team/chuck-whittaker.jpg" style="margin-bottom: 6px;"/>
      <p style="margin-bottom: 3px;">
        <a style="margin-bottom: 1px;" href="https://www.ri.cmu.edu/ri-people/warren-whittaker/">Warren Whittaker</a>
      </p>
      <p style="margin-bottom: 3px;">Senior Field Robotics Specialist</p>
      <p>Carnegie Mellon University</p>
    </td>
    <td style="text-align: center;">
      <img class="circular_image" src="/img/iccv_organizers/iccv_members/daman.png" style="margin-bottom: 6px;"/>
      <p style="margin-bottom: 3px;">
        <a style="margin-bottom: 1px;" href="https://www.linkedin.com/in/damanpreet-singh-289a46163/">Damanpreet Singh</a>
      </p>
      <p style="margin-bottom: 3px;">Graduate Student</p>
      <p>Carnegie Mellon University</p>
     <tr>
  

<script>
let calibrations;
let datasetsStr, datasets;
let datasetTable;
let chipsInput;
let options = {
    placeholder: "Filter datasets...",
    secondaryPlaceholder: "+Tag",
    autocompleteOptions: {
        data: {
            Lidar: null,
            IMU: null,
            Thermal: null,
            Subt: null,
            UAV: null,
            UGV: null,
        },
        limit: Infinity,
        minLength: 0,
    },
};

document.addEventListener("DOMContentLoaded", function () {
    let elems = document.querySelectorAll(".chips");
    M.Chips.init(elems, options);
    chipsInput = M.Chips.getInstance(elems[0]);
});

datasetTable = document.getElementById("datasetTable");
loadCalibrationCsv(() => { loadDatasetCsv(); });

function openAutoComplete() {
    setTimeout(function () {
        if (!chipsInput.autocomplete.isOpen) {
            console.log("openAutoComplete");
            chipsInput.autocomplete.open();
        }
    }, 200);
}

function onFilterButton() {
    let startTime = new Date().getTime();
    let filter = chipsInput.chipsData.map((chip) => chip.tag.toLowerCase());
    filterTable(filter);
    console.log("Filter time used: " + (new Date().getTime() - startTime) + "ms");
}

function loadCalibrationCsv(callback) {
    makeRequest("/datasets/calibrations.csv", "", (str) => {
        let rows = $.csv.toArrays(str);
        calibrations = {};
        for (let i = 0; i < rows.length; i++) {
           calibrations[rows[i][0]] = rows[i][1];
        }
        if (callback) callback();
    });
}

function loadDatasetCsv(callback) {
    makeRequest("/datasets/datasets.csv", "", (str) => {
        datasetsStr = str.split("\n");
        for (let i = 0; i < datasetsStr.length; i++) {
            datasetsStr[i] = datasetsStr[i].toLowerCase();
        }
        let rows = $.csv.toArrays(str);
        datasets = [];
        for (let i = 0; i < rows.length; i++) {
            let dataset = {};
            dataset.id = rows[i][0].trim();
            dataset.name = rows[i][1].trim();
            dataset.location = rows[i][2].trim();
            dataset.description = rows[i][3].trim();
            dataset.robot = rows[i][4].trim();
            dataset.sensors = rows[i][5].trim();
            dataset.degraded = rows[i][6].trim();
            dataset.trajectoryLength = rows[i][7].trim();
            dataset.duration = rows[i][8].trim();
            dataset.returnToOrigin = rows[i][9].trim();
            dataset.size = rows[i][10].trim();
            dataset.image =
                rows[i][11].trim() !== "" ? rows[i][11].trim() : `/datasets/img/${dataset.id}.png`;
            dataset.link = rows[i][12].trim();
            datasets.push(dataset);
        }

        datasetTable.innerHTML = "";
        for (let i = 1; i < datasets.length; i++) {
            let row = datasets[i];
            generateRow(datasetTable, i, [
                makeDownloadLink(row.name, row.link),
                row.location,
                makeRobotIDs(row.robot),
                row.sensors,
                row.description,
                row.degraded,
                makeLengthDuration(row.trajectoryLength, row.duration),
                row.returnToOrigin,
                row.size,
                makePicture(i),
            ]);
        }
        filterTable();
        if (callback) callback();
    });
}

function filterTable(filters) {
    if (filters === undefined) filters = [];
    let count = 0;
    for (let i = 1; i < datasets.length; i++) {
        let isIncluded = true;
        for (let j = 0; j < filters.length; j++) {
            if (datasetsStr[i].indexOf(filters[j]) < 0) {
                isIncluded = false;
                break;
            }
        }
        if (isIncluded) {
            document.getElementById(`row-${i}`).style.display = "";
            count++;
        } else {
            document.getElementById(`row-${i}`).style.display = "none";
        }
    }
    document.getElementById("numResultLabel").innerHTML = `(Showing ${count} datasets)`;
}

function generateRow(table, rowIdx, dataArr) {
    let row = document.createElement("tr");
    row.id = "row-" + rowIdx;
    for (let i = 0; i < dataArr.length; i++) {
        let cell = document.createElement("td");
        if (typeof dataArr[i] === "string") {
            cell.innerHTML = dataArr[i];
        } else {
            cell.appendChild(dataArr[i]);
        }
        row.appendChild(cell);
    }
    return table.appendChild(row);
}

function makeLengthDuration(length, duration) {
    return `${length} <br> (${duration})`;
}

function makePicture(idx) {
    let img = document.createElement("img");
    img.id = `picture-${idx}`;
    img.idx = idx;
    img.src = datasets[idx].image;
    img.alt = "Loading...";
    img.style.width = "178px";
    img.style.height = "100px";
    img.style.objectFit = "scale-down";
    return img;
}

function makeRobotIDs(allIds) {
    let ids = allIds.split(",");
    let result = "";
    for (let i = 0; i < ids.length; i++) {
        let id = ids[i].trim();
        if (id === "") continue;
        result += makeCalibrationLink(id);
        if (i < ids.length - 1) result += ", ";
    }
    return result;
}

function makeCalibrationLink(name) {
    if (calibrations[name] === undefined) alert("Calibration not found: " + name);
    let link = calibrations[name];
    if (link.indexOf("https://") < 0 && link.indexOf("http://") < 0) link = "https://" + link;
    let result = `<a class="tooltip" onclick="window.open('${link}','_blank')">${name}`;
    result += `<span class="tooltiptext">Download ${name} calibration</span>`;
    result += `</a>`;
    return result;
}

function makeDownloadLink(name, link) {
    if (link.indexOf("https://") < 0 && link.indexOf("http://") < 0) link = "https://" + link;
    let result = `<a class="tooltip" onclick="window.open('${link}','_blank')">${name}`;
    result += `<span class="tooltiptext">Download dataset</span>`;
    result += `</a>`;
    return result;
}

function makeDownloadButton(link) {
    if (link.indexOf("https://") < 0 && link.indexOf("http://") < 0) link = "https://" + link;
    return `<a class="waves-effect waves-light btn-small" onclick="window.open('${link}','_blank')">Download</a>`;
}

function makeRequest(url, data, callback) {
    let httpRequest = new XMLHttpRequest();
    if (!httpRequest) return false;

    function receivedResponse() {
        if (httpRequest.readyState === XMLHttpRequest.DONE) {
            if (httpRequest.status === 200) {
                console.log("RECEIVED RESPONSE: " + httpRequest.responseText);
                callback(httpRequest.responseText);
            } else {
                console.log("ERROR: Request failed");
                alert("Unable to load datasets.");
            }
        }
    }

    httpRequest.timeout = 0;
    httpRequest.onreadystatechange = receivedResponse;
    console.log("SENDING REQUEST: " + url);
    httpRequest.open("GET", url, true);
    httpRequest.setRequestHeader("Content-Type", "application/x-www-form-urlencoded");
    httpRequest.send(data);
}
</script>
