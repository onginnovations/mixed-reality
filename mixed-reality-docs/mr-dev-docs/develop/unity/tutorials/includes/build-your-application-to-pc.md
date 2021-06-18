# [Unity 2020 + OpenXR](#tab/openxr)

### 1. Switching Build Platform

In the Unity menu, select File > Build Settings to open the Build Settings window.

In the Build Settings window, select **PC, Mac & Linux Standlone** Platform and click the Switch Platform button:

![Switching Build Platform](../images/mrlearning-pc-holographic-remoting/Tutorial2-Section2-Step4-1.png)

When Unity has finished switching the platform, click the red x icon to close the Build Settings window.

### 2. Set the project settings

In the Unity menu, select Edit > Project Settings > XR Plug-in Management > switch to PC, Mac & Linux Standlone tab and set the **OpenXR** and **Windows Mixed Reality feature set** checkbox.

![Enable OpenXR and Windows Mixed Reality feature set](../images/mrlearning-pc-holographic-remoting/Tutorial2-Section2-Step4-2.png)

In Project Settings, select OpenXR > switch to PC, Mac & Linux Standlone tab and change the Depth submission mode from None to **Depth 16 Bit** and in interaction profiles add **Eye Gaze Interaction Profile** and **Microsoft Hand Interaction Profile** by clicking on the + symbol.

![Add Eye Gaze Interaction Profile and Microsoft Hand Interaction Profile](../images/mrlearning-pc-holographic-remoting/Tutorial2-Section2-Step4-3.png)

Under Open XR feature groups > All features > Set the **Holographic App Remoting** checkbox.

![Enable Holographic App Remoting](../images/mrlearning-pc-holographic-remoting/Tutorial2-Section2-Step4-4.png)

And also under Open XR feature groups, set Windows Mixed Reality and **Holographic App Remoting** checkbox.

![Enable Windows Mixed Reality Holographic App Remoting](../images/mrlearning-pc-holographic-remoting/Tutorial2-Section2-Step4-5.png)

### 3. Build the Unity Project

In the Unity menu, select File > Build Settings to open the Build Settings window.

In the Build Settings window, click the ***Add Open Scenes*** button to add your current scene to the Scenes. In the Build list, then click the ***Build button*** to open the PC, Mac & Linux Standlone platform window:

![Unity Build Settings window with scene added](../images/mrlearning-pc-holographic-remoting/Tutorial2-Section2-Step4-6.png)

In the Build PC, Mac & Linux Standlone platform window, choose a suitable location to store your build, for example, Documents\MixedRealityLearning. Create a new folder and give it a suitable name, for example, PCHolographicRemoting. Then click the ***Select Folder*** button to start the build process:

![Unity Build Settings window with Select Folder prompt window](../images/mrlearning-pc-holographic-remoting/Tutorial2-Section2-Step4-7.png)

Wait for Unity to finish the build process.

![Unity build process in progress](../images/mrlearning-pc-holographic-remoting/Tutorial2-Section2-Step4-8.png)

# [Legacy WSA](#tab/wsa)

### 1. Set the player settings

In the **XR Settings** section, select the **WSA Holographic Remoting Supported** checkbox and enable the Holographic Remoting.

![Unity XR Settings window with WSA Holographic Remoting Supported enabled](../images/mrlearning-pc-holographic-remoting/Tutorial2-Section2-Step1-1.png)

### 2. Build the Unity Project

In the Unity menu, select File > Build Settings to open the Build Settings window.

In the Build Settings window, click the ***Add Open Scenes*** button to add your current scene to the Scenes. In the Build list, then click the ***Build button*** to open the Build Universal Windows Platform window:

![Unity Build Settings window with scene added](../images/mrlearning-pc-holographic-remoting/Tutorial2-Section2-Step2-1.png)

In the Build Universal Windows Platform window, choose a suitable location to store your build, for example, Documents\MixedRealityLearning. Create a new folder and give it a suitable name, for example, PCHolographicRemoting. Then click the ***Select Folder*** button to start the build process:

![Unity Build Settings window with Select Folder prompt window](../images/mrlearning-pc-holographic-remoting/Tutorial2-Section2-Step2-2.png)

Wait for Unity to finish the build process.

![Unity build process in progress](../images/mrlearning-pc-holographic-remoting/Tutorial2-Section2-Step2-3.png)

### 3. Build and deploy the application

When the build process is completed, Unity will prompt Windows File Explorer to open the location you stored the build. Navigate inside the folder, and double-click the .sln file to open it in Visual Studio:

![Windows Explorer with newly created Visual Studio Solution selected](../images/mrlearning-pc-holographic-remoting/Tutorial2-Section2-Step3-1.png)

> [!NOTE]
> If Visual Studio asks you to install new components, take a moment to ensure that all prerequisite components are installed as specified in the Install the Tools documentation.

Configure Visual Studio for PC by selecting the Release configuration, the x64 architecture, and Local Machine as target:

![Visual Studio configured for Local Machine](../images/mrlearning-pc-holographic-remoting/Tutorial2-Section2-Step3-2.png)

Click the button that says ***Local Machine***. It starts to build and deploy the application on to your PC. The application will be installed in your PC by default.
