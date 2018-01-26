# AR Course
A primary practice of augmented reality with object identification and tracking.

## Bag of visual words model
The bag-of-visual-words (BoW) model is a simple assumption used in natural language processing and information retrieval, and has been widely applied in the computer vision field. The procedure includes two parts: learning and recognition. 

In the learning procedure, 
- (i) Select a large set of images as the training data.
- (ii) Extract the SURF descriptors points of all the images in the training set and obtain the SURF descriptor for each interest point extracted. 
- (iii) Quantize these descriptors by K-means clustering algorithm to form a codebook. 
- (iv) Obtain the result of clustering as the visual vocabulary. 
- (v) Extract the interest points of the object image. 
- (vi) Obtain SURF descriptor for each interest point. 
- (vii) Match the feature descriptors with the vocabulary by KNN algorithm. 
- (viii) Build the histogram of object image.

In the recognition procedure, the object images are represented by visual vocabulary. Each vocabulary has its own value so that the object image can be represented by vectors. Normally, different image will be transformed to different histograms which also can be represented as different vectors. Next, this characteristic will be used to check the similarity between object image and one frame image.

## Object tracking
The tracking solution is to find the strong enough corners and then compute sparse optical flow using multi-scale Lucas-Kanade algorithm.

## Result
![image](https://github.com/JeffreyHoa/ar_course/blob/master/images/figure13.png)

![image](https://github.com/JeffreyHoa/ar_course/blob/master/images/figure21.png)

