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

