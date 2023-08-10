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

# Challenge

In this track, we exclusively offer access to high-quality **visual-inertial** datasets sourced from SubT-MRS and TartanAir. These datasets encompass various challenging conditions such as **"lighting changes, darkness, smoke, self-similar environments and more"** providing a test from **simulation to real-world**.

## SubT-MRS Datasets

- <b> Multiple Modalities: </b>
Our dataset includes hardware time-synchronized data from 4 RGB cameras, 1 LiDAR, 1 IMU, and 1 thermal camera, providing diverse and precise sensor inputs.

- <b> Diverse Scenarios: </b>
    Collected from multiple locations, the dataset exhibits varying environmental setups, encompassing indoors, outdoors, mixed indoor-outdoor, underground, off-road, and buildings, among others.

- <b> Multi-Degraded: </b>
   By incorporating multiple sensor modalities and challenging conditions like fog, snow, smoke, and illumination changes, the dataset introduces various levels of sensor degradation.

- <b> Heterogeneous Kinematic Profiles:</b>
  The SubT-MRS Dataset uniquely features time-synchronized sensor data from diverse vehicles, including RC cars, legged robots, drones, and handheld devices, each operating within distinct speed ranges. 

   File structure inside Subt-MRS datasets:  

    ```
    Visual_Inertial_Track
    ├── rosbag
    │   ├── TartanAir_visual_{places ...}_noise0.bag
    │   └── SubT_MRS_{trajectory names ...}_{robot types ...}.zip
    │       └── (zipped) raw_data_{...}yyyy-mm-dd-hh-mm-ss{...}.bag
    ├── folder
    │   ├── TartanAir_visual_{places ...}.zip
    │   │   ├── (zipped) imu
    │   │   │   └── [acc/gyro/imu/imu_time].[npy/txt]
    │   │   └── (zipped) image_lcam_front
    │   │       ├── {...}_lcam_front.png
    │   │       └── timestamps.txt
    │   └── SubT_MRS_{trajectory names ...}_{robot types ...}.zip
    │       ├── (zipped) cam_0
    │       │   ├── {...}.png
    │       │   └── timestamps.txt
    │       ├── (zipped) imu
    │       │   └── imu_data.csv
    │       └── (zipped) tf
    │           └── tf_data.csv
    └── calibration
        ├── SubT_MRS_{trajectory names ...}_{robot types ...}_Extrinsics.yaml
        └── SubT_MRS_{trajectory names ...}_{robot types ...}_Intrinsics.yaml
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
<br>
<br>
<br>
<br>
<br>
<br>
<br>



## Tartan Air Datasets

This benchmark is based on the [TartanAir dataset](http://theairlab.org/tartanair-dataset/), which is collected in photo-realistic simulation environments based on the AirSim project. A special goal of this dataset is to focus on the challenging environments with changing light conditions, adverse weather, and dynamic objects. The four most important features of our dataset are:

   - **Large size diverse realistic data.** We collect the data in diverse environments with different styles, covering indoor/outdoor, different weather, different seasons, urban/rural.
   - **Multimodal ground truth labels.** We provide RGB stereo, depth, optical flow, and semantic segmentation images, which facilitates the training and evaluation of various visual SLAM methods. 
   - **Diversity of motion patterns.**  Our dataset covers much more diverse motion combinations in 3D space, which is significantly more difficult than existing datasets.
   - **Challenging Scenes.** We include challenging scenes with difficult lighting conditions, day-night alternating, low illumination, weather effects (rain, snow, wind and fog) and seasonal changes.Please refer to the TartanAir Dataset and the paper for more information. 

   File structure inside the Tartan Air dataset: 

```
    visual_envname
    |
    --- image_lcam_front                        # image folder 
    |       |
    |       ---- timestamps.txt                 # image timestamp
    |       ---- 000000_lcam_front.png          # RGB image 000000
    |       ---- 000001_lcam_front.png          # RGB image 000001
    |       .
    |       .
    |       ---- 000xxx_lcam_front.png          # RGB image 000xxx
    |
    --- imu                                     # IMU folder 
    |       |
    |       ---- acc.npy                        # IMU acceleration
    |       ---- acc.txt                        # IMU acceleration
    |       ---- gyro.npy                       # IMU gyroscope
    |       ---- gyro.txt                       # IMU gyroscope
    |       ---- imu.npy                        # IMU acceleration and gyroscope
    |       ---- imu.txt                        # IMU acceleration and gyroscope
    |       ---- imu_time.npy                   # IMU timestamp
    |       ---- imu_time.txt                   # IMU timestamp

```


<!-- ![GIF Figure 1](img/slam_challenge/abandonedfactory.gif) ![GIF Figure 2](img/slam_challenge/gascola.gif) \\
![GIF Figure 3](img/slam_challenge/hospital.gif) ![GIF Figure 4](img/slam_challenge/jananesealley.gif) -->

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
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>


## Download

To download the sensor data for visual-inertial sensor fusion track, <span style="font-size:1.3em;">**click [here](https://drive.google.com/drive/folders/1drrdOTp7L02QhPJtIvpKo6zB21NoNlYb) for ROS bags and click [here](https://drive.google.com/drive/folders/1GR9vavG2iPbXpwlEoH_WzchHspF0ZfQ6) for processed folders**</span>.

| Name | Source  | Location  | Robot |Sensor | Description | Trajectory Length (m)| Duration (s) |  Video | Calibration (Extrinsics) | Calibration (Intrinsics) |
|---|-----------|---------|-----------|-----------|------------|-----------|-------------|-----------|---------------|--------------|
|Handheld1|SubT-MRS|Lauren Cavern      |RC7 Payload|IMU,RGB|Darkness     |400.61|816|[link](https://youtu.be/4L7FiBxsMR0)| [google](https://drive.google.com/file/d/1_ULJWK00Ul41KTwGt_8cpI56BLwg5Ko6/view?usp=drive_link)| [google](https://drive.google.com/file/d/1pt92EAS_5QQoGIKX0c2eu_umdnanx3EJ/view?usp=drive_link)|
|Handheld2|SubT-MRS|Lauren Cavern      |RC7 Payload|IMU,RGB|Darkness     |583.19|739|[link](https://youtu.be/QYLY2Zc3j1w)| [google](https://drive.google.com/file/d/1f7P6IKrLUrIp2icrOr4fQCk2WcDQl_Nh/view?usp=drive_link)| [google](https://drive.google.com/file/d/1z8CCOMW-FkgGNgM_Vct8RvhpvmWWE4KI/view?usp=drive_link)|
|OverExposure      |SubT-MRS|Hawkins   |RC7 Payload|IMU,RGB|Over Exposure|456.26|2128|[link](https://youtu.be/uxAn72fgroM)| [google](https://drive.google.com/file/d/1CN8Jt5d6BpE01_pyU-8xgSeur0jlS7k5/view?usp=drive_link)| [google](https://drive.google.com/file/d/1UrtFgdCWRvJdO-LexkXiaVSBNLh3DCdj/view?usp=drive_link)|
|Endofworld        | TartanAir | Simulation | Virtual Sensors| IMU,RGB | Fog              | 280 | 70.8  |[link](https://youtu.be/umIsv2jDHCY)|[google](https://drive.google.com/file/d/1myGAvGuNf0FcYAteNVHC73ElsglPmMO4/view?usp=drive_link)   |[google](https://drive.google.com/file/d/1Rss0KOY22kyXQ_7LA5-cIERgva3xz4R2/view?usp=drive_link)   |
|Moon              | TartanAir | Simulation | Virtual Sensors| IMU,RGB | Shaddow          | 850 | 346.9 |[link](https://youtu.be/-xiAdl6mOXY)|[google](https://drive.google.com/file/d/1myGAvGuNf0FcYAteNVHC73ElsglPmMO4/view?usp=drive_link)   |[google](https://drive.google.com/file/d/1Rss0KOY22kyXQ_7LA5-cIERgva3xz4R2/view?usp=drive_link)   |
|Westerndesert     | TartanAir | Simulation | Virtual Sensors| IMU,RGB | Day-night Circle | 600 | 180.5 |[link](https://youtu.be/YVAnT3mVF90)|[google](https://drive.google.com/file/d/1myGAvGuNf0FcYAteNVHC73ElsglPmMO4/view?usp=drive_link)   |[google](https://drive.google.com/file/d/1Rss0KOY22kyXQ_7LA5-cIERgva3xz4R2/view?usp=drive_link)   |

## Bonus Tracks(Can also be found in the Multi Modal Fusion Track)

🚀 We also provide 3 extra datasets from   [Sensor Fusion Challenge](/iccv23_challenge_Mul) as bonus in the competition. 
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
|Smoke_Room   |SubT-MRS|Hawkins|RC7|RGB,Thermal,IMU|Visual Degraded|104.84|418|[link](https://youtu.be/Ti2eAbDRMNk)| [google](https://drive.google.com/file/d/1HjWlRVQQvgrFGlgRxcczRt92Xy_P-5Ij/view?usp=drive_link) | [Baidu](dummy) [google](https://drive.google.com/file/d/1Q0JiqiIgGZ-7DZKZDNJ68F7rpC2rrLtT/view?usp=drive_link) |
|Outdoor_Night|SubT-MRS|Hawkins|SP1|RGB,Thermal,IMU|Visual Degraded|254.03|484|[link](https://youtu.be/p3Gmdem0LoU)| [google](https://drive.google.com/file/d/1Zkb4FybZBx2skEXxYnffL4jNneTmd8pQ/view?usp=drive_link) | [Baidu](dummy) [google](https://drive.google.com/file/d/1hbIyPUJ24YSyX1vISjkMUeqX5K0rrSkU/view?usp=drive_link) |
|FlashLight   |SubT-MRS|Hawkins|SP1|RGB,Thermal,IMU|Visual Degraded|147.75|279|[link](https://youtu.be/RybUmK27fyY)| [google](https://drive.google.com/file/d/10YJQ3FMRw95F3_yhOsX2bbuMuvQbtnVV/view?usp=drive_link) | [Baidu](dummy) [google](https://drive.google.com/file/d/13iTBn_po_GWxt3X8kNWVGZ2wwQ38Eou0/view?usp=drive_link) |


## Evaluation 
The submission will be ranked based on Absolute Trajectory Error (ATE) and Relative Pose Error (RPE). Specifically, The ATE and RPE of every trajectory in the visual inertial track and its bonus track will be evaluated. The final score for a submitted trajectory will be assigned according to which interval the weighted sum of the ATE and RPE lies in.  

## Submit the results. 

### Prepare the trajectory
For each of the 9 trajectories of **visual-inertial track**, you need to compute the **poses in IMU coordinate frame**, and save them in the text file with the name sequnce_name.txt. Put all 9 files into a zip file with the following structure: 


```
    visual_inertial_track.zip
    --- SubT_MRS_Laurel_Caverns_Handheld1.txt     # result file for the trajectory Laurel_Caverns_Handheld1
    --- SubT_MRS_Laurel_Caverns_Handheld2.txt     # result file for the trajectory Laurel_Caverns_Handheld2
    --- SubT_MRS_OverExposure_LegRobot.txt        # result of te trajectory OverExposure_LegRobot
    --- TartanAir_visual_endofworld.txt           # result file for the trajectory Urban_Challenge_UGV1
    --- TartanAir_visual_moon.txt                 # result file for the trajectory Urban_Challenge_UGV2
    --- TartanAir_visual_westerndesert.txt        # result file for the trajectory Laurel_Cavern
    Bonus_track 
    --- SubT_MRS_Flash_Light_LegRobot.txt         # result file for the trajectory Flash Light
    --- SubT_MRS_Hawkins_Smoke_Handheld.txt       # result file for the smoke room 
    --- Subt_MRS_Outdoor_Night_LegRobot.txt       # result file for the outdoor night

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
- The format of each line is 'tx ty tz qx qy qz qw'. 
- tx ty tz (3 floats) give the position of IMU sensor to the world origin in the world frame.
- qx qy qz qw (4 floats) give the orientation of IMU in the form of a unit quaternion with respect to the world frame. 
- The trajectory can have an arbitrary initial position and orientation. However, we are using the IMU frame to define the motion. That is to say, the x-axis is pointing to forward, the y-axis is pointing left, the z-axis is pointing up.

### Submit in Gradescope  (@wenshan)

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

## Challenge Rules 
1. Participants are welcome to form teams. A participant cannot be in multiple teams and a team must make submissions under a single account.  
2. Every day a team can submit for at most once on gradescope and the submission must be in a certain time window: 12:00 P.M. - 11:59 P.M. UTC. 
3. The size of every trajectory file submitted should be no more than 2 MB.  
4. Organizers reserve the right to make changes to the rules and timeline.  
5. Violation of the rules or other unfair activities may result in disqualification.  

##  🎉Visual-inertial Leaderboard 🎉

| Rank | Algorithm       | ATE (m)  | RPE (%)  | Use Loop Closure | Learning/Traditional|sensor | Run-time (ms) | Memory (MB) |
|------|-----------------|----------|----------|------------------|---------------------|------------------|---------------|------------|
| 1    | Algorithm A     | 0.15     | 0.85     | True             | 90.2                | Visual, IMU              | 28.3          | 235.5      |
| 2    | Algorithm B     | 0.21     | 1.20     | False            | 89.1                | Visual, IMU             | 35.6          | 281.8      |
| 3    | Algorithm C     | 0.28     | 1.55     | False            | 85.6                | Visual, IMU            | 43.2          | 320.1      |
| 4    | Algorithm D     | 0.35     | 2.01     | False            |  82.4               | Visual, IMU              | 50.8          | 352.5      |
| 5    | Algorithm E     | 0.41     | 2.45     | False            | 79.8                | Visual, IMU            | 58.1          | 389.7      |

## Contact us

If you have any issues on the SLAM challenge, please post issues on this [github](git@github.com:shibowing/ICCV2023_SLAM_Challenge.git). 
