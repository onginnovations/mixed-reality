# 2. Initializing your project and configuring MRTK profiles

To create an immersive experience for Windows Mixed Reality, you'll have to configure your unity project to support Windows Mixed Reality development. Initializing your project for Windows Mixed Reality development is a manual process. All the steps must be carried out whenever you create a new project or open the project shared with you. Your application will do the basic holographic rendering and spatial input once the project is initialized and configured. In this module, you'll be able to understand the need for configuring Unity before Windows Mixed Reality development.

## Universal Windows Platform (UWP)

Universal Windows Platform is a computing platform for Windows Mixed Reality development. Apps developed on Universal Windows Platform run on Windows 10, Windows 10 mobile, Xbox One, and HoloLens without rewriting the code for each. Your unity project must be set to export apps as Universal Windows Platform apps to target Windows Mixed Reality. However, if you wish to export your apps specific to devices, you can change the settings to Target Device.

## TextMesh Pro

Some of the MRTK assets and prefabs require TextMesh Pro. TextMesh Pro is Unity’s text component. TextMesh Pro helps in dynamically changing the appearance by directly changing the material properties. It uses custom shaders and advanced text rendering techniques to deliver visual quality improvements. TextMesh Pro must be added to your project through importing TMP Essential Resources.

## MRTK Unity Foundational Package

MRTK provides you with various packages that make it easy for you to have a smooth Mixed Reality development experience. Among the packages provided by MRTK, the Mixed Reality Toolkit Foundational Package must be customized and imported to use MRTK in your project.  The latest version of the packages is found in the Mixed Reality Feature Tool. Mixed Reality Toolkit Foundational Package comprises a set of code that enables your application to utilize standard functionalities across Mixed Reality platforms. You can import the Foundational Package of version 2.5.x or higher.

After MRTK is added to the scene and configured. You will see two new objects in your scene hierarchy window:

* MixedRealityToolkit
* MixedRealityPlayspace

The MixedRealityToolkit object contains the toolkit itself, which can be customized. The MixedRealityPlayspace object ensures the hardware like controllers/headsets and other required systems are managed accurately in the scene.

Parenting the MixedRealityPlayspace to the Main Camera helps the developers understand what is happening in the scene before entering the play mode.

## XR Plugin Management

Unity introduced XR Plugin architecture to enable developers to access common features across available AR and VR devices. Windows XR Plugin helps in accessing mixed reality features on HoloLens 2 and Windows Mixed Reality headsets. It is efficiently supported in Unity 2020, but has some incompatibilities with Azure Spatial Anchors in Unity 2019 version.

## Audio Spatializer

Imagine you hear a voice from a distant source, your brain unconsciously interprets the change in frequency to tell if an object is in front of, behind or even below or above us. To include this effect in your application you can make use of the Audio Spatializer. It enhances the way audio travels from the audio source to the surrounding space. Based on the distance and the angle between the AudioSource and AudioListener, the gains on the left and right ear are calculated. Customizing Audio Spatializer property is optional but a preferred step.

## Stabilizing Holograms

To achieve better hologram stability from the perception of the user, Depth Buffer Sharing should be enabled. By turning this on, Unity will share the depth map produced by your app with the Windows Mixed Reality platform. The platform will then be able to better optimize hologram stability specifically for your scene for any given frame being rendered by your app.

With regards to performance, selecting the 16-bit depth format compared to 24-bit will significantly reduce the bandwidth requirements as less data will need to be moved/processed.

## MRTK Configuration Profile

One of the ways to configure MRTK is through its profiles available in the Foundation Package. Profiles control the behavior of MRTK core components. The MixedRealityToolkit object is attached with an active profile which is visible in the Inspector window. By default the DefaultMixedRealityToolkitConfigurationProfile is preselected. The DefaultMixedRealityToolkitConfigurationProfile serves general use cases; to support a more specific one, you can choose an appropriate MRTK Profile in the dropdown.

The MRTK profile is a tree of nested profiles that make up the configuration information for how the MRTK systems and features should be initialized. The top-level Profile, the Configuration Profile, contains nested profiles for each of the primary core systems. Each nested Profile is designed to configure the behavior of their corresponding system.

To retain a common ground, the default MRTK profiles can not be modified. These profiles must be cloned to be able to make changes. Cloning an MRTK Profile is just creating a copy of the Profile where you can edit the underlying properties. To modify the sub-profiles settings, you must also clone the sub-profiles.

## Spatial Awareness

You might have a holographic character or avatar sit on a chair in your room during a game. To achieve this, you will need the spatial understanding module to find the part of a room that is a sitting surface. MRTK's spatial mapping module provides you with the resources you need to include your project's spatial mapping capabilities. Spatial mapping uses the sensors on a Mixed Reality headset to create a virtual map of the physical surroundings. The MRTK provides resources to use this map or mesh to hide or occlude objects behind the mesh, interact with the mesh, and visualize it.

[Next](exercise-initializing-your-project-and-configuring-mrtk-profiles.md)
