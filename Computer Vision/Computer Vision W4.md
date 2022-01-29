# Computer Vision Week 4


- Object Classification
- Object Detection
- Precision and Recall
- Intersection over union
- Mean Average Precision

## Open CV , CustomVision and Lobe
- [Open CV Image Processing approaches discussed](https://github.com/sandheepgopinath/Code-Repository/tree/main/Computer-Vision/Opencv/Basic%20Image%20Processing)

- OpenCV shall be used whenever possible and can help to reduice the complexity of certain problems without using Deep Learning Models
- If not possible by Basic Image Processing Libraries or OpenCV, try Deep Learning
- [Create the models using CustomVision.ai automcatically](https://azure.microsoft.com/en-us/services/cognitive-services/custom-vision-service/)
- The trained models can be downloaded in Tensorflow/ Tensorflow lite format
- Might need to make some minor tweaks to change the threshold accuracy, maximum number of objects detected in a single frame etc, based on your use case
- [Lobe.ai is another wonderful solution acquired by Microsoft](https://www.lobe.ai/)
- However, the usage of lobe may be restricted in certain use cases. Usually with Binary predictions/ classifications. 
-
## Classification and Object Localization

![Architecture](https://miro.medium.com/max/1838/1*NTVoRZYBWbwRxNidyLCxPw.png)
- The top right part is the classification part
- Bottom right part is where we can use any regression model to prediction the cordinates of top left of bounding box, height and width. The box can be then defined using the height and width and a simple Mean Square error can help in estimation of the error

---
## Intersection over Union

![IOU](https://www.researchgate.net/profile/Rafael-Padilla/publication/343194514/figure/fig2/AS:916944999956482@1595628132920/Intersection-Over-Union-IOU.ppm)
- Intersection over Union is a better way of calculating how well the bounding boxes were predicted. 
---
## Precision and Recall
![Precision vs Recall](https://cdn-images-1.medium.com/fit/t/1600/480/1*Ub0nZTXYT8MxLzrz0P7jPA.png)
- #### Precision = TP/(TP+FP)
- #### Recall = TP/ (TP+FN)
- It is important to monitor both precision and recall as they help in giving a better picture
- Eg : 100 data points, 60 Positive, 40 Negative .
    -  Observer Recall and Precision in this case and observe    
---



## Object detection Methods

1. Single Stage apporaches uses a single stage of detection and focusses on speed. Some examples are YOLO, RetinaNet, SSD etc. Does not have region proopsal. Instead they use Anchor boxes
2. Two stage approaches uses two stages of detection .Here the priority os for  accuracy. In first stage, we come up with a set of Region of Interests and then these are iterated. Examples are RCNN, Faster RCNN , Mask RCNN, Cascade RSCNN etc. They use region proposals

#### Region proposals
- Images which are likely to contain objects
- Eg : Selective search classifies the images into small segments and then combine them
![](https://media.geeksforgeeks.org/wp-content/uploads/home/Step2-660x168.PNG)
- Later networks were used to do this.


### Region Convolutional Neural Networks
![RCNN](https://miro.medium.com/max/1400/1*REPHY47zAyzgbNKC6zlvBQ.png)
- Image fed to network
- Comes up with region proposals
- Convert all regions to a fixed size
- Pass it through a CNN which does classification
- It does redundant computations
- 


