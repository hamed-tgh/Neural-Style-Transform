# Neural-Style-Transform


acording to wikipedia, Neural style transfer (NST) refers to a class of software algorithms that manipulate digital images, or videos, in order to adopt the appearance or visual style of another image.

in this project by using VGG-16 we combine the style of one of Vincent van Gogh, The Starry Night, painting with content of another image, one one paris pictures.

let's take a brief look at the whole project.

![image](https://github.com/hamed-tgh/Neural-Style-Transform/assets/47190471/be21ebe8-9b8d-4ab0-a3c0-f2f33a296755)

![image](https://github.com/hamed-tgh/Neural-Style-Transform/assets/47190471/8c2f098f-743b-4269-9d98-6d4b13c73b06)



we know that in the lower layers of a CNN we look for low level features such as lines or blobs. As we go to the higher layers, out features become increasingly complex. thus, we can conclude that ConvNets develop a hierarchical representation of features.


in NST, while doing style transfer, we are not training a neural network. Rather, what we're doing is we start from a blank image composed of random pixel values, and we optimize a cost function by changing the pixel values of the image. in other words, while training neural networks we update our weights and biases, but in style transfer, we keep the weights and biases constant, and instead, update our image based on a error function which is like bellow:

![image](https://github.com/hamed-tgh/Neural-Style-Transform/assets/47190471/2221a380-54d1-44fc-8750-d6fbf8f54d01)

![image](https://github.com/hamed-tgh/Neural-Style-Transform/assets/47190471/d896f4a3-9e77-431c-943d-8e144d0abf66)

in which, P^l is the representation of the original image and F^l is the representation of the generated image in the feature maps of layer l.

![image](https://github.com/hamed-tgh/Neural-Style-Transform/assets/47190471/279b63b6-a2a4-41f6-b995-c9560c8a824e)

in wich, G is the Gram matrix of a vector X is X.X_transpose. and The intuition behind using gram matrix is that we’re trying to capture the statistics of the lower layers.




Finally our output would be like bellow:



![image](https://github.com/hamed-tgh/Neural-Style-Transform/assets/47190471/ad8d764b-ac7b-4f02-9d54-ab13f950da09)




