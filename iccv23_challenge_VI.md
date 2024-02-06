---
title: ‎ 
subtitle: ‎ 
layout: page
show_sidebar: false
menubar_toc: true
hide_footer: true
hero_height: is-medium
hero_image: /img/iccv/VI.gif
---

# 🎉 Welcome to ICCV'23 Visual-Inertial SLAM Challenge! 🎉

In the visual-inertial track, we exclusively offer access to high-quality **visual-inertial** datasets sourced from SubT-MRS and TartanAir. These datasets encompass various challenging conditions such as **"lighting changes, darkness, smoke, self-similar environments and more"** providing a test from **simulation to real-world**. For the other two tracks, see here: [Lidar-Inertial SLAM Challenge](https://superodometry.com/iccv23_challenge_LiI) and [Sensor Fusion SLAM Challenge](https://superodometry.com/iccv23_challenge_Mul).

Seize this chance to demonstrate your skills and compete among the finest in the field!

Three separate awards will be given for each track.
Join us now to become a vital part of cutting-edge advancements in robotics and sensor fusion! 🤖💡 Let your expertise shine in this thrilling competition!

<span style="font-size:1.3em;"><font color="red"> <b> Important Latest Updates:</b> </font></span>
<br>
<br>
Hello everyone!
<br>
<br>
Thanks for participating the SLAM challenge!
<br>
<br>
As the competition deadline approaches, many teams asked for an extension. To ensure fairness, we've extended **the deadline to 11:59 PM EDT, October 15th, 2023**. It is important to note that each team **must provide answers to all questions in the report template**. A high-quality report will also be **factored into your final score** and assessed as a reference for the submitted trajectory.
<br>
<br>
Starting from September 25th, each team is limited to a maximum of 30 submissions. Please be aware that exceeding this limit will result in the **30th submission being considered as the final one**.
<br>
<br>
Additionally, registering multiple accounts is strictly prohibited now. Feel free to let us know if you have more questions.
<br>
<br>
We wish you the best of luck in the challenge! ^^
<br>
<br>
<span style="font-size:1.3em;"><font color="red"> <b> Previous Updates:</b> </font></span>

1. To facilitate better algorithm debugging for everyone recently, we allow multiple daily submissions until 20 Sept. Starting from 21 Sept, only one submission per day is allowed.

2. We've observed an issue with the extrinsics of three trajectories, i.e., Endofworld, Moon, and Westerndesert. Please download the extrinsics calibration file again. We are very sorry for any inconvenience caused.


<span style="font-size:1.3em;">If you have any question, please do not hesitate to post issues on this [github website](https://github.com/water-horse/ICCV2023_SLAM_Challenge.git). We would love to hear from your feedback! Every post will be responded with no spared effort within 36 hours.<span>

<font color="red"> <b> Please note challenge deadline updated: 15th October 2023 11:59 PM EDT. </b> </font> 
<br>
Time remaining:
<p1 id="demo"></p1>

File structure: 

```
rosbag
├── TartanAir_visual_{places ...}_noise0.bag
└── SubT_MRS_{trajectory names ...}_{robot types ...}.zip
    └── (zipped) raw_data_{...}yyyy-mm-dd-hh-mm-ss{...}.bag

folder
├── TartanAir_visual_{places ...}.zip
│   ├── (zipped) imu
│   │   └── [acc/gyro/imu/imu_time].[npy/txt]
│   └── (zipped) image_lcam_front
│       ├── {...}_lcam_front.png
│       └── timestamps.txt
└── SubT_MRS_{trajectory names ...}_{robot types ...}.zip
    ├── (zipped) cam_0
    │   ├── {...}.png
    │   └── timestamps.txt
    ├── (zipped) imu
    │   └── imu_data.csv
    └── (zipped) tf
        └── tf_data.csv
```
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

## SubT-MRS Datasets

- <b> Multiple Modalities: </b>
Our dataset includes hardware time-synchronized data from 4 RGB cameras, 1 LiDAR, 1 IMU, and 1 thermal camera, providing diverse and precise sensor inputs.

- <b> Diverse Scenarios: </b>
    Collected from multiple locations, the dataset exhibits varying environmental setups, encompassing indoors, outdoors, mixed indoor-outdoor, underground, off-road, and buildings, among others.

- <b> Multi-Degraded: </b>
   By incorporating multiple sensor modalities and challenging conditions like fog, snow, smoke, and illumination changes, the dataset introduces various levels of sensor degradation.

- <b> Heterogeneous Kinematic Profiles:</b>
  The SubT-MRS Dataset uniquely features time-synchronized sensor data from diverse vehicles, including RC cars, legged robots, drones, and handheld devices, each operating within distinct speed ranges. 

## Tartan Air Datasets

This benchmark is based on the [TartanAir dataset](http://theairlab.org/tartanair-dataset/), which is collected in photo-realistic simulation environments based on the AirSim project. A special goal of this dataset is to focus on the challenging environments with changing light conditions, adverse weather, and dynamic objects. The four most important features of our dataset are:

   - **Large size diverse realistic data.** We collect the data in diverse environments with different styles, covering indoor/outdoor, different weather, different seasons, urban/rural.
   - **Multimodal ground truth labels.** We provide RGB stereo, depth, optical flow, and semantic segmentation images, which facilitates the training and evaluation of various visual SLAM methods. 
   - **Diversity of motion patterns.**  Our dataset covers much more diverse motion combinations in 3D space, which is significantly more difficult than existing datasets.
   - **Challenging Scenes.** We include challenging scenes with difficult lighting conditions, day-night alternating, low illumination, weather effects (rain, snow, wind and fog) and seasonal changes.Please refer to the TartanAir Dataset and the paper for more information. 

   Folder structure inside the Tartan Air dataset: 

```
    visual_envname
    ├── image_lcam_front                        # image folder
    │   ├── timestamps.txt                      # image timestamp
    │   ├── 000000_lcam_front.png               # RGB image 000000
    │   ├── 000001_lcam_front.png               # RGB image 000001
    │   ├── ... ...
    │   └── 000xxx_lcam_front.png               # RGB image 000xxx
    │
    └── imu                                     # IMU folder
        ├── acc.npy                             # IMU acceleration
        ├── acc.txt                             # IMU acceleration
        ├── gyro.npy                            # IMU gyroscope
        ├── gyro.txt                            # IMU gyroscope
        ├── imu.npy                             # IMU acceleration and gyroscope
        ├── imu.txt                             # IMU acceleration and gyroscope
        ├── imu_time.npy                        # IMU timestamp
        └── imu_time.txt                        # IMU timestamp

```


<!-- ![GIF Figure 1](img/slam_challenge/abandonedfactory.gif) ![GIF Figure 2](img/slam_challenge/gascola.gif) \\
![GIF Figure 3](img/slam_challenge/hospital.gif) ![GIF Figure 4](img/slam_challenge/jananesealley.gif) -->
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

## Download

<span style="font-size:1.3em;">ROS bag format:&emsp;**[Google](https://drive.google.com/drive/folders/1drrdOTp7L02QhPJtIvpKo6zB21NoNlYb)** Baidu</span>  
<span style="font-size:1.3em;">Folder format:&ensp;&ensp;&ensp;&nbsp;&nbsp;**[Google](https://drive.google.com/drive/folders/1GR9vavG2iPbXpwlEoH_WzchHspF0ZfQ6)** Baidu</span>

| Name | Source  | Location  | Robot |Sensor | Description | Trajectory Length (m)| Duration (s) |  Video | Calibration (Extrinsics) | Calibration (Intrinsics) |
|---|-----------|---------|-----------|-----------|------------|-----------|-------------|-----------|---------------|--------------|
|Handheld1|SubT-MRS|Lauren Cavern      |RC7|IMU,RGB|Darkness     |400.61|816|[link](https://youtu.be/4L7FiBxsMR0)| [Google](https://drive.google.com/file/d/1_ULJWK00Ul41KTwGt_8cpI56BLwg5Ko6/view?usp=drive_link) Baidu | [Google](https://drive.google.com/file/d/1pt92EAS_5QQoGIKX0c2eu_umdnanx3EJ/view?usp=drive_link) Baidu |
|Handheld2|SubT-MRS|Lauren Cavern      |RC7|IMU,RGB|Darkness     |583.19|739|[link](https://youtu.be/QYLY2Zc3j1w)| [Google](https://drive.google.com/file/d/1f7P6IKrLUrIp2icrOr4fQCk2WcDQl_Nh/view?usp=drive_link) Baidu | [Google](https://drive.google.com/file/d/1z8CCOMW-FkgGNgM_Vct8RvhpvmWWE4KI/view?usp=drive_link) Baidu |
|OverExposure      |SubT-MRS|Hawkins   |RC7|IMU,RGB|Over Exposure|456.26|2128|[link](https://youtu.be/uxAn72fgroM)| [Google](https://drive.google.com/file/d/1CN8Jt5d6BpE01_pyU-8xgSeur0jlS7k5/view?usp=drive_link) Baidu | [Google](https://drive.google.com/file/d/1UrtFgdCWRvJdO-LexkXiaVSBNLh3DCdj/view?usp=drive_link) Baidu |
|Endofworld        | TartanAir | Simulation | Virtual Sensors| IMU,RGB | Fog              | 280 | 70.8  |[link](https://youtu.be/umIsv2jDHCY)|[Google](https://drive.google.com/file/d/1I3MxLngx9tRIkaSJNGvPOda4l51wBb6D/view?usp=drive_link) Baidu |[Google](https://drive.google.com/file/d/1Rss0KOY22kyXQ_7LA5-cIERgva3xz4R2/view?usp=drive_link) Baidu |
|Moon              | TartanAir | Simulation | Virtual Sensors| IMU,RGB | Shaddow          | 850 | 346.9 |[link](https://youtu.be/-xiAdl6mOXY)|[Google](https://drive.google.com/file/d/1I3MxLngx9tRIkaSJNGvPOda4l51wBb6D/view?usp=drive_link) Baidu |[Google](https://drive.google.com/file/d/1Rss0KOY22kyXQ_7LA5-cIERgva3xz4R2/view?usp=drive_link) Baidu |
|Westerndesert     | TartanAir | Simulation | Virtual Sensors| IMU,RGB | Day-night Circle | 600 | 180.5 |[link](https://youtu.be/YVAnT3mVF90)|[Google](https://drive.google.com/file/d/1I3MxLngx9tRIkaSJNGvPOda4l51wBb6D/view?usp=drive_link) Baidu |[Google](https://drive.google.com/file/d/1Rss0KOY22kyXQ_7LA5-cIERgva3xz4R2/view?usp=drive_link) Baidu |

## Bonus Tracks

🚀 We also provide 3 extra datasets from   [Sensor Fusion Challenge](/iccv23_challenge_Mul) as bonuses in the competition. 
You will get **extra scores** if you test your algoithm on Bonus Track and submit the results to us. 

<!-- 
Three separate awards will be given for each track.

Your SLAM performance in <b>the Sensor Fusion track will not impact</b> the scores in other tracks. -->

<!-- 
Join us now to become a vital part of cutting-edge advancements in robotics and sensor fusion! 🤖💡 Let your expertise shine in this thrilling competition! -->

<!-- We invite you to test your VIO algorithm with our Bonus datasets (3 extra datasets). -->

<!-- 
The intention behind this separation is to allow participants ample time for fine-tuning their algorithms without the added pressure of immediate scoring.

Nonetheless, it is mandatory for all participants to provide the results from the Bonus track to complete their entry in the visual-inertial track competition. 
This will aid in a comprehensive evaluation of the algorithms and showcase their adaptability to diverse and complex datasets. -->


| Name | Source    | Location  | Robot     |Sensor     | Description | Trajectory | Duration  |  Video | Calibration (Extrinsics) | Calibration (Intrinsics) |
|------|-----------|-----------|-----------|-----------|-------------|-----------|-------------|-----------|---------------|--------------|
|Smoke_Room   |SubT-MRS|Hawkins|RC7|RGB,Thermal,IMU|Visual Degraded|104.84|418|[link](https://youtu.be/Ti2eAbDRMNk)| [Google](https://drive.google.com/file/d/1HjWlRVQQvgrFGlgRxcczRt92Xy_P-5Ij/view?usp=drive_link) Baidu | [Google](https://drive.google.com/file/d/1Q0JiqiIgGZ-7DZKZDNJ68F7rpC2rrLtT/view?usp=drive_link) Baidu |
|Outdoor_Night|SubT-MRS|Hawkins|SP1|RGB,Thermal,IMU|Visual Degraded|254.03|484|[link](https://youtu.be/p3Gmdem0LoU)| [Google](https://drive.google.com/file/d/1Zkb4FybZBx2skEXxYnffL4jNneTmd8pQ/view?usp=drive_link) Baidu | [Google](https://drive.google.com/file/d/1hbIyPUJ24YSyX1vISjkMUeqX5K0rrSkU/view?usp=drive_link) Baidu |
|FlashLight   |SubT-MRS|Hawkins|SP1|RGB,Thermal,IMU|Visual Degraded|147.75|279|[link](https://youtu.be/RybUmK27fyY)| [Google](https://drive.google.com/file/d/10YJQ3FMRw95F3_yhOsX2bbuMuvQbtnVV/view?usp=drive_link) Baidu | [Google](https://drive.google.com/file/d/13iTBn_po_GWxt3X8kNWVGZ2wwQ38Eou0/view?usp=drive_link) Baidu |


## Evaluation 
The submission will be ranked based on Absolute Trajectory Error (ATE) and Relative Pose Error (RPE). Specifically, The ATE and RPE of every trajectory in the visual inertial track and its bonus track will be evaluated. The final score for a submitted trajectory will be assigned according to which interval the weighted sum of the ATE and RPE lies in.  

## Submit the results. 

### Prepare the trajectory
For each of the 9 trajectories of **visual-inertial track**, you need to compute the **poses in IMU coordinate frame**, and save them in the text file with the name sequnce_name.txt. Put all 9 files into a zip file with the following structure: 


```
    visual_inertial_track.zip
    ├── SubT_MRS_Laurel_Caverns_Handheld1.txt     # result file for the trajectory Laurel_Caverns_Handheld1
    ├── SubT_MRS_Laurel_Caverns_Handheld2.txt     # result file for the trajectory Laurel_Caverns_Handheld2
    ├── SubT_MRS_OverExposure_LegRobot.txt        # result of te trajectory OverExposure_LegRobot
    ├── TartanAir_visual_endofworld.txt           # result file for the trajectory Urban_Challenge_UGV1
    ├── TartanAir_visual_moon.txt                 # result file for the trajectory Urban_Challenge_UGV2
    ├── TartanAir_visual_westerndesert.txt        # result file for the trajectory Laurel_Cavern
    │   (Below are Bonuses)
    ├── SubT_MRS_Flash_Light_LegRobot.txt         # result file for the trajectory Flash Light
    ├── SubT_MRS_Hawkins_Smoke_Handheld.txt       # result file for the smoke room 
    └── Subt_MRS_Outdoor_Night_LegRobot.txt       # result file for the outdoor night

```



<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>



The text file should have the following format: 

```
# timestamp_s tx ty tz qx qy qz qw
1.403636580013555527e+09 0.0 0.0 0.0 0.0 0.0 0.0 0.0

```
<br>
<br>
<br>
<br>
<br>

It is a text file containing the translation and orientation of the IMU in a fixed coordinate frame. The estimated trajectory file should satisfy the following requirements.
- Each line in the text file contains a single pose.
- The format of each line is 'timestamp_s tx ty tz qx qy qz qw'. 
- tx ty tz (3 floats) give the position of IMU sensor to the world origin in the world frame.
- qx qy qz qw (4 floats) give the orientation of IMU in the form of a unit quaternion with respect to the world frame. 
- The trajectory can have an arbitrary initial position and orientation. However, we are using the IMU frame to define the motion. That is to say, the x-axis is pointing to forward, the y-axis is pointing left, the z-axis is pointing up.

### Submit in Gradescope

To submit the estimated trajectory into the submission system, you can follow the steps listed below:

1. Register a account in the [GradeScope](http://gradescope.com/) and log into the website.
2. Click the right-bottom `Add Course` button and enter the course-entry code: `V5NPPX` , Then you can find the `iccv-vi` courses in your GradeScope homepage.
3. Click the `iccv-vi` course and you will see the assignment named `Trajectory-result-submission` in the dashboard.
4. Click the assignment and upload your `visual-inertial-track.zip` file. Also please remember to input the group name as the leaderboard name. Then click the upload button.
    - You should directly compress the estimated result files of the trajectories into a zip file, not the folder containing the result files.
5. After around 1 minutes, you will see the APE and RPE result of your trajectory in the leaderboard.


- Note: 
    1. You must submit all the 9 trajectories for visual inertial track.
    2. The trajecotry should be complete. The duration of estimated trajecotry should be roughly same with ground truth trajectory. 

### Submit Report

Participants are requested to submit a report describing their methods along with the gradescope submission. A template for the same is provided here : <a href="Report/ICCV_Report_Template.zip" download> ICCV_Template_Report </a> . Please include your report pdf in the `visual-inertial-track.zip` file.

## Challenge Rules 
1. Participants are welcome to form teams. A participant cannot be in multiple teams and a team must make submissions under a single account.  
2. Every day a team can submit for at most once on gradescope and the submission must be in a certain time window: 12:00 P.M. - 11:59 P.M. UTC. 
3. The size of every trajectory file submitted should be no more than 2 MB.  
4. Every team <b>must submit a report</b> along with the gradescope submissions.  
5. Organizers reserve the right to make changes to the rules and timeline.  
6. Violation of the rules or other unfair activities may result in disqualification.  

##  🎉Visual-inertial Leaderboard🎉
As of 11:59 PM EDT, October 15th, 2023.

| ATE Rank | Team             | Mean(1/ATE)  |
|------|----------------------------|--------|
| 1    | Xiongfeng Peng, et al.     | 6.5149 |
| 2    | Yunlong Jiang, et al.      | 0.8052 |
| 3    | Shuaixin Li, et al.        | 0.3228 |
| 4    | Thien Hoang Nguyen, et al. | 0.2546 |
| 5    | Songkang Dai, et al.       | 0.0764 |

| RPE Rank | Team              | Mean(1/RPE)  |
|------|----------------------------|---------|
| 1    | Xiongfeng Peng, et al.     | 73.9029 |
| 2    | Shuaixin Li, et al.        |  6.0059 |
| 3    | Thien Hoang Nguyen, et al. |  3.9882 |
| 4    | Yunlong Jiang, et al.      |  2.3515 |
| 5    | Songkang Dai, et al.       |  1.3427 |

Note: The ATE(RPE) rank is according to the mean of the reciprocal of each trajectory's ATE(RPE) score, weighted by the trajectory length.

<!-- Leaderboard will be open when there is still enough time before the challenge ends. -->

## Contact us

If you have any question or see anything wrong, please do not hesitate to <b>post issues on this [github website](https://github.com/water-horse/ICCV2023_SLAM_Challenge.git) </b>. We would love to hear from your feedback! Every post will be responded with no spared effort within 36 hours.

## Summary 
We summarized the SLAM performance of above top teams. Feel free to check our [Paper](https://arxiv.org/abs/2307.07607) 

```
@misc{zhao2023subtmrs,
      title={SubT-MRS Dataset: Pushing SLAM Towards All-weather Environments}, 
      author={Shibo Zhao and Yuanjun Gao and Tianhao Wu and Damanpreet Singh and Rushan Jiang and Haoxiang Sun and Mansi Sarawata and Yuheng Qiu and Warren Whittaker and Ian Higgins and Yi Du and Shaoshu Su and Can Xu and John Keller and Jay Karhade and Lucas Nogueira and Sourojit Saha and Ji Zhang and Wenshan Wang and Chen Wang and Sebastian Scherer},
      year={2023},
      eprint={2307.07607},
      archivePrefix={arXiv},
      primaryClass={cs.RO}
}

```

## Disclaimer
Due to the rapidly changing nature of the SLAM, the above competitation results and SLAM summary is updated on October 15th 2023.
In addition, due to the rich body of literature, there
may be inaccuracies or mistakes in the paper. We welcome readers to send pull requests to our GitHub repository (inside https://github.com/water-horse/ICCV2023_SLAM_Challenge.git) so we may continue to update our references, correct the mistakes and inaccuracies,
as well as updating the entries of the studies in the paper. 

<!-- Display the countdown timer in an element -->
<style>

p1 {
  text-align: center;
  font-size: 60px;
  margin-top: 0px;
  margin-left: 350px;
}
</style>
<!-- <p1 id="demo"></p1> -->

<script>
// Set the date we're counting down to
// var countDownDate = new Date("Sept 25, 2023 15:37:25").getTime();
var countDownDate = Date.UTC(2023, 09, 16, 4, 0, 0);

// Update the count down every 1 second
var x = setInterval(function() {

  // Get today's date and time
  var now = new Date().getTime();
// var new=Date.UTC(date.getUTCMonth(),
// date.getUTCDate(), 
// date.getUTCFullYear(), 
// date.getUTCHours(),
// date.getUTCMinutes(), 
// date.getUTCSeconds());
// let utc= new Date(utcString);
//   var now = new (Date().getTime()).getTimezoneOffset();
// console.log(dt); // Gives Tue Mar 22 2016 09:30:00 GMT+0530 (IST)

//   var now=dt.setTime(dt.getTime()+dt.getTimezoneOffset());
// console.log(dt); // Gives Tue Mar 22 2016 04:00:00 GMT+0530 (IST)

// var offset = -300; //Timezone offset for EST in minutes.
// var estDate = new Date(dt.getTime() + offset*60*1000);
// console.log(estDate); //Gives Mon Mar 21 2016 23:00:00 GMT+0530 (IST)

  // Find the distance between now and the count down date
  var distance = countDownDate - now;

  // Time calculations for days, hours, minutes and seconds
  var days = Math.floor(distance / (1000 * 60 * 60 * 24));
//   var days=distance;
  var hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
  var minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
  var seconds = Math.floor((distance % (1000 * 60)) / 1000);

  // Display the result in the element with id="demo"
  document.getElementById("demo").innerHTML = days + "d " + hours + "h "
  + minutes + "m " + seconds + "s ";

  // If the count down is finished, write some text
  if (distance < 0) {
    clearInterval(x);
    document.getElementById("demo").innerHTML = "EXPIRED";
  }
}, 1000);
</script>
