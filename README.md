# Exp-10--Record-IMPLEMENTATION-OF-OPENING-AND-CLOSING
## Aim:
To implement Opening and Closing using Python and OpenCV.

## Software Required:
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
**Step-1:**

Import the necessary packages

**Step-2:**

Create the Text using cv2.putText

**Step-3:**

Create the structuring element

**Step-4:**

Use Opening operation

**Step-5:**

Use Closing Operation


```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("Fish.jpg")  
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
plt.figure(figsize=(10, 5))
plt.subplot(1, 3, 1)
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")

```

### Display the input Image:

<img width="632" height="455" alt="image" src="https://github.com/user-attachments/assets/a219af3f-5fb0-4956-83c1-d53099bea71a" />


<br>

```python

opening_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)

image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
opening_image_rgb = cv2.cvtColor(opening_image, cv2.COLOR_BGR2RGB)

plt.subplot(1, 3, 2)
plt.imshow(opening_image_rgb)
plt.title("Opening Operation")
plt.axis("off")
```

### Display the result of Opening:

<img width="626" height="448" alt="image" src="https://github.com/user-attachments/assets/36657f5b-f97e-4990-898e-ff83af5b20c9" />


<br>

```python

closing_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
closing_image_rgb = cv2.cvtColor(closing_image, cv2.COLOR_BGR2RGB)
plt.subplot(1, 3, 3)
plt.imshow(closing_image_rgb)
plt.title("Closing Operation")
plt.axis("off")

plt.tight_layout()
plt.show()

```
### Display the result of Closing:


<img width="767" height="540" alt="image" src="https://github.com/user-attachments/assets/3c19d90b-ee4e-47e2-8b70-6af1a84494fb" />


<br>
## Result:
Thus,the Opening and Closing operation is used in the image using python and OpenCV.
