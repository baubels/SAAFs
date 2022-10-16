# SAAFs

This is an unsupervised learning scheme for smoothing images. A single 780x720x3 image takes approx 20 seconds per smoothing iterate on a modern laptop. In tests, the grayscale smoothing performed quite well, RGB not so much.

This is an implementation of the classical 'Gradient inverse weighted smoothing scheme and the evaluation of its performance' paper found here: https://www.sciencedirect.com/science/article/abs/pii/0146664X81900770.

Structural adaptive filtering is a non-global convolutional scheme assuming a lipshitz signal. It constructs custom kernels at each local region of the image, in this case opting to smooth the image.

To use the function `compute_inverse_gradient`, give a rank-3 numpy array representation of an image (RGB), an odd integered 'distance' representing the size of the kernel for which to convolve the image with, and a positive integer 'iterates' denoting the number of full convolutional passes (smoothing operations) to apply. A smoothed NumPy array representing the image is returned.
