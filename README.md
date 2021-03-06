#Edge Template Tracker
Code for IROS 2018 paper '[*Real-Time Edge Template Tracking via Homography Estimation*](https://webdocs.cs.ualberta.ca/~xuebin/IROS2018.pdf)', [Xuebin Qin](https://webdocs.cs.ualberta.ca/~xuebin/),  Shida He, Zichen Zhang, Masood Dehghan, Jun Jin and Martin Jagersand. In IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS), 2018. [(Data)](https://github.com/NathanUA/Edge_Template_Tracking_Dataset) [(Video)](https://www.youtube.com/watch?v=ohnUCm-Ffc4&feature=youtu.be)

__Contact__: xuebin[at]ualberta[dot]ca

## Required libraries
OpenCV 2.4.9 (make sure QT enabled when installing Opencv)<br>

## Usage
1. clone this repo
```
git clone https://github.com/NathanUA/EdgeTemplateTracker.git
```
and Download the dataset
```
git clone https://github.com/NathanUA/Edge_Template_Tracking_Dataset.git
```

2. Go to the root directory run ```./STPF_main```. If it doesn't work, then you have to recompile it by command ```make```.

3. Run on different modes <br>.
Run the code on recorded videos by commend: ```./STPF_main 1 ../../data/videos_avi/box_359.avi``` (video path should be configured according to your settings).<br>
Run the code on webcam videos by commend: ```./STPF_main 0```.<br>

4. Initialize to-be-tracked edge template in the first frame.<br>
(1) Sequentially select the edge fragments by mouse left button clicking (mouse middle button scroll for zoom-in or zoom-out).<br>
(2) You could split some long fragments by moving your cursor to target position and pressing key ```b```.<br>
(3) Press ```f``` can undo the selection of the last fragment.<br>
(4) Press ```a``` to switch between the edge fragment selection mode and line segments drawing mode.<br>
(5) Press ```o``` or ```c``` to indicate open or closed (start and end pixels of the selected edge fragments will be connected after mouse middle button clicking in step (6)) edge template.<br>
(6) Click mouse middle button for finishing the edge template selection.<br>

5. ```Is it the last boundary of the object ?``` Press ```y``` to initialize another target, press ```n``` to continue labeling of the same target.<br>

6. Press ```Enter``` to test tracking on single frame or press ```Space``` to test tracking on the whole sequence.<br>

## Citation
```
@InProceedings{Qin2018ETTracker,
  author = {Qin, Xuebin and He, Shida and Zhang, Zichen and Dehghan, Masood and Jin, Jun and Jagersand, Martin.},
  title = {Real-Time Edge Template Tracking via Homography Estimation},
  booktitle={IEEE/RSJ IROS},
  year = {2018}
}
```

