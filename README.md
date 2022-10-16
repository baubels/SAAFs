# SAAFs

I implement the classical 'Gradient inverse weighted smoothing scheme and the evaluation of its performance' paper found here: https://www.sciencedirect.com/science/article/abs/pii/0146664X81900770.

Structural adaptive filtering is a non-global convolutional scheme assuming a lipshitz signal. It constructs custom kernels at each local region of the image, in this case opting to smooth the image.

To use the function `compute_inverse_gradient`, give a rank-3 numpy array representation of an image (RGB), an odd integered 'distance', and positive integer 'iterates'. A smoothed NumPy array representing the image is returned.
