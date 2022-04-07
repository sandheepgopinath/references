---
title: Computer Vision project
created: '2022-04-07T08:56:40.709Z'
modified: '2022-04-07T10:18:53.406Z'
---

# Computer Vision project

- Approach 

- User interface created using PyQt5 tool
- Interface has three options. 
  - To turn on/off the webcam
  - To start face detection
  - To start face feature detection
- Face feature detection will not work unless the face detection is turned on. 


- ## Face detection
Approach tried. 
  - Mobile net for training the WIDER dataset
  - IoU was used as the loss function
  - The accuracy was not good enough to be combined with feature extraction
  - Hence, we have used HAAR CASCADE classifier to do the same

- ## Key point detection
  - We have created a CNN , which was trained on the given dataset
  - Root Mean Square was used as the loss function 
  - The architecture used was similar to a VGG 16 , where the depth was increasing and the size was decreasing as we went further down the network
  - The model was able to accurately predict the keypoints in a face, provided the image is close enough to the camera / cropped
  
 - ## Detection process
  - Once the user starts tracking, the faces will be detected and will be indicated by a blue bounding box. The window along with the main window, will show details about the number of faces detected
  -Once the user turns on key point detection, the key points will also be marked on the image in red circles. 
  - The image detected by the face detection algorithm will be fed to the will become the input to the keypoint detection algorithm, thus making the keypoint detection feature more effective as we have the exact frame of the face, identified and being fed to the model. 


