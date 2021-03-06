# HRI-Gestures: Gesture Recognition Dataset for Human Robot Interaction
HRI-Gestures is a gesture recognition dataset for Human Robot Interaction. More information can be found in "put paper link"

HRI-Gestures consists of RGB images, depth images and joint positions extracted with human detection and pose estimation.

For questions regarding the dataset please contact the paper authors.

### Access to the dataset
The skeleton/joint files can be downloaded [here](https://nextcloud.sdu.dk/index.php/s/AiyBziPXNGFmTTw).

For access to the image data please contact norbert@mmmi.sdu.dk. The data can only be used for research purposes.

### Dataset structure
HRI-Gestures includes samples from 17 different subjects, 20 action classes, and 4 views. Each sample includes:
* Sequence of RGB images
* Sequence of depth images
* Skeleton file

All files are named in the format AaaaSsssRrrrCccc, where Aaaa is the action class (A001-A020), Ssss is the subject ID (S001-S020), Rrrr is the repetition ID (R001-R010) and Cccc is the camera ID (C001-C004). Name example: A001S002R003C004.

All data is divided into Ssss folders containing all data recording for said subject.

C001-C003 are Intel RealSense D415 cameras and C004 is a Intel RealSense D455 camera.

**Data Resolution:**
Both RGB and depth images of all 4 cameras have a resolution of 1280x720.
The skeletons are comprised of the 3D positions of the 17 joints (*Nose*, *Left Eye*, *Right Eye*, *Left Ear*, *Right Ear*, *Left Shoulder*, *Right Shoulder*, *Left Elbow*, *Right Elbow*, *Left Wrist*, *Right Wrist*, *Left Hip*, *Right Hip*, *Left Knee*, *Right Knee*, *Left Ankle*, *Right Ankle*)

Skeletons are extracted using [https://www.scitepress.org/Papers/2020/98884/pdf/index.html](https://www.scitepress.org/Papers/2020/98884/pdf/index.html)

### Action classes
Actions are divided into two categories: Interactive and passive.
**Interactive** classes include A001-A015 in the following order
* Stop
* Go Right
* Go Left
* Come Here
* Follow Me
* Go Sway
* Agree
* Disagree
* Go There
* Get Attention
* Be Quiet
* Don???t Know
* Turn Around
* Take This
* Pick Up

**Passive** actions include A015-A020 with the following order:
* Standing Still
* Being Seated
* Walking Towards
* Walking Away
* Talking on Phone

### Evaluation Methods
Cross-Subject (CS) and Cross-Repetition (CR) evaluations are introduced in (paper). CS: S0xx, S0xx and S0xx are used for validation. CR: all even numbered repetitions are used for validation

### Example Code
* How to read/visualise skeleton files:
* Train simple network based on the RA-GCN.
