# Exercise: Initializing your project and configuring MRTK profiles

In this exercise, you'll learn how to create a new Unity project, configure it for Mixed Reality Toolkit (MRTK) development, and import MRTK. You'll also walk through configuring, building, and deploying a basic Unity scene from Visual Studio to your HoloLens 2. Once you have deployed it to your HoloLens 2, you should see a spatial mapping mesh covering the surfaces that are perceived by the HoloLens. Additionally, you should see indicators on your hands and fingers for hand tracking and a frame rate counter for keeping an eye on app performance.

## Creating the Unity project

1. Launch **Unity Hub**, select the **Projects** tab, and click the **down arrow** next to the **New** button:

![Unity Hub with New button highlighted](images/mr-learning-base/base-02-section1-step1-1.png)

2. In the dropdown, select the Unity **version** specified in the [Prerequisites](beginner-mrtk-tutorials-introduction.md#prerequisites):

![Unity Hub with NEW version selector dropdown](images/mr-learning-base/base-02-section1-step1-2.png)

> [!TIP]
> If the particular Unity version is not available in Unity Hub, you can initiate the installation from Unity's <a href="https://unity3d.com/get-unity/download/archive" target="_blank">Download Archive</a>.

3. In the Create a new project window:

* Ensure **Templates** is set to **3D**
* Enter a suitable **Project Name**, for example, _MRTK Tutorials_
* Choose a suitable **Location** to store your project, for example, _D:\MixedRealityLearning_
* Click the **Create** button to create and launch your new Unity project

![Unity Hub with Create a new project window filled out](images/mr-learning-base/base-02-section1-step1-3.png)

> [!CAUTION]
> When working on Windows, there is a MAX_PATH limit of 255 characters. Consequently, you should save the Unity project close to the root of the drive.

Wait for Unity to create the project:

![Unity create new project in progress](images/mr-learning-base/base-02-section1-step1-4.png)

## Switching the build platform

[!INCLUDE[](includes/switching-build-platform.md)]

## Importing the TextMeshPro Essential Resources

1. In the Unity menu, select **Window** > **TextMeshPro** > **Import TMP Essential Resources** to open the Import Unity Package window:

![Unity Import TMP Essential Resources menu path](images/mr-learning-base/base-02-section3-step1-1.png)

2. In the Import Unity Package window, click the **All** button to ensure all the assets are selected, then click the **Import** button to import the assets:

![Unity TMP Essential Resources import window](images/mr-learning-base/base-02-section3-step1-2.png)

## Importing the Mixed Reality Toolkit and Configuring the Unity project

To Import Mixed Reality Toolkit into the Unity Project you will have to use Mixed Reality Feature Tool which allows developers to discover, update, and add Mixed Reality feature packages into Unity projects. You can search packages by name or category, see their dependencies, and even view proposed changes to your projects manifest file before importing.

1. Open the executable file **MixedRealityFeatureTool** from the downloaded folder to launch the Mixed Reality Feature Tool.

![Opening MixedRealityFeatureTool](images/mr-learning-base/base-02-section4-step1-1.png)

[!INCLUDE[](includes/importing-mrtk.md)]

## Creating the scene and configuring MRTK

1. In the Unity menu, select **File** > **New Scene**:
