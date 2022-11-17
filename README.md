# DeepLabCut-Live
Learn to install and use DeepLabCut-Live to conduct real time pose estimation on a video. The methods discussed were performed on a linux system.

## Installation

### 1. Create/Activate Python Environment:
    virtualenv --python python3.7 dlc-live
    source dlc-live/bin/activate
    pip install tensorflow==1.13.1

### 2. Pip Install DeepLabCut-Live:
    pip install deeplabcut-live

### 3. Check Installation:
    dlc-live-test
      -If installed properly, a video of a dog will appear labeled in a pop up window.
      
## Real Time Pose Estimation on a Video 

### 1. Export your DLC model. Do the following in python:
    Import deeplabcut
    deeplabcut.export_model(cfg_path, iteration=None, shuffle=1, trainingsetindex=0, snapshotindex=None, TFGPUinference=True, overwrite=False,  make_tar=True)
### 2. Call benchmark_videos function in python in your dlc-live pyenv. Do the following in python:
    from dlclive import benchmark_videos
    benchmark_videos(exported_model_path, test_video_path, display=True, resize=0.5, pcutoff=0.25, save_video=True)
        -Labeled video is saved in the same directory that the test video is in. The labeled video is in .avi format. 
