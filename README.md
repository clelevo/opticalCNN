# opticalCNN

NOTE: If you have a more up-to-date version of scipy, you may need to change the scipy.misc.imsave function to imageio.imwrite. Also, it appears there is an unresolved bug that is producing different results when running the onn_maskopt.py function. I apologize I have not maintained the code as I have finished my PhD since working on this project. - Julie Chang


Our code was run with Python 3.5.5 and Tensorflow 1.9.0 

Example to optimize a single-layer optical correlator for QuickDraw-16:

0. Download quickdraw-16 training dataset (see below) into assets folder
1. onn_quickdraw-16-tiled.py: optimizes a single-layer tiled kernel PSF model for the quickdraw-16 dataset
2. Walk through ONNMaskOpt.ipynb until the "Visualization of phase mask optimization" section. You can use the saved checkpoint folder we link below, or the checkpoint from running onn_quickdraw-16-tiled.py
3. onn_maskopt.py: optimizes a phase mask to correspond to a pre-computed PSF. You can use the sample psf in the assets folder or use the one you save from the ONNMaskOpt.ipynb walkthrough
4. Walk through ONNMaskOpt.ipynb from "Visualization of phase mask optimization" and plug in the checkpoint from onn_maskopt.py. 

Other code:
- jupyter notebooks are useful for visualization, but in the current state they rely on files that may not be added yet
- other scripts are added, but they are not completely demo-ready
- the core code for hybrid two-layer networks have "hybrid" in the filename

Downloads:
- quickdraw-16 training dataset: https://drive.google.com/file/d/1nD5NhRfEqiDao2FWX4X54uPnQWAyusyG/view?usp=sharing (the test dataset is already in the assets folder) 
- checkpoint folder used in ONNMaskOpt.ipynb: https://drive.google.com/file/d/1IoUa81VjPKK1zGxFSgQV_NSbkKLciVbW/view?usp=sharing 

Additional code used to interface with prototype hardware is available upon request.

# Paper

Title: Hybrid optical-electronic convolutional neural networks with optimized diffractive optics for image classification

Authors: Julie Chang*, Vincent Sitzmann, Xiong Dun, Wolfgang Heidrich, and Gordon Wetzstein*

*Correspondence to: juliechchang@gmail.com, gordon.wetzstein@stanford.edu

Link to our paper:
https://www.nature.com/articles/s41598-018-30619-y

# Website

Link to our project page:
http://www.computationalimaging.org/publications/hybrid-optical-electronic-convolutional-neural-networks/

# Data

The original images used in all experiments were downloaded directly from MNIST, CIFAR-10, or Google QuickDraw source websites. The If you are interested in the CIFAR-10 dataset captured by our prototype, please send us an email.
