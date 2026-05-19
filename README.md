# Image_Processing_Pattern_Recognition
Lab 1: Gray Scale Image and Histogram Generation

THEORY

<b> Histogram in Image Processing </b>

A histogram is a graphical representation of the intensity distribution of an image. It shows how frequently each pixel intensity value occurs in the image.

In a histogram:

The X-axis represents the pixel intensity values, usually ranging from 0 to 255.
The Y-axis represents the number of pixels corresponding to each intensity value.

Histograms help in understanding important characteristics of an image such as:

i)   Brightness
ii)  Contrast
iii) Intensity distribution
iv)  Dynamic range of pixel values

By analyzing the histogram, we can determine whether an image is too dark, too bright, or has low contrast.

Parameters of cv2.calcHist()


images --> Source image whose histogram is to be calculated. It should be passed inside square brackets like [img].

channels --> Specifies the index of the channel. For grayscale image use [0]. For color images: [0] = Blue, [1] = Green, [2] = Red.

mask --> Mask image used to calculate histogram for a specific region. Use None for the entire image.

histSize --> Number of bins used in the histogram. Normally [256] for grayscale images.

ranges --> Range of pixel intensity values. Usually [0,256].


Gray Scale Image

A grayscale image contains only intensity information and does not contain color information. Each pixel in a grayscale image represents a brightness value ranging from:

0 → Black
255 → White

Grayscale images are simpler to process and are widely used in image processing applications.

Histogram Equalization

Histogram Equalization is a technique used to improve the contrast of an image.

Sometimes an image may contain pixel values concentrated only within a limited intensity range:

Bright images contain mostly high intensity values.
Dark images contain mostly low intensity values.

As a result, the image may appear unclear or have poor contrast.

Histogram Equalization redistributes the intensity values across the full range of the histogram, thereby improving the overall contrast of the image.

This process:

Enhances visibility of details
Improves image quality
Spreads pixel intensities more uniformly

In OpenCV, histogram equalization can be performed using:
cv2.equalizeHist()

Applications of Histogram

Histograms are widely used in:

Image enhancement
Medical image analysis
Computer vision
Object detection
Image segmentation
Contrast adjustment
Conclusion

Histograms provide an effective way to analyze the intensity distribution of an image. By studying the histogram, we can better understand the brightness and contrast properties of an image. Histogram Equalization further improves image quality by enhancing contrast and distributing intensity values more evenly across the image.
