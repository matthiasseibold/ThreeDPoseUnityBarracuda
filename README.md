# ThreeDPoseUnityBarracuda
This project is a fork from:
https://github.com/digital-standard/ThreeDPoseUnityBarracuda

and stripped to only display the skeleton on top of the webcam stream.

![demo](Assets/StreamingAssets/ScreenShots/skeleton.png)

## Outline
ThreeDPoseUnityBarracuda is a sample source which read the onnx by Barracuda and do threeD pose estimation on Unity.
the accuracy got better than pre model. </br>
*Be aware of that the target should be only one person. It does not work for multi target. </br></br>
This sample lets the avatar named as "Unity chan" behaves same as the man on real time by estimating the 3D positions on the movie.</br>


Ported to Unity 2020.3.31f1.</br>
Currently works with Barracuda 1.0.5

## Performance Report
### GPU </br>
GeForce RTX2070 SUPER ⇒ About 30 FPS </br>
GeForce GTX1070 ⇒ About 20 FPS </br>
<font color="Red">**※Without GPU, it does not work fine basically**</font>

## Install and Tutorial
### Download and put files
1. Download/clone this repo to your local PC and open the project with Unity 2020.3.31f1.

2. Download onnx from our home page by clicking following URL in our HP.</br>
   https://digital-standard.com/threedpose/models/Resnet34_3inputs_448x448_20200609.onnx
   Place the ONNX model in Assets/Scripts/Model/ 
   and drag-and-drop it to "NN Model" in Gameobject named as "BarracudaRunner" in Inspector view.
     

## How to make a good estimate?

The frame that can be optionally displayed in the upper left corner (InputTexture) is the input image to the trained model.
Make sure that the whole body fits in this frame.
It is not possible to correctly estimate if the limbs stick out due to the edges of this frame. Since the program is performed assuming that the whole body is always in the frame, the error will increase if it exceeds the limit.
Also, the background is as simple as possible, and pants are better than skirts.

## Info
・Record</br>
If you want to record the motion, the following package might be suitable.</br>
https://github.com/zizai-inc/EasyMotionRecorder</br>

## License
### Non-commercial use</br>
・Please use it freely for hobbies and research. </br>
  When redistributing, it would be appreciated if you could enter a credit (Digital-  Standard Co., Ltd.).</br></br>

### Commercial use</br>
・Non-commercial use only.</br>
  
