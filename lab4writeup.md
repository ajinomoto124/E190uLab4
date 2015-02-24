# E190uLab4
## Lab4 Write-Up
#### Introduction:
Modified cuda and c++ code for image modification on the Jetson Tk1

#### Design & Testing Methodology:
When I first saw the procedure for the lab, I was immediately interested in trying out an edge detection convolution matrix for the image processing part of the lab.  After looking through the .cu script for where the convolution kernel was applied to the image I realized that there wasn't exactly a matrix applied for the convolution but rather a set of loops went through segments of the image in a similar way to common matrix convolution techniques.  Thus, I set up some conditionals for different cases of modification to different parts of the image. Once I had confirmed the code compiled I took a look at my output image and adjusted my cases until I found the right one for edge detection.

From there, I wanted to try some other image convolution techniques. A quick google search led me to find an "emboss" matrix kernel and I applied that to the image using another set of conditionals.  I felt that this resulted in an interesting modification depending on the radius of the kernel applied.


#### Results & Discussion
My edge detection technique resulted in the following two images:
![alt text](https://github.com/ajinomoto124/E190uLab4/blob/master/edgedetBryan.jpg)
![alt text](https://github.com/ajinomoto124/E190uLab4/blob/master/edgedetBryan2.jpg)

Unfortunately, this only worked when the radius of the convolution kernel was set to the smallest possible size (1).

My Emboss method resulted in these images:

![alt text](https://github.com/ajinomoto124/E190uLab4/blob/master/embBryan9.jpg)

The above image has a radius set to 9

![alt text](https://github.com/ajinomoto124/E190uLab4/blob/master/embBryan16.jpg)

And this one has radius set to 16

#### Conclusions
Time spend on lab: about 3 hours.
While I understood the techniques used in CUDA programming that were given in the sample of this lab, I found that I did not have to implement any memory allocation or management in the code I wrote as additions to this code.  This left me somewhat confused as to whether or not I was doing this lab properly.
