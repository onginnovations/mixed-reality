# [Unity 2020 + OpenXR](#tab/openxr)


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
