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
