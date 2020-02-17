---
layout: post
title: Numpy Matrix Maniupations
description: Cropping and Padding a Matrx in Numpy
---

Numpy indexing is different than MATLAB and R, and slightly not as intuitive.  This is just a few things to note down
when working with matrices.

When using *np.nonzero* it will return a the indices as tuples, you want to transpose this to get a NXD matrix where N are 
the observations and D is the corresponding axis.

To crop a section of a matrix find the min/max indicies across each dimension.  So for example if you have a 128x128 matrix
and region of interest that is identified by the results of *np.nonzero* such that the array is 64x2.  Then to crop it you must do

```python
min_dim_x_Roi = np.min(ROI[:,0])
max_dim_x_Roi = np.min(ROI[:,0])
min_dim_x_Roi = np.min(ROI[:,1])
max_dim_y_Roi = np.min(ROI[:,1])
newCrop = initial_matrix[min_dim_x_Roi:max_dim_x_Roi, min_dim_y_Roi:max_dim_y_Roi]
```
To zero pad your crop, create a new matrix of zeros:

```python
padMat = np.zeros(128,128)
padMat[:newCrop.shape[0],:newCrop.shape[1]] = newCrop
```

You can also use np.pad, but I found the previous method more intuitive.

