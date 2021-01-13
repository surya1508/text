# Sign-To-Speech_conversion
Unable to communicate verbally is a disability. In order to communicate there are many ways, one of the most popular methods is the use of predefined sign languages. The purpose of this project is to bridge the research gap and to contribute to recognize American sign languages(ASL) with maximum efficiency. This repository focuses on the recognition of ASL in real time, converting predicted characters to sentences and output is generated in terms of voice formats. The system is trained by convolutional neural networks for the classification of 26 alphabets and one extra alphabet for null character. The proposed work has achieved an efficiency of 99.88% on the test set.

## Data Distribution
A total of 17113 images have been included in the field of study. There are around 600 images per alphabet. A total of 12845 images were considered for the training set. Out of these, 0.3% of the images were used for validation. A total of 4368 images were used in the testing phase to evaluate the accuracy of the model.
The dataset used in this field of study can be downloaded from:
https://drive.google.com/drive/folders/16ce6Hc4U5Qr6YBArcozoYom6TT5-7oSc?usp=sharing

## Data-Preprocessing
The images from the dataset were pre-processed by eliminating the background noise. Several crucial preprocessing steps are listed below:
* Gaussian Blur: Gaussian filter is used to blur the given image, reduce noise and smoothen the images. 
* Grayscale Conversion: A grayscale image has equal intensities in RGB space. It becomes easier to differentiate such images from any other sort of colour image as the number of color channels are reduced.
* Canny Edge Detector:  A multistage algorithm used to detect a wide range of edges in images. 
* Normalization: Input stream of pixel values(0-255) in the data is converted to a scale of 0 to 1 by broadcasting a division by 255. It makes the system to better understand and gives almost an equal importance to each of the pixel values. 

## Feature Extraction
* A Gaussian filter is applied to make the image smooth and  remove the noise.
* Intensity gradients of the image are calculated.
* Non-maximum suppression is applied to remove the possibility of a false response. 
* Double thresholding is done to detect or determine the possible edges. 
* Edges are finalized by identifying and removing all other edges that are weak and not linked to strong edges.

## Proposed Flow

## Results and Analysis
The model has been trained on a python based environment on Jupyter platform for 20 epochs. The model has achieved an accuracy of 97.45 % on Training Set with 99.88 % accuracy on the Validation set. The prescribed model has also been evaluated on a Test set where it has yielded an accuracy of 99.85% with loss of 0.60 %.


The training phase data has been evaluated on the Heatmap Plotting representation. The prescribed inference suggests that the trained classes are highly correlated with the same class of the data. 


The model has been evaluated for Precision, Recall, F1-score metrics for all the 26 classes along with a null class. The analysis carried has been shown in the classification report attached below. 

## Results


