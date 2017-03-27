# R-CNN-understanding
This repo serves as a summary of the paper "Rich feature hierarchies for accurate object detection and semantic segmentation Tech report (v5)".

## Abstract
Two key insights:
 1) One can apply high-capacity convolutional neural networks (CNNs) to bottom-up region proposals in order to localize and segment objects.
 2) When labeled training data is scarce, supervised pre-training for an auxiliary task, followed by domain specific fine-tuning, yields a significant performance boost.
 
 high-capacity here refers to the complexity of the underlying pattern that the neural network is able to learn. Usually going deep increases the capacity of the neural network by increasing the number of model parameters which means it can fit more complex functions.

Two problems need to be justified:
1) Localizing objects with a deep network.  ==>  operating within the "recognition using regions" paradigm
2) Training a high-capacity model with only a small quantity of annotated detection data.  ==>  
Unlike image classification, detection requires localization objects within an image.
