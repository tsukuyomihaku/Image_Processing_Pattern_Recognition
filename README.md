# Image_Processing_Pattern_Recognition
<b>Lab 1: Gray Scale Image and Histogram Generation</b>

<b>THEORY</b>

<b> <u> Histogram in Image Processing </u> </b>

A histogram is a graphical representation of the intensity distribution of an image. It shows how frequently each pixel intensity value occurs in the image.
In a histogram the X-axis represents the pixel intensity values, usually ranging from 0 to 255 and the Y-axis represents the number of pixels corresponding to each intensity value.

Histograms help in understanding important characteristics of an image such as:

i)   Brightness
ii)  Contrast
iii) Intensity distribution
iv)  Dynamic range of pixel values

By analyzing the histogram, we can determine whether an image is too dark, too bright, or has low contrast.



<b><u> HISTOGRAM CALCULATION USING OpenCV</b></u>

In OpenCV, the histogram of an image can be calculated using the following function:
cv2.calcHist(images, channels, mask, histSize, ranges)

<b> Parameters of cv2.calcHist() </b>


images --> Source image whose histogram is to be calculated. It should be passed inside square brackets like [img].

channels --> Specifies the index of the channel. For grayscale image use [0]. For color images: [0] = Blue, [1] = Green, [2] = Red.

mask --> Mask image used to calculate histogram for a specific region. Use None for the entire image.

histSize --> Number of bins used in the histogram. Normally [256] for grayscale images.

ranges --> Range of pixel intensity values. Usually [0,256].


<b> <u> GRAY SCALE IMAGE </u></b>

A grayscale image contains only intensity information and does not contain color information. Each pixel in a grayscale image represents a brightness value ranging from:

0 → Black
255 → White

Grayscale images are simpler to process and are widely used in image processing applications.

<b> <u> Histogram Equalization </u></b>

Histogram Equalization is a technique used to improve the contrast of an image. Sometimes an image may contain pixel values concentrated only within a limited intensity range:

Bright images contain mostly high intensity values.
Dark images contain mostly low intensity values.

As a result, the image may appear unclear or have poor contrast.

Histogram Equalization redistributes the intensity values across the full range of the histogram, thereby improving the overall contrast of the image.

This process:

i)    Enhances visibility of details
ii)   Improves image quality
iii)  Spreads pixel intensities more uniformly

In OpenCV, histogram equalization can be performed using:
cv2.equalizeHist()



<b><u>APPLICATION OF HISTOGRAM</b></u>

Histograms are widely used in:

Image enhancement
i)    Medical image analysis
ii)   Computer vision
iii)  Object detection
iv)   Image segmentation
v)    Contrast adjustment



<b><u> CONCLUSION </b></u>

Histograms provide an effective way to analyze the intensity distribution of an image. By studying the histogram, we can better understand the brightness and contrast properties of an image. Histogram Equalization further improves image quality by enhancing contrast and distributing intensity values more evenly across the image.
