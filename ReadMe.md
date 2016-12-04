# UE4 MixedReality Plugin

## Supported UE4 version

Unreal Engine 4.14.x

## Preparation
<br /> ・HTC vive
<br /> ・One additional Vive Controller (3 in all)
<br /> ・Capture board
<br /> ・Video Camera
<br /> ・Camera Rig
<br /> ・The Unreal Engine 4.12.5 download from GitHub
<br /> ・Install OBS Studio
## Introduction
<br /> Please unzip the downloaded zip file. Please copy the resulting "Engine" folder over the Engine folder in the Unreal Engine 4.14 acquired from GitHub, then Build using Visual Studio 2015. 
<br /> When you want to use it, add the following in the DefaultEngine.ini file of the project you want to use it in.
 
<br /> [SteamVR.Settings]
<br /> WindowMirrorMode=3

## How to run the sample
<br /> Open the folder "MixedRealitySample".
<br /> Right-click on the "MixedRealitySample.uproject", please select "Switch Engine Version". Specify the engine version you have <br /> built during the Introduction step.

<br /> This sample contains the following features.
<br /> ・BP_VRCapture2D
<br /> The BP class to synchronize the third controller and the video camera.
<br /> ・ForwardPost
<br /> Post effects to get the foreground by calculating the distance from the camera to the HMD.
<br /> ・MPC_
<br /> Materials collection, the "SearchDepth" is set to the distance from camera to HMD.


<br /> Please enable the RenderCustomDepthPass for objects that you want to display in the foreground.


<br /> Please enter the offset between the controller and the camera for the camera position to be correctly in the VR space.

<br /> When you run a VR preview foreground and background will be shown on the 4 split screen as below:

<br /> The upper left corner is the greened screen foreground, and lower right corner is the background.

<br /> Captures video at OBS Studio, and overlay the videos as follow while keying out (making transparent) the green parts:
<br /> 1. Foreground
<br /> 2. Video camera of the video
<br /> 3. Background
<br /> The resulting video is the Mixed Reality using Unreal Engine 4.

<br /> ※Depending on the video camera, you will need to correct the distortion of the video. Please add extension settings for the camera you use to make it easier for everyone!
