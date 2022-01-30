## Types of convolution and their differences

### Conv1D
<body>
Conv1D is used for input signals which are similar to the voice. By employing them you can find patterns across the signal. For instance, you have a voice signal and you have a convolutional layer. Each convolution traverses the voice to find meaningful patterns by employing a cost function.
</body><br>


---
### Conv2D
<body>
Conv2D is used for images. This use case is very popular. The convolution method used for this layer is so called convolution over volume. This means you have a two-dimensional image which contains multiple channels, RGB as an example. In this case, each convolutional filter should be a three-dimensional filter to be convolved, cross-correlated actually, with the image to find appropriate patterns across the image.
</body><br>



---
### Conv3D
<body>
Conv3D is usually used for videos where you have a frame for each time span. These layers usually have more parameters to be learnt than the previous layers. The reason we call them 3D is that other than images for each frame, there is another axis called time containing discrete values, and each of them corresponds to a particular frame
</body><br>



Credits : Green Falcon. https://datascience.stackexchange.com/users/28175/green-falcon
