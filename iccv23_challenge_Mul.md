---
title: ‎ 
subtitle: ‎ 
layout: page
show_sidebar: false
hide_footer: true
menubar_toc: true
hero_height: is-medium
hero_image: /img/iccv/Mul.gif
---

# 🎉 Welcome to ICCV'23 Sensor-Fusion SLAM Challenge! 🎉

# Challenge

In this track, we exclusively offer access to high-quality **sensor-fusion** datasets sourced from SubT-MRS. These datasets encompass various challenging conditions such as **"lighting changes, darkness, smoke, self-similar environments and more"**.


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
    Multi_Modal_Sensor_Fusion_Track
    ├── rosbag
    │   └── SubT_MRS_{trajectory names ...}_{robot types ...}.zip
    │       └── (zipped) raw_data_{...}yyyy-mm-dd-hh-mm-ss{...}.bag
    ├── folder
    │   ├── SubT_MRS_{trajectory names ...}_{robot types ...}.zip
    │   │   ├── (zipped) cam_0
    │   │   │   ├── {...}.png
    │   │   │   └── timestamps.txt
    │   │   ├── (zipped) imu
    │   │   │   └── imu_data.csv
    │   │   ├── (zipped) lidar
    │   │   │   ├── {...}.las
    │   │   │   └── timestamps.txt
    │   │   └── (zipped) tf
    │   │       └── tf_data.csv
    │   └── SubT_MRS_{trajectory names ...}_{robot types ...}.zip
    │       ├── (zipped) cam_0
    │       │   ├── {...}.png
    │       │   └── timestamps.txt
    │       ├── (zipped) imu
    │       │   └── imu_data.csv
    │       ├── (zipped) tf
    │       │   └── tf_data.csv
    │       └── (zipped) thermal
    │           ├── {...}.png
    │           └── timestamps.txt
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
<br>
<br>


<!-- ![GIF Figure 1](img/slam_challenge/abandonedfactory.gif) ![GIF Figure 2](img/slam_challenge/gascola.gif) \\
![GIF Figure 3](img/slam_challenge/hospital.gif) ![GIF Figure 4](img/slam_challenge/jananesealley.gif) -->



## Download

To download the sensor data for multi-modal sensor fusion track, click [here](https://drive.google.com/drive/folders/1bV5oCLrpVoc6xKcIduUcco47nG0jPH6i) for ROS bags and click [here](https://drive.google.com/drive/folders/1E4EFVY-Bnef7sSBprnfL5Z49HAc89dLr) for processed folders.

| Name | Source  | Location  | Robot |Sensor | Description | Trajectory | Duration  | Size  |  Video | Calibration (Extrinsics) | Calibration (Intrinsics) |
|---|-----------|---------|-----------|-----------|------------|-----------|-------------|-----------|---------------|--------------|
|Multi_Floor|SubT-MRS|Hawkins|SP1|Lidar,RGB,IMU|Multi Floor|270|480|21.2G|[link](https://youtu.be/QcHjVLlsyXE)| [Baidu](dummy) [google](https://drive.google.com/file/d/1BV87D60W35UGzIaHjKD64c_J1G0U70jf/view?usp=drive_link) | [Baidu](dummy) [google](https://drive.google.com/file/d/1uH4wFmLeQNrIGlsUsO--PQuyEIOSOGvR/view?usp=drive_link) |
|Long_Corridor|SubT-MRS|Hawkins|RC2|Lidar,RGB,IMU|Multi Floor|616.45|332|14.6G|[link](https://youtu.be/prmBxGRGwNY)| [Baidu](dummy) [google](https://drive.google.com/file/d/1bB3jfEJeTf_XoLUHKOaxCNF_MCkiQTol/view?usp=drive_link) | [Baidu](dummy) [google](https://drive.google.com/file/d/10rv5dg5un7kUveTPS3XBx8IuIYGg9r2h/view?usp=drive_link) |
|BlockLiDAR|SubT-MRS|Mill19|RC3|Lidar,RGB,IMU|Block Lidar|307.55|677|17.1G|[link](https://youtu.be/2r4Z1XKTJHs)| [Baidu](dummy) [google](https://drive.google.com/file/d/1NscQVVsQc_CN-16O_VLpLQnmTWgBmf93/view?usp=drive_link) | [Baidu](dummy) [google](https://drive.google.com/file/d/1zCqwibpnmJ6I9lv29OUEnjyK2SxN4TbV/view?usp=drive_link) |
|BlockVisual|SubT-MRS|Mill19|RC3|Lidar,RGB,IMU,Thermal|Block Visual/Thermal|186.02|359|19.8G|[link](https://youtu.be/_vl2ClHvxPE)| [Baidu](dummy) [google](https://drive.google.com/file/d/136vuMpzb7OrO_6f8w2-p6g1xyXn09u--/view?usp=drive_link) | [Baidu](dummy) [google](https://drive.google.com/file/d/1f8DjHgZHH9-fCVUq1Q7kra5Tr5OtNBe-/view?usp=drive_link) |
|SmokeRoom|SubT-MRS|Hawkins|RC7|RGB,Thermal,IMU|Visual Degraded|104.84|418|20G|[link](https://youtu.be/Ti2eAbDRMNk)| [Baidu](dummy) [google](https://drive.google.com/file/d/1HjWlRVQQvgrFGlgRxcczRt92Xy_P-5Ij/view?usp=drive_link) | [Baidu](dummy) [google](https://drive.google.com/file/d/1Q0JiqiIgGZ-7DZKZDNJ68F7rpC2rrLtT/view?usp=drive_link) |
|OutdoorNight|SubT-MRS|Hawkins|RC7|RGB,Thermal,IMU|Visual Degraded|254.03|484|22.9G|[link](https://youtu.be/p3Gmdem0LoU)|  [Baidu](dummy) [google](https://drive.google.com/file/d/1Zkb4FybZBx2skEXxYnffL4jNneTmd8pQ/view?usp=drive_link) | [Baidu](dummy) [google](https://drive.google.com/file/d/1hbIyPUJ24YSyX1vISjkMUeqX5K0rrSkU/view?usp=drive_link) |
|FlashLight|SubT-MRS|Hawkins|RC7|RGB,Thermal,IMU|Visual Degraded|147.75|279|13G|[link](https://youtu.be/RybUmK27fyY)|  [Baidu](dummy) [google](https://drive.google.com/file/d/10YJQ3FMRw95F3_yhOsX2bbuMuvQbtnVV/view?usp=drive_link) | [Baidu](dummy) [google](https://drive.google.com/file/d/13iTBn_po_GWxt3X8kNWVGZ2wwQ38Eou0/view?usp=drive_link) |



## Evaluation 
The submission will be ranked based on completeness of the trajectory as well as on the position accuracy (ATE,RPE).

We will directly use ATE and RPE to evaluate the accuracy of trajectory. 


## Submit the results. 

### Prepare the trajectory
For each of the 5 trajectories of **sensor-fusion track**, you need to compute the **poses in IMU coordinate frame**, and save them in the text file with the name sequnce_name.txt. Put all 5 files into a zip file with the following structure: 

```
    Multi_Model_Sensor_Fusion.zip
    

--- SubT_MRS_Hawkins_Long_Corridor_RC.txt            # result file for the trajectory Long Corridor 
    --- SubT_MRS_Hawkins_Multi_Floor_LegRobot.txt        # result file for the trajectory Multi Floor 
    --- SubT_MRS_MILL19_Block_LiDAR.txt                  # result file for the trajectory Block LiDAR 
    --- SubT_MRS_MILL19_Block_Visual.txt                 # result file for the trajectory Block Visual   
    --- SubT_MRS_Flash_Light_LegRobot.txt                # result file for the trajectory Flash Light
    --- SubT_MRS_Hawkins_Smoke_Handheld.txt              # result file for the smoke room 
    --- Subt_MRS_Outdoor_Night_LegRobot.txt              # result file for the outdoor night
  
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
2. Click the right-bottom `Add Course` button and enter the course-entry code: `G2YGGB0`, Then you can find the `iccv-lii` courses in your GradeScope homepage.
3. Click the `iccv-lii` course and you will see the assignment named `Trajectory-result-submission` in the dashboard.
4. Click the assignment and upload your `sensor_fusion_track.zip` file. Also please remember to input the group name as the leaderboard name. Then click the upload button.
    - You should directly compress the estimated result files of the trajectories into a zip file, not the folder containing the result files.
5. After around 1 minutes, you will see the APE and RPE result of your trajectory in the leaderboard.

##  🎉Sensor-Fusion Leaderboard 🎉

| Rank | Algorithm       | ATE (m)  | RPE (%)  | Use Loop Closure | Learning/Traditional|sensor | Run-time (ms) | Memory (MB) |
|------|-----------------|----------|----------|------------------|---------------------|------------------|---------------|------------|
| 1    | Algorithm A     | 0.15     | 0.85     | True             | 90.2                | Visual, IMU              | 28.3          | 235.5      |
| 2    | Algorithm B     | 0.21     | 1.20     | False            | 89.1                | Visual, IMU             | 35.6          | 281.8      |
| 3    | Algorithm C     | 0.28     | 1.55     | False            | 85.6                | Visual, IMU            | 43.2          | 320.1      |
| 4    | Algorithm D     | 0.35     | 2.01     | False            |  82.4               | Visual, IMU              | 50.8          | 352.5      |
| 5    | Algorithm E     | 0.41     | 2.45     | False            | 79.8                | Visual, IMU            | 58.1          | 389.7      |

## Contact us

If you have any issues on the SLAM challenge, please post issues on this [github](git@github.com:shibowing/ICCV2023_SLAM_Challenge.git). 