---
layout: post
title: Matlab Notes

---

Useful for plotting matrices for bioinformatics.  It's in the documentation, but is not readily visible.  So to use the DataMatrix object you have to do either bioma.data.Datamatrix(...) or import bioma.data.Datamatrix

% Mask the 3D image called "image3D" with 2D image called "mask".
masked3DImage = bsxfun(@times, image3D, cast(mask, class(image3D)));
