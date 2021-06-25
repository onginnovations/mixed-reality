## 5.Exercise :Creating a Holographic Remoting PC application

In this tutorial, you will learn how to create a PC app for Holographic Remoting and connect to HoloLens 2 at any point, providing a way to visualize 3D content in mixed reality.

## Configuring the capabilities
In the Project Settings window, expand the **Publishing Settings**, scroll down to the Capabilities section and select the below-shown capability checkbox in addition to the existing capabilities.

* Internet Clint server
* Private Network Client Server
(images/)

Unity 2020+OpenXR
## Configuring your scene for Holographic Remoting
In this section, you will configure your project to stream your Mixed Reality experience to your HoloLens 2 device from your PC in real-time over a Wi-Fi connection.

In the Project window, navigate to the **Assets > MRTK.Tutorials.PCHolograhicRemoting > Prefabs** folder, and click and drag **HolographicRemoting** prefab into your scene.
(images/)

Legacy WSA
## Configuring your scene for Holographic Remoting
In this section, you will configure your project to stream your Mixed Reality experience to your HoloLens 2 device from your PC in real-time over a Wi-Fi connection.

In the Project window, navigate to the **Assets > MRTK.Tutorials.PCHolograhicRemoting > Prefabs** folder, and click and drag **HolographicRemoting** prefab into your scene.
(images/)

## Build your application to PC

Unity 2020+ OpenXR

Your Holographic Remoting app is now ready to build on your PC. Follow the below steps and make these changes to build this application on to your PC.
(images/)
When Unity has finished switching the platform, click the x icon to close the Build Settings window.

## 2. Set the project settings
In the Unity menu, select **Edit > Project Settings > XR Plug-in Management** ensure that you are in Windows Standalone tab and check the **OpenXR** and **Windows Mixed Reality feature** set checkbox.
(images/)

In Project Settings window, select **OpenXR** and ensure that you are in Windows Standalone tab and change the **Depth submission mode** from None to **Depth 16** Bit.

In interaction profiles tab add **Eye Gaze Interaction Profile**and **Microsoft Hand Interaction Profile** by clicking on the + symbol.
(images/)
Under **Open XR feature groups > All features** > check the Holographic App Remoting checkbox.
(images/)
next select the **Windows Mixed Reality** check box and under Windows Mixed Reality group select the **Holographic App Remoting** checkbox.
(images/)
## 3. Build the Unity Project
In the Unity menu, select File > Build Settings to open the Build Settings window.

In the Build Settings window, click the **Add Open Scenes** button to add your current scene to the Scenes. In the Build list, then click the **Build** button:
(images/)
choose a suitable location to store your build, for example, Documents\MixedRealityLearning. Create a new folder and give it a suitable name, for example, PCHolographicRemoting. Then click the Select Folder button to start the build process:
(images/)
Wait for Unity to finish the build process.
(images/)
double click on the Executable file to open the PC Holographic Remoting Application in your PC.

 >[!Note]

>Due to some known issues in Holographic Remoting for PC app Built as UWP we are Building the PC App as Windows Standalone for OpenXR.

Legacy WSA
## 1. Set the player settings
In the **XR Settings** section, select the **WSA Holographic Remoting Supported** checkbox and enable the Holographic Remoting.
(images/)

## 2. Build the Unity Project
In the Unity menu, select File > Build Settings to open the Build Settings window.

In the Build Settings window, click the **Add Open Scenes**button to add your current scene to the Scenes. In the Build list, then click the **Build** button to open the Build Universal Windows Platform window:
(images/)

In the Build Universal Windows Platform window, choose a suitable location to store your build, for example, Documents\MixedRealityLearning. Create a new folder and give it a suitable name, for example, PCHolographicRemoting. Then click the **Select Folder** button to start the build process:
(images/)

Wait for Unity to finish the build process.
(images/)

## 3. Build and deploy the application
When the build process is completed, Unity will prompt Windows File Explorer to open the location you stored the build. Navigate inside the folder, and double-click the .sln file to open it in Visual Studio:
(images/)
 >[!Note]
>If Visual Studio asks you to install new components, take a moment to ensure that all prerequisite components are installed as specified in the Install the Tools documentation.

Configure Visual Studio for PC by selecting the Release configuration, the x64 architecture, and Local Machine as target:
(images/)
Click the button that says Local Machine. It starts to build and deploy the application on to your PC. The application will be installed in your PC by default.

## Testing Holographic Remoting remote application
To connect your PC application to your HoloLens 2, follow the below process:

## 1. Install the Remoting Player application on HoloLens 2 device
* On your HoloLens 2, visit the Store app and search for **"Remoting Player."**
* Select the **Remoting Player** app.
* Tap **Install** to download and install the app.

## 2. Connect the Holographic remoting PC app to the Remoting Player
* Start the **Remoting Player** on your HoloLens.
* Take note of the HoloLens **IP address**. It will be displayed as a hologram by the **Remoting Player** as soon as it launches.
* Open the Holographic Remoting PC application on your PC.
* Once the application is launched, enter the **IP address** and click on the **Connect** button to connect.