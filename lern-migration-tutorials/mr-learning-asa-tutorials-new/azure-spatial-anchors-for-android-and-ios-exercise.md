## 8.EXERCISE:Azure Spatial Anchors for Android and iOS

In this tutorial, you will learn how to build your project to Android and iOS devices using AR Foundation, ARCore XR Plugin, and ARKit XR Plugin.

## Installing inbuilt Unity packages

Unity 202 + Windows XR Plugin

In this section, you will upgrade or install the following inbuilt packages:

ARCore XR Plugin 4.0.12 for Android support
ARKit XR plugin 4.0.12 for iOS support
add the above mentioned packages from the Unity package manager.

>[Caution]

>Not all version are compatible with MRTK and only certain version works together, so make sure you install the exact versions listed above.

>[!Tip]
>For a reminder on how to upgrade and install inbuilt packages, you can refer to the Installing inbuilt Unity packages instructions.

>[Note]

>If you are developing this project for Android, there is no need to install the ARKit XR Plugin package. Similarly, if you are developing this project for iOS, you do not need to install the ARCore XR Plugin.

Legacy WSA

In this section, you will upgrade or install the following inbuilt packages:

* XR Legacy Input Helpers 2.1.6
* ARCore XR Plugin 3.1.3 for Android support
* ARKit XR plugin 3.1.3 for iOS support

add the above mentioned packages from the Unity package manager.

>[Caution]

>Not all version are compatible with MRTK and only certain version works together, so make sure you install the exact versions listed above.

>[Tip]
>For a reminder on how to upgrade and install inbuilt packages, you can refer to the Installing inbuilt Unity packages instructions.

 >[Note]

>If you are developing this project for Android, there is no need to install the ARKit XR Plugin package. Similarly, if you are developing this project for iOS, you do not need to install the ARCore XR Plugin.

## Configure MRTK for AR Foundation Camera

In this section, you will learn how to configure MRTK for deploying to a mobile device.

In the Hierarchy window, select the **MixedRealityToolkit** object. Then in the Inspector window, select the **Camera** tab, clone the camera profile, and give it a suitable name, for example, **AzureSpatialAnchors_ARCameraProfile**:

![](images/mr-learning-asa/asa-05-section2-step1-1.png)

>[!Tip]

>For a reminder on how to clone MRTK profiles, you can refer to the Configuring the Mixed Reality Toolkit profiles instructions.

With the **Camera** tab still selected in the Inspector window, expand the **Camera Setting** Providers and by clicking the "-" remove the **Windows Mixed Reality Camera Setting** or **XR SDK Windows Mixed Reality Camera Setting**:
![](images/mr-learning-asa/asa-05-section2-step1-2.png)
and click the + **Add Camera Setting Provider** button, then expand the newly added **New data provider**:
![](images/mr-learning-asa/asa-05-section2-step1-3.png)
Using the **Type** dropdown, change the type to **Microsoft.MixedReality.Toolkit.Experimental.UnityAR** > **UnityARCameraSettings**:
![](images/mr-learning-asa/asa-05-section2-step1-4.png)
Update the MRTK UnityAR scripting defines by invoking the menu item: Mixed Reality > Toolkit > Utilities > **UnityAR** > Update Scripting Defines

## Building your application to your Android device

In this section, you will learn how to configure your project to build and deploy it to an Android device.

In the Unity menu, select **File** > **Build Settings**... to open the Build Settings window and then switch the platform to Android:
![](images/mr-learning-asa/asa-05-section3-step1-1.png)

>[!Tip]

>For a reminder on how to switch build platform, you can refer to the Switching the build platform instructions.

Close the Build Settings window.

In the Unity menu, select **Mixed Reality** > **Toolkit** > **Utilities** > **Configure Project for MRTK** to open the **MRTK Project Configurator** window, ensure all options are selected, then click the **Apply** button to apply the settings:
![](images/mr-learning-asa/asa-05-section3-step1-2.png)
In the Unity menu, select **Edit** > **Project Settings**... to open the Player Settings window, then locate the **Player** > **Other Settings** section, select **Vulkan** and remove it by clicking the "-" symbol:
![](images/mr-learning-asa/asa-05-section3-step1-2-1.png)

Unity 2020 + Windows XR Plugin
In the Unity menu, select Edit > Project Settings... > XR Plug-in management, check the ARcore checkbox.
![](images/mr-learning-asa/asa-05-section3-step1-3.png)
In the Build Settings window, click the **Add Open Scenes** button to add your current scene to the **Scenes In Build** list. Then, use a USB cable, connect your Android device to your computer and select it from the **Run Device** dropdown:
******image******

>[!Note]

>If your device does not appear in the Run Device dropdown, you might need to press the Refresh button next to the dropdown.

In the Build Settings window, click the **Build And Run** button to open the Build Android window.

Choose a suitable location to store your build, for example, D:\MixedRealityLearning\Builds, then give the apk a suitable name, for example, MRTKTutorials-AzureSpatialAnchors, and click the **Save** button to start the build process:
![](images/mr-learning-asa/asa-05-section3-step1-5.png)

>[Note]

>If you get any error in the Unity Console window related to Android SDK, NDK, or JDK modules, you need to open Unity Hub and install the associated Android Build Support modules.

When the build process is complete, your apps should automatically load on your Android device.

Legacy WSA
In the Unity menu, select **Edit** > **Project Settings**... >**Player**> **XR Setting**, make sure you are in Android platform and check the **Virtual Reality Supported** checkbox then click the + icon, and select None:
![Close the Player Settings window and open the Build Settings window again.](images/mr-learning-asa/asa-05-section3-step1-2-1.png)

In the Build Settings window, click the **Add Open Scenes** button to add your current scene to the **Scenes In Build** list. Then, use a USB cable, connect your Android device to your computer and select it from the **Run Device** dropdown:
![](images/mr-learning-asa/asa-05-section3-step1-4.png)

 >[Note]

>If your device does not appear in the Run Device dropdown, you might need to press the Refresh button next to the dropdown.

In the Build Settings window, click the **Build And Run** button to open the Build Android window.

Choose a suitable location to store your build, for example, D:\MixedRealityLearning\Builds, then give the apk a suitable name, for example, MRTKTutorials-AzureSpatialAnchors, and click the **Save** button to start the build process:
![](images/mr-learning-asa/asa-05-section3-step1-5.png)

>[Note]

>If you get any error in the Unity Console window related to Android SDK, NDK, or JDK modules, you need to open Unity Hub and install the associated Android Build Support modules.

When the build process is complete, your apps should automatically load on your Android device.

## Building your application to your iOS device

In this section, you will learn how to configure your project, to build and deploy it to your iOS device.

In the Unity menu, select **File** > **Build Settings**... to open the Build Settings window and switch platform to iOS:
![](images/mr-learning-asa/asa-05-section4-step1-1.png)

 >[Tip]

>For a reminder on how to switch build platform, you can refer to the Switching the build platform instructions.

Close the Build Settings window.

In the Unity menu, select **Mixed Reality** > **Toolkit** > **Utilities** > **Configure Project** for MRTK to open the **MRTK Project Configurator** window, ensure all options are selected, then click the **Apply** button to apply the settings:
![](images/mr-learning-asa/asa-05-section4-step1-2.png)

Unity 2020 + Windows XR Plugin 

In the Unity menu, select **Edit** > **Project Settings**... > **XR Plug-in management**, check the ARKit checkbox.



In the Unity menu, select **Edit** > **Project Settings**... to open the Player Settings window, then locate the **Player** > **Other Settings** section, uncheck the **Strip Engine Code** checkbox to disable it:
![](images/mr-learning-asa/asa-05-section4-step1-3.png)

Close the Player Settings window and open the **Build Settings** window again.

In the Build Settings window, click the **Add Open Scenes** button to add your current scene to the **Scenes In Build** list:
![](images/mr-learning-asa/asa-05-section4-step1-4.png)
In the Build Settings window, click the **Build** button to open the Build iOS window.

Choose a suitable location to store your Xcode project, for example, D:\MixedRealityLearning\Builds, create a new folder and give it a suitable name, for example, MRTKTutorials-AzureSpatialAnchors, and then click the **Select Folder** button to start the build process:
![](images/mr-learning-asa/asa-05-section4-step1-5.png)
When the build process is complete, follow the [Export the Xcode project](../../) instructions to learn to deploy your Xcode project to your iOS device.





