# Computer-vision-OpenCv-Canny-edge-detection

The process in the Canny edge detection method is:
a) First the image is turned into a grayscale image (by use of ‘cvtColor’
method) and then the Gaussian filter is used to remove the noise in the 
image and smoothing the image for greater clarity. The noise in the image 
is removed in order to reduce the false detection of the edge in the image. 
To smoothen the image, the Gaussian filter is adopted to use the 
‘Gaussian filter kernel’ with the image. The kernel size should be 
implemented properly. The larger the size, the lower the detection to 
noise.

b) After applying the Gaussian filter, the intensity gradient of the image is 
to be find out. An edge in the image can point to any direction. So, the 
Canny edge algorithm uses 4 filters to detect the edges in horizontal, 
vertical and the diagonal edges in the image. Every edge will be either 
0,45,90 degree. Every edge will be in a specific angle.

c) Application of gradient magnitude takes place in which the pixels which 
are of no use to form an edge are removed. This removes the all un-
necessary data in the image and the only image left behind is the image 
with lines. This method is known as ‘lower bound thresholding’. This 
technique compares the current edge and the remaining edge from a point. 
If the edge is of more strength than the other edge, the value is preserved. 
Otherwise, the value will be suppressed. 

d) Application of double threshold to detect the potential edges. In this 
technique the edges with weak gradient value are removed and the edges 
with strong gradient value are retained. If the edge pixel’s gradient value 
is high than the high threshold value, the edge is said to be the strongest. 
If the edge pixel’s gradient value is low than the high threshold value and 
high than the low threshold value, then the edge is said to be weak edge. 
And if the edge pixel’s gradient value is low than the low threshold value, 
the edge is suppressed. 

e) The final step in this algorithm is the hysteresis method. This method is 
also known as edge tracking by hysteresis. In this method, the strong 
edges and the weak edges are examined. The strong edges are preserved. 
But, the weak edges are examined whether they are drawn because of the 
noise or are they an edge in the image. So, for this purpose, the weak edge
is examined whether it is connected to a strong edge. If not, the edge is 
removed. And hence we get an image with just the accurate edges of the 
original image.
