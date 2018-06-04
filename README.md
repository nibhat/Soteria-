# Soteria-
Intrusion Detection System

People have wired their premises with commodity/NEST cameras for home surveillance. One of the big challenges is how to look at the streaming data and identify in real time if the person or vehicle approaching is a legit visitor to your property or not and also detect if they are a threat. The idea behind this is to create a intrusion detect system which can alert the consumer of possible incidents, with details of what whitelist of people which can access or not.

INSPIRATION
High school shootings have been a cause of pain for me. If there was a way to process livestream in real time, identify subjects of interest and measure instruments/articles the subjects carry, it will create a real time system of threat detection and possibly identifying guns on campus. Once identified, this can alert the school authorities and law enforcement agencies for lock down and mitigation before the actual incidents and possibly save lives.
There is a lack of intelligent AI/ML based system for consumers who want to secure their premises and process livestream of their premise with threat detection. The commodity intelligence available is pretty low grade and does not account for whitelist/noise cancellation/high fidelity solution. 
 
 
HOW IT WILL WORK / HOW IT WILL BE BUILT
 
1) Use Azure face recognition API for face detection in white list or not
2) Use Azure speech recognition for audio match if face detection fails
3) Do this at scale
4) wire it with existing streams of video traffic
5) use azure video indexer for checking against videos
6) for object recognition inside a frame, use CNTK or TensorFlow
 
I plan to use Azure video indexer API
https://docs.microsoft.com/en-us/azure/cognitive-services/video-indexer/
The challenge though is that it supports static videos, not livestream of videos. Want to support detection in offline videos as well as livestream
Also, look at Azure Face recognition(cognitive API) for pictures. That is for picture identification
Plan to use CNTK for object detection first
https://docs.microsoft.com/en-us/cognitive-toolkit/Object-Detection-using-Fast-R-CNN
