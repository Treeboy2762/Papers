Challenge: arbitrary number of instances

# Previous Approaches
*Instance Categories?*

## Two approaches

### Top Down
Detect -> Segment (Mask R-CNN)

### Bottom UP
Predict embedding vectors -> Clustering (Discriminative Loss)

Both paradigms are step-wise and indirect; they depend on accurate bounding box detection / embedding learning + clustering algorithm

# SOLO
What differentiates object instances?

- Center Locations
- Object Sizes

Introduces grid of S x S cells
- How about multiple centers in a cell?
  - Not really our concern as we usually have centers far apart

Instance location category: approximates the location of the object center
- Essentially a classification task

## Variations

### Vanilla SOLO

### Decoupled SOLO

### Dynamic SOLO
Maybe allows dynamic input resolution?
Uses absolute positions

## Post-processing

Matrix NMS
- Performs NMS in matrix operations


