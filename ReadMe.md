# UE4 MixedReality Plugin

## Supported UE4 version

Unreal Engine 4.14.x

## Preparation
・HTC vive
・One additional Vive Controller (3 in all)
・Capture board
・Video Camera
・Camera Rig
・The Unreal Engine 4.12.5 download from GitHub
・Install OBS Studio
## Introduction
Please unzip the . Please copy the resulting "Engine" folder over the Engine folder in the Unreal Engine 4.14 acquired from GitHub, then Build using Visual Studio 2015. 
When you want to use it, add the following in the DefaultEngine.ini file of the project you want to use it in.

[SteamVR.Settings]
WindowMirrorMode=3

## How to run the sample
Open the folder "MixedRealitySample".
Right-click on the "MixedRealitySample.uproject", please select "Switch Engine Version". Specify the engine version you have built during the Introduction step.

This sample contains the following features.
・BP_VRCapture2D
The BP class to synchronize the third controller and the video camera.
・ForwardPost
Post effects to get the foreground by calculating the distance from the camera to the HMD.
・MPC_
Materials collection, the "SearchDepth" is set to the distance from camera to HMD.


Please enable the RenderCustomDepthPass for objects that you want to display in the foreground.


Please enter the offset between the controller and the camera for the camera position to be correctly in the VR space.

When you run a VR preview foreground and background will be shown on the 4 split screen as below:

The upper left corner is the greened screen foreground, and lower right corner is the background.

Captures video at OBS Studio, and overlay the videos as follow while keying out (making transparent) the green parts:
1. Foreground
2. Video camera of the video
3. Background
The resulting video is the Mixed Reality using Unreal Engine 4.

※Depending on the video camera, you will need to correct the distortion of the video. Please add extension settings for the camera you use to make it easier for everyone!
