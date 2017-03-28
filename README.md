# R-CNN-understanding
This repo serves as a summary of the paper "Rich feature hierarchies for accurate object detection and semantic segmentation Tech report (v5)".

## Abstract
### Two key insights:
 1) One can apply high-capacity convolutional neural networks (CNNs) to bottom-up region proposals in order to localize and segment objects.
 2) When labeled training data is scarce, supervised pre-training for an auxiliary task, followed by domain specific fine-tuning, yields a significant performance boost.
 
 high-capacity here refers to the complexity of the underlying pattern that the neural network is able to learn. Usually going deep increases the capacity of the neural network by increasing the number of model parameters which means it can fit more complex functions.


### Two problems need to be justified:
1) Localizing objects with a deep network.  ==>  operating within the "recognition using regions" paradigm
2) Training a high-capacity model with only a small quantity of annotated detection data.  ==>  supervised pre-training on a large auxiliary dataset, followed by domain-specific fine-tuning on a small dataset


Unlike image classification, detection requires localization objects within an image.

## Object detection
### Three modules:
1) A Module that generates category-independent region proposals.
        ----> selective search  (see paper: chrome-extension://ikhdkkncnoglghljlkmcimlnlhkeamad/pdf-viewer/web/viewer.html?file=https%3A%2F%2Fivi.fnwi.uva.nl%2Fisis%2Fpublications%2F2013%2FUijlingsIJCV2013%2FUijlingsIJCV2013.pdf)
2) A large CNN that extracts a fixed-length feature vector from each region.
        ----> five convolutional layers and two fully connected layers. Forward propagation
3) A set of class specific linear SVMs.
        ----> score each extracted feature vector using the SVM for that class
        
Given all scored regions in an image, apply a greedy non-maximum suppression that rejects a region if it has an intersection-over-union (IoU) overlap with a higher scoring selected region larger than a learned threshold.
For more information about non-maximum suppression, refer to this blog: http://www.pyimagesearch.com/2014/11/17/non-maximum-suppression-object-detection-python/)

Note: All CNN parameters are shared across all categories, however, less flexible. (Why can we share all the parameters?)

### Training












