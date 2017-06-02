Key: a single stage training algorithm that jointly learns to classify object proposals and refine their spatial locations.
- Spatial pyramid pooling networks (SPPNets) are proposed to speed up R-CNN by sharing computation

## Fast R-CNN Architecture and training
# input image and multiple Regions of Interest (RoIs) -> fully convolutional network -> RoI pooling layer 
# -> fully connected layers -> two output vectors per RoI: softmax probabilities and per-class bounding-box regression offsets
