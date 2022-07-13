Released: 2 Aug 2019

# Previous Methods

Two branches

1. Proposal based (Mask R-CNN)

High accuracy, but low resolution and fps

Also, spatial-invariance of FCN is nto suitable for embedding methods.

2. Proposal free (discriminative loss)

Flexible but not so accurate

# Spatial Embeddings

The loss function **optimizes the iou** of each object's mask.

During inference, instances are recovered by clustering around the learned centers.

Kendall et al. proposed to assign pixels to objects by pointing to its object's center (how?)
- Avoids spatial-invariance by learning position relative offset vetcors

## Method

Instance segmentation = pixel assignment problem (classification?)

Segmentation pipeline is divided into two parts: 
