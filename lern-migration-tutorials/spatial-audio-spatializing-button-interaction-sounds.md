# 3. Spatializing button interaction sounds

## Audio feedback
Audio feedback is a special kind of positive loop gain which occurs when a sound loop exists between an audio input and an audio output. In this example, a signal received by the microphone is amplified and passed out of the loudspeaker. The sound from the loudspeaker can then be received by the microphone again, amplified further, and then passed out through the loudspeaker again.
## Audio mixer
The Unity Audio Mixer allows you to mix various audio sources, apply effects to them, and perform mastering.udio Mixer which is basically a tree of Audio Mixer Groups. An Audio Mixer group is essentially a mix of audio, a signal chain which allows you to apply volume attenuation and pitch correction; it allows you to insert effects that process the audio signal and change the parameters of the effects. There is also a send and return mechanism to pass the results from one bus to another.


## Spatial blend
It sets how much this AudioSource is affected by 3D spatialisation calculations (attenuation, doppler etc). 0.0 makes the sound full 2D, 1.0 makes it full 3D.
Aside from determining if this AudioSource is heard as a 2D or 3D source, this property is useful to morph between the two modes.3D spatial calculations are applied after stereo panning is determined and can be used in conjunction with panStereo.Morphing between the 2 modes is useful for sounds that should be progressively heard as normal 2D sounds the closer they are to the listener.
## Spatialize
It enables or disables spatialization.Custom spatializer effects improve the realism of sound propagation by incorporating the binaural head-related transfer function (HRTF) such that the listener can better sense the directionality of the sound through the filtering of the head and the micro-delays between the ears. Unity supports custom spatialization effects as optional plugins through the native audio plugin system, and in case such plugins are present, will show a "Spatialize" checkbox on the AudioSource that corresponds to this property. If no plugin is present (and selected in the project audio settings), attempts to set this property to true will fail with a warning.

