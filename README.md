# Implementation of Erosion and Dilation Using OpenCV
## Developed By

**Name:** KISHORE N

**Register No:** 212223230106

## Aim

To write a Python program using OpenCV to perform morphological operations such as Erosion and Dilation on an image.

The program performs the following operations:

- Image Erosion
- Image Dilation

## Software Used

- Anaconda – Python 3.7
- Jupyter Notebook / VS Code
- OpenCV (cv2)
- NumPy
- Matplotlib

## Algorithm

### Step 1:

Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:

Create a blank image using NumPy.

### Step 3:

Insert text onto the image using OpenCV's text drawing function.

### Step 4:

Display the original image.

### Step 5:

Create a structuring element (kernel) of suitable size.

### Step 6: Image Erosion

- Apply the erosion operation using the created kernel.
- Remove pixels from the boundaries of foreground objects.
- Display the eroded image.

### Step 7: Image Dilation

- Apply the dilation operation using the same kernel.
- Add pixels to the boundaries of foreground objects.
- Display the dilated image.

### Step 8:

Compare the original, eroded, and dilated images.

## Program and Output

### Original Image
```
import cv2
import matplotlib.pyplot as plt
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.title("Input Image with Text")
plt.axis("off")
plt.show()
```
<img width="792" height="527" alt="WhatsApp Image 2026-09-18 at 10 51 13 AM" src="https://github.com/user-attachments/assets/110bbe2f-1957-454a-a420-5e03568034b0" />

### Erosion
```
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
erosion = cv2.erode(img, kernel, iterations=1)
plt.imshow(erosion, cmap="gray")
plt.title("Image Erosion")
plt.axis("off")
plt.show()
```

<img width="793" height="556" alt="WhatsApp Image 2026-09-18 at 10 51 23 AM" src="https://github.com/user-attachments/assets/4183b592-5cb4-4b4a-857e-fc77a900f6ca" />



### Dilation
```
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
dilation = cv2.dilate(img, kernel, iterations=1)
plt.imshow(dilation, cmap="gray")
plt.title("Image Dilation")
plt.axis("off")
plt.show()
```
<img width="654" height="545" alt="WhatsApp Image 2026-09-18 at 10 51 34 AM" src="https://github.com/user-attachments/assets/3ad0c299-3510-4182-a918-0f1b7718f324" />



## Result

Thus, the morphological operations **Erosion** and **Dilation** are successfully implemented using OpenCV.
