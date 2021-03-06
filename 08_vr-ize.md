# Getting Started with the Oculus Rift SDK
At this point, our game is playable and in theory is ready to go - by default, Unity allows you to export your game project in several formats for desktop and mobile, but we want to add an additional layer to it that allows us to build out our environment and make it fully immersive using the Oculus SDK.

## Installing the Oculus SDK
The first thing that we're going to want to do here is install the SDK that Oculus provides for developing. You'll need to start by installing the tools that we need in order to utilize the in-game components that Oculus has created for VR development.

Create Oculus dev account
If you haven't already, create an Oculus developer account

Download vr tools
Download and install the Oculus developer tools


### Oculus VR: Deploying for the Rift

There are several components that we'll need to install to begin working with the Oculus SDK: we'll need to install the SDK itself, as well as the Oculus Runtime and Integration components.

Head over to the <a href="https://developer.oculus.com/downloads/"> Oculus Developer portal </a> to download the tools. We'll be using the Oculus 0.4.3 beta tools and downloading the following packages:

* Oculus Runtime for Mac OS / Windows
* Oculus SDK for Mac OS / Windows
* Unity 4 Integration

### Mobile VR: Deploying for Samsung Gear VR
If you have a Samsung Galaxy Note 4 & Gear VR headset, you can deploy your game to run on mobile with the Oculus Mobile SDK for Gear VR. We won't cover this in depth here, but there are several resources to get you started.

[Oculus Developer Portal Mobile SDK](https://developer.oculus.com/downloads/)

[Video: Developing for Gear VR in Unity Free](https://www.youtube.com/watch?v=0vkRtsaP3co)

[Gear VR Development Concerns](http://ralphbarbagallo.com/2014/11/13/samsung-gear-vr-development-challenges-with-unity3d/)

### Replace the main camera with the Oculus Controller & Camera Rig
After downloading the Oculus SDK and Unity 4 integration components, you will need to replace your current character controller and camera with the Oculus renderer. Luckily, this is fairly straightforward, regardless of which option you're deploying for, because Oculus has created prefabricated controls to use.

Import Oculus Asset Package
Import Oculus Assets

Add Character
Add the OVRCharacterController

Note: This section is out of date with the later versions of Unity, but may be similar for specialized headsets that require a new prefab object.

Because Oculus has included a prefab version of their character, changing our current maze to support the Oculus Rift simply requires swapping out our current First Person Controller for the Oculus one: the OVRPlayerController. Under the Assets tab in your project hierarchy, expand OVR -> Prefabs and drag and drop the OVRPlayerController into the scene. In the Scene Hierarchy, select your First Person Controller, right-click, and delete it - we only need one controller in this scene. Depending on your placement of the OVRPlayerController, you may need to move it up on the Y-axis slightly to keep it from falling through the bottom of your maze.

Press play to make sure that the camera is rendering correctly. You should briefly see the Oculus warning message, and your character is ready to play!
