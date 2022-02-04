# Image segmentation

- Semantic Segmentation
	- A label over every pixel in the image
	- Can do a convolution over a selected area which is then moved around in the image. This process needs large number of convolutions which is very expensive. 
	- Dilated convolutions can help in reducing the number of operations
	![](https://miro.medium.com/freeze/max/395/0*3cTXIemm0k3Sbask.gif)
<br>
	- However, the number of convolutions needed are still high. Hence we go for different approaches<br><br>
    ##### Approach 1
	-  Follow something like an encoder-decoder network. This can be done with or without convolution operations as a fully connected layer. But it can overfit the images. So we usually use convolutions over fully connected when it comes to images.
    
	![](https://miro.medium.com/max/1838/1*44eDEuZBEsmG_TCAKRI3Kw@2x.png)
    	- This will produce the output image in the same size as the input. 
    - <a href='https://github.com/sandheepgopinath/Code-Repository/blob/main/Development/Artificial%20Intelligence/AutoEncoders/Deep_Autoencoder.ipynb'>Deep Autoencoder </a>

	- #### How do we do upsampling?
    	- Transposed convolution
        - Fractionally strided convolution
        - Max unpooling
        
        ![](https://www.researchgate.net/profile/Eli_David/publication/306081538/figure/fig2/AS:418518853013507@1476794078414/Pooling-and-unpooling-layers-For-each-pooling-layer-the-max-locations-are-stored-These.png)
        - Remembers the location from where the maximum values were selected and restores values into that locations
        
        

  
- Instace level Segmentation
- Mask RCNN
- 