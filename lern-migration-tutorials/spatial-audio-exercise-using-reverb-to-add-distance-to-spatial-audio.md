# 10. Exercise: Using reverb to add distance to spatial audio


In previous module, you have added spatialization for the sounds to give them a sense of direction in this module you'll add a reverb effect to give sounds a sense of distance.



## Add a mixer group and a reverb effect

In [Spatializing button interaction sounds Tutorial](unity-spatial-audio-ch2.md), we added a mixer. The mixer includes one **Group** by default called **Master**. Because we'll only want to apply a reverb effect to some sounds, let's add a second Group for those sounds. To add a Group, right click on the Master group in the **Audio Mixer** choose **Add child group** and give suitable name for example _Room Effect_:

![Add child group](images/spatial-audio/spatial-audio-05-section1-step1-1.png)

Each **Group** has its own set of effects. Add a reverb effect to the new group by clicking **Add...** on the new group, and choosing **SFX Reverb**:

![Add SFX Reverb](images/spatial-audio/spatial-audio-05-section1-step1-2.png)

In audio terminology, the original, unreverberated audio is called the _dry path_, and the audio after filtering with the reverb filter is called the _wet path_. Both paths are sent to the audio output, and their relative strengths in this mixture is called the _wet/dry mix_. The wet/dry mix strongly affects the sense of distance.

The **SFX Reverb** includes controls to adjust the wet/dry mix within the effect. Because the **Microsoft Spatializer** plugin handles the dry path, we'll be using the **SFX Reverb** only for the wet path. On the Inspector pane of your **SFX Reverb**:

* Set the **Dry Level** property to the lowest setting (-10000 mB)
* Set the **Room property** to the highest setting (0 mB)

![SFX Reverb properties](images/spatial-audio/spatial-audio-05-section1-step1-3.png)

The other settings control the feel of the simulated room. In particular, **Decay Time** is related to perceived room size.

## Enable reverb on the video playback

There are two steps to enable reverb on an audio source:

* Route the **Audio Source** to the appropriate **Group**
* Set the **Microsoft Spatializer** plugin to pass audio into the **Group** for processing

In the following steps, you will adjust the script to control the audio routing, and attach a control script provided with the **Microsoft Spatializer** plugin to feed data into the reverb.

With the **Quad** selected in the Hierarchy click **Add Component** On the Inspector window and add the **Room Effect Send Level(Script)**:

![Add send level script](images/spatial-audio/spatial-audio-05-section2-step1-1.png)

> [!NOTE]
> Unless you enable **Room Effect Send Level** feature of the **Microsoft Spatializer** plugin, it doesn't send any audio back to the Unity audio engine for effect processing.

The **Room Effect Send Level** component includes a graph control that sets the level of the audio sent to the Unity audio engine for reverb processing. To open the graph control, click on the **Room Effect Send Level**.  Click and drag the green curve downwards to set the level to about -30dB:

![Adjust reverb curve](images/spatial-audio/spatial-audio-05-section2-step1-2.png)

Next, uncomment the 4 commented lines in the **SpatializeOnOff** script. The script will now look like this:

```c#
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.Audio;

[RequireComponent(typeof(AudioSource))]
public class SpatializeOnOff : MonoBehaviour
{
    public GameObject ButtonTextObject;
    public AudioMixerGroup RoomEffectGroup;
    public AudioMixerGroup MasterGroup;

    private AudioSource m_SourceObject;
    private bool m_IsSpatialized;
    private TMPro.TextMeshPro m_TextMeshPro;

    public void Start()
    {
        m_SourceObject = gameObject.GetComponent<AudioSource>();
        m_TextMeshPro = ButtonTextObject.GetComponent<TMPro.TextMeshPro>();
        SetSpatialized();
    }

    public void SwapSpatialization()
    {
        if (m_IsSpatialized)
        {
            SetStereo();
        }
        else
        {
            SetSpatialized();
        }
    }

    private void SetSpatialized()
    {
        m_IsSpatialized = true;
        m_SourceObject.spatialBlend = 1;
        m_TextMeshPro.SetText("Set Stereo");
        m_SourceObject.outputAudioMixerGroup = RoomEffectGroup;
    }

    private void SetStereo()
    {
        m_IsSpatialized = false;
        m_SourceObject.spatialBlend = 0;
        m_TextMeshPro.SetText("Set Spatialized");
        m_SourceObject.outputAudioMixerGroup = MasterGroup;
    }

}
```

Once these lines are Uncommented  it adds two properties to the Inspector of the **SpatializeOnOff script**. assign these on the Inspector window of **SpatializeOnOff** component of the **Quad**.

With the Quad object still selected in the Hierarchy , in the Inspector window locate the **SpatializeOnOff Script** component and :

* Set the **Room Effect Group** property to your new Room Effect mixer group
* Set the **Master Group** property to the Master mixer group

![Spatialize On Off Extended](images/spatial-audio/spatial-audio-05-section2-step1-3.png)

# Knowledge check

# Summary
In this module series you have learnt:-
* To Import and enable the Microsoft Spatializer plugin and also to enable the spatial audio on your workstation. 

* To spatialize the button interaction sounds and to use an audio clip to test spatialized button interaction.
* To spatialize audio from an video source Try out your app on a HoloLens 2 or in the Unity editor. You'll see and hear the video, and the audio from the video is spatialized.

* To enable and disable spatialization at run time, test out the app on a HoloLens 2 or in the Unity editor. In the app, you can now click the button to activate and deactivate spatialization of the audio.

