
## 2. Getting started with PC Holographic Remoting-Exercise

Welcome to the HoloLens 2 tutorials. In this two-part tutorial series, you will learn how to create a mixed reality experience demonstration and how to create a PC app for Holographic Remoting.

In this tutorial, you'll learn how to create a mixed reality experience. It will demonstrate UI elements, 3D model manipulation, model clipping, and eye-tracking features.

In the second tutorial, Create a Holographic Remoting application, you will learn how to create a PC app for Holographic Remoting. And connect to HoloLens 2 at any point, providing a way to visualize 3D content in mixed reality.

We strongly recommend completing the Getting started tutorials series or some basic prior experience with Unity and MRTK before continuing.

>[! Important]
>This tutorial series supports Unity 2020 LTS(currently 2020.3.x) if you are using Open XR and Unity 2019 LTS (currently 2019.4.x) if you are using Legacy WSA This supersedes any Unity version requirements stated in the prerequisites linked above.

## Creating and preparing the Unity project

In this section, you will create a new Unity project and get it ready for MRTK development.

For this, first follow the [Initializing your project and first application](../../), excluding the [Build your application to your device](../../) instructions, which includes the following steps:

1. [Creating the Unity project](../../) and give it a suitable name, for example, MRTK Tutorials

2. [Switching the build platform](../../)

3. [Importing the TextMeshPro Essential Resources](../../)

4. [Importing the Mixed Reality Toolkit and Configuring the Unity project](../../)

5. [Creating and setting the scene](../../) and give the scene a suitable name, for example, PC Holographic Remoting.

Then follow the [Changing the Spatial Awareness Display Option](../../) instructions to change the MRTK configuration profile for your scene to the **DefaultHoloLens2ConfigurationProfile**. Change the display options for the spatial awareness mesh to **Occlusion**.

## Importing the tutorial assets

Unity 2020 + OpenXR
Download and import the <a herf=" ">MRTK.Tutorials.PCHolographicRemoting.unitypackage</a>

>[!Tip]
>For a reminder on how to import a Unity custom package, you can refer to the Importing the Mixed Reality Toolkit instructions.

After importing the tutorial assets, your Project window should look similar to this:
![](images/PC-holographic-tutorials/a.png)

Legacy WSA

Download and import the <a herf="">MRTK.Tutorials.PCHolographicRemoting.unitypackage</a>.

> [!Tip]
>For a reminder on how to import a Unity custom package, you can refer to the Importing the Mixed Reality Toolkit instructions.

After importing the tutorial assets, your Project window should look similar to this:
![](images/PC-holographic-tutorials/b.png)


## Configuring and preparing the scene
In this section, you will prepare the scene by adding some of the tutorial prefabs.

In the Project window, navigate to **Assets** > **MRTK.Tutorials.PCHolograhicRemoting** > **Prefabs** folder. While holding down the CTRL button, click on the below six prefabs.

* ButtonParent
* ClippingObjects
* HandSpatialMapButton
* Instructions
* ModelParent
* Platform
![](images/PC-holographic-tutorials/c.png)
Drag-and-drop these models from the prefabs folder into the **Hierarchy** window.
![](images/PC-holographic-tutorials/d.png)
To focus in on the objects in the scene, you can double-click on the ModelParent object, and then zoom slightly in again:
(images/)
>[!Tip]
>If you find the large icons in your scene, such as, the large framed 'T' icons distracting, you can hide these by <a herf =" ">toggling the Gizmos</a> to the off position.
## Configuring the buttons to operate the scene
In this section, you will add scripts into the scene to create button events demonstrating the fundamentals of model switching and clipping functionality.

## 1. Configuring the Interactable (Script) component
In the Hierarchy window, expand the **ButtonParent** object and select the NextButton. In the Inspector window, locate the **Interactable (Script)** component and click on + icon under **OnClick ()** event.
![](images/PC-holographic-tutorials/e.png)
With the **NextButton** object still selected in the Hierarchy window, click-and-drag the **ButtonParent** object from the Hierarchy window into the empty **None (Object)** field of the event you just added to make the ButtonParent object listen for button click event from this button:
![](images/PC-holographic-tutorials/f.png)
Click the **No Function**  dropdown of the same event. Then select ViewButtonControl > NextModel () to set the NextModel () function as the action that is triggered when the button pressed events is fired from this button:
![](images/PC-holographic-tutorials/g.png)

## 2. Configuring the remaining buttons
For each of the remaining buttons, complete the process outlined above to assign functions to the **OnClick ()** events:

For PreviousButton object, assign the **ViewButtonControl** > **PreviousModel ()** function.

For ClippingButton select **ToggleButton** > **ToggleClipping ()** function.

## 3. Configuring the View Button Control (Script) and Toggle Button (Script) components
Now your buttons are configured to demonstrate the model switching and clipping functionality. It is time to add 3D models and the clipping objects to the script.

We have provided six different 3D models for demonstration, expand the **ModelParentobject** to expose these 3D models.

With the ButtonParent object still selected in the Hierarchy window, in the Inspector window, locate the **View Button Control (Script)** component and expand the **Models** variable.

In the **Size** field, enter the number of 3D models you would like to have in your scene. In this case, it would be six. It will create fields for adding new 3D models.
![](images/PC-holographic-tutorials/h.png)
Drag and drop each child object of ModelParent Object into these fields.
![](images/PC-holographic-tutorials/i.png)
Drag and drop the **ClippingObjects** object from the Hierarchy window to the **Toggle Button (Script)** component **Clipping Object** field.

>[!Note]

>Stay in button parent object only.

![](images/PC-holographic-tutorials/j.png)
In the Hierarchy window, select the ClippingObjects prefab and enable it in the Inspector window to turn on the **Clipping objects**.

## Configuring the clipping objects to enable clipping feature

In this section, you will add MarsCuriosityRover object's child objects renderer into an individual **clipping object** to demonstrate the clipping of the MarsCuriosityRover model.

In the Hierarchy window, expand the **ClippingObjects** object to expose the three different clipping objects that you will be using in this project.

To configure the **ClippingSphere** object, click on it, and in the Inspector window, locate the **Clipping Sphere (Script)** component. Enter the number of renderers in the size field that you need to add for your 3D model. In this case, add 10 for MarsCuriosityRover child objects. It will create fields for adding renderers, drag and drop MarsCuriosityRover Object's child model objects into these fields.
![](images/PC-holographic-tutorials/k.png)
In the Hierarchy window, select the ClippingObjects prefab and enable it in the Inspector window to turn on the Clipping objects.

## Configuring the clipping objects to enable clipping feature
In this section, you will add MarsCuriosityRover object's child objects renderer into an individual clipping object to demonstrate the clipping of the MarsCuriosityRover model.

In the Hierarchy window, expand the **ClippingObjects** object to expose the three different clipping objects that you will be using in this project.



To configure the **ClippingSphere** object, click on it, and in the Inspector window, locate the **Clipping Sphere (Script)** component. Enter the number of renderers in the size field that you need to add for your 3D model. In this case, add 10 for MarsCuriosityRover child objects. It will create fields for adding renderers, drag and drop MarsCuriosityRover Object's child model objects into these fields.
![](images/PC-holographic-tutorials/l.png)
Follow the same process and add MarsCuriosityRover's child objects renderers to the **ClippingBox** and **ClippingPlane** objects.

In this tutorial, only the MarsCuriosityRover model will be used for demonstrating the clipping feature. They were adding clipping features to more models, increasing the size of the renderer, and adding their individual mesh renderers.

## Configuring eye-tracking to highlight tooltips
In this section, you will explore how to enable eye tracking in your project. For example, you will implement the functionality to highlight tooltips attached to MarsCuriosityRover's parts while looking at them and hiding them, while you are looking away from them.

## 1. Identify target objects and associated tooltips
In the Hierarchy window, select the ModelParent object. Expand the **MarsCuriosity** -> **Rover** to find five main parts of the MarsCuriosityRover: **POI-Camera, POI-Wheels, POI-Antena, POI-Spectrometer, POI-RUHF Antenna**.

* Observe five corresponding tooltip objects associated with MarsCuriosityRover parts in the Hierarchy window.
* You will be configuring these objects to highlight the experience when you look at the MarsCuriosityRover parts.
![](images/PC-holographic-tutorials/m.png)
## 2. Implement While Looking At Target () & On Look Away () events
In the Hierarchy window, select the **POI-Camera** object. In the Inspector window, locate the Eye Tracking Target (Script) component and configure the **While Looking At Target () & On Look Away ()** events as follows:

* To **None (Object)** field, assign the **POI-Camera ToolTip** object
* From **No Function** dropdown of **While Looking At Target ()**event, select **GameObject > SetActive (bool)**. Select the Checkbox under it to highlight the tooltip as the action that is triggered when you look at the target object.
![](images/PC-holographic-tutorials/n.png)
* Follow the same process and click on the **No Function** dropdown of the **On Look Away ()** event listener. Then select **GameObject > SetActive (bool)** and leave the Checkbox empty to hide the tooltip as the action that is triggered when you look away from the target object.
![](images/PC-holographic-tutorials/o.png)
Follow the same process and assign respective tooltip objects to their same MarsCuriosityRover parts While Looking At Target () & On Look Away () events.

To enable eye tracking, please follow these <a herf="">guidelines</a>.



