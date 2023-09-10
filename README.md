# HISTOGRAM
# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
Step1:
Load the image using a suitable library like OpenCV.

Step2:
Convert the image to grayscale using cvtColor() if needed.

Step3:
Calculate the histogram using calcHist() and plot it with Matplotlib.

Step4:
Perform histogram equalization using equalizeHist() for enhanced contrast.

Step5:
Visualize results by plotting histograms and displaying original and equalized images side by side.
## Program:
```
# Developed By: PERARASU M
# Register Number: 212222100033
import cv2
import matplotlib.pyplot as plt
```
```
For a grayscale image
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Load a grayscale image
image_path = 'G.jpg'
gray_image = cv2.imread(image_path, cv2.IMREAD_GRAYSCALE)

# Calculate histogram
hist = cv2.calcHist([gray_image], [0], None, [256], [0, 256])

# Plot the histogram
plt.plot(hist)
plt.xlabel('Pixel Value')
plt.ylabel('Frequency')
plt.title('Histogram of Grayscale Image')
plt.show()
```
```
For colour image

import cv2
import numpy as np
import matplotlib.pyplot as plt

#### Load a color image
image_path = 'M.jpg'
color_image = cv2.imread(image_path, cv2.IMREAD_COLOR)

#### Convert color image to grayscale
gray_image = cv2.cvtColor(color_image, cv2.COLOR_BGR2GRAY)

#### Calculate histogram
hist = cv2.calcHist([gray_image], [0], None, [256], [0, 256])

#### Plot the histogram
plt.plot(hist)
plt.xlabel('Pixel Value')
plt.ylabel('Frequency')
plt.title('Histogram of color Image')
plt.show()
```

# Write your code to find the histogram of gray scale image and color image channels.
```
Histogram of Grayscale image

import cv2
import numpy as np
import matplotlib.pyplot as plt

#### Load a grayscale image
image_path = 'mi.jpg'
gray_image = cv2.imread(image_path, cv2.IMREAD_GRAYSCALE)

#### Calculate histogram
hist = cv2.calcHist([gray_image], [0], None, [256], [0, 256])

#### Plot the histogram
plt.plot(hist)
plt.xlabel('Pixel Value')
plt.ylabel('Frequency')
plt.title('Histogram of Grayscale Image')
plt.show()




```
# Display the histogram of gray scale image and any one channel histogram from color image

```

import cv2
import numpy as np
import matplotlib.pyplot as plt

#### Load a grayscale image
image_path = 'im.jpg'
gray_image = cv2.imread(image_path, cv2.IMREAD_GRAYSCALE)

#### Perform histogram equalization
equalized_image = cv2.equalizeHist(gray_image)

#### Calculate histograms before and after equalization
hist_before = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
hist_after = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])

#### Plot the histograms
plt.figure(figsize=(10, 6))

plt.subplot(2, 1, 1)
plt.plot(hist_before)
plt.title('Original Histogram')
plt.xlabel('Pixel Value')
plt.ylabel('Frequency')

plt.subplot(2, 1, 2)
plt.plot(hist_after)
plt.title('Equalized Histogram')
plt.xlabel('Pixel Value')
plt.ylabel('Frequency')

plt.tight_layout()
plt.show()

#### Display the original and equalized images
cv2.imshow('Original Grayscale Image', gray_image)
cv2.imshow('Equalized Grayscale Image', equalized_image)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
## Output:
### Input Grayscale Image and Color Image

![image](https://github.com/PERARASU10/HISTOGRAM/assets/118348589/e4c4e63e-5db9-4716-a7c5-083f75013583)



![image](https://github.com/PERARASU10/HISTOGRAM/assets/118348589/ae89ed54-efe7-4f5b-bfa5-1d82cdd89bcb)


###Histogram of Color Image:

![image](https://github.com/PERARASU10/HISTOGRAM/assets/118348589/53d44447-c8d1-490c-ba01-edb1b0b2683c)

![image](https://github.com/PERARASU10/HISTOGRAM/assets/118348589/91bdfea1-da33-4b51-a665-47a89abe114e)

### Histogram of Grayscale Image and any channel of Color Image
![image](https://github.com/PERARASU10/HISTOGRAM/assets/118348589/de4daf15-3609-4f44-8cab-1a6a980493a4)
![image](https://github.com/PERARASU10/HISTOGRAM/assets/118348589/6f3020f4-02a4-4a4b-a783-c7fda9f096f8)


### Histogram Equalization of Grayscale Image
![image](https://github.com/PERARASU10/HISTOGRAM/assets/118348589/c3b049af-b18e-4565-904b-62a9dda98079)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
