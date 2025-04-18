# ProjectAriaNotes
These are my notes reading the project aria documentation

# Sensors
- The reason that some sensors have different sampling rates is so that the errors that are produced by them are uncorrelated
- It is also not feasible or practical to record all of the sensors at max resolution and framerate
- Decide on what recording profile that you want to use before you start recording

# Vrs and data recording
- Utilize MPS rather than raw IMU data
```
$ vrs check <file.vrs>
$ vrs checksum <file.vrs>
```

# Data extraction
```
$ vrs extract-images <file.vrs> --to <image_folder>
$ vrs extract-audio <file.vrs> --to <audio_folder>
vrs extract-images <file.vrs> --raw-images --to <image_folder>
vrs extract-all <file.vrs> --to <folder>
```

# For time sync across multiple devices
- Can use TISync

# Vrs data viewing
- Install the following tool
```
# Pixi https://prefix.dev/
# Local install
pixi add vrs
# Global install
# pixi global install vrs
```

Once installed, use the following command to view vrs file:
```
vrsplayer sample_file_name_.vrs
```

# Vrs Sample Data:
![image](https://github.com/user-attachments/assets/f7b96b5f-5230-47d1-ad5b-d96c234348ca)

# MPS Sample Data:
- Trajectory and point cloud
- ![image](https://github.com/user-attachments/assets/14d8ee33-03ca-4c11-b66d-8c6d129a6f9c)

- Summay JSON also contains the status and information regarding the MPS data

# Requesting SLAM (Simulatenous localization And Mapping) data will yield the following:
6DoF Trajectory data
![image](https://github.com/user-attachments/assets/0866b4a1-709a-415e-a472-23d3f8d2bb74)
- Can pull x,y,z, roll, yaw, pitch
- Can pull Semi-Dense Point clouds
- Sensor calibration data

# Multi Slam
- Can combine multiple recordings to see side by side 3d global trajectories

# Eye Gaze
- general_eye_gaze.csv contains all of the data points that can be used to determine where the user is looking

# Hand Tracking
- MPS offers a json file that contains the coordinates for wrist and palm locations

# 2D Image coordinate system conventions

https://facebookresearch.github.io/projectaria_tools/docs/data_formats/coordinate_convention/2d_image_coordinate_system_convention





