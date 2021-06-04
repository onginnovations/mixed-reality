# User Interface and interaction models

The key to the success of the application lies in its user interface. It is the first layer of the encounter between your application and the user; creating a good impact through the user interface will help outreach your application. In this module, you will learn how to create a simple user interface using MRTK's button and menu prefabs alongside Unity's TextMeshPro component. You will also learn how to configure the buttons to trigger events and add dynamic tooltip UI elements to provide the user with additional information. You will learn how to enable near and far manipulation of 3D objects and limit the allowed types of manipulation. You will also learn how to add bounds control around 3D objects to make it easier to control the object manipulation.

## UI Buttons and Menus

Buttons help the user to trigger an immediate action. It is one of the foundational components provided by MRTK. Various kinds of button prefabs can be used depending on your situation. The Button is primarily based totally on the Interactable idea to offer smooth UI controls for buttons or different interactive surfaces. The Interactable module is an all-in-one box to make any item interactable and conscious. Interactable acts as a catch-considering all forms of entering consisting of touch, hand rays, speech, and so on and funnel those interactions into activities and visible subject responses.

Menu is a UX control which offers a set of buttons or different UI components. It is floating across the user's frame and effortlessly available anytime. Since it is loosely coupled with the person, it does now no longer disturb the user's interplay with the target content. The user can use the 'Pin' button to world-lock/unlock the menu. The menu may be grabbed and located at a selected position.

## Tooltips

A tooltip is a brief description that is related to some other manipulate or object. They're used to deliver a hint or extra data upon closer inspection. Tooltips assist users recognize strange items in the physical surroundings that are not defined directly.

## Manipulating 3D Objects

What fun would it be when you place holograms in the surrounding, but things get interesting when you can manipulate those holograms using your hands or any input source. To manipulate and grab an object with tracked hands, the objects must have the following components attached to them:

1. Collider: Collider components outline the form of a GameObject for bodily collisions. An invisible collider does not want to be the precisely identical form as the GameObject’s mesh. A rough approximation of the mesh is frequently more efficient and indistinguishable in gameplay.
2. Object Manipulator(Script): The ObjectManipulator script makes an object movable, scalable, and rotatable using one or both hands. The object manipulator can be configured to manipulate how the item will reply to numerous inputs. The script must work with maximum sorts of interaction, including HoloLens 2 articulated hand, HoloLens 2 hand rays, HoloLens 1 gaze and gestures, and immersive headset motion controller input. 
3. NearInteractionGrabbable: The NearInteractionGrabbable component helps you grab the object near his/her tracked hands.

## Bounds Control

The BoundsControl presents a simple capability for remodeling objects in mixed reality. A bounds control will display a container across the hologram to suggest that it can be interacted with. Handles at the corners and edges of the box will permit scaling, rotating, or translating the object. The bounds control additionally reacts to your input. On HoloLens 2, for example, the bounds control responds to finger proximity, offering visible remarks to help understand the space from the object. All interactions and visuals may be effortlessly customized.
