# 5. Spatializing audio from a video

## Transcode
When enabled by ticking the checkbox, the source is transcoded into a format that is compatible with the target platform.If disabled, the original content is used, bypassing the potentially lengthy transcoding process.
## Codec
Codec used for encoding the video track.
## Bitrate mode
Low, Medium, or High bitrate is relative to the chosen codec’s baseline profile.
## Spatial quality
This setting dictates whether video images are reduced in size during transcoding, which means they take up less storage space. However, resizing images also results in blurriness during playback.

* Low Spatial Quality:
The image is significantly reduced in size during transcode (typically to a quarter of its original dimensions), and then expanded back to its original size upon playback. This is the highest amount of resizing, meaning it saves the most storage space but results in the largest amount of blurriness upon playback.
* Medium Spatial Quality:
The image is moderately reduced in size during transcode (typically to half of its original dimensions), and then expanded back to its original size upon playback. Although there is some resizing, images will be less blurry than those that use the Low Spatial Quality option, and there is some reduction in required storage space.
* High Spatial Quality:
No resizing takes place if this option is selected. This means the image is not reduced in size during transcode, and therefore the video’s original level of visual clarity is maintained.
## Render texture
A Render Texture is a type of Texture
 that Unity creates and updates at run time. To use a Render Texture, create a new Render Texture using Assets > Create > Render Texture and assign it to Target Texture in your Camera
 component. Then you can use the Render Texture in a Material
 just like a regular Texture.