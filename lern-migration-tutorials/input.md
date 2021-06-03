# Input

The Mixed Reality Toolkit enables you to consume inputs from various input sources such as 6DoF (degrees of freedom) controllers, articulated hands, or speech. Choosing the interaction model best suited for your mixed reality experience requires you to identify your user, their goals and consider any situational or environmental factors that may impact their experience.

## Eye-Tracking

MRTK is highly considerate about the way humans communicate and express themselves. HoloLens 2 offers an exciting and powerful new input: Eye-tracking! Eye-tracking enables you to quickly and effortlessly engage with holograms across their view and make your system smarter by better identifying your intention. There are many use cases of Eye-tracking like user intent, implicit actions, attention tracking, gaming, text entry, etc.

## Voice Commands

Speech input providers, like Windows Speech Input, do not create any controllers; however, as a substitute, it assists you in outlining key phrases to improve speech input events when recognized. The Speech Commands Profile in the Input System Profile is wherein you configure the key phrases to recognize.  For each command you can also:

* Select an input action to map it to. This way you can for example use the keyword Select to have the same effect as a left mouse click, by mapping both to the same action.
* Specify a key code that will produce the same speech event when pressed.
* Add a localization key that will be used in UWP apps to obtain the localized keyword from the app resources.
