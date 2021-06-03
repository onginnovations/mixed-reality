# Exercise: Initializing your project and configuring MRTK profiles

In this exercise, you'll learn how to create a new Unity project, configure it for Mixed Reality Toolkit (MRTK) development, and import MRTK. You'll also walk through configuring, building, and deploying a basic Unity scene from Visual Studio to your HoloLens 2. Once you have deployed it to your HoloLens 2, you should see a spatial mapping mesh covering the surfaces that are perceived by the HoloLens. Additionally, you should see indicators on your hands and fingers for hand tracking and a frame rate counter for keeping an eye on app performance.

## Creating the Unity project

1. Launch **Unity Hub**, select the **Projects** tab, and click the **down arrow** next to the **New** button:

![Unity Hub with New button highlighted](images/mr-learning-base/base-02-section1-step1-1.png)

2. In the dropdown, select the Unity **version** specified in the [Prerequisites](introduction.md#prerequisites):

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
