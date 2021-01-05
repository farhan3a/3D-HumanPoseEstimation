# 3D-HumanPoseEstimation

### Abstract
<p> The project aims to perform 3D human pose estimation on monocular RGB images and videos and make an interactive tool that helps in using this technology with convenience. We divided the project into 2 phases. </p>
<p> We dedicated phase I to scrutinizing well-known human pose estimation models and setting up a working prototype and pipeline. Existing research and pre-trained models for 3D-HPE have their strong points and weaknesses. We scrutinized models and found the most promising model combination: HRNet and GAST-Net. After HRNet receives input image or video and produces 2D output, GAST-Net receives the 2D input and returns the 3D output. </p>
<p> During Phase II, the inherent problems of human pose estimation models such as jittering, occlusion, and depth-ambiguity were fixed by improving the 2D Keypoints prediction step. Finally, Django was used to build a web application, and the deployment was done on Amazon AWS Cloud Server for strong computational power. </p>

### Datasets
<p> It is very challenging to build an in-the-wild dataset. Finalizing and training the model on the right dataset was one of the most crucial and challenging parts of 3D HPE. We spent a good amount of time exploring and deciding on them. Let’s quickly take an overview of the final datasets which we have decided on for the 2 different stages of our project. </p>
<p> For training our model to produce 2D keypoint predictions from the input video, we have worked on the COCO and MPII Human Pose dataset. Both of these are publicly available benchmark datasets for object detection, segmentation, and pose estimation. Each of them has 50K+ images with 80+ subjects covering 300+ human activities. </p>
<p> For transforming the estimated 2D keypoints into 3D pose estimation, the models were trained and tested on two state-of-the-art datasets: Human3.6M and HumanEva-I. Human3.6M has 3.6 million video frames with 11 professional subjects performing 15 daily activities. HumnaEva-I, on the other hand, is a much smaller dataset and contains only 4 subjects with 6 everyday actions. </p>
