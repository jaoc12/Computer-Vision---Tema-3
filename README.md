# Hog-face-detector

Python program to detect multi-size human faces in images. For detection I've used histograms of oriented gradients to check if a subsample from the image contains a face.
<br/>
<br/>
## Data
I've used a dataset from MIT which contains 6713 images of human faces. All the pictures where 36*36 px. For a better performance I also use the mirrored version of the image.
<br/>
For negative exemples I choose 10000 random subsamples from images without faces.
