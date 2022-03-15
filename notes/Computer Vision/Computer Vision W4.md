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

#### Region proposals ( Selective Search )
- Images which are likely to contain objects/Blobs are detected in this process so that we do not have to scan the entire image as in Bruite Force/ Sliding Window
- Cannot be run on a GPU
- Eg : Selective search classifies the images into small segments and then combine them
![](https://media.geeksforgeeks.org/wp-content/uploads/home/Step2-660x168.PNG)
- Later networks were used to do this.


## Region Convolutional Neural Networks
![RCNN](https://miro.medium.com/max/1400/1*REPHY47zAyzgbNKC6zlvBQ.png)
- Image fed to network
- Comes up with region proposals
- Convert all regions to a fixed size
- Pass it through a CNN which does classification
- It does redundant computations hence slow
-
## Fast R-CNN
![FCNN](https://miro.medium.com/max/1095/1*jYDMaYeH-TrcoofDqCdxug.jpeg)

- Images are fed into a CNN which creates region proposals of different sizes. 
- The feature maps are then fed into a ROI pooling layer which converts all these regions into a fixed size
- This is later fed into a DNN and then to a classification layer for Object classification and to a regression layer for predicting the bounding boxes
- The back propogation can happen only till the region proposal area, as before that it is selective search which happens. 
- This problem is cleared in the Faster RCNN networks. 
- Here, Unlike the RCNN network each region does need not be passed through a convolutional layer. Rather only selected images has to be passed through the same. 

#### ROI Pooling
![ROIPooling](https://miro.medium.com/max/1316/1*zlfIBgjS0P435lhJLoW8SA.png)

- To convert region proposals of different sizes into same size
- It divides the matrices in an effective way to get the output of the required sizes

## Faster RCNN
![Faster RCNN](https://media.geeksforgeeks.org/wp-content/uploads/20200219125702/faster-RCNN.png)
- Make CNN do proposals
- Selective search was taking up most of the time
- A region proposal network would do the work instead of a selective search
- ROI pooling will make it the same sizes
- DNN would do further predictions
- Classification & Regression / Any of them based on the use case

- With a Region proposal network for the region proposals, this gives the ability to back propogate as it uses neural network for Region proposal as well
---
# One stage approaches

They are faster than Two Stage approaches/ Detectors, but they have lower accuracy

## YOLO ( You Only Look Once ) 
![YOLO](https://leimao.github.io/images/blog/2019-04-15-YOLOs/yolo_v1_diagram.png)

- Looks at the image once
- For every grid box, predict n  boxes
- Each box would have (x,y,h,w, confidence ) output
- So each box for an image of size sxs there would be sxs(5xn) outputs
- Each of the s\*s boxes produces n bounding boxes. Each of these bounding boxes has lets say 5 classes. So 5 probability values will be generated for each box. If the value of proabability is more than a threshold, then that box is considered. After this process, a number of bounding boxes are dropped which does not meet the threshold requirements. 
- Combine the boxes

#### Non Maximal Supression
![NMS](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRIer0Gn04CYowFSuSE1A2kYIKslL6P0JJWrnt1XFKSgmN5j5-zvhyNqomKJfTILbV72wM&usqp=CAU)

- Supression of overlapping boxes to come up with a single boxes
- Get box with Maximum score from the list of bounding boxes
- Compute IOU of every other box with the box with maximum score
- Remove bounding boxes with high IOU

#### Single Shot Detector ( By Google )
![SSD](https://cdn-images-1.medium.com/fit/t/1600/480/1*hdSE1UCV7gA7jzfQ03EnWw.png)
- Pre defined bounding boxes, called Anchor boxes
- Network chooses between these Anchor boxes
- This becomes a classification problem
- SSD takes features from multiple layers whereas YOLO does this from a single layer. 


---

### Summary 
![Summary](https://i.ibb.co/BZjFrDC/2022-01-29-20-28.png)
- The base networks will change the speed, accuracy etc
- Object detection architecture will affect the speed of object identification



