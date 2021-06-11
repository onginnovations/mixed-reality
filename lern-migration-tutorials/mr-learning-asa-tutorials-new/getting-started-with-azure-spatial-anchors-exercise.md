## 3. Exercise: Getting started with Azure Spatial Anchors
In this tutorial, you will explore the various steps required to start and stop an Azure Spatial Anchors session and to create, upload, and download Azure Spatial Anchors on a single device.

## Creating and preparing the Unity project
In this section, you will create a new Unity project and get it ready for MRTK development.

First, follow the [Initializing your project and deploying your first application](../../), excluding the Build your application to your device instructions, which includes the following steps:

1. [Creating the Unity project](../../) and give it a suitable name, for example, MRTK Tutorials
2. [Switching the build platform](../../)
3. [Importing the TextMeshPro Essential Resources](../../)
4. [Importing the Mixed Reality Toolkit and Configuring the Unity project](../../)
5. [Creating and configuring the scene](../../) and give the scene a suitable name, for example, AzureSpatialAnchors

Then follow the Changing the Spatial Awareness Display Option instructions to ensure the MRTK configuration profile for your scene is DefaultHoloLens2ConfigurationProfile and change the display options for the spatial awareness mesh to Occlusion.

Installing inbuilt Unity packages and Importing the tutorial assets

Unity 2020 + Open XR

In the Unity menu, select **Window** > **Package Manager**  to open the Package Manager window, then verify that **AR Foundation** > **4.1.7** version is installed.
![install package through package manager](images/mr-learning-asa/asa-02-section2-step1-1.png)



Unity 2020 + Windows XR Plugin

In the Unity menu, select **Window** > **Package Manager** to open the Package Manager window, then select **AR Foundation** > **4.0.12** version and click the Install button to install the package:
![install package ](images/mr-learning-asa/asa-02-)

Legacy WSA
In the Unity menu, select Window > Package Manager to open the Package Manager window, then select AR Foundation > 3.1.3 version and click the Install button to install the package:
![install package ](images/mr-learning-asa/asa-02-)

## Importing the tutorial assets
Add AzurespatialAnchors SDK V2.10 to your project, to add the packages please follow this tutorial

Download and **import** the following Unity custom packages in the order they are listed:

* MRTK.HoloLens2.Unity.Tutorials.Assets.GettingStarted.2.4.0.unitypackage
* MRTK.HoloLens2.Unity.Tutorials.Assets.AzureSpatialAnchors.XRplugginManagement.2.5.3.unitypackage
After you have imported the tutorial assets your Project window should look similar to this:
![install package ](images/mr-learning-asa/asa-02-section3-step1-1.png)

>![Note]
> If you see any CS0618 warnings regarding 'WorldAnchor.SetNativeSpatialAnchorPtr(IntPtr)' is obsolete, you can ignore these warnings.

>![Tip]
>For a reminder on how to import a Unity custom package, you can refer to the [Importing the tutorial assets instructions](../../).

## Preparing the scene
In this section, you will prepare the scene by adding some of the tutorial prefabs.

In the Project window, navigate to the **Assets** > **MRTK.Tutorials.AzureSpatialAnchors** > **Prefabs** folder, then click-and-drag the following prefabs into the Hierarchy window to add them to your scene:

**ButtonParent** prefabs
**DebugWindow** prefabs
**Instructions** prefabs
**ParentAnchor** prefabs
![Prefabs ](images/mr-learning-asa/asa-02-section4-step1-1.png)
>![Tip]
>If you find the large icons in your scene, for example, the large framed 'T' icons distracting, you can hide these by <a herf = " ">toggling the Gizmos</a> to the off position, as shown in the image above.

Select **MixedRealityToolkit** object in the Hierarchy window, use the **Add Component** button in the Inspector window to add the following components:

AR Anchor Manager (Script)
DisableDiagnosticsSystem (Script)
![Prefabs ](images/mr-learning-asa/asa-02-section5-step1-1.png)

>![Warning]
>There is a known issue with ASA v2.9.0 and v2.10.0-preview.1 that requires two additional objects to be placed in the scene. Please use the Add Component button in the inspector window to add an AR Camera Manager (Script) and an AR Session (Script) to the **MixedRealityToolkit** object. Be sure to disable the Camera that is created automatically while adding the AR Camera Manager (Script) by unchecking the checkbox next to the Camera object in the inspector window. This issue will be addressed in the full release of ASA v2.10.0.

>![Note]
>When you add the AR Anchor Manager (Script) component, the AR Session Origin (Script) component is automatically added because it is required by the AR Anchor Manager (Script) component.

## Configuring the buttons to operate the scene
In this section, you will add scripts to the scene to create a series of button events that demonstrate the fundamentals of how both local anchors and Azure Spatial Anchors behave in an app.

In the Hierarchy window, expand the **ButtonParent** object and select the first child object named **StartAzureSession**, in the Inspector window, configure the **Button Config Helper (Script)** component's **On Click ()** event as follows:

* Assign the **ParentAnchor** object to the **None (Object)** field
From the **No Function** dropdown, select **AnchorModuleScript** > **StartAzureSession** () to set this function as the action to be executed when the event is triggered
![Unity with StartAzureSession button OnClick event configured](images/mr-learning-asa/asa-02-section5-step1-2.png)



In the Hierarchy window, select the next button named **StopAzureSession**, then in the Inspector window, configure the **Button Config Helper (Script)** component's **On Click ()** event as follows:

Assign the **ParentAnchor** object to the **None (Object)** field
From the **No Function** dropdown, select **AnchorModuleScript** > **StopAzureSession** () to set this function as the action to be executed when the event is triggered
![Unity with StopAzureSession button OnClick event configured](images/mr-learning-asa/asa-02-section5-step1-3.png)



In the Hierarchy window, select the next button named **CreateAzureAnchor**, then in the Inspector window, configure the **Button Config Helper(Script)** component's **On Click ()** event as follows:

Assign the **ParentAnchor** object to the **None (Object)** field
From the **No Function** dropdown, select **AnchorModuleScript** > **CreateAzureAnchor** () to set this function as the action to be executed when the event is triggered
Assign the **ParentAnchor** object to the empty **None (Game Object)** field to make it the argument for the **CreateAzureAnchor ()** function
![Unity with CreateAzureAnchor button OnClick event configured](images/mr-learning-asa/asa-02-section5-step1-4.png)




In the Hierarchy window, select the next button named **RemoveLocalAnchor**,then in the Inspector window, configure the **Button Config Helper (Script)** component's **On Click ()** event as follows:

* Assign the **ParentAnchor*8 object to the **None (Object)** field
From the **No Function** dropdown, select **AnchorModuleScript** > **RemoveLocalAnchor** () to set this function as the action to be executed when the event is triggered
* Assign the **ParentAnchor** object to the empty **None (Game Object)** field to make it the argument for the **RemoveLocalAnchor** () function
Unity with **RemoveLocalAnchor** button **OnClick** event configured
![Unity with CreateAzureAnchor button OnClick event configured](images/mr-learning-asa/asa-02-section5-step1-5.png)


In the Hierarchy window, select the next button named **FindAzureAnchor**,then in the Inspector window, configure the **Button Config Helper (Script)** component's **On Click ()** event as follows:

* Assign the **ParentAnchor** object to the **None (Object)** field
From the No Function dropdown, select **AnchorModuleScript** > **FindAzureAnchor** () to set this function as the action to be executed when the event is triggered
![Unity with FindAzureAnchor button OnClick event configured](images/mr-learning-asa/asa-02-section5-step1-6.png)




In the Hierarchy window, select the next button named **DeleteAzureAnchor**, then in the Inspector window, configure the **Button Config Helper (Script)** component's **On Click** () event as follows:

* Assign the **ParentAnchor** object to the **None (Object)** field
* From the No Function dropdown, select **AnchorModuleScript** > **DeleteAzureAnchor** () to set this function as the action to be executed when the event is triggered
![Unity with DeleteAzureAnchor button OnClick event configured](images/mr-learning-asa/asa-02-section6-step1-1.png)



## Connecting the scene to the Azure resource
In the Hierarchy window, select the **ParentAnchor** object, then in the Inspector window, locate the **Spatial Anchor Manager** (Script) component. Configure the **Credentials** section with the credentials from the Azure Spatial Anchors account created as part of the [Prerequisites](../../) for this tutorial series:


* In the **Spatial Anchors Account ID** field, paste the **Account ID** from your Azure Spatial Anchors account
* In the **Spatial Anchors Account Key** field, paste the primary or secondary **Access Key** from your Azure Spatial Anchors account
In the **Spatial Anchors Account Domain** field, paste the **Account Domain** from your Azure Spatial Anchors account
![Unity with Spatial Anchor Manager configured](images/mr-learning-asa/asa-02-section7-step1-1.png)




## Trying the basic behaviors of Azure Spatial Anchors
Azure Spatial Anchors can not run in Unity, so to test the Azure Spatial Anchors functionality, you need to build the project and deploy the app to your device.

 >![Tip]

>For a reminder on how to build and deploy your Unity project to HoloLens 2, you can refer to the Building your application to your HoloLens 2 instructions.

When the app runs on your device, follow the on-screen instructions displayed on the Azure Spatial Anchor Tutorial Instructions panel:

1. Move the cube to a different location
2. Start Azure Session
3. Create Azure Anchor (creates an anchor at the location of the cube).
4. Stop Azure Session
5. Remove Local Anchor (allows the user to move the cube)
6. Move the cube somewhere else
7. Start Azure Session
8. Find Azure Anchor (positions the cube at the location from step 3)
9. Delete Azure Anchor
10. Stop Azure session
![Unity with Instructions object selected
](images/mr-learning-asa/asa-02-section7-step1-1.png)


 >![Caution]

>Azure Spatial Anchors uses the internet to save and load the anchor data, so make sure your device is connected to the internet.

## Anchoring an experience
In the previous sections, you learned the fundamentals of Azure Spatial Anchors. We used a cube to represent and visualize the parent game object with the attached anchor. In this section, you will learn how to anchor an entire experience by placing it as a child of the ParentAnchor object.

In the Hierarchy window, select the **ParentAnchor** object, then in the Inspector window, configure the Transform components as follows:

Change **Scale X** to 1.1
Change **Scale Z** to 1.1
![Unity with ParentAnchor object selected, positioned, and scaled
](images/mr-learning-asa/asa-02-section8-step1-1.png)



In the Project window, navigate to the **Assets** > **MRTK.Tutorials.GettingStarted** > **Prefabs** > **Rover** folder, then click-and-drag the **RoverExplorer_Complete** prefab into the Hierarchy window to add it to the scene:
![Unity with newly added RoverExplorer_Complete prefab selected
](images/mr-learning-asa/ asa-02-section8-step1-2.png)




With the newly added RoverModule_Complete object still selected in the Hierarchy window, drag it onto the **ParentAnchor** object to make it a child of the ParentAnchor object:
![Unity with RoverExplorer_Complete object set as child of ParentAnchor
](images/mr-learning-asa/asa-02-section8-step1-3.png)




If you now rebuild the project and deploy the app to your device, you can now reposition the entire Rover Explorer experience by moving the resized cube.

 >![Tip]

>A variety of user experience flows for repositioning experiences, including the use of a repositioning object (such as the cube used in this tutorial), the use of a button to toggle a bounds control that surrounds the experience, the use of position and rotation gizmos, and more.
