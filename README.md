# Hog-face-detector

Python program to detect multi-size human faces in images. For detection I've used histograms of oriented gradients to check if a subsample from the image contains a face.
<br/>
<br/>
## Data
I've used a dataset from MIT which contains 6713 images of human faces. All the pictures where 36*36 px. For a better performance I also used the mirrored version of the image.
<br/>
For negative exemples I chose 10000 random subsamples from images without faces.
<br/>
![Oops there should be an image](https://iq.opengenus.org/content/images/2019/07/hog-vis.png)
<br/>
## Training
As a classifier I've used a SVM as implemented in the linearSVC from sklearn library. The only parameter changed was the regularization c, for which I've used 10^(-2).
<br/>

## Testing
To detect faces in an image I've used the sliding window technique.
<br/>
![Oops there should be a gif](https://pyimagesearch.com/wp-content/uploads/2014/10/sliding_window_example.gif "Exemple of sliding window")
<br/>
For faster results, with the same precision, the image was transformed in a Hog descriptor and the sliding window was applied on it. Also to detect multiscale faces the image is repeatedly downscaled.
