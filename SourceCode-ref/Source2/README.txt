Matlab implementation of Model Transfer SVM methods used in:

Tabula Rasa: Model Transfer for Object Category Detection
Y. Aytar and A. Zisserman
IEEE International Conference on Computer Vision(ICCV), 2011

This code has been tested on Matlab R2008b. It should work on any
version of Matlab >= R2008b. MOSEK optimization toolkit is strongly
advised for faster QP optimization which is used in Model Transfer SVM
learning procedures.

This package contains the following files and directories:

1) demo.m: This demo file shows how to use A-SVM, PMT-SVM, DA-SVM on a
simple classification example.

2) compile_mex.m: Compiles the mex file needed for HOG feature
extraction (Inherited from DPM code by Pedro Felzenszwalb).

3) svms: This directory contains three model transfer method
implementations namely:

- (a) Adaptive SVM (A_SVM.m)
- (b) Projective Model Transfer SVM (PMT_SVM.m)
- (c) Deformable Adaptive SVM (DA_SVM.m)

4) utils: This directory contains utility files:

- (a) computeAP.m : Computes the average precision for the given scores
and ground truth.
- (b) drawComparisonFigure.m: Plots a performance of model transfer
methods as a function of number of positive training samples.
- (c) extractHOGFeatures.m : Extracts HOG features from the given set of
images.
- (d) readImages.m : Reads images from the given directory.

5) data: Directory for images used in training and testing of transfer
learning methods.

To start using the code, follow these steps:

1) Run compileMex.m to compile the mex files.
2) Run demo.m in order to run classification demo using model transfer methods.

The demo file (demo.m) shows how to use A-SVM, PMT-SVM, DA-SVM on a
simple classification example. Images are extracted from the PASCAL
VOC 2007 dataset. The task is to learn a bicycle classifier by
transferring information from a motorbike classifier via the guidance
of a few bicycle samples. For the performance analysis, Average
Precision (AP) is plotted as a function of the number of positive
training samples. There are two situations with corresponding
performance plots: "results_balanced_samples.png" and
"results_unbalanced_samples.png" for balanced (same number of training
and testing samples) and unbalanced training of model transfer
methods, respectively.

If you use this package in your research please cite: 

Y. Aytar and A. Zisserman, Tabula Rasa: Model Transfer for Object
Category Detection, ICCV 2011


