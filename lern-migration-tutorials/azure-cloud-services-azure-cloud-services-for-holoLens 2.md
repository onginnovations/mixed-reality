# 1. Azure Cloud Services for HoloLens 2
## Azure cloud services
Azure Cloud Services is an example of a platform as a service (PaaS). Like Azure App Service, this technology is designed to support applications that are scalable, reliable, and inexpensive to operate. In the same way that App Service is hosted on virtual machines (VMs), so too is Azure Cloud Services
## Azure storage
Azure Storage includes object, file, disk, queue, and table storage. There are also services for hybrid storage solutions, and services to transfer, share, and back up data.
## Azure custom vision
With Azure Custom Vision (part of the Azure Cognitive Services) you can associate to Tracked Objects a set of images, train a machine learning model on the set and detect the Tracked Object.
## Azure spatial anchors
To store a Tracked Object location and give a guided directions to find it, you use Azure Spatial Anchors.
## Azure bot service
The application is mainly driven by traditional UI, so you use the Azure Bot Service to add some personality and act as a new interaction method.
## InternetClient
Apps can receive incoming data from the Internet. It cannot act as a server. No local network access.
## Microphone
Accesses the microphone’s audio feed, which allows the app to record audio from connected microphones.
## Spatial Perception
Provides programmatic access to spatial mapping data, giving mixed reality apps information about surfaces in application-specified regions of space near the user. Declare the spatialPerception capability only when your app will explicitly use these surface meshes, as the capability is not required for mixed reality apps to perform holographic rendering based on the user’s head pose.

## Internet client server
Apps can receive incoming data from the Internet. Cannot act as a server. No local network access.It also enables peer-to-peer (P2P) scenarios where the app needs to listen for incoming network connections.
## Private network client server
Provides inbound and outbound access to home and work networks through the firewall. This capability is typically used for games that communicate across the local area network (LAN), and for apps that share data across a variety of local devices.
## Webcam
Accesses the video feed of a built-in camera or external webcam, which allows the app to capture photos and videos.
Note: This only grants access to the video stream. In order to grant access to the audio stream as well, the Microphone capability must be added.