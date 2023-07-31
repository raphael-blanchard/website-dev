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

In this track, we exclusively offer access to high-quality **visual-inertial** datasets sourced from SubT-MRS and Tartan Air. These datasets encompass various challenging conditions such as **"lighting changes, darkness, smoke, self-similar environments and more"** providing a test from **simulation to real-world**.


🚀 Don't Forget: The [Sensor Fusion Challenge](/iccv23_challenge_Mul) is a Must!
Seize this chance to demonstrate your skills and compete among the finest in the field!

Three separate awards will be given for each track.
Your SLAM performance in <b>the Sensor Fusion track will not impact</b> the scores in other tracks.
Join us now to become a vital part of cutting-edge advancements in robotics and sensor fusion! 🤖💡 Let your expertise shine in this thrilling competition!

## SubT-MRS Datasets

- <b> Multiple Modalities: </b>
Our dataset includes hardware time-synchronized data from 4 RGB cameras, 1 LiDAR, 1 IMU, and 1 thermal camera, providing diverse and precise sensor inputs.

- <b> Diverse Scenarios: </b>
    Collected from multiple locations, the dataset exhibits varying environmental setups, encompassing indoors, outdoors, mixed indoor-outdoor, underground, off-road, and buildings, among others.

- <b> Multi-Degraded: </b>
   By incorporating multiple sensor modalities and challenging conditions like fog, snow, smoke, and illumination changes, the dataset introduces various levels of sensor degradation.

- <b> Heterogeneous Kinematic Profiles:</b>
  The SubT-MRS Dataset uniquely features time-synchronized sensor data from diverse vehicles, including RC cars, legged robots, drones, and handheld devices, each operating within distinct speed ranges. 

   File structure:  (@YuanJun)

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


## Tartan Air Datasets

This benchmark is based on the [TartanAir dataset](http://theairlab.org/tartanair-dataset/), which is collected in photo-realistic simulation environments based on the AirSim project. A special goal of this dataset is to focus on the challenging environments with changing light conditions, adverse weather, and dynamic objects. The four most important features of our dataset are:

   - **Large size diverse realistic data.** We collect the data in diverse environments with different styles, covering indoor/outdoor, different weather, different seasons, urban/rural.
   - **Multimodal ground truth labels.** We provide RGB stereo, depth, optical flow, and semantic segmentation images, which facilitates the training and evaluation of various visual SLAM methods. 
   - **Diversity of motion patterns.**  Our dataset covers much more diverse motion combinations in 3D space, which is significantly more difficult than existing datasets.
   - **Challenging Scenes.** We include challenging scenes with difficult lighting conditions, day-night alternating, low illumination, weather effects (rain, snow, wind and fog) and seasonal changes.Please refer to the TartanAir Dataset and the paper for more information. 

   File structure: 

    ```
    mono
    |
    --- ME000                             # monocular easy trajectory 0 
    |       |
    |       ---- 000000.png          # RGB image 000000
    |       ---- 000001.png          # RGB image 000001
    |       .
    |       .
    |       ---- 000xxx.png           # RGB image 000xxx
    |
    +-- ME001                             # monocular easy trajectory 1 
    .
    .
    +-- ME007                            # monocular easy trajectory 7 
    |
    +-- MH000                            # monocular hard trajectory 0 
    .
    .
    |
    +-- MH007                            # monocular hard trajectory 7
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


## Download (@WenShan)

Click [here](dummy) to download the testing data for visual-inertial track. (Size: 7.65 GB)

| Name | Source  | Location  | Robot |Sensor | Description | Trajectory | Duration  | Size  |  Video | Download Link|
|---|-----------|---------|-----------|-----------|------------|-----------|-------------|-----------|---------------|--------------|
|Handheld1|SubT-MRS|Lauren Cavern      |RC7 Payload|IMU,RGB|Darkness     |400.61|816|45.3G|[link](dummy)|[Baidu](dummy) [google](dummy)|
|Handheld2|SubT-MRS|Lauren Cavern      |RC7 Payload|IMU,RGB|Darkness     |583.19|739|38.4G|[link](dummy)|[Baidu](dummy) [google](dummy)|
|OverExposure      |SubT-MRS|Hawkins   |RC7 Payload|IMU,RGB|Over Exposure|456.26|2128|46.1G|[link](dummy)|[Baidu](dummy) [google](dummy)|
|Endofworld        | Tartan Air        |  Simulation       | IMU,RGB          |           |            |           |             |           |[link](dummy)|[Baidu](dummy) [google](dummy)              |
|Moon              | Tartan Air        |  Simulation       | IMU,RGB          |           |            |           |             |           |[link](dummy)|[Baidu](dummy) [google](dummy)               |
|Westerndesert     | Tartan Air        |  Simulation       | IMU,RGB          |           |            |           |             |           |[link](dummy)|[Baidu](dummy) [google](dummy)  

## Bonus Tracks(Can also be found in the Multi Modal Fusion Track)

We invite you to test your VIO algorithm with our Bonus datasets (3 extra datasets).

**Please note that the results obtained from the Bonus track will not be factored into the final scoring for the visual-inertial track.** 
The intention behind this separation is to allow participants ample time for fine-tuning their algorithms without the added pressure of immediate scoring.

Nonetheless, it is mandatory for all participants to provide the results from the Bonus track to complete their entry in the visual-inertial track competition. 
This will aid in a comprehensive evaluation of the algorithms and showcase their adaptability to diverse and complex datasets.


| Name | Source    | Location  | Robot     |Sensor     | Description | Trajectory | Duration  | Size  |  Video | Download Link|
|------|-----------|-----------|-----------|-----------|-------------|-----------|-------------|-----------|---------------|--------------|
|Smoke_Room   |SubT-MRS|Hawkins|Handheld|RGB,Thermal,IMU|Visual Degraded|104.84|418|20G|[link](dummy)| [Baidu](dummy) [google](dummy)              |
|Outdoor_Night|SubT-MRS|Hawkins|Legrobot|RGB,Thermal,IMU|Visual Degraded|254.03|484|22.9G|[link](dummy)|  [Baidu](dummy) [google](dummy)               |
|FlashLight   |SubT-MRS|Hawkins|Legrobot|RGB,Thermal,IMU|Visual Degraded|147.75|279|13G|[link](dummy)|  [Baidu](dummy) [google](dummy)               |


## Evaluation (@ Wenshan)
The submission will be ranked based on completeness of the trajectory as well as on the position accuracy (ATE,RPE).

We will directly use ATE and RPE to evaluate the accuracy of trajectory. 

## Submit the results. 

### Prepare the trajectory
For each of the 9 trajectories of **visual-inertial track**, you need to compute the **poses in IMU coordinate frame**, and save them in the text file with the name sequnce_name.txt. Put all 5 files into a zip file with the following structure: 


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
- The number of lines/poses must be the same as the number of image frames in that trajectory. **(TODO: do we need this assumption? @wenshan)**  
- The format of each line is 'tx ty tz qx qy qz qw'. 
- tx ty tz (3 floats) give the position of IMU sensor to the world origin in the world frame.
- qx qy qz qw (4 floats) give the orientation of IMU in the form of a unit quaternion with respect to the world frame. 
- The trajectory can have an arbitrary initial position and orientation. However, we are using the IMU frame to define the motion. That is to say, the x-axis is pointing to forward, the y-axis is pointing left, the z-axis is pointing up.

### Submit in Gradescope  (@wenshan)

To submit the estimated trajectory into the submission system, you can follow the steps listed below:

1. Register a account in the [GradeScope](http://gradescope.com/) and log into the website.
2. Click the right-bottom `Add Course` button and enter the course-entry code: `V5NPPX0` , Then you can find the `iccv-vi` courses in your GradeScope homepage.
3. Click the `iccv-vi` course and you will see the assignment named `Trajectory-result-submission` in the dashboard.
4. Click the assignment and upload your `visual-inertial-track.zip` file. Also please remember to input the group name as the leaderboard name. Then click the upload button.
    - You should directly compress the estimated result files of the trajectories into a zip file, not the folder containing the result files.
5. After around 1 minutes, you will see the APE and RPE result of your trajectory in the leaderboard.

After submitted your trajectory zip file, the system will perform two checks:

- Note: 
    1. You must submit all the 9 trajectories for visual inertial track.
    2. The trajecotry should be complete. The duration of estimated trajecotry should be roughly same with ground truth trajectory. 

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